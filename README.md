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
### How to make URLs with the path() function
```python
urlpatterns = [
  path('route/', views.route1_name, name='route1_name'),
  path('route/<string_variable>', views.route2_name, name='route2_name'),
  path('route/<int:variable_name>', view.route3_name, name='route3_name'),
]
```

### How to make a view function:
```python
def route1_name(request):
  return render(request, 'template1.html')

def route2_name(request, string_variable):
  return render(request, 'template2.html', {'data': string_variable})
  
def route3_name(request, variable_name):
  return render(request, 'template3.html', {'data': variable_name})
```

### How to get running from start (boilerplate)
Add application name to settings.py
Include main_app.urls to django project's urls.py
Create templates folder within app directory
Create urls.py file within app directory
Add static folder

Step 1. Create URL route 
  `path('', views.index, name="index")`
Step 2. Create the View
  ```
  def index(request):
    return render(request, 'index.html')
  ```
Step3. Create the template
  Create base.html:
    ```
    !html boilerplate...
    {% block content %}
    {% endblock %}
    ```
  Create index.html:
    ```
    {% extends 'base.html' %}
    {% block content %}
    {% endblock %}
    ```

  

