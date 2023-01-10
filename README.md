# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram:

![Entity Relationship Diagram](./ORM2.png)

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
clone the problem from github

### STEP 2:
create a newapp

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute django admin and create 10 employees

## PROGRAM
```
Model.py

from django.db import models
from django.contrib import admin
class Employee(models.Model):
    eid=models.CharField(max_length=20,help_text="EmployeeID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

Admin.py

from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
```

## OUTPUT
![OUTPUT](./ORM1.png)


## RESULT:
program is successfully executed
