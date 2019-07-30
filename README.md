# Django-practice

Watching a django tutorial and coding along

SETUP:

1. pip install pipenv
2. pipenv shell
3. pipenv install django djangorestframework django-rest-knox
4. django-admin startproject API-MANAGER (or whatever you want to call it)
5. cd API-MANAGER
6. ctrl, shift, p, -> select python interpreter and then select the app you're currently in
7. python manage.py startapp API-FOLDER
8. go into settings in API-MANAGER, API-MANAGER folders and under INSTALLED_APPS type the following..

   'leads',
   'rest_framework'

CREATING MIGRATIONS:

1. Go into API-FOLDER into models.py and create a data model
2. After creating data model, in terminal run: python manage.py makemigrations leads
3. next run: python manage.py migrate

SERIALIZERS:

With restframework we need a serializer, which basically takes querysets and model instances and converts them to python datatypes that can easily be rendered into JSON, JML, etc

1. create a new file in API-FOLDER and call it serializers, then create a class like in serializers.py

API

1. Next create a file in API-FOLDER and call it api.py
2. In api.py create a viewset

A viewset allows us to create a full CRUD API without having to specify explicit methods for the functionality

3. Next we need to create URLs by going into urls.py in API-MANAGER
4. then create a new urls.py file in leads like so
5. then run python manage.py runserver

---

SETUP FRONTEND:

1. Open a new terminal and then in parent API-MANAGER run pipenv shell to start virtual env
2. In terminal run: python manage.py startapp frontend
3. In terminal run: mkdir -p ./frontend/src/components
4. Within frontend create 2 folders called templates and static and each one will have a frontend folder inside it

src = All of our components, redux, react, etc..
templates = handles index.html file that gets loaded
static = Compiled js - webpack takes react app, looks at it and compiles it to main.js inside static

5. CD into main directory (one with pipfile, etc) and then run the following: npm init -y
6. next run: npm i -D webpack webpack-cli
7. npm i -D @babel/core babel-loader @babel/preset-env @babel/preset-react babel-plugin-transform-class-properties
8. npm i react react-dom prop-types

---- Other Django Tutorial ----

SETTINGS:

INSTALLED_APPS: if you add a folder name to installed apps you can acess a fil by doing foldername.\_\_\_

Steps:

1. python manage.py migrate
2. python manage.py createsuperuser
3. python manage.py runserver
4. Once models are created run: python manage.py makemigrations

FOREIGN KEYS explination 29 mins into video

Notes:

- by default django makes everything not nullable, so to combat that use blank-True and null=True (51 mins)

- djangorestframework add above custom apps in INSTALLED_APPS

---

provided:
{
"room_id": "?",
"title": "Shop",
"description": "You are standing in a shop. You can sell your treasure here.",
"coordinates": "?",
"players": [],
"items": [],
"exits": ["e"],
"cooldown": 2.0,
"errors": [],
"messages": ["I'll give you 100 gold for that Small Treasure.", "(include 'confirm':'yes' to sell Small Treasure)"]
}

our storage:

{
team_score: 0,
messages: [],
map: {0: {n: ?, e:?, w:?, s:?}, - 499},
teammate_location: {player_1: 0, player_2: 0, player_3: 0, player_4: 0},
}
