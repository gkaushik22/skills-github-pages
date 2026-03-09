---
title: "My-First_BLOG"
date: 2026-03-09
---

### Adding High Score Persistence to Stack Overflown 🎮

Today I implemented a small but important feature in my **Stack Overflown game project** — saving and loading the player's high score using **localStorage**.

Previously, the score would reset every time the page refreshed. To improve the user experience, I added logic that stores the highest score in the browser so players can try to beat their previous record.

The following code loads the saved high score when the game starts:

```javascript
// Load high score from localStorage
highScore = parseInt(localStorage.getItem("stackOverflownHighScore")) || 0;
document.getElementById("high-score").textContent = highScore;
```

This works by retrieving the stored value from `localStorage`, converting it into a number using `parseInt`, and displaying it in the high score section of the interface.

Now, whenever the game loads, the previous high score is displayed automatically. This makes the gameplay more engaging because players always have a record to beat.

Next step: updating the high score dynamically whenever the player achieves a new record.
