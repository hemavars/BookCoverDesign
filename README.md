# Ex.05 Book Front Cover Page Design
## Date:16.12.2025

## AIM:
To design a book front cover page using HTML and CSS.

## DESIGN STEPS:

### Step 1:
Create a Django Admin project.

### Step 2:
Create an app in the Django interface.

### Step 3:
Create a folder named 'static' in the app folder.

### Step 4:
Create a new HTML file in the static folder.

### Step 5:
Write the HTML code with relevant CSS properties.

### Step 6:
Choose the appropriate style and color scheme.

### Step 7:
Insert the images in their appropriate places.

### Step 8:
Publish the website in the LocalHost.

## PROGRAM:
```
urls.py
from django.contrib import admin
from django.urls import path
from bookapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.book_cover),

]

```
```
views.py
from django.shortcuts import render

def book_cover(request):
    return render(request,'books.html')

```
```
books.html
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Book Cover</title>

<style>
  body {
    margin: 0;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(135deg, #d86aa8, #4b2b63);
    font-family: Georgia, serif;
  }

 
  .book-cover {
    
    background-size: 100% 100%;
    width: 300px;
    height: 500px;
    position: relative;
    padding: 20px;
    text-align: center;
    border-radius: 8px;
    box-shadow: 0 20px 50px rgba(203, 193, 210, 0.8);
  }


  .inner-border {
    position: absolute;
    top: 2.5%;
    left: 2.5%;
    width: 95%;
    height: 95%;
    border: 2px solid rgba(230, 210, 255, 0.6);
    border-radius: 6px;
  }

  h1 {
    margin-top: 70px;
    font-family: 'Cinzel', serif;
    font-size: 36px;
    font-weight: 600;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #f3e9ff;
    line-height: 1.3;
    text-shadow: 2px 2px 8px rgba(184, 148, 201, 0.8);
  }

 
  h4 {
    margin-top: 12px;
    font-style: italic;
    font-size: 16px;
    color: #d6b4ff;
    letter-spacing: 1px;
  }


  .divider {
    position: absolute;
    bottom: 80px;
    left: 25%;
    width: 50%;
    border: 1px solid rgba(230, 200, 255, 0.7);
  }


  .author {
    position: absolute;
    bottom: 30px;
    left: 50%;
    transform: translateX(-50%);
    text-align: center;
  }

  .author img {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    border: 2px solid #d6b4ff;
    margin-bottom: 6px;
    object-fit: cover;
  }

  .author p {
    margin: 0;
    font-size: 14px;
    font-weight: bold;
    color: #f5ecff;
    letter-spacing: 1px;
  }
</style>
</head>

<body>

<div class="book-cover">
  <div class="inner-border"></div>

  <h1>Whispers<br> Beneath <br>the <br>Unfinished <br>Sky</h1>
  <h4>A secret world waits where the sky never quite finishes its story.</h4>

  <hr class="divider">

  <div class="author">
    <img src="{% static 'author.jpg' %}" alt="Author">
    <p>HEMAVARSHINI</p>
  </div>
</div>

</body>
</html>
```

## OUTPUT:
![books.html](<Screenshot 2025-12-15 090220.png>)

## RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
