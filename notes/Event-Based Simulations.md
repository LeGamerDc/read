---
tags: [BehaviorTree]
title: Event-Based Simulations
created: '2024-02-14T10:29:09.776Z'
modified: '2024-02-14T13:12:39.361Z'
---

# Event-Based Simulations

[ref](https://www.gameaipro.com/GameAIProOnlineEdition2021/GameAIProOnlineEdition2021_Chapter02_Efficient_Event_Based_Simulations.pdf)

## 动机

1. 每帧检查game object效率太低，因为大部分game object没有动作。
2. 按帧均分game object只消减波峰，并没有实质上提高效率。

## 优化

1. 按事件驱动触发 update。
2. 每种行为单独计算下次触发时间，绑定到game object上。
3. 每次game object上的某种行为触发时，要检查所有行为的触发器(推迟、提前、移除)。因为同一个game object 的各个行为间存在相互影响关系。


