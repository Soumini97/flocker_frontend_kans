---
layout: post
title: Prototype of Website 
description: Book Review website
hide: true
menu: nav/home.html
---



<html>
<h1 style="font-family: Garamond">Book Review</h1>
<style>
        .image {
            position: relative; /* or absolute */
            left: 200px; /* move right */
            top: -65px; /* move down */
        }
    </style>
<!-- book image thing -->
<!-- book image thing -->
<!-- book image thing -->
<img src="{{site.baseurl}}/images/books.jpg" alt="image of books" style="width:6%" class="image">


<!-- star thingies -->
<!-- star thingies -->
<!-- star thingies -->
<!-- star thingies -->
<!-- star thingies -->
<!-- star thingies -->
<!-- star thingies -->
<style>
        .container {
            position: relative; /* Establish a positioning context */
            width: 500px; /* Width of the container */
            height: 500px; /* Height of the container */
            /* border: 1px dashed #ccc;           border for container */
        }

        .star-button {
            width: 25px;
            height: 25px;
            background-color: #FFD700; /* Gold color */
            border: none;
            cursor: pointer;
            clip-path: polygon(
                50% 0%, 
                61% 35%, 
                98% 35%, 
                68% 57%, 
                79% 91%, 
                50% 70%, 
                21% 91%, 
                32% 57%, 
                2% 35%, 
                39% 35%
            );
            position: absolute; /* Position each button absolutely */
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: white;
            
        }

        /* Positioning each star button */ /* NIKITH CHANGE THESE TO CHANGE POSITION */
        .star1 { top: 20px; left: 20px; }
        .star2 { top: 20px; left: 50px; }
        .star3 { top: 20px; left: 80px; }
        .star4 { top: 20px; left: 110px; }
        .star5 { top: 20px; left: 140px; }
    </style>
<body>

<div class="container">
    <button class="star-button star1"></button>
    <button class="star-button star2"></button>
    <button class="star-button star3"></button>
    <button class="star-button star4"></button>
    <button class="star-button star5"></button>
</div>

</body>

<html>