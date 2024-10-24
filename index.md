---
layout: post
title: Prototype of Website 
description: Book Review website
hide: true
menu: nav/home.html
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Light Brown Background</title>
    <style>
        body {
            background-color: #D2B48C; /* Light brown color */
            color: #333; /* Dark text for contrast */
            font-family: Arial, sans-serif; /* Optional: change font */
        }
    </style>
</head>
<body>

# Your Markdown Title

Your content goes here.

</body>
</html>

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
            width: 20px;
            height: 20px;
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
        .star1 { top: -40px; left: 170px; }
        .star2 { top: -40px; left: 200px; }
        .star3 { top: -40px; left: 230px; }
        .star4 { top: -40px; left: 260px; }
        .star5 { top: -40px; left: 290px; }
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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Book Reviews</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
            color: #333;
        }
        h1 {
            text-align: center;
        }
        #reviewForm {
            background: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 500px;
            margin: 20px auto;
        }
        #reviews {
            margin-top: 20px;
        }
        .review {
            background: #e9ecef;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
        }
        .review h3 {
            margin: 0 0 5px;
        }
        .review p {
            margin: 0;
        }
    </style>
</head>
<body>

    <h1>Book Reviews</h1>
    
    <div id="reviewForm">
        <h2>Submit Your Review</h2>
        <form id="form">
            <label for="bookTitle">Book Title:</label>
            <input type="text" id="bookTitle" required><br><br>
            
            <label for="bookAuthor">Author:</label>
            <input type="text" id="bookAuthor" required><br><br>
            
            <label for="bookReview">Your Review:</label><br>
            <textarea id="bookReview" rows="4" required></textarea><br><br>
            
            <button type="submit">Submit Review</button>
        </form>
    </div>

    <div id="reviews">
        <h2>Reviews</h2>
        <div id="reviewList"></div>
    </div>

    <script>
        document.getElementById('form').addEventListener('submit', function(event) {
            event.preventDefault(); // Prevent form submission
            
            const title = document.getElementById('bookTitle').value;
            const author = document.getElementById('bookAuthor').value;
            const review = document.getElementById('bookReview').value;
            
            // Create a new review element
            const reviewDiv = document.createElement('div');
            reviewDiv.classList.add('review');
            reviewDiv.innerHTML = `<h3>${title} by ${author}</h3><p>${review}</p>`;
            
            // Add the new review to the review list
            document.getElementById('reviewList').appendChild(reviewDiv);
            
            // Clear the form
            document.getElementById('form').reset();
        });
    </script>

</body>
</html>
