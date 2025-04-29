# Ex.08 Design of Interactive Image Gallery
# Date:29-04-2025
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
home.html:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
    <link rel="stylesheet" href="home.css">
</head>
<body>
    <h1>Interactive Photo Gallery</h1>
    <div class="gallery">
        <img src="doreamon.png" alt="Image 1" onclick="openModal(this)">
        <img src="Nobita.png" alt="Image 2" onclick="openModal(this)">
        <img src="shizuka.png" alt="Image 3" onclick="openModal(this)">
        <img src="sunio.png" alt="Image 4" onclick="openModal(this)">
        <img src="Jaian.png" alt="Image 5" onclick="openModal(this)">
    </div>

    <div class="modal" id="imageModal">
        <span onclick="closeModal()">&times;</span>
        <img id="modalImage" src="" alt="">
    </div>
    <script src="home.js"></script>
</body>
</html>


home.css:
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    text-align: center;
    background-color: #f4f4f4;
    background-image: url("doraemonbg.png.jpg");
    background-size:cover;
    
}

h1 {
    margin-top: 20px;
    margin-top:50px;
    font-family:"caveat";
    font-size:70px;
    color:#ffffff;
}

.gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 15px;
    padding: 20px;
    margin-top:110px;
}

.gallery img {
    width: 200px;
    height: 150px;
    border: 2px solid #ccc;
    border-radius: 8px;
    cursor: pointer;
    transition: transform 0.3s, box-shadow 0.3s;
}

.gallery img:hover {
    transform: scale(1.1);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    justify-content: center;
    align-items: center;
    z-index: 1000;
}

.modal img {
    max-width: 90%;
    max-height: 90%;
    border: 4px solid white;
    border-radius: 10px;
}

.modal span {
    position: absolute;
    top: 20px;
    right: 40px;
    font-size: 30px;
    color: white;
    cursor: pointer;
    font-weight: bold;
}

home.js:

function openModal(image) {
    const modal = document.getElementById('imageModal');
    const modalImg = document.getElementById('modalImage');
    modal.style.display = 'flex';
    modalImg.src = image.src;
}

// Function to close the modal
function closeModal() {
    const modal = document.getElementById('imageModal');
    modal.style.display = 'none';
}
```
# OUTPUT:
![alt text](<Screenshot 2025-04-29 060951.png>)
![alt text](<Screenshot 2025-04-29 061001.png>)
![alt text](<Screenshot 2025-04-29 061011.png>)
![alt text](<Screenshot 2025-04-29 061020.png>)
![alt text](<Screenshot 2025-04-29 061032.png>)
![alt text](<Screenshot 2025-04-29 061043.png>)
# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
