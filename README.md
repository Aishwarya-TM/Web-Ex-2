# Ex02 Django ORM Web Application
## Date: 31.03.2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

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
### Index.html:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>Hello!!</p>
</body>
</html>
```

### views.py:
```
from django.shortcuts import render
def homePage(request):
    return render(request,'index.html')
```

### urls.py:
```
from django.contrib import admin
from django.urls import path
from app1 import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.homePage)
]
```
### models.py:
```
from django.db import models

class Book(models.Model):
    title=models.CharField(max_length=20)
    author=models.CharField(max_length=20)
    genre=models.CharField(max_length=20)
    publication=models.IntegerField()
    ISBN=models.IntegerField()

```

### admin.py
```
from django.contrib import admin
from app1.models import Book
admin.site.register(Book)
```


## OUTPUT

![Screenshot 2024-03-31 200309](https://github.com/Aishwarya-TM/Web-Ex-2/assets/127846109/a9c513f6-879c-4253-a5a2-61983c8ff073)

![Screenshot 2024-03-31 200326](https://github.com/Aishwarya-TM/Web-Ex-2/assets/127846109/b52b998d-bbef-43b4-a19e-4bc981baf126)

![Screenshot 2024-03-31 200349](https://github.com/Aishwarya-TM/Web-Ex-2/assets/127846109/48d1c028-f99b-4319-895d-c63a76d58bf2)

![Screenshot 2024-03-31 200404](https://github.com/Aishwarya-TM/Web-Ex-2/assets/127846109/4d0815d0-8774-4785-bbb0-2ebe27573f7e)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
