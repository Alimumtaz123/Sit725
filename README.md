# Sit725
{
// Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "type": "chrome",
            "request": "launch",
            "name": "Launch Chrome against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
 30 changes: 30 additions & 0 deletions30  
index.html
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,30 @@
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>SIT 725 Prac 1</title>
<meta name="description" content="basic template for SIT 725 Prac 1">
<meta name="author" content="SitePoint">
<meta property="og:title" content="SIT 725 Prac 1">
<meta property="og:type" content="website">
<meta property="og:description" content="basic template for SIT 725 Prac 1">
<!-- Compiled and minified CSS -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.min.css">
</head>
<body>
<div class="container">
<div class="row">
<div class="col s12">
<h1 id="heading" class="center-align">SIT 725</h1>
</div>
<div class="col s12 center-align">
<a class="waves-effect waves-light btn" onclick="changeText()">Change Text</a>
</div>
</div>
</div>
<!-- Compiled and minified JavaScript -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/js/materialize.min.js"></script>
<script src="js/server.js"></script>
</body>
</html>
 10 changes: 10 additions & 0 deletions10  
js/server.js
Original file line number	Diff line number	Diff line change
@@ -0,0 +1,10 @@
function changeText(){
    var textsArray = ["Text 1","Text 2", "Text 3", "Text 4", "Text 5"]
    var number = getRandomNumberBetween(0,textsArray.length - 1)
    console.log("Index: ", number)
    document.getElementById("heading").innerHTML = textsArray[number];
}

function getRandomNumberBetween(min,max){
        return Math.floor(Math.random()*(max-min+1)+min);
