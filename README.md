# ⚡ TYPONIX — Cyberpunk Arcade Typing Engine

[![Live Demo](https://img.shields.io/badge/Live_Demo-Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://typonix-zeta.vercel.app/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)]()
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)]()
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

> **Submission for Hackathon Evaluation**  
> 🌐 **Live Application:** [https://typonix-zeta.vercel.app/](https://typonix-zeta.vercel.app/)

---

## 📌 Executive Summary

**Typonix** (also branded as *Cyber Type*) is a high-speed, retro-futuristic browser arcade game that reimagines touch-typing practice through dynamic gameplay loop mechanics. Built using pure vanilla JavaScript, Web Audio API, Web Speech API, and HTML5 Canvas, the application runs entirely client-side with **zero external dependencies or heavy JS frameworks**, delivering high performance and low-latency interaction.

Players eliminate falling code packets before system perimeters are breached, managing active combat utilities, procedural system perks, real-time combo chains, and tailored visual modes.

---

## 💡 Problem Statement & Solution

* **The Problem:** Traditional typing tutors are repetitive, lack player engagement, and rely on static input tests without dynamic stress conditions.
* **The Solution:** Typonix merges arcade combat mechanics—such as dynamic target switching, real-time WPM calculation, custom word velocity scaling, interactive power-ups, and post-run precision diagnostics—to transform muscle memory development into an immersive gaming experience.

---

## 🔥 Key Technical Features

### 1. 🧮 Dynamic Difficulty & Game Engine
* **Dynamic Speed Scaling:** Word velocity scales according to both player level and word length ($V_{\text{speed}} = f(\text{level}, \text{length})$).
* **Perimeter Collision Detection:** Real-time tracking of element positions with visual explosion particle bursts upon destruction or system breach.
* **Target Lock Mechanics:** Intelligent target isolation locks onto active typing targets based on the initial keypress, supporting simultaneous target management.

### 2. ⚡ Active Power-Ups & Procedural Perks
* **❤️ Heart Bonus:** Restores system integrity[cite: 1].
* **💣 EMP Blast:** Clears all active on-screen code packets instantly[cite: 1].
* **⏱️ Time Freeze:** Applies a temporal slow-down multiplier to descending targets[cite: 1].
* **🆙 Procedural System Upgrades:** Every 5 levels, players pick 1 of 3 randomized perks (*Bonus Magnet*, *Heart Surplus*, *Overclock*, *Precision Engine*) to adapt their strategy[cite: 1].

### 3. 🔊 Custom Audio Synthesizer & Speech Engine
* **Web Audio API Engine:** Synthesizes custom keypress audio, error indicators, level-up arpeggios, and overdrive frequencies programmatically without external audio files[cite: 1].
* **Web Speech Integration:** Vocalizes incoming words and power-up activations dynamically using browser speech synthesis[cite: 1].
* **Audio Profiles:** Toggle between **Cyber Synth** and **Mechanical Keyboard** audio responses[cite: 1].

### 4. 🎨 Deep Customization & Responsive FX
* **Canvas Visuals:** Includes particle burst systems, mouse-following light cursors, matrix rain generators, and perspective 3D grid scroll animations[cite: 1].
* **Interactive Themes & Typography:** Offers 4 CSS variable-driven visual themes (*Cyber Cyan*, *Neon Purple*, *Matrix Green*, *Synth Pink*) and 6 custom Google Fonts (*Orbitron*, *JetBrains Mono*, *Press Start 2P*, *Rubik Glitch*, *Cinzel Decorative*, *Dancing Script*)[cite: 1].

### 5. 📊 Real-Time Analytics & Diagnostic Feedback
* Tracks real-time **Words Per Minute (WPM)**, **Accuracy %**, and **Combo Multipliers** during gameplay[cite: 1].
* **Weak Key Analysis:** Evaluates keypress history to highlight specific keys with low accuracy ratings on the post-game summary screen[cite: 1].

---

## 🎮 How to Play

| Key / Action | Function |
| :--- | :--- |
| <kbd>SPACE</kbd> | Launch game from start / restart screen[cite: 1] |
| <kbd>A</kbd> – <kbd>Z</kbd> | Type matching on-screen targets[cite: 1] |
| <kbd>ESC</kbd> | Pause / Resume session[cite: 1] |

1. **Targeting:** Type the first letter of a falling word to target it, then complete the full word to destroy it[cite: 1].
2. **Combo Chains:** Chain accurate words to raise combo multipliers and trigger **Overdrive Mode**[cite: 1].
3. **Power-Ups:** Target special power-up words to trigger abilities like Time Freeze and EMP blasts[cite: 1].

---

## 🛠️ Architecture & Tech Stack

```text
       ┌─────────────────────────────────────────────────────────┐
       │                       INDEX.HTML                        │
       │  (DOM Structure, Modals, SVGs, Dynamic CSS Variables)   │
       └───────────────────────────┬─────────────────────────────┘
                                   │
         ┌─────────────────────────┼─────────────────────────┐
         ▼                         ▼                         ▼
┌──────────────────┐     ┌──────────────────┐     ┌──────────────────┐
│   CANVAS ENGINE  │     │   GAME STATE     │     │   AUDIO ENGINE   │
│ • Particle Burst │     │ • Speed Scaling  │     │ • Web Audio Synth│
│ • 3D Grid Scroll │     │ • Target Lock    │     │ • Speech Synthesis│
│ • Mouse Glow FX  │     │ • Analytics/WPM  │     │ • Sound Profiles │
└──────────────────┘     └──────────────────┘     └──────────────────┘
