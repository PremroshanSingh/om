# om
Shiv ajj bhi GURU hai 
# 🔮 Astrology Web App

Welcome to the **Astrology Web App** – a multi-page interactive experience that lets users explore zodiac signs, daily horoscopes, and astrological compatibility.

Built with ❤️ by **PREMROSHAN**

---

## 🌠 Features

- 🧭 Select your zodiac sign and view personalized horoscopes
- 💞 Check compatibility between two signs
- 📅 Daily, weekly, and monthly predictions
- 🎨 Stylish, responsive design for mobile and desktop

---

## 🛠️ Tech Stack

- **HTML5** – Structure
- **CSS3** – Styling and layout
- **JavaScript** – Interactivity and logic
- *(Optional)* **Bootstrap** – Responsive design
- *(Optional)* **API Integration** – For live horoscope data

---

## 🚀 How to Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/astrology-app.git
<!DOCTYPE html>
<html>
<head>
  <title>Astrology App – Home</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <nav>
    <a href="index.html">Home</a>
    <a href="horoscope.html">Horoscope</a>
    <a href="compatibility.html">Compatibility</a>
    <a href="birthchart.html">Birth Chart</a>
  </nav>

  <h1>🔮 Welcome to PREMROSHAN's Astrology App</h1>
  <p>Find your zodiac sign:</p>
  <input type="date" id="birthdate">
  <button onclick="findZodiac()">Find My Sign</button>
  <h2 id="zodiacResult"></h2>

  <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html>
<head>
  <title>Daily Horoscope</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <nav>
    <a href="index.html">Home</a>
    <a href="horoscope.html">Horoscope</a>
    <a href="compatibility.html">Compatibility</a>
    <a href="birthchart.html">Birth Chart</a>
  </nav>

  <h1>📖 Your Daily Horoscope</h1>
  <button onclick="getHoroscope()">Show Horoscope</button>
  <p id="horoscope"></p>

  <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html>
<head>
  <title>Compatibility Checker</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <nav>
    <a href="index.html">Home</a>
    <a href="horoscope.html">Horoscope</a>
    <a href="compatibility.html">Compatibility</a>
    <a href="birthchart.html">Birth Chart</a>
  </nav>

  <h1>💞 Check Zodiac Compatibility</h1>
  <select id="sign1">
    <option>Aries</option><option>Taurus</option><option>Gemini</option>
    <option>Cancer</option><option>Leo</option><option>Virgo</option>
    <option>Libra</option><option>Scorpio</option><option>Sagittarius</option>
    <option>Capricorn</option><option>Aquarius</option><option>Pisces</option>
  </select>
  <select id="sign2">
    <option>Aries</option><option>Taurus</option><option>Gemini</option>
    <option>Cancer</option><option>Leo</option><option>Virgo</option>
    <option>Libra</option><option>Scorpio</option><option>Sagittarius</option>
    <option>Capricorn</option><option>Aquarius</option><option>Pisces</option>
  </select>
  <button onclick="checkCompatibility()">Check</button>
  <p id="compatibilityResult"></p>

  <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html>
<head>
  <title>Birth Chart Calculator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <nav>
    <a href="index.html">Home</a>
    <a href="horoscope.html">Horoscope</a>
    <a href="compatibility.html">Compatibility</a>
    <a href="birthchart.html">Birth Chart</a>
  </nav>

  <h1>🧮 Birth Chart Calculator</h1>
  <input type="date" id="birthdate">
  <input type="time" id="birthtime">
  <input type="text" id="location" placeholder="City of birth">
  <button onclick="calculateChart()">Calculate</button>
  <div id="chartResult"></div>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(to right, #1e3c72, #2a5298);
  color: white;
  text-align: center;
  padding: 50px;
}

nav {
  background-color: #222;
  padding: 10px;
  text-align: center;
}
nav a {
  color: white;
  margin: 0 15px;
  text-decoration: none;
  font-weight: bold;
}
nav a:hover {
  color: #ff9800;
}

input, button, select {
  padding: 10px;
  font-size: 16px;
  margin: 10px;
  border-radius: 5px;
  border: none;
}
button {
  background-color: #ff9800;
  color: white;
  cursor: pointer;
}
function findZodiac() {
  const date = new Date(document.getElementById("birthdate").value);
  const month = date.getMonth() + 1;
  const day = date.getDate();
  let sign = "";

  if ((month == 1 && day >= 20) || (month == 2 && day <= 18)) sign = "Aquarius ♒";
  else if ((month == 2 && day >= 19) || (month == 3 && day <= 20)) sign = "Pisces ♓";
  else if ((month == 3 && day >= 21) || (month == 4 && day <= 19)) sign = "Aries ♈";
  else if ((month == 4 && day >= 20) || (month == 5 && day <= 20)) sign = "Taurus ♉";
  else if ((month == 5 && day >= 21) || (month == 6 && day <= 20)) sign = "Gemini ♊";
  else if ((month == 6 && day >= 21) || (month == 7 && day <= 22)) sign = "Cancer ♋";
  else if ((month == 7 && day >= 23) || (month == 8 && day <= 22)) sign = "Leo ♌";
  else if ((month == 8 && day >= 23) || (month == 9 && day <= 22)) sign = "Virgo ♍";
  else if ((month == 9 && day >= 23) || (month == 10 && day <= 22)) sign = "Libra ♎";
  else if ((month == 10 && day >= 23) || (month == 11 && day <= 21)) sign = "Scorpio ♏";
  else if ((month == 11 && day >= 22) || (month == 12 && day <= 21)) sign = "Sagittarius ♐";
  else if ((month == 12 && day >= 22) || (month == 1 && day <= 19)) sign = "Capricorn ♑";

  document.getElementById("zodiacResult").innerText = `Your zodiac sign is: ${sign}`;
  localStorage.setItem("userSign", sign);
}

async function getHoroscope() {
  const sign = localStorage.getItem("userSign")?.split(" ")[0] || "Aries";
  const response = await fetch(`https://aztro.sameerkumar.website/?sign=${sign}&day=today`, {
    method: 'POST'
  });
  const data = await response.json();
  document.getElementById("horoscope").innerText = data.description;
}

function checkCompatibility() {
  const s1 = document.getElementById("sign1").value;
  const s2 = document.getElementById("sign2").value;
  const compatiblePairs = {
    Aries: ["Leo", "Sagittarius"],
    Taurus: ["Virgo", "Capricorn"],
    Gemini: ["Libra", "Aquarius"],
    Cancer: ["Scorpio", "Pisces"],
    Leo: ["Aries", "Sagittarius"],
    Virgo: ["Taurus", "Capricorn"],
    Libra: ["Gemini", "Aquarius"],
    Scorpio: ["Cancer", "Pisces"],
    Sagittarius: ["Aries", "Leo"],
    Capricorn: ["Taurus", "Virgo"],
    Aquarius: ["Gemini", "Libra"],
    Pisces: ["Cancer", "Scorpio"]
  };
  const result = compatiblePairs[s1].includes(s2)
    ? "💞 Compatible!"
    : "⚠️ Might need some cosmic effort!";
  document.getElementById("compatibilityResult").innerText = `${s
  
