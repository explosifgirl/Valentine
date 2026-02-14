# ValentineHtml
Copier le code
<!DOCTYPE html>
<html>
<head>
<title>Valentine Game 💖</title>
<style>
body {
  text-align:center;
  font-family:Arial;
  background-color:pink;
  height:100vh;
  margin:0;
  overflow:hidden;
}
button {
  padding:15px 30px;
  font-size:20px;
  margin:10px;
  position:relative;
  cursor:pointer;
}
#message {
  font-size:22px;
  margin-top:20px;
  color:darkred;
}
</style>
</head>
<body>

<h1>Will you be my Valentine? 💘</h1>

<button onclick="yes()">Yes 💖</button>
<button id="noBtn" onmouseover="move()">No 😭</button>
<button onclick="surprise()">Secret button 🤫</button>

<p id="message"></p>

<script>
function yes() {
  // Message de validation quand il clique sur Yes
  document.getElementById("message").innerHTML = "Yaaay 💕 I love you!";
}

function move() {
  // Bouger le bouton No et ajouter un message rigolo
  var x = Math.random() * (window.innerWidth - 100);
  var y = Math.random() * (window.innerHeight - 50);
  var btn = document.getElementById("noBtn");
  btn.style.position = "absolute";
  btn.style.left = x + "px";
  btn.style.top = y + "px";

  // Message de validation qui change à chaque mouvement
  document.getElementById("message").innerHTML = "Try again! 😏";
}

function surprise() {
  // Message secret
  document.getElementById("message").innerHTML = "You found the secret! 🎉💖";
}
</script>

</body>
</html>
