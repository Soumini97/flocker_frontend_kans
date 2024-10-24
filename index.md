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
        .star-button {
            width: 30px; /*if u want to change size of star change these values*/
            height: 30px; /*if u want to change size of star change these values*/
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
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: white;
            position: relative; /* or absolute */
            left: 200px; /* move right */
            top: -65px; /* move down */

        }
    </style>

<button class="star-button"></button>

<html>