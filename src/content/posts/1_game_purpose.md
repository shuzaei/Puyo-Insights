---
title: 'Purpose of Puyo'
published: 2024-04-25
description: ''
image: ''
tags: ['General', 'Rules']
category: 'Basic Strategy'
draft: false 
---

# Purpose of Puyo

## Winning Conditions

The purpose of Puyo is not limited to just winning the game. We might have many different purposes when we play Puyo, such as:

- To win the game
- To improve our skills and strategies
- To create long chains and beautiful patterns
- To try suprise attacks and tricks
- To increase the winning rate using disconnection bugs :(
- To insult the opponent with random movements when we win :(

But, most of the time, we play Puyo to win the game.

We have a clear winning condition in Puyo: To fill the (3, 12) cell with any kind of Puyo. Then, we can divide the winning condition into two sub-conditions:

- Send too many garbage Puyos not to be able to avoid the game over
- Wait for the opponent to accidentally fill the (3, 12) cell with a colored Puyo

![Winning Conditions](src/assets/images/1_game_purpose_01.png)

There are several ways to achieve the first condition; However, there is only one way in the ideal situation. Let's talk about some game-theoretical aspects of Puyo before we discuss that.

## Game Theory

Puyo is technically defined as a two-player non-cooperative game with imperfect information and random elements. The game has imperfect information because we cannot wait for the opponent's next move before we make our move. The game has random elements because the colors of the next Puyos and the last positions of the garbage Puyos are determined randomly. (Note: in some versions of Puyo, the colors of the next Puyos including garbage can be predicted based on the first 4 Puyo pairs.)

Because of its imperfect information, we cannot determine the optimal strategy for Puyo. (Let's consider rock-paper-scissors as an example.) However, we can determine the Nash equilibrium with stochastic strategies. Considering the current situation in shogi when AI has been introduced, we can say that we will continue to use "human-friendly" strategies such as GTR, but we might need to reconsider adjusting our strategies in detail.

## How to win the game

Again, there are several ways to win the game, but there is only one way in the ideal situation. In a perfect game, especially for this game is non-zero-sum, we can say that if the sum of the utility (= amount of garbage Puyos sent to the opponent) of us surpasses the sum of the utility of the opponent by the rest space in row-3 in the opponent's field, we can win the game. The amount of garbage Puyos sent to the opponent is determined by the chain length and the number of chains that we clear in a sequence. Thus, they are both important to have a chain with a maximum length and to have multiple chains to respond to the opponent's moves.

## How to measure the strength of a player

The strength of a player can be measured by the winning rate against the same opponent. Because we have broken rating systems especially in SEGA Puyo Puyo due to the disconnection bugs and techniques, we cannot rely on the rating system to measure the strength of a player. However, we can measure the strength of a player by the winning rate against the same opponent. If the winning rate is over 30%, we cannot say that the player is weak than the opponent. Also as Saikyo League has been introduced, we can measure the strength of a player by other multiple factors such as chain length, response time, creativity, and so on.