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
    <title>Book Review Funsies</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f3c6b6;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background-color: #fff;
            width: 60%;
            max-width: 800px;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
            text-align: center;
            font-size: 16px;
            color: #4b4b4b;
        }
        .title {
            font-size: 36px;
            font-weight: bold;
            margin-bottom: 20px;
        }
        .review-section {
            display: flex;
            justify-content: space-between;
            margin-bottom: 30px;
        }
        .photo-section {
            width: 40%;
            height: 250px;
            border: 2px dashed #4b4b4b;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            background-color: #fbe9e7;
            color: #4b4b4b;
        }
        .photo-section p {
            font-weight: bold;
            font-size: 18px;
            color: #4b4b4b;
        }
        .details-section {
            width: 55%;
            text-align: left;
            background-color: #fbe9e7;
            padding: 20px;
            border-radius: 10px;
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
            font-size: 16px;
            background-color: white;
            color: black;
        }
        .rating {
            text-align: center;
            margin: 20px 0;
        }
        .rating h3 {
            margin-bottom: 10px;
        }
        .stars {
            color: #ff69b4;
            font-size: 30px;
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
            margin-bottom: 20px;
            font-size: 16px;
            background-color: white;
            color: black;
        }
        button {
            background-color: #ff69b4;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        button:hover {
            background-color: #ff1493;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="title">Book Review</h1>
        <!-- Book Photo and Details -->
        <div class="review-section">
            <div class="photo-section">
                <p>PHOTO HERE</p>
            </div>
            <div class="details-section">
                <div class="input-field">
                    <label for="bookTitle">Title:</label>
                    <input type="text" id="bookTitle" required>
                </div>
                <div class="input-field">
                    <label for="bookAuthor">Author:</label>
                    <input type="text" id="bookAuthor" required>
                </div>
                <div class="input-field">
                    <label for="bookYear">Year:</label>
                    <input type="text" id="bookYear" required>
                </div>
                <div class="input-field">
                    <label for="bookPage">Page:</label>
                    <input type="text" id="bookPage" required>
                </div>
            </div>
        </div>
        <!-- Rating Section -->
        <div class="rating">
            <h3>Rate</h3>
            <div class="stars">
                <span>&#9733;</span>
                <span>&#9733;</span>
                <span>&#9733;</span>
                <span>&#9733;</span>
                <span>&#9733;</span>
            </div>
        </div>
        <!-- Review Section -->
        <div class="input-field">
            <label for="bookReview">Review:</label>
            <textarea id="bookReview" class="review-textarea" required></textarea>
        </div>
        <button type="submit" id="submitBtn">Submit Review</button>
        <!-- Displayed Reviews -->
        <div id="reviews">
            <h2>Reviews</h2>
            <div id="reviewList"></div>
        </div>
    </div>
    <script>
        document.getElementById('submitBtn').addEventListener('click', function(event) {
            event.preventDefault(); // Prevent form submission
            const title = document.getElementById('bookTitle').value;
            const author = document.getElementById('bookAuthor').value;
            const review = document.getElementById('bookReview').value;
            const year = document.getElementById('bookYear').value;
            const page = document.getElementById('bookPage').value;
            // Create a new review element
            const reviewDiv = document.createElement('div');
            reviewDiv.classList.add('review');
            reviewDiv.innerHTML = `<h3>${title} by ${author} (${year}, ${page} pages)</h3><p>${review}</p>`;
            // Add the new review to the review list
            document.getElementById('reviewList').appendChild(reviewDiv);
            // Clear the form fields
            document.getElementById('bookTitle').value = '';
            document.getElementById('bookAuthor').value = '';
            document.getElementById('bookYear').value = '';
            document.getElementById('bookPage').value = '';
            document.getElementById('bookReview').value = '';
        });
    </script>
</body>
</html>
