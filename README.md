<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Happy Birthday</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #f9d5e5, #ffd6a5);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Segoe UI', Arial, sans-serif;
      padding: 20px;
    }

    .card {
      background: linear-gradient(145deg, #fff3f8, #fff8e1);
      padding: 40px;
      border-radius: 25px;
      text-align: center;
      box-shadow: 0 15px 30px rgba(0,0,0,0.2);
      max-width: 650px;
      transition: all 0.5s ease;
      position: relative;
    }

    h1 {
      font-size: 48px;
      color: #e91e63;
      margin-bottom: 15px;
      text-shadow: 2px 2px #ffe0e6;
    }

    p {
      font-size: 18px;
      color: #555;
      line-height: 1.6;
      text-align: left;
      white-space: pre-wrap;
    }

    .cake {
      font-size: 60px;
      margin: 20px 0;
    }

    button {
      margin-top: 25px;
      padding: 12px 30px;
      font-size: 18px;
      border: none;
      border-radius: 25px;
      background: #ff4081;
      color: #fff;
      cursor: pointer;
      box-shadow: 0 5px 10px rgba(0,0,0,0.2);
      transition: transform 0.2s, background 0.3s;
    }

    button:hover {
      background: #e73370;
      transform: scale(1.05);
    }

    /* Surprise text style */
    .surprise-text {
      font-size: 20px;
      color: #d81b60;
      line-height: 1.6;
      text-align: left;
      white-space: pre-wrap;
      animation: fadeIn 1s ease;
      background: linear-gradient(135deg, #fff0f5, #fff8e1);
      padding: 25px;
      border-radius: 20px;
      box-shadow: 0 10px 20px rgba(0,0,0,0.1);
      position: relative;
    }

    /* Elegant flowers on top */
    .flowers {
      font-size: 50px;
      margin-bottom: 20px;
      display: inline-block;
      animation: floatIn 1s ease;
      text-shadow: 2px 2px #fff;
    }

    /* Confetti */
    .confetti {
      position: absolute;
      top: 0;
      font-size: 20px;
      animation: fall 3s linear forwards;
      pointer-events: none;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.95); }
      to { opacity: 1; transform: scale(1); }
    }

    @keyframes floatIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fall {
      to {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

  <div class="card" id="card">
    <h1>Happy Birthday!</h1>
    <div class="cake">🎂</div>
    <p>
      Wishing you a day filled with love, happiness,<br>
      and lots of sweet surprises!
    </p>

    <button onclick="showSurprise()">Click here for surprise 🎁</button>
  </div>

  <script>
    function showSurprise() {
      const card = document.getElementById("card");

      // Replace the card content with elegant message + flowers
      card.innerHTML = `
        <div class="surprise-text">
          <div class="flowers">💐🌸🌺💐</div>
happy birthdayyy ishh !!! 

im sorry for late greeetings huhu , its my final week huhu .
thats why i made a code for you ! this is all i can do for now since where not in the same country hehe
anw , happy birthday again ishiiii !! u'r 19 naa!!!! one more age and you will be removed to teen section HAHAHAH
JOKE. yushikoo baeza OR should i call ishiee (my favorite name for u), i know paulit ulit mo na to naririnig saken 
IM SO PROUDDD OF YOU!!! i wish in ur next journey will be filled with joy, laughter , love and peace ilovyouu ishhh enjoy ur day!! 
(drink responsively)
        </div>
      `;

      // Add some confetti
      for (let i = 0; i < 30; i++) {
        const confetti = document.createElement("div");
        confetti.className = "confetti";
        confetti.textContent = "🎉";
        confetti.style.left = Math.random() * 100 + "vw";
        confetti.style.animationDuration = (Math.random() * 2 + 2) + "s";
        document.body.appendChild(confetti);
        setTimeout(() => confetti.remove(), 3000);
      }
    }
  </script>

</body>
</html>
