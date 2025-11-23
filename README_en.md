# One Shot, One Room 🎯

> **Status:** Playable Prototype (MVP)  
> **Genre:** Top-Down Action / Puzzle / Stealth

**One Shot, One Room** is a tactical game prototype developed in pure HTML5 and JavaScript (Vanilla JS). The game combines the fast-paced lethality of *Hotline Miami* with physics and ricochet mechanics.

The player has only **one piece of ammunition**. The magic ball does not reload on its own; it must be physically recovered after each shot, creating a constant cycle of tension between attack and vulnerability.

---

## 🎮 How to Play

The objective is to survive waves of enemies by using the layout of the rooms to your advantage.

### Controls
| Action | Input (Keyboard/Mouse) |
| :--- | :--- |
| **Move** | `W`, `A`, `S`, `D` or Arrow Keys |
| **Aim** | Mouse |
| **Shoot** | Left Click (LMB) |
| **Reload** | Walk to the stationary ball to pick it up |

### Core Mechanics
1.  **The Single Bullet:** Your weapon is a physical projectile. If you miss or the ball stops far away, you will be defenseless until you run and retrieve it.
2.  **Lethal Geometry:** The ball ricochets off walls. Use angles to hit enemies in other rooms without exposing yourself.
3.  **Line of Sight (LOS) System:** Enemies use Line of Sight. They do not see you through walls.
    * 🔴 **Dark Red:** Patrolling/Idle (Has not seen you).
    * 🚨 **Bright Red:** Chasing (Has seen you).

---

## 🚀 How to Run the Game

This is a pure client-side project. It does not require any installation (Node, Python, etc.).

1.  Download the `index.html` file (or clone this repository).
2.  Open the file directly in any modern browser (Chrome, Firefox, Edge, Brave).
3.  The game will start automatically.

---

## 🔮 Roadmap & Future Improvements

Although the core mechanic is functional, the plan to turn this prototype into a commercial game (Steam/Itch.io) includes the following expansions:

### 1. Visuals & "Game Juice" (Polish)
* [ ] **Dynamic Lighting:** Implement a light and shadow system (Raycasting). Unvisited rooms should be dark (Fog of War), illuminated only by the ball's trail.
* [ ] **Visceral Feedback:** Add Screen Shake on impacts and Hit Stop (millisecond freezes) when eliminating enemies.
* [ ] **Permanent Decals:** Eliminated enemies leave marks on the ground, telling the story of the battle.

### 2. Enemy Design (Archetypes)
To force new strategies beyond "run and shoot":
* [ ] **The Sniper:** A stationary enemy with a long line of sight and a hitscan shot.
* [ ] **The Shield Bearer:** Has frontal armor. The player is **forced** to use wall ricochets to hit them from behind.
* [ ] **The Kamikaze:** Explodes upon death, creating a temporary danger zone that prevents the player from immediately recovering the ball.

### 3. Meta-Game (Roguelike)
* [ ] **Procedural Generation:** Replace the fixed map with random generation of rooms and corridors.
* [ ] **Relic System:** At the end of each level, the player chooses an upgrade:
    * *Magnet:* The ball slowly returns when holding the spacebar.
    * *Heavy Ball:* Pierces the first enemy and kills the second.
    * *Trail Blaze:* The ball leaves a trail of fire that causes area damage.

### 4. Immersive Audio
* [ ] **Dynamic Soundtrack:** The music smoothly transitions between "Low/Tension" (Stealth) and "Drums/Aggressive" (Combat) depending on the enemies' state.

### 5. Technology Migration
* [ ] Port the logic from pure JavaScript to a dedicated engine (**Godot 4** or **GameMaker**) to ensure native performance, controller support (gamepad), and easier exporting.

---

## 🛠️ Technologies and Algorithms

This prototype was created to demonstrate Game Design concepts without external dependencies.

* **Rendering:** HTML5 Canvas API.
* **Collision:** AABB (Axis-Aligned Bounding Box) for tiles and Circle-Collision for the ball.
* **AI:** Simple Raycasting for wall detection between the Enemy and the Player.

---

*Project created for Game Design and Rapid Prototyping study purposes.*