# django-cheatsheet

### How to create a new Django project
```bash
django-admin startproject projectname
```

### How to start the Django development server
```bash
python3 manage.py runserver
```

### How to create a new application in the project
```bash
python3 manage.py startapp main_app (or another custom name)
```

### Django directory structure
```
djangoproject
|
|- djangoproject
  |- settings.py: Main settings for our project (db, apps, config, etc.)
  |- urls.py: Main URLs for the entire project
|
|- application_name
  |- static: (dir) This folder holds all static files (css, js, images, aux. forms)
  |- templates: (dir) This folder holds all HTML template files
  |- migrations: (dir) This folder holds all data migration files
  |- admin.py: This is where we register data models
  |- models.py: This is where we put all data models
  |- views.py: This is where we put the function that run our routes
  |- urls.py: Every URL for our site is defined here
|
|- manage.py: Lets us manage everything about the project
```
