FROM python:3

WORKDIR /usr/src/app

COPY requirements.txt /usr/src/app/requirements.txt
RUN apt-get update & apt-get install -y gcc
RUN pip3 install --no-cache-dir -r requirements.txt

EXPOSE 5000

ENV FLASK_APP app.py 

COPY . /usr/src/app/