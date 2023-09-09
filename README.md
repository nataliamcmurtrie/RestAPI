# RestAPI
Testing out Rest API's using python/flask/postman

## Postman

API calls are made using Postman, for mac OS the desktop client works best.

## Terminal setup

Environmental Variables (run this every time you open a fresh terminal)
	
	export FLASK_APP=application.py 
	export FLASK_ENV=development
	
Call

	flask run --port 8000
	
To start the web-app. Port 8000 is used because using the default port
of 5000 can cause issues with Mac OS. 

## Database setup

From the terminal:

	python3
	>>>> from application import db
	>>>> db.create_all()

## Postman

Create a POST request that points to the database
	
	http://127.0.0.1:8000/drinks

And select Body, raw, in JSON format with the following 

	{
    "name": "Sprite",
    "description": "Bad"
	}

By making this POST request a drink named Sprite is added to
the database with the description Bad. An id is returned. 

A GET request which points to the database

	http://127.0.0.1:8000/drinks

Will return all drinks that have been added using POST
