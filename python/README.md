# Create Python/Django App instructions

1. Run ' virtualenv myapp '

2. Windows - Run ' source myapp/Scripts/activate '
   Mac - source myapp/bin/activate
    * If you close your terminal window and reopen need to do the source command again.

3. Run ' pip install Django ' (in production you want to do Pip install Django==<version>. That way entire team install's the same version.

4. Run ' django-admin startproject app '

5. run ' python manage.py startapp <name of folder> '

6. Open VSC. In app open the settings.py file. In INSTALLED_APPS add <'users.apps.UsersConfig',> to last line underneath <'django.contrib.staticfiles',>

7. Copy paste the following to views.py file in the users folder.

    from django.shortcuts import render
    from django.http import HttpResponse

    # Create your views here.
    def home(request):
        response = "<h1>Hello world!</h1>"
        return HttpResponse(response)

8. Create a urls.py file in the users folder. Copy paste the following to the file that was just created

    from django.urls import path
    from . import views

    urlpatterns = [
        path('home/', views.home),
    ]

9. In the app folder copy and paste the following in the urls.py file

    from django.contrib import admin
    from django.urls import path
    from django.urls import include

    urlpatterns = [
        path('admin/', admin.site.urls),
        path('', include('users.urls'))
    ]

11. Run ' python manage.py runserver '

11. Add /home/ to the end of the url. Should see hello world

12. Run ' python manage.py makemigrations && python manage.py migrate '

13. To use the python shell with app created run ' python manage.py shell '