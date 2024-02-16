---
attachments: [Clipboard_2024-02-14-21-14-59.png, Clipboard_2024-02-14-21-25-04.png, Clipboard_2024-02-14-21-30-33.png]
tags: [BehaviorTree]
title: Unreal Behavior Tree
created: '2024-02-14T13:12:01.136Z'
modified: '2024-02-14T15:00:28.369Z'
---

# Unreal Behavior Tree

## 特点

### event driven

unreal 的行为树是事件触发的而不是每帧轮询。节点的 decorator 配置状态检查器，相关事件触发背景变量改变(HasLineOfSight)，而不是每次运行时检查条件满足。

![](@attachment/Clipboard_2024-02-14-21-14-59.png)

### 条件检测尽量使用 decorator

使用 decorator 做条件检测有助于使得行为节点和条件分离，更容易理解。并且条件检测在控制节点也有助于事件触发执行的效率。

![](@attachment/Clipboard_2024-02-14-21-25-04.png)

### 并行节点

unreal 使用简单并行模式，并行节点下挂一个主要任务节点和多个次要行为树。当主要任务节点结束时，次要行为树自动结束(可以设置为等待次要行为树结束)。

![](@attachment/Clipboard_2024-02-14-21-30-33.png)

## 详细[文档](https://docs.unrealengine.com/5.0/en-US/behavior-tree-node-reference-in-unreal-engine/)

### Composites

### Decorators

### Services

### Tasks










