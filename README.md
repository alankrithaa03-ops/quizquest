# QuizQuest — Demo Build

A single HTML file, no install needed. Double-click `index.html` to open it in a browser, or drop the folder into Netlify/Vercel/GitHub Pages for a live link.

## What's working in this demo
- **Avatar builder** — pick a color and an accessory, see a live preview.
- **Solo Practice** — pick a subject/chapter, play a full timed quiz, see your score.
- **Group Lobby** — "Create a Lobby" gives you a 4-digit room code; "Join a Lobby" lets a friend enter that code and see themselves added to the player list in real time.
- **Live quiz battle** — synced questions, countdown timer with speed bonus, live standings after every question, final podium.
- **Personal leaderboard** ("My Stats") — tracks quizzes played, correct answers, accuracy, and best score across sessions on this device.
- **Question bank** — 4 subjects × 2 chapters × 5 questions (Math, Science, History, Geography), plus a "type your own topic" option that instantly generates placeholder questions so you can demo the concept of AI-generated content.

## How to demo the multiplayer lobby
Multiplayer sync uses the browser's `BroadcastChannel`, which only works between tabs/windows on the **same device and browser** — there's no backend yet. For the demo:
1. Open `index.html` in one tab, enter a name, choose **Create a Lobby**, note the room code.
2. Open a second tab (or a couple more) to the same page, enter a different name, choose **Join a Lobby**, and type the code.
3. Back on the host tab, pick a subject and hit **Start Game** — all tabs will play the same questions and see each other's live scores.

## What's explicitly out of scope for tomorrow (say this to judges)
- Real cross-device multiplayer would need a backend (WebSockets or Firebase) instead of `BroadcastChannel` — same UI, different plumbing underneath.
- Real AI-generated questions from any topic — right now custom topics use a placeholder generator so the flow is demoable without needing an API key.
- Accounts/login, so the leaderboard could be shared across everyone instead of living per-device.

Framing it this way shows the judges you understand exactly what's prototype vs. what a v1 would need.
