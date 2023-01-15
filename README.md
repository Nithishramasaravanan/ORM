# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![Entity Relationship Diagram](./dataproject/ORM.png)

## DESIGN STEPS

### STEP 1:
clone the problem from github

### STEP 2:
create a new app and enter the code for admin.py and model.py 

### STEP 3:
Execute Django admin and create 10 Employee Eid


## PROGRAM

```
Models.py

from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
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

![Output](./dataproject/EID.png)


## RESULT

Program Executed Successfully