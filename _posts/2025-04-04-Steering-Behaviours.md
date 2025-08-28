---
layout: post
title: Steering Behaviours
description: >
  A practice project in Unreal Engine to experiment with classic steering behaviours: separation, cohesion, alignment, and obstacle avoidance.
image: 
  path: /assets/img/posts/SteeringBehaviours/SteeringBehaviours_Main.png
srcset:
    1920w: /assets/img/posts/SteeringBehaviours/SteeringBehaviours_Main.png
    960w:  /assets/img/posts/SteeringBehaviours/SteeringBehaviours_Main@0,5x.png
    480w:  /assets/img/posts/SteeringBehaviours/SteeringBehaviours_Main@0,25x.png
excerpt_separator: <!--more-->
sitemap: true
hide_last_modified: true
---

As part of my learning process with **Unreal Engine**, I developed this project to **practice and visualize steering behaviours** in a simple yet interactive environment.  
Steering behaviours are widely used in games and simulations to give autonomous agents (*boids*) lifelike motion without predefined paths.  

The goal was to experiment with how different behaviours interact when combined, and to provide a way to **tune their influence in real time** through sliders.

<!--more-->

* toc
{:toc}

## Introduction

Steering behaviours are a classic set of techniques in **artificial intelligence for games**, especially when dealing with groups of agents (commonly called *boids*).  
They allow autonomous agents to move in a way that feels **natural, organic, and responsive**, without needing predefined paths or animations.  

👉 [**Try it yourself here**](https://legno9.itch.io/steeringbehaviours)  

In the demo, you can move sliders to define how much each behaviour (from `0` to `1`) affects the movement of the agents (balls).  

- **Black arrow** → final resulting movement.  
- **Red arrow** → separation force.  
- **Green arrow** → cohesion force.  
- **Blue arrow** → alignment force.  
- **Yellow arrow** → obstacle avoidance.  

## Implemented Behaviours in Unreal Engine

All calculations are performed **every tick** for each agent (ball). The logic was built entirely using **Blueprints**.

## Implemented Behaviours in Unreal Engine

All behaviours are calculated every tick in **Blueprints** and combined into a final movement vector.

- **Cohesion (Green):** pulls each agent towards the center of its neighbors. In Unreal, this is done by averaging neighbor positions and generating a force in that direction.

![Image of cohesion](/assets/img/posts/SteeringBehaviours/SteeringBehaviours_Cohesion.jpg)  


- **Separation (Red):** pushes agents apart to prevent collisions. Implemented by calculating repulsion vectors that grow stronger the closer two agents are.  

![Image of separation](/assets/img/posts/SteeringBehaviours/SteeringBehaviours_Separation.jpg)


- **Alignment (Blue):** aligns each agent with the average heading of its neighbors. In Blueprints, this means weighting neighbors’ velocities and steering towards that combined direction.  

![Image of alignment](/assets/img/posts/SteeringBehaviours/SteeringBehaviours_Aligment.jpg)


- **Obstacle Avoidance (Yellow):** prevents collisions with objects. A forward **Line Trace** detects obstacles and applies a repulsion force based on the hit normal.  

![Image of Obstacle avoidance](/assets/img/posts/SteeringBehaviours/SteeringBehaviours_OAvoindance.jpg)


## Final Movement (Black)

The four vectors are summed and normalized into a single **final direction**. This direction is then applied as torque and velocity to the physics component of each agent.  
Forces reset each tick, ensuring smooth and dynamic motion that depends only on the current state of the environment.

---

## Conclusion

This small Unreal Engine project was a great way to practice both **vector math** and **AI programming for agents**.  
Even with just a handful of behaviours, the resulting motion feels dynamic and natural, and adjusting the sliders makes the demo an effective tool for **learning and experimentation**.