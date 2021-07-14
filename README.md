# Django-Hello-World
Django is full-stack web development Framework
 
Creating a Django Application requires few commands on the CMD like,

First of all check whether it is installed or not, checking through (pip list)

Django-admin startproject project_name (for starting to create an application)

Executing this command will create a folder with some of the file like, _init.py, views.py, urls.py, etc.

In the folder there will be a file named as manage.py using it we can create the application. 

Python manage.py startapp app_name 

Now we need to manage internal files like giving the paths and setting the reference

First we have to add URL to the urls.py file of our project (refer the URL of our application)

from django.contrib import admin

from django.urls import path, include

urlpatterns = [

path('admin/', admin.site.urls),

path('',include('Task01.urls'))

]

After this setting of URL we need to go to the URL file our application (It is created by user it’s not automatically created)

Also in that urls.py file we need to add paths of the file where we show the data , like in the views.py we need to display the data at our screen so we can add that path in urls.py like:

from django.urls import path

from .import views

urlpatterns = [

path('', views.Task_1)

]

In views we can create a program like:

from django.shortcuts import render, HttpResponse

def Task_1(request):

return HttpResponse("Hello The World of Aleins")

In setting we need to add the name of application in the list of INSTALLD_APPS

After completing this we need to run server and execute the program at the given URL.

