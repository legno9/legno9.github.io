---
layout: post
title: Supermarket Rush
description: >
  Supermarket Rush is a simple 3-lane runner game made in Unreal Engine with Blueprints. Players compete to reach the supermarket first while avoiding cars and collecting coins and power-ups.
image: 
  path: /assets/img/posts/SupermarketRush/SupermarketRush_Main.png
srcset:
    1920w: /assets/img/posts/SupermarketRunner/SupermarketRush_Main.png
    960w:  /assets/img/posts/SupermarketRunner/SupermarketRush_Main@0,5x.png
    480w:  /assets/img/posts/SupermarketRunner/SupermarketRush_Main@0,25x.png
categories: [Unreal]
excerpt_separator: <!--more-->
sitemap: true
hide_last_modified: true
---

Developed in just **one week as a team project**, **Supermarket Rush** is a 3-lane runner game where players race to reach the supermarket while avoiding cars, collecting coins, and using power-ups to gain an advantage or hinder opponents.  

<!--more-->

* toc
{:toc}

## Project Context

**Supermarket Rush** is a fast-paced runner with a **third-person perspective**. Players automatically move forward, gradually accelerating, and must:

- **Avoid cars** traveling down three parallel lanes.  
- **Collect coins** to boost score.  
- **Use power-ups** strategically to gain an advantage or slow the opponent.  
- Compete in **local multiplayer or against AI**, aiming to reach the supermarket first.  

The main goal is **to outpace your opponent**, combining quick reflexes with strategic collection and use of power-ups.

![Supermarket Rush Screenshot](/assets/img/posts/SupermarketRush/SupermarketRush_Menu.png)

---

## My Contributions

I focused on the **player character and core gameplay systems**, ensuring smooth and responsive interactions:

- **Character Movement:** Implemented lane switching, forward movement, gradual acceleration, and input handling for both single and local multiplayer setups.  
- **Collision Handling:** Programmed reactions to collisions with cars, including triggering the death animation and resetting the player state.  
- **Power-Up & Coin Integration:** Developed the collection system and UI feedback, allowing players to pick up power-ups and coins; I integrated the effects for the player, though the actual gameplay logic for each power-up was implemented by a teammate.  
- **Animation Integration:** Created Blueprint-based animations for running, lane switching, and collision events, ensuring visual feedback aligns with gameplay.  

Although **AI behavior and power-up effects were handled by other team members**, I made sure the player experience was seamless and all interactive elements worked correctly.

---

## Reflection

Developing **Supermarket Rush** in just a week was an excellent exercise in **rapid prototyping, teamwork, and iterative design**:

- Unreal Engine **Blueprints enabled fast implementation** of player movement, collisions, and collection systems.  
- Coordinating with teammates required careful integration of **player input, animations, and power-up feedback**, highlighting the importance of modular design and testing.  
- Despite its simplicity, the project demonstrates how **well-polished mechanics and competitive elements** can create engaging gameplay experiences in a short time.

---

## [Try it out now](https://legno9.itch.io/supermarket-rush)