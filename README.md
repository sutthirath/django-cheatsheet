# django-cheatsheet

## How to create a new a Django project
```bash
django-admin startproject projectname
```

## How to start the Django developement server
```bash
python3 manage.py runserver
```


## How do you stop it?
```

```


## How to create a new application in the project
```bash
python3 manage.py startapp main_app
```

## Django directory structure
```
djangoproject
|
 - djangoproject
|  |
    - settings.py: main settings for prject (db, apps, config, etc.)
    -urls.py: main urls for the entire project
|
 - application_name
   |- static: (dir) holds all static files (css, js, images, aux, forms)
   |- templates: (dir) holds all HTML template files
   |- migrations: (dir) this holds all data migration files
   |- admin.py: this is where we register data models
   |- models.py: this is where we put all models
   |- views.py: this is where we put the functions that run our routes
   |- urls.py: every url for our site is defined here
   |
   |- manage.py: let's us manage everything about our project
```
