---
title: 'Creating Chains'
published: 2024-04-25
description: ''
image: ''
tags: ['Basic']
category: 'Basic Strategy'
draft: false 
---

# Creating Chains

## What is a Chain?

In Puyo, 4 or more connected Puyos of the same color are cleared at the same time. After the Puyos are cleared, the Puyos above the cleared Puyos fall down to fill the empty spaces. If the same condition is met again, the chain continues.

When the chain finishes, the garbage Puyos are calculated based on the point system. Here is the point system for the garbage Puyos:

- Falling Bonus: 1 point for each Puyo that manually falls down by 1 cell
- Chain Bonus: max((the number of all Puyos cleared in a chain) * (A + B + C) * 10, 40)
  - A = chain length bonus:
    | n | chain length bonus |
    |---|---------------------|
    | 1 | 0                   |
    | 2, 3 | 8 * (n - 1)      |
    | 4+ | 32 * (n - 3)       |
  - B = chain connection bonus: (for each connected component)
    | n | chain connection bonus |
    |---|-------------------------|
    | 4 | 0                       |
    | 5 ~ 10 | n - 3               |
    | 11+ | 10                    |
  - C = chain color bonus:
    | n | chain color bonus |
    |---|-------------------|
    | 1 | 0                 |
    | 2+ | 3 * 2 ^ (n - 2)  |
- All Clear Bonus: 3600 points
- The number of garbage Puyos sent to the opponent is calculated by the following formula:
  - floor((Points) / 70)

## How to Create Chains

There are many ways to create chains in Puyo. Also, it is important not to consider there is only one way to trigger a chain. Here are some examples of how to create chains:

![Creating Chains](src/assets/images/1_chain_01.png)
![Creating Chains](src/assets/images/1_chain_02.png)
![Creating Chains](src/assets/images/1_chain_03.png)

Let's consider the third example. We can see that there is a GTR left down in the field. We can trigger this chain by putting a red puyo on column 4 after we put a red puyo on column 2. Then we get a 10-chain. However, if we put a red puyo on column 6, we can immediately trigger a 7-chain. It is less unusual that things like this happen, but it is important to consider all possibilities when creating chains. Though it is also important to create chains with a high flexibility, the most important thing is to think about how we can extend the chain in many ways.

## Do Not Make the Entire Chain, Just Make Small Mechanics

When creating chains, it is important to think about how to extend the chain. However, it is not always necessary to make the entire chain. It is important to make small mechanics that can be extended in many ways. Let's see the second example. We can see that there is a GTR left down in the field. This is counted as a small mechanic. There is a avalanche mechanic after the GTR, there is a multiple stacking mechanic above the GTR, and there is a typical reflection mechanic on the upper right. We can learn many mechanics like this, watching other players' gameplay streams or videos.