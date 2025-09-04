---
layout: post
title: Tower Defense — C++ vs Unity
description: >
  Two takes on the same project: building a Tower Defense first in pure C++ with SFML and then recreating it in Unity, exploring the trade-offs of both approaches.
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
---

I developed the same **Tower Defense game** twice, completely on my own: once in **pure C++ with SFML and CMake**, and a second time in **Unity with C#**. Each version explores different development approaches, highlighting trade-offs in **control, performance, modularity, and development speed**.  

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

### [C++ version on github](https://github.com/legno9/Cpp_towerDefense)  

## C++ SFML Version

The C++ implementation focused on **low-level control and modular design**:

- **Game Architecture:** Managers for rendering, objects, UI, input, and assets. Object lifecycles handled manually with `std::unique_ptr`.  
- **Data-Driven Design:** Enemy stats, tower properties, wave layouts, and animations stored in JSON files for easy configuration.  
- **Animation & Event System:** Frame-based callbacks synchronize attacks and projectiles with animations.  
- **Custom UI:** Fully built HUD and tower selection interface using SFML primitives.  

#### Key Advantages

1. **Maximum Control:** Every object, update, and memory allocation is explicit.  
2. **Performance:** Direct memory access and no runtime overhead.  
3. **Flexibility:** Full freedom to implement mechanics exactly as desired.  

#### Challenges

- Manual memory management and object lifecycle required careful design.  
- More development time due to coding every system from scratch.  
- Complex systems needed careful implementation.  

![C++ gameplay image](/assets/img/posts/TowerDefense/TowerDefense_CPP.png)

![C++ visual studio code image](/assets/img/posts/TowerDefense/TowerDefense_VSCode.png)

---

### [Unity version on github](https://github.com/legno9/TD-OniSiege)

## Unity C# Version

The Unity version prioritized **rapid development and polish**:

- **Scriptable Objects & Prefabs:** Modular architecture for enemies, towers, waves, and stats.  
- **Built-in UI Components:** Easy implementation of HUD, tower selection bar, and interactive elements.  
- **Enhanced Visuals:** Multiple levels, improved animations, and special effects.  
- **Modular Game Systems:** Health, enemies, towers, waves, and attacks designed for easy expansion.  

#### Key Advantages

1. **Faster Development:** The same game implemented in **1 week** instead of 3–4.  
2. **Rapid Iteration:** Drag-and-drop assets and prefabs simplified workflow.  
3. **Engine Tools:** Built-in animation and UI components reduce boilerplate.  
4. **Automatic Lifecycle & Memory Management:** Garbage collection handles objects safely, reducing potential errors.  

![Unity gameplay image](/assets/img/posts/TowerDefense/TowerDefense_Main.png)

![Unity screenshot](/assets/img/posts/TowerDefense/TowerDefense_Unity.png)

---

## Technical Challenge: Predictive Health & Dirty Flags

Both versions required a **predictive health system** to optimize turret behavior:

- Turrets calculate expected enemy health immediately when firing.  
- Enemies marked as “doomed” by incoming attacks are skipped by subsequent turrets.  
- Dirty flags mark enemies to be removed once damage reaches them visually.  

This system ensures **no wasted projectiles** and efficient targeting. The implementation is conceptually the same in C++ and Unity, though in C++ it required explicit memory and lifecycle handling.

---

## Reflection

Developing the same game twice highlights the trade-offs of **low-level versus engine-driven development**:

| Feature | C++ SFML | Unity C# |
|---------|-----------|----------|
| Development Time | 3–4 weeks | 1 week |
| Control | Absolute | Medium (engine handles low-level details) |
| Performance | High, optimized | Medium |
| Memory Management | Manual, explicit | Automatic, garbage collected |
| Modularity & Expansion | Requires careful design | Scriptable Objects & Prefabs simplify it |
| UI & Visuals | Custom built | Built-in components |

**Takeaways:**  

- C++ offers **maximum control, speed, and memory management**, but requires careful planning and longer development.  
- Unity allows **fast iteration, easy content management, and polished presentation**, making it ideal for rapid prototyping.  
- Both approaches reinforce **game architecture principles**, modular design, and gameplay optimization.

### [Try them out on itch.io](https://legno9.itch.io/tower-defense-c-vs-unity)