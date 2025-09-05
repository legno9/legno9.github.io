---
layout: post
title: Supermarket Rush
description: >
  Supermarket Rush is a 3-lane runner game made in Unreal Engine with Blueprints.
image: 
  path: /assets/img/posts/SupermarketRush/SupermarketRush_Menu.png
srcset:
    1920w: /assets/img/posts/SupermarketRush/SupermarketRush_Menu.png
    960w:  /assets/img/posts/SupermarketRush/SupermarketRush_Menu@0,5x.png
    480w:  /assets/img/posts/SupermarketRush/SupermarketRush_Menu@0,25x.png
categories: [Unreal]
excerpt_separator: <!--more-->
sitemap: true
hide_last_modified: true
weight: 100
---

Developed in just **one week as a team project**, **Supermarket Rush** is a 3-lane runner where players race to reach the supermarket while **avoiding cars, collecting coins, and using power-ups** to gain an edge or hinder opponents.

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

![Supermarket Rush Screenshot](/assets/img/posts/SupermarketRush/SupermarketRush_Main.png)

---

## My Contributions

I focused on the **player character and core gameplay systems**, making interactions responsive and consistent:

- **Character Movement:** Lane switching, forward progression, acceleration, and input handling for both single and local multiplayer.  
- **Collision Handling:** Programmed reactions to crashes, including triggering the death animation and resetting the player.  
- **Power-Up & Coin Integration:** Built the collection system and feedback UI. I connected power-ups to the player, while a teammate implemented their specific effects.  
- **Animation Integration:** Created Blueprint-based animations for running, switching, and collisions to ensure clear visual feedback.  

---

## Reflection

Developing **Supermarket Rush** in one week was an excellent exercise in **rapid prototyping, teamwork, and iteration**:

- Unreal Engine **Blueprints enabled quick implementation** of movement, collisions, and pickups.  
- Coordinating with teammates showed the value of **modular design and careful integration**.  
- Despite its simplicity, the project demonstrates how **polished mechanics and competitive elements** can create engaging gameplay in a short timeframe.

---

## Link  

- 🕹️ [Try out Supermarket Rush!](https://legno9.itch.io/supermarket-rush)