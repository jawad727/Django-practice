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
4.
5.
6.
