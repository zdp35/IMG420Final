# Tempest Relics

## Team Members
- **Zackary Pond**
- **Ryan Wood**
- **Kayden Vicenti**
---

## Module Overview
**Tempest Relics** is a simple yet unique 2D platformer where you play as an exploring Gale traveling through a world dominated by chaotic wind forces.  
Your objective: find all 7 ancient relics hidden throughout the map to complete the level and win.

## Wind-Based Gameplay
Wind is everything in this world. The environment shifts due to dynamic wind systems, each affecting the player differently:

- **Tornadoes** – Pull you in and launch you upward  
- **Hurricanes** – Spin you around and disrupt movement  
- **Wind Gusts** – Appear randomly with unpredictable strength and duration  

These elements create a unique movement experience centered around navigating the wind.

---

# Godot Extension: WindMap System

To make gameplay feel mechanically distinct, we developed a Godot extension that manages all wind behavior in the game.

### What Does it Do?

- Extends Godot’s built-in Area2D node  
- Collects all wind forces acting within a defined region  
- Assigns wind sources a priority hierarchy depending on wind type  
- Combines all active forces into one unified force vector
- Outputs this final vector that affects the player

---

## Features

### Core Features
- Player movement and physics  
- Obstacle interactions  
- Win/loss detection  
- UI menus (victory menu, quit menu)  
- Background music and sound effects  
- State management

## Tempest Relics — Development Challenges

Throughout development, several technical and gameplay issues emerged.  
This outlines the major challenges faced and the solutions implemented to improve the game.

---

## Challenge 1: Severe Framerate Drop

### **Problem**
- Around version 8, the game's framerate dropped to 4 FPS.
- A wind gust max speed value was mistakenly set to 900,000.
- The TileMap was duplicating itself, causing massive rendering and collision overhead.

### **Solution**
- Reset wind gust speeds to normal gameplay values.
- Removed duplicated TileMap nodes.
- Restored the game's performance back to stable, smooth framerates.

---

## Challenge 2: Overpowered Wind Forces

### **Problem**
- Players were getting stuck inside the Hurricane Zone.
- Wind gusts could trap the player and slam them against walls.
- Movement became unpredictable and broke gameplay flow.

### **Solution**
- Implemented a maximum movement speed cap for the player.
- Wind forces can no longer exceed this velocity limit.
- Ensured consistent movement and prevented uncontrollable wind behavior.

---

## Challenge 3: Relics Scaling with Wind Forces

### **Problem**
- Relics were visually getting bigger and smaller when gusts activated.
- Their collision boxes were interacting incorrectly with wind forces.
- This caused strange animations and gameplay inconsistencies.

### **Solution**
- Updated gustmanager.cs to ensure relics do not interact with wind gust layers.
- Stabilized relic visuals and collision behavior.
- Improved reliability of relic collection mechanics.

---

### Screenshots
<img width="2251" height="1409" alt="image" src="https://github.com/user-attachments/assets/73d37a77-2f72-4320-a9e4-b6e90e40c56f" />

<img width="2253" height="1413" alt="image" src="https://github.com/user-attachments/assets/041d3d93-e81c-4abc-a2f1-d0a1110a56ac" />

---

## Installation & Build Instructions

### Requirements
- Godot Engine 4.4 +
- .NET SDK (if using C# scripts)

### Setup
```bash
git clone https://github.com/zdp35/IMG420Final.git
```

- Open the project in Godot.
- Press F5 to run the game.

# Controls & Gameplay Instructions

## Controls

| Action              | Key(s)                     |
|---------------------|----------------------------|
| Move Left / Right   | **Arrow Keys**             |
| Jump                | **Up Arrow**               |

---

## Gameplay Flow

- Explore the map and discover new areas  
- Use wind forces to navigate or avoid hazards  
- Collect all 7 relics hidden throughout the level  
- Once all relics are collected, the victory screen will appear  
- Restart or quit using the in-game menu buttons

## Resources and References

- Godot Source and Documentation: https://godotengine.org/
- Music Coding Website: https://strudel.cc/	
- Game Engine Book: https://www.gameenginebook.com/

  ## Link to demo video
  
