# Ex.08 Design of Interactive Image Gallery
## Date:17/12/2024

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
gallery.html

<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Creative Gallery</title>
    <style>
        
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: url('color.png') no-repeat center center/cover; 
            color: rgb(233, 227, 227);
            text-align: center;
        }

        h1 {
            margin-top: 20px;
            font-size: 3em;
            text-shadow: 2px 2px 4px black;
        }

        
        .gallery-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr); 
            gap: 10px;
            padding: 20px;
            max-width: 90%;
            margin: 0 auto;
            background-color: rgba(0, 0, 0, 0.5); 
            border-radius: 10px;
        }

        
        .gallery-container img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            border: 3px solid #faf4f4;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        
        .gallery-container img:hover {
            transform: scale(1.05);
        }

        
        #modal {
            display: none;
            position: fixed;
            z-index: 1000;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
        }

        #modal img {
            margin: auto;
            display: block;
            max-width: 80%;
            max-height: 80%;
            position: relative;
            top: 10%;
        }

        #close {
            position: absolute;
            top: 20px;
            right: 30px;
            color: rgb(253, 250, 250);
            font-size: 2em;
            cursor: pointer;
        }
        footer {
            background: rgba(0, 0, 0, 0.7);
            color: #ddd;
            text-align: center;
            padding: 10px;
            font-size: 1em;
        }
        footer a {
            color: #fff;
            text-decoration: none;
            font-weight: bold;
        }
        footer a:hover {
            color: #00c3ff;
        }
    </style>
</head>
<body>
    
    <h1>My Creative Gallery</h1>

    
    <div class="gallery-container">
        <img src="1.png" alt="Image 1" onclick="openModal(this)">
        <img src="2 (3).png" alt="Image 2" onclick="openModal(this)">
        <img src="3.png" alt="Image 3" onclick="openModal(this)">
        <img src="4.png" alt="Image 4" onclick="openModal(this)">
        <img src="5.png" alt="Image 5" onclick="openModal(this)">
        <img src="6.png" alt="Image 6" onclick="openModal(this)">
        <img src="7.png" alt="Image 7" onclick="openModal(this)">
        <img src="8.png" alt="Image 8" onclick="openModal(this)">
    </div>

    <div id="modal">
        <span id="close" onclick="closeModal()">&#10006;</span>
        <img id="modalImage" src="" alt="Expanded View">
    </div>

    <footer>
        <p>Designed and Developed by: V Rishon Anand (24900460) </p>
    </footer>


    
    <script>
        
        function openModal(image) {
            const modal = document.getElementById("modal");
            const modalImage = document.getElementById("modalImage");
            modal.style.display = "block";
            modalImage.src = image.src;
        }

        
        function closeModal() {
            document.getElementById("modal").style.display = "none";
        }
    </script>
</body>
</html>

```

## OUTPUT:
![alt text](<Screenshot 2024-12-17 092239.png>)
![alt text](<Screenshot 2024-12-17 092416.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
