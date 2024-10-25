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
    <title>Book Review</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #8B0000 !important;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background-color: #f3c6b6;
            width: 60%;
            max-width: 800px;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
        }
        .title {
            text-align: center;
            font-size: 36px;
            font-weight: bold;
            margin-bottom: 20px;
        }
        .book-shelf {
            display: flex;
            justify-content: center;
            margin-bottom: 30px;
        }
        .book-shelf img {
            width: 120px;
        }
        .review-section {
            display: flex;
            justify-content: space-between;
        }
        .photo-section {
            width: 40%;
            text-align: center;
            border: 2px dashed #000;
            padding: 20px;
        }
        .photo-section p {
            margin-top: 100px;
            font-weight: bold;
        }
        .details-section {
            width: 55%;
            padding: 20px;
        }
        .input-field {
            margin-bottom: 10px;
        }
        .input-field label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        .input-field input {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .rating {
            text-align: center;
            margin: 20px 0;
        }
        .stars {
            color: pink;
            font-size: 24px;
        }
        .stars span {
            cursor: pointer;
        }
        .review-textarea {
            width: 100%;
            height: 120px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="title" style="color:#8B0000;">Book Review</div>
        <div class="book-shelf">
            <img src="https://content.mycutegraphics.com/graphics/book/bookshelf-clipart-book-clip-art.png" alt="Bookshelf Image">
        </div>
        
        <div class="review-section">
            <!-- Photo Section -->
            <div class="photo-section">
                <p>PHOTO HERE</p>
            </div>
            <!-- Book Details -->
            <div class="details-section">
                <div class="input-field">
                    <label for="title" style="color:#8B0000;">Title:</label>
                    <input type="text" id="title" placeholder="Enter book title">
                </div>
                <div class="input-field">
                    <label for="author" style="color:#8B0000;">Author:</label>
                    <input type="text" id="author" placeholder="Enter author name">
                </div>
                <div class="input-field">
                    <label for="year" style="color:#8B0000;">Year:</label>
                    <input type="text" id="year" placeholder="Enter year of publication">
                </div>
                <div class="input-field">
                    <label for="pages" style="color:#8B0000;">Page:</label>
                    <input type="text" id="pages" placeholder="Enter number of pages">
                </div>
            </div>
        </div>

        <!-- Rating and Review Section -->
        <div class="rating">
            <p style="color:#8B0000;">Rate:</p>
            <div class="stars">
                <span>&#9733;</span>
                <span>&#9733;</span>
                <span>&#9733;</span>
                <span>&#9733;</span>
                <span>&#9733;</span>
            </div>
        </div>

        <div class="review-section">
            <label for="review" style="color:#8B0000;">Review:</label>
            <textarea id="review" class="review-textarea" placeholder="Write your review here"></textarea>
        </div>
    </div>
</body>
</html>
