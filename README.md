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
control + c
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

## How to make URLs with the path() function:
```python
urlpatterns = [
 path('route/', views.route_name, name='route_name')
 path('route/<string_variable>', views.route2_name, name='route_name'),
 path('route/<int:variable_name>', views.route3_name, name='route3_name'),
] 
```

## How to make a view function:
```python
def route1_name(request):
    return render(request, 'template1.html')

def route2_name(request, variable_name):
    return render(request, 'template2.html', {'data': string_variable})
    
def route3_name(request):
    return render(request, 'template3.html', {'data': variable_name})
    
```
