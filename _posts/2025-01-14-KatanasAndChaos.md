---
layout: post
title: Katanas and Chaos
description: >
  Katanas and Chaos is a third-person dungeon crawler built in Unity, featuring multiple weapons, modular melee combat, and AI-driven enemies with diverse behaviors. 
image: 
  path: /assets/img/posts/KatanasAndChaos/KatanasAndChaos_Main.png
srcset:
    1920w: /assets/img/posts/KatanasAndChaos/KatanasAndChaos_Main.png
    960w:  /assets/img/posts/KatanasAndChaos/KatanasAndChaos_Main@0,5x.png
    480w:  /assets/img/posts/KatanasAndChaos/KatanasAndChaos_Main@0,25x.png
categories: [Unity]
excerpt_separator: <!--more-->
sitemap: true
hide_last_modified: true
---

**Katanas and Chaos** is a third-person dungeon crawler developed in Unity as a two-person collaborative project.
The player starts imprisoned at the bottom of a castle and must fight their way through enemies, collect resources, and ultimately face a **Dark Souls-inspired boss battle**.  

<!--more-->

* toc
{:toc}

---

## Project Context

The game focuses on **combat variety and enemy AI**. Players can choose from multiple weapons:  

- **Melee:** Katana (with parry system) and bare-handed combos (punches, kicks).  
- **Ranged:** Bazooka, shotgun, and machine gun.  

Enemies patrol the castle, react to sound and sight, and display distinct behaviors. As the player progresses through the castle’s halls and rooms, they gather ammo and health packs dropped by enemies or placed in corners.  

At the end lies the **final boss**, designed around katana combat, where the **parry mechanic** becomes essential to succeed.  

---

![Gameplay Screenshot](/assets/img/posts/KatanasAndChaos/KatanasAndChaos_Gameplay00.png)


---

## My Contributions

I was responsible for:  

- Designing and implementing **all enemy AI behaviors** (Ambusher, Cautious, Guardian, Sassy).  
- Programming the **melee combat system**, including modular combos and parries.  
- Integrating animations for both **player and enemies**.  
- Preparing the full **castle/dungeon layout**, placing resources and encounter spaces.  

---

![Katana gameplay screenshot](/assets/img/posts/KatanasAndChaos/KatanasAndChaos_Gameplay03.png)

## Technical Highlights

This project stood out because of two core systems I built from scratch:  

- **Custom Modular Combat System**  
  - Allowed chaining of **primary** and **secondary attacks** into fluid combos, instead of relying on Unity’s default Animator state machines.  
  - Attacks were completely interchangeable: developers could add, remove, or swap animations without touching the core logic.  
  - The **parry mechanic** was tightly integrated into this system, giving precise timing windows and rewarding player skill.  

- **AI with Distinct Archetypes**  
  - Four behaviors were implemented (Ambusher, Cautious, Guardian, Sassy), each requiring specific movement logic and animation handling.  
  - Enemies combined **sight and sound detection**, forcing players to consider both stealth and positioning.  
  - This diversity of AI created varied encounters, from sudden ambushes to territorial defenses.  

- **Boss Fight Design**  
  - The final boss exploited the parry mechanic, requiring mastery of the katana to succeed.  

---

![Boss gameplay screenshot](/assets/img/posts/KatanasAndChaos/KatanasAndChaos_Gameplay04.png)

## Link  

- 🕹️ [Try out Katanas and Chaos!](https://legno9.itch.io/katanasandchaos)








