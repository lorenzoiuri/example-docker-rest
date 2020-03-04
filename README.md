# Example code for a Rest web service built using Python (Flask) and Postgres

This repository is adaptation of the work at
https://medium.com/@hmajid2301/implementing-sqlalchemy-with-docker-cb223a8296de
## Installation 

Assuming you have `docker` and `docker-compose` installed 
* run `docker-compose build` inside the repository, this will download the images for `python` and for `postgres`
* then run `docker-compose up`, the first time the server crashed so `ctrl-c` and repeat `docker-compose up`, this time it should work. 

The service should be accessible at the computer ip (both localhost and LAN) at port `5000`.

The web service allows to send informations about cats and retrieve them.

Test the web service using:
* `curl -XPOST -H "Content-type: application/json" -d '{"name": "catty mcCatFace", "price": 5000, "breed": "bengal"}' '127.0.0.2:5000/add'` to send a `POST` request to add a cat
* go on `127.0.0.1:5000` to send a `GET` and fetch the cat list.

Note: using postman to send a post request put in the body 
`{ "name": "Cat", "price": 5000, "breed": "None" }`, in the header Key `Content-Type` and in the header value `application/json`. the POST to `127.0.0.1:5000/add`.

Note: The usage of Rest convetions followed in this example is not corrent but this example has the only purpose to show how to configure python + flask + postgres inside docker.
