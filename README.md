# Sample-website
#My first ever sample website

#Html code
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
    <link href="styles/style.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&family=Fuggles&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Ruslan+Display&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Shadows+Into+Light&display=swap" rel="stylesheet">
  </head>
  <body>

    <h1>“Taking an image, freezing a moment, reveals how rich reality truly is.”</h1>
    <img src="images/camera.jpg" alt="Image of a camera">
    <p>*Packed with an array of powerful features in an incredibly compact frame, the Nikon D750 is the ideal companion on your shooting journeys.Experience improved convenience with the tilting LCD monitor as well as the built-in Wi-Fi® function for on-the-spot sharing.<a href="https://www.nikon.co.in/en_IN/product/digital-slr-cameras/d750#features_explained/1">Click Shick</a> With the most sought after features in one complete package, the Nikon D750 is truly the camera you have been waiting for.</p>
    <ul>
      <li>Enhanced maneuverability now combined with FX format and 24.3 megapixels</li>
      <li>Compact,lightweight and slim body with a tough, durable desugn to expand the field of potential</li>
      <li>Three image area options to change your angle of view</li>
    </ul>
    <script src="scripts/main.js"></script>
    <button>Change user</button>
  </body>
</html> 

#CSS code
h1
{
    text-align: center;
  font-family: 'Ruslan Display', cursive;
}
p
{
  font-family: 'Dancing Script', cursive;
  letter-spacing: 1px;   
}
ul
{
  font-family: 'Shadows Into Light', cursive;
}
html
{
  background-color: #08919B;
}
body {
  width: 800px;
  margin: 0 auto;
  background-color: #8E089B;
  padding: 0 20px 20px 30px;
  border: 5px solid black;
}
img {
  display: block;
  margin: 0 auto;
}

#Javascript code
let myImage = document.querySelector('img');

myImage.onclick = function() {
    let mySrc = myImage.getAttribute('src');
    if(mySrc === 'images/firefox-icon.png') {
      myImage.setAttribute('src','images/water-scenary.jpg');
    } else {
      myImage.setAttribute('src','images/water-scenary.jpg');
    }
}

let myButton = document.querySelector('button');
let myHeading = document.querySelector('h1');

function setUserName() {
  let myName = prompt('Please enter your name.');
  localStorage.setItem('name', myName);
  myHeading.textContent = 'Mozilla is cool, ' + myName;
}

if(!localStorage.getItem('name')) {
  setUserName();
} else {
  let storedName = localStorage.getItem('name');
  myHeading.textContent = 'Life becomes beautiful when you capture shots., ' + storedName;
}
myButton.onclick = function() {
  setUserName();
}

function setUserName() {
  let myName = prompt('Please enter your name.');
  if(!myName) {
    setUserName();
  } else {
    localStorage.setItem('name', myName);
    myHeading.textContent = 'Mozilla is cool, ' + myName;
  }
}

#I have take pictures from unsplash,content from Nikon website and help of code from MDN
#My first step of learning web development begins from here.
