# Rock ✊🧻✌️ Paper Scissors — HTML · CSS · JavaScript

A small, responsive, and accessible **Rock Paper Scissors** web game built with plain HTML, CSS and JavaScript — perfect for a GitHub repo demo, beginner portfolio project, or a tiny playable component to embed in other pages.

---

## 🚀 Live demo

Include a GitHub Pages link here after you publish the repo (for example: `https://<shivam-1325>.github.io/rock-paper-scissors/`).

---

## 🎯 Features

* Pure vanilla HTML/CSS/JS (no frameworks or build tools)
* Responsive layout that works on desktop and mobile
* Simple game logic: player vs computer
* Score tracking (session-only — resets on page reload)
* Smooth animations and visual feedback for wins/losses/ties
* Keyboard support and accessible buttons
* Easy to read and extend — great for beginners

---

## 🧩 Gameplay

1. Choose **Rock**, **Paper**, or **Scissors** by clicking a button (or using keyboard keys).
2. The computer randomly selects its move.
3. The result (Win / Lose / Tie) is shown with a short animation and the scores update.

Rules: Rock beats Scissors, Scissors beats Paper, Paper beats Rock.

---

## 📁 Repo structure (suggested)

```
rock-paper-scissors/
├─ index.html
├─ css/
│  └─ style.css
├─ js/
│  └─ script.js
├─ assets/
│  └─ (images, icons, or a demo.gif)
└─ README.md
```

---

## 🛠️ Installation & usage

1. Clone the repo:

```bash
git clone https://github.com/<your-username>/rock-paper-scissors.git
cd rock-paper-scissors
```

2. Open `index.html` in your browser, or serve with a static server:

```bash
# using Python 3
python -m http.server 8000
# then open http://localhost:8000
```

---

## ✨ Example `index.html` (minimal)

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Rock Paper Scissors</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <main class="game">
    <h1>Rock Paper Scissors</h1>
    <div class="scoreboard">
      <span id="player-score">0</span> : <span id="computer-score">0</span>
    </div>
    <div class="choices">
      <button data-move="rock">✊ Rock</button>
      <button data-move="paper">🧻 Paper</button>
      <button data-move="scissors">✌️ Scissors</button>
    </div>
    <div id="result" class="result" aria-live="polite"></div>
  </main>
  <script src="js/script.js"></script>
</body>
</html>
```

---

## 🧠 Example `script.js` (core logic)

```js
const moves = ['rock','paper','scissors'];
const getComputerMove = () => moves[Math.floor(Math.random()*moves.length)];

const decide = (player, computer) => {
  if (player === computer) return 'tie';
  if (
    (player === 'rock' && computer === 'scissors') ||
    (player === 'scissors' && computer === 'paper') ||
    (player === 'paper' && computer === 'rock')
  ) return 'win';
  return 'lose';
};

// Hook up DOM, update scoreboard & show animations — keep UI code separate from logic for clarity.
```

---

## ♻️ Customization ideas

* Add persistent scores using `localStorage`
* Add animations or sound effects for feedback
* Add themes (dark/light) and keyboard-only controls
* Add multiplayer over WebRTC or simple turn-based using Firebase

---

## ✅ Contribution

Contributions welcome! Open an issue or pull request with improvements, bug fixes, or new features.

---

## 📄 License

Choose a license for your repo (MIT recommended for small demos). Add a `LICENSE` file.

---

If you want, I can also:

* generate the `index.html`, `css/style.css`, and `js/script.js` files for you, ready to copy into your repo
* create a short demo GIF or instructions for publishing on GitHub Pages

Happy coding — have fun! 🎮
# Rock-Scissor-Game
