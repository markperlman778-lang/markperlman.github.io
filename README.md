[indext.html.txt](https://github.com/user-attachments/files/23267633/indext.html.txt)# markperlman.github.io[style.css](https://github.com/user-attachments/files/23267607/style.css)
body {
  font-family: Arial, sans-serif;
  background-color: #121212;
  color: white;
  text-align: center;
  margin-top: 50px;
}

button {
  margin: 10px;
  padding: 10px 20px;
  cursor: pointer;
}

input {
  padding: 10px;
  width: 200px;
}
[Uploading indext.ht<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Kid Laroi Heardle</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <h1>Kid Laroi Heardle</h1>
    <button id="playBtn">Play Song Snippet</button>
    <input type="text" id="guess" placeholder="Type the song name">
    <button id="checkBtn">Guess</button>
    <p id="message"></p>
  </div>
  <script src="script.js"></script>
</body>
</html>
ml.txt…]()[script.js.txt](https://github.com/user-attachments/files/23267637/script.js.txt)
// List of songs (just examples, you can replace with real Kid Laroi songs)
const songs = [
  { name: "Without You", file: "songs/without-you.mp3" },
  { name: "Stay", file: "songs/stay.mp3" },
];

let currentSong = songs[0]; // just use the first song for now

const playBtn = document.getElementById("playBtn");
const checkBtn = document.getElementById("checkBtn");
const guessInput = document.getElementById("guess");
const message = document.getElementById("message");

playBtn.addEventListener("click", () => {
  let audio = new Audio(currentSong.file);
  audio.play();
});

checkBtn.addEventListener("click", () => {
  const guess = guessInput.value.trim().toLowerCase();
  if (guess === currentSong.name.toLowerCase()) {
    message.textContent = "✅ Correct!";
  } else {
    message.textContent = "❌ Try again!";
  }
});


