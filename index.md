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
