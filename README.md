# Ex02 Django ORM Web Application
## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).
## Entity Relationship Diagram
![image](https://github.com/Harevasu/ORM/assets/147985044/caf461e1-90d5-4f92-9e0f-18a19bccf0a6)
## DESIGN STEPS
### STEP 1:
Clone the problem from GitHub
### STEP 2:
Create a new app in Django project
### STEP 3:
Enter the code for admin.py and models.py
### STEP 4:
Execute Django admin and create details for 10 books
## PROGRAM
```
admin.py
from django.contrib import admin
from .models import Book,BookAdmin
admin.site.register(Book,BookAdmin)

models.py
from django.db import models
from django.contrib import admin
class Book(models.Model):
    book_id=models.IntegerField(primary_key=True)
    book_name=models.CharField(max_length=50)
    publisher_name=models.CharField(max_length=50)
    author_name=models.CharField(max_length=50)
    publisher_year=models.DataField()
class BookAdmin(admin.ModelAdmin):
    list_display=('book_id','book_name','publisher_name','publisher_year','author_name')
```
## OUTPUT :
![image](https://github.com/Harevasu/ORM/assets/147985044/09fcd00d-9022-4dac-9a42-d850d3e11e96)
## RESULT
Thus the program for creating a database using ORM hass been executed successfully
