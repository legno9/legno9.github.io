---
layout: post
title: Vorax Breakout
description: >
  Vorax Breakout is a turn-based roguelike developed in Unity as a master's final project.
image: 
  path: /assets/img/posts/VoraxBreakout_Main.png
srcset:
    1920w: /assets/img/posts/VoraxBreakout_Main.png
    960w:  /assets/img/posts/VoraxBreakout_Main@0,5x.png
    480w:  /assets/img/posts/VoraxBreakout_Main@0,25x.png
excerpt_separator: <!--more-->
sitemap: true
hide_last_modified: true
---

In [**Vorax Breakout**](https://eva-qube.itch.io/vorax-breakout), players manage teams of creatures (Vorax) with unique abilities, strategizing their placement and energy before each automated, round-based battle. The game features preparation, combat, and reward phases, offering tactical depth and replayability.

<!--more-->

* toc
{:toc}

---

![Combat phase](/assets/img/posts/VoraxBreakout_Battle.gif)

## Project Context

Developed as a collaborative effort, this project aimed to demonstrate **advanced game programming skills**, create a **scalable, modular game architecture**, and provide a **replayable demo** ready for potential expansion.  

The demo serves as a proof of concept for strategic mechanics, modular content, and engaging gameplay, laying the foundation for further development like node-based maps and asynchronous PvP.

## My Contributions

#### 1. Modular Game Architecture

- **Core systems built with Scriptable Objects**, separating data from behavior.  
- Easily add new creatures, abilities, or mechanics without touching the core code.  
- Family effects, passive/active abilities, and combat states dynamically handled.

![Diagram of architecture](/assets/img/posts/VoraxBreakout_Main_Architecture00.png)

---

![Diagram of scriptable objects](/assets/img/posts/VoraxBreakout_Main_Architecture01.png)

#### 2. Interactive Tutorial
- Guides new players through game mechanics step-by-step.  
- Highlights UI elements and important actions.  
- Modular and adaptable for future expansion.  
- Includes tooltips and optional videos for clarity.

![GIF showing tutorial in action](/assets/img/posts/VoraxBreakout_Tutorial.gif)

## Gameplay Snapshot

**Vorax Breakout** operates in **three main phases per round**:

1. **Preparation:** Organize team, rest Vorax, place on combat grid.  
2. **Combat:** Automated resolution of abilities, damage, and status effects.  
3. **Rewards:** Choose new Vorax to add or replace in the team.

![Screenshot showing inventory and combat interface](/assets/img/posts/VoraxBreakout_Preparation.gif)

---

## Technical Highlights

- **Scalable, modular architecture** with Scriptable Objects.  
- **Integrated, interactive tutorial** supporting new players.  
- **Dynamic combat system** handling multiple Vorax interactions and passive/active effects.  
- **UI/UX optimizations** for clarity in a visually rich, autobattler interface.

---

## [Try it out now](https://eva-qube.itch.io/vorax-breakout)