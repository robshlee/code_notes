# Django Notes

**start new django PROJECT**  
django-admin startproject django_blog

**start new APP in django**  
python manage.py startapp projectApp  
-don't forget to add the app config to settings.py

**create superuser**  
python manage.py createsuperuser

**wsgi**  
-this is how the app and web server communicate

**running server locally**  
python manage.py runserver

**running django shell**  
python manage.py shell

**how django works**  
-urls map to a view => views map to other things like templates  
-create context data in view then pass it to the template  
-save method is like commit in sqlalchemy to make changes to the database

**template notes**
-create context data in view then pass it to the template  
-receive context to template with {% context_here %}  
-for loop ex:  
{% for post in posts %}  
    <h1>{{ post.title }} is the title</h1> # this is how you pass a context variable
{% endfor %}  
-view function returns statements look like, return render(request, template_name, context_data)  
-user information can be used without context put in as its already built in.  
ie: you can use user.username as variable without passing context into the template first.

**template link to another page example**  
<a class="ml-2" href="{% url 'login' %}">Sign In</a>

**template if example** 
{% if title %}  
    <title></title>  
{% else %}  
    <title></title>  
{% endif %}

**loading static files to templates**  
{% load static %} (at the top of html doc)  
{% static 'blog/main.css' %}" (this will pull the static file through context)

**loading url in template**  
{% url 'blog-home' %}

**admin page notes**  
-if you want to add model to admin page, register it through admin.py in the app directory


**views notes**  
-form.isvalid() automatically does the checks against the database. ie: if the form has a duplicate username against the db it will be false  
-form.save() will save the form data to the db  

**urls notes**  
-specify template location example: path('login/', auth_views.LoginView.as_view(template_name='users/login.html'), name='login')  


**models notes**  
-__str__ method for a model will make it so you can print out information on the object instead of just the object name  

**migration steps**  
python manage.py makemigrations  
**this creates the migration file**  
**for docker you need to then copy the file out and place it into your local branch**  
**to migrate the migration file into your database run migrate**  
python manage.py migrate  