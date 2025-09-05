---
layout: post
title: Vorax Breakout
description: >
  Vorax Breakout is a turn-based roguelike developed in Unity as a master's final project.
image: 
  path: /assets/img/posts/VoraxBreakout/VoraxBreakout_Main.png
srcset:
    1920w: /assets/img/posts/VoraxBreakout/VoraxBreakout_Main.png
    960w:  /assets/img/posts/VoraxBreakout/VoraxBreakout_Main@0,5x.png
    480w:  /assets/img/posts/VoraxBreakout/VoraxBreakout_Main@0,25x.png
categories: [Unity]
excerpt_separator: <!--more-->
sitemap: true
hide_last_modified: true
---

In [**Vorax Breakout**](https://eva-qube.itch.io/vorax-breakout), players manage teams of creatures (Vorax) with unique abilities, strategizing their placement and energy before each automated, round-based battle. The game features preparation, combat, and reward phases, offering tactical depth and replayability.

<!--more-->

* toc
{:toc}

---

![Combat phase](/assets/img/posts/VoraxBreakout/VoraxBreakout_Battle.gif)

## Project Context

Developed collaboratively as a **master’s final project**, the goal was to showcase **advanced programming**, design a **modular, scalable architecture**, and deliver a **replayable demo** ready for future features like node-based maps or asynchronous PvP.  

The demo serves as a proof of concept for both strategic mechanics and modular content.


## My Contributions

### 1. Modular Game Architecture

- **Core systems built with Scriptable Objects**, separating data from behavior.  
- Easily add new creatures, abilities, or mechanics without touching the core code.  
- Designed and implemented the **attack priority system**, which dynamically calculates the main target and affected targets based on multiple criteria (lane, HP, HP ratio, randomness, etc.).   


![Diagram of architecture](/assets/img/posts/VoraxBreakout/VoraxBreakout_Main_Architecture00.png)

---

![Diagram of scriptable objects](/assets/img/posts/VoraxBreakout/VoraxBreakout_Main_Architecture01.png)

### 2. Interactive Tutorial
- Guided players step by step through mechanics.  
- Highlighted UI and actions with tooltips and optional videos.  
- Built modularly to support future additions.  

![GIF showing tutorial in action](/assets/img/posts/VoraxBreakout/VoraxBreakout_Tutorial.gif)

## Gameplay Snapshot

**Vorax Breakout** operates in **three main phases per round**:

1. **Preparation:** Organize team, rest Vorax, place on combat grid.  
2. **Combat:** Automated resolution of abilities, damage, and status effects.  
3. **Rewards:** Choose new Vorax to add or replace in the team.

![Screenshot showing inventory and combat interface](/assets/img/posts/VoraxBreakout/VoraxBreakout_Preparation.gif)

---

## Technical Highlights

- **Scalable, modular architecture** with Scriptable Objects, separating data from behavior.  
- **Dynamic attack priority system**: determines targets based on lane, HP, or randomness, fully supporting new abilities and Vorax types.  
- **Integrated, interactive tutorial** for new players.  
- **Dynamic combat system** managing multiple Vorax interactions and effects.  
- **UI/UX optimizations** for clarity in a visually rich autobattler interface.

---

## Reflection

Working on **Vorax Breakout** strengthened my skills in **system architecture, data-driven design, and player onboarding**.  
It also showed how modular thinking and teamwork can transform a student prototype into a polished, expandable foundation.

---

## Link  

- 🕹️ [Try out Vorax Breakout!](https://eva-qube.itch.io/vorax-breakout)