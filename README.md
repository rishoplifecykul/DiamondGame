# Diamond Game - Project Breakdown

## Overview
This project implements a strategy card game (also known as "Goofspiel") where players bid for prize cards using their own suit of cards.

## Game Mechanics
- **Objective**: Collect the most points from the Prize deck (Diamonds).
- **Players**: 2 or 3 (Human vs Computer).
- **Flow**: 
    1. A Prize card is revealed.
    2. Players secretly choose a bid card.
    3. Highest bid wins the Prize.
    4. Ties split the points.

## Components Breakdown

### 1. Card & Deck System
- **Card**: Represents a standard playing card (Suit + Rank).
- **Deck**: Manages shuffling and dealing.
- **Ranks**: 2-10 (Face Value), J(11), Q(12), K(13), A(14).

### 2. Player System
- **Human Player**: Inputs moves via console.
- **Computer Player**: Automates moves using a Strategy engine.
- **State**: Tracks current Hand and Score.

### 3. Strategy Engine
The AI needs to be smarter than random guessing.
- **Random Bot**: Unpredictable but inefficient.
- **Smart Bot**: 
    - **Value Evaluation**: Bids higher for valuable prizes.
    - **Memory**: Remembers what high cards you have played. If you wasted your Ace on a 2, it knows it can beat you later with a King.

### 4. Game Loop (Main)
- Handles the 13 rounds of play.
- Prints status: "Prize is [D-K]. You played [H-K]. CPU played [S-A]. CPU Wins!"
- Calculates final scores.

## Roadmap
1. **Model Implementation**: Create the basic Card/Deck/Player classes.
2. **Game Engine**: Get the loop working with 2 players (Random vs Random).
3. **Strategy Development**: Implement the "Smart" logic.
4. **Interactive UI**: Polish the text output for the human player.
