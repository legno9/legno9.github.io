---
layout: post
title: Tower Defense — C++ vs Unity
description: >
    A Tower Defense game built first in C++ with SFML, then recreated in Unity, comparing different development approaches.
image: 
  path: /assets/img/posts/TowerDefense/TowerDefense_Main.png
srcset:
    1920w: /assets/img/posts/TowerDefense/TowerDefense_Main.png
    960w:  /assets/img/posts/TowerDefense/TowerDefense_Main@0,5x.png
    480w:  /assets/img/posts/TowerDefense/TowerDefense_Main@0,25x.png
categories: [Unity, Unreal]
excerpt_separator: <!--more-->
sitemap: true
hide_last_modified: true
weight: 700
---

I developed the same **Tower Defense game** twice: first in **C++ with SFML**, then in **Unity with C#**. Each version explores different approaches, highlighting trade-offs in **control, performance, modularity, and development speed**.

<!--more-->

* toc
{:toc}

---

## Project Context

The objective was to create a **2D Tower Defense game** where players strategically place turrets to defend against waves of enemies. The game includes:

- Multiple tower types with unique mechanics.  
- Enemy waves with varying behaviors and health.  
- A gold-based economy for building and upgrading towers.  
- Projectile mechanics including homing, area damage, and slowing effects.  

The two implementations differ in **tools and workflow**:

- **C++ with SFML (3–4 weeks):** Everything built from scratch, including rendering, UI, object lifecycle, and game logic.  
- **Unity with C# (1 week):** Leveraging engine features such as prefabs, Scriptable Objects, and built-in UI to recreate the game faster and more polished.  

---

- 💻 [C++ version on github](https://github.com/legno9/Cpp_towerDefense)  

## C++ SFML Version

Focused on **low-level control and modularity**:

- **Game Architecture:** Managers for rendering, objects, UI, input, and assets. Object lifecycles handled manually with `std::unique_ptr`.  
- **Data-Driven Design:** Stats, properties, waves, and animations stored in JSON.  
- **Animation & Events:** Frame-based callbacks to sync attacks with animations.  
- **Custom UI:** HUD fully built with SFML primitives.  

#### Key Advantages

1. **Full Control:** Every object and memory allocation explicit.  
2. **Performance:** No engine overhead.  
3. **Flexibility:** Freedom to implement mechanics exactly as intended.  

#### Challenges

- Manual memory management required caution.  
- Slower development due to coding every system.  
- Complex systems demanded careful design.   

![C++ gameplay image](/assets/img/posts/TowerDefense/TowerDefense_CPP.png)

![C++ visual studio code image](/assets/img/posts/TowerDefense/TowerDefense_VSCode.png)

---

- 💻 [Unity version on github](https://github.com/legno9/TD-OniSiege)

## Unity C# Version

The Unity version prioritized **rapid development and polish**:

- **Scriptable Objects & Prefabs:** Modular data-driven design.  
- **Built-in UI:** Quick setup of HUD, tower bar, and menus.  
- **Improved Visuals:** Multiple levels, animations, effects.  
- **Reusable Systems:** Health, towers, enemies, and attacks designed for easy expansion.  

#### Key Advantages

1. **Fast Development:** 1 week vs 3–4 weeks.  
2. **Quick Iteration:** Drag-and-drop workflow.  
3. **Engine Tools:** Animation and UI built-in.  
4. **Automatic Lifecycle:** Garbage collection simplifies memory handling, reducing potential errors. 

![Unity gameplay image](/assets/img/posts/TowerDefense/TowerDefense_Main.png)

![Unity screenshot](/assets/img/posts/TowerDefense/TowerDefense_Unity.png)

---

## Technical Challenges:

Both versions required a **predictive health system** to optimize turret behavior:

- Turrets calculate expected enemy health immediately when firing.  
- Enemies marked as “doomed” by incoming attacks are skipped by subsequent turrets.  
- Dirty flags mark enemies to be removed once damage reaches them visually.  

This system ensures **no wasted projectiles** and efficient targeting. The implementation is conceptually the same in C++ and Unity, though in C++ it required explicit memory and lifecycle handling.

---

## Reflection

Developing the same game twice highlighted the trade-offs of **low-level vs engine-driven development**:

| Feature | C++ SFML | Unity C# |
|---------|-----------|----------|
| Development Time | 3–4 weeks | 1 week |
| Control | Absolute | Medium (engine-managed) |
| Performance | High | Medium |
| Memory Management | Manual | Automatic |
| Modularity | Requires custom design | Built-in (SO & Prefabs) |
| UI & Visuals | Fully custom | Built-in components |

---

**Key Takeaways:**  
- C++ gives **maximum control and performance**, but at higher cost in time and complexity.  
- Unity enables **fast prototyping, polish, and modular expansion**.  
- Both reinforce principles of **game architecture and optimization**.

---

## Links  

- 🕹️ [Try both versions on itch.io!](https://legno9.itch.io/tower-defense-c-vs-unity) 
