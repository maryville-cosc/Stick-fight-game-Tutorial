# Build a Stick-Fight Game in the Browser Using an AI Assistant

If you've never seen a two-fighter arcade brawler before, think of it like a very simple version of a fighting game: two stick figures on a stage, one you control and one the computer controls, punching until someone's health runs out.

In this activity, you will build a simple fighting game that runs entirely in your web browser. You will not install any software, and you will not use a server. Everything will be plain HTML and JavaScript that you can double-click and run from your hard drive.

Instead of writing all the code yourself, you will learn how to **direct an AI assistant** (like ChatGPT or Claude) to help you build the game step by step using *good prompting*. This is a powerful skill used by professional programmers today.

> **Goal:** Learn how to think like a programmer and how to communicate clearly with an AI tool.

---

## How to Prompt Your AI Assistant Properly

AI assistants work best when you give them **very small, clear instructions**. Do *not* ask for the whole game at once.

### Good Prompt Examples

- "Draw a stick figure — a circle for the head, lines for the body, arms, and legs — standing on a line near the bottom of the canvas."
- "Make my stick figure move left and right when I press A and D."
- "Add a jump when I press W, using gravity so it comes back down and lands on the ground."
- "Add a punch when I press Space that only lands as a hit if the two fighters are close together and facing each other."

### Bad Prompt Examples

- "Make the whole fighting game."
- "Add everything a real fighting game would have."
- "It doesn't work" (without saying what is wrong).

---

## Debugging Tip

When something looks wrong, describe **exactly what you see**:

- "My fighter walks straight through the edge of the canvas instead of stopping."
- "The punch damages the enemy even when I'm standing far away from them."
- "The enemy throws a punch every single frame instead of pausing between swings."
- "Pressing jump while I'm already in the air lets me fly off the top of the screen."

This is how real programmers debug problems — not "it's broken," but a precise description of the wrong behavior.

---

## What You're Really Learning

- How a game keeps track of state (position, health, cooldowns) one frame at a time
- How a game loop (`requestAnimationFrame`) and gravity/physics work
- How hit detection and attack cooldowns work
- How simple game AI is often just a handful of `if`/`else` rules, not "real" intelligence
- How to debug problems logically
- How to communicate clearly with an AI coding assistant

> You are not just building a game — you are learning how modern programmers work.

---

## Before You Start

1. Open your browser and go to an AI chat tool — for example ChatGPT (chatgpt.com) or Claude (claude.ai).
2. Depending on the tool, you may be able to use it for free without logging in, or you may need a free account. Either is fine for this project.
3. On your Desktop, create an empty file named `stick-fight.html`.
4. Open `stick-fight.html` in a plain text editor (Notepad, TextEdit, or VS Code). This is where you will paste the code the AI gives you.
5. Also open `stick-fight.html` in a browser window by double-clicking it, so you have a live view of your game.
6. Each time the AI gives you code, paste it into `stick-fight.html` in your text editor, save it, then switch to the browser tab and refresh.
7. Test your changes after every single step — do not wait until the end to check anything.
8. Fix bugs as they appear. This is normal, even for professional programmers.

---

## Step-by-Step Build Plan

Ask your AI assistant for each step **one at a time**.

The bulleted items below are not the prompts. You will need to experiment to turn them into your own clear instructions. A few full example prompts are given further down to help you get started.

### Step 1 – Your Fighter

Here's your first prompt to get you started:

> I want to create a new web page to play a simple stick-figure fighting game. I'd like it to be front-end only, contained in a single stick-fight.html file. Start with an HTML canvas showing one stick figure — a circle for the head, and lines for the body, arms, and legs — standing on a ground line near the bottom of the screen.

- Draw a head, body, arms, and legs using simple shapes.
- Draw a ground line near the bottom of the canvas.
- Keep the character standing still for now — movement comes next.

### Step 2 – Movement

- Make the fighter move left when you hold A and right when you hold D.
- Keep the fighter from walking off either edge of the canvas.

### Step 3 – Jumping

- Make the fighter jump when you press W.
- Use gravity so the fighter falls back down and lands on the ground instead of floating.

### Step 4 – Punching

- Add a punch animation when you press Space.
- Make the punch only count as a hit if an opponent is within range and you're facing them.
- Add a short cooldown so you can't punch nonstop.

### Step 5 – The Opponent

- Add a second stick figure in a different color, standing on the other side of the stage.
- For now, it can just stand still — the computer will control it starting in Step 7.

### Step 6 – Health Bars & Damage

- Give each fighter a health bar at the top of the screen.
- Reduce an opponent's health whenever a punch lands on them.

### Step 7 – Simple AI

- Make the opponent walk toward you when it's far away.
- Make it throw its own punch when it's close enough, on its own cooldown.

### Step 8 – Win, Lose, and Restart

- End the round and show a message when either fighter's health reaches zero.
- Add a button that resets both fighters to full health so you can play again.

### Step 9 – Balance the Fight

- Play a few rounds. If the opponent feels too relentless (or too passive), describe that feeling to your AI assistant and ask it to adjust.
- A good fix is usually: make it hesitate sometimes instead of always attacking, and have it back off for a moment after landing a hit instead of chaining punches.
- This step is great practice for describing a *feeling* about how the game plays, rather than a technical bug — that's a different (and just as important) kind of instruction to give an AI.

---

## AI Ethics Checkpoint

Choose three topics below. For each one, paste the prompt into your AI assistant, read the answer, and decide what you think. These are discussion prompts, not coding prompts.

1. **Authorship and credit** — If the AI helped write this game, what did I create, and what should I give credit for?
2. **Learning vs. outsourcing** — How can I use AI for help without letting it do all the learning for me? Give me three practical rules.
3. **Copying and originality** — Does AI make it easier to copy someone else's game? What responsibility do I have to make my version original?
4. **Trust but verify** — What are three things in this game's code I should check myself instead of trusting the AI automatically?
5. **Transparency** — If I show this game to someone, should I tell them AI helped build it? Give both sides briefly, then give your recommendation.
6. **Privacy** — What personal information should I avoid typing into an AI chat tool on a shared computer? Keep it practical.
7. **Responsibility** — What responsibilities do I have when using AI to create software? Give me five short points.
8. **Bias and accessibility** — Could an AI helper forget about players with different abilities (reaction speed, colorblindness, etc.)? How could I make this game easier for more people to play?

---

## Example Prompts

These are full example prompts, written the way you'd actually type them, to help you get unstuck if you're not sure how to phrase your own.

**Getting started:**

> I want to create a new web page to play a simple stick-figure fighting game. I'd like it to be front-end only, contained in a single stick-fight.html file. Start with a canvas showing one stick figure standing on a ground line near the bottom of the screen.

**Adding movement and jumping:**

> Make my stick figure move left when I hold A and right when I hold D, and stop it from walking off either edge of the canvas. Also let it jump when I press W — use gravity so it comes back down and lands on the ground line instead of floating.

**Adding the punch:**

> Add a punch when I press Space. Show a short animation where the arm reaches out in front of the fighter. It should only count as a hit if an opponent is within about 70 pixels and the fighter is facing them, and there should be a short cooldown before it can punch again.

**Adding the opponent and simple AI:**

> Add a second stick figure in a different color as my opponent. Give it simple AI: if it's far from me, have it walk closer; if it's close enough, have it stop and throw its own punch on its own cooldown. It should always face toward me.

**Adding health, win/lose, and restart:**

> Give both fighters a health bar at the top of the screen. When a punch lands, subtract damage from the health of whoever got hit. When either fighter's health reaches zero, stop the game, show "YOU WIN" or "CPU WINS," and show a button that resets both fighters to full health so we can play again.

**Balancing the AI:**

> Right now the opponent attacks constantly and it doesn't feel fair. Can you make it hesitate sometimes instead of always advancing or attacking, and have it back away for a bit after it lands a punch instead of immediately swinging again?

---

*A finished reference version of this game (`stick-fight.html`) is available separately if you'd like to compare your result or use it as an answer key.*
