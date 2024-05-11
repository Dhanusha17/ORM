# Ex02 Django ORM Web Application 
## Date:23-03-24
## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).
## Entity Relationship Diagram
<img width="451" alt="er diagram booklist ss" src="https://github.com/Dhanusha17/ORM/assets/151549957/b36e7d99-7306-4caa-94ed-8b67850bb3a2">
## DESIGN STEPS
### STEP 1:
clone the respository from github
### STEP 2:
create on admin interface for django
### STEP 3:
create an folder and edit settings.py
### STEP 4:
makemigration and migrate the changes
### STEP 5:
create admin.py and write program for admin and models
## PROGRAM
```
models.py
class Book(models.Model):
  Book_id=models.IntegerField(primary_key=True);
  Book_author=models.CharField(max_length=20);
  Book_name=models.CharField(max_length=50);
  publication=models.DateField();
  price=models.IntegerField();
class BookAdmin(admin.ModelAdmin):
  list_display=("Book_id","Book_author","Book_name","publication","price");
admin.py
from django.contrib import admin
from .models import Book,BookAdmin
admin.site.register(Book,BookAdmin)
```
## OUTPUT
<img width="958" alt="booklist ss" src="https://github.com/Dhanusha17/ORM/assets/151549957/63bd0ecb-a623-4a05-9694-bc60d74bdfef">
## RESULT
Thus the program for creating a database using ORM hass been executed successfully.
