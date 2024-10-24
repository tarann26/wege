# Wege Game Implementation

This project is a JavaFX-based implementation of the game **Wege** (also known as *The Legend of Landlock*). The game is designed for two players, where one plays as "Land" and the other as "Water". The goal is to create connected paths of land or water, touching as many edges of the board as possible.

## Table of Contents
- [Project Requirements](#project-requirements)
- [Classes](#classes)
  - [DLNode](#1-dlnode)
  - [LinkedList](#2-linkedlist)
  - [WegeCard](#3-wegecard)
  - [WegeButton](#4-wegebutton)
  - [Wege](#5-wege)
- [How to Run](#how-to-run)
  - [Optional Parameters](#optional-parameters)
- [Features](#features)
- [Acknowledgements](#acknowledgements)

## Project Requirements

- **JavaFX**: The project uses JavaFX for the GUI components.
- **Linked List**: The card deck is managed using a custom linked list implementation(personal implementation included).
- **Two Players**: The game must support two players, "Land" and "Water".

## Classes

### 1. **DLNode**
Represents a node in a doubly linked list. Each node contains references to the previous and next nodes in the list.

### 2. **LinkedList**
This class implements a linked list data structure to manage the deck of cards used in the game. Cards are stored in a random order and drawn from the front of the list during gameplay.

### 3. **WegeCard**
This class represents the individual cards in the game. Each card can depict one of the following:
- **Land**: A path of land.
- **Water**: A stream of water.
- **Bridge**: Crossing paths of land and water.
- **Cossack**: A special card that depicts neither land nor water.

Additionally, some cards contain gnomes, which can influence the scoring.

### 4. **WegeButton**
This class extends JavaFX `Button` and is used to display a `WegeCard` on the game board. It provides methods to:
- Display a card
- Rotate the card
- Clear the card from the button

### 5. **Wege**
This is the main class that handles the game logic and user interface. It uses a 2D array of `WegeButton` objects to create the game board. The game progresses by drawing cards, placing them on the board, and ensuring the paths connect correctly.

## How to Run

To run the game, execute the following in your terminal:

```bash
java Wege
```

## Optional Parameters
You can customize the game by providing additional parameters:
- `java Wege 7 5`: Starts a game with a 7x5 grid.
- `java Wege 7 5 2`: Starts a game with a 7x5 grid and modifies the card deck to contain 2 of each special card type.
- `java Wege 5`: Starts a game with a 6x6 grid and 5 of each special card type.

## Features

- **Turn-based gameplay**: Players take turns drawing and placing cards.
- **Card rotation**: Cards can be rotated 90 degrees before being placed on the board.
- **Scoring system**: Points are awarded based on connected paths, islands, ponds, and gnome interactions.
- **Flexible grid size**: The game board size can be customized via command line arguments.
- **Dynamic card deck**: The deck is shuffled and drawn randomly.

## Acknowledgements

I would like to express my gratitude to Professor Harold Connamacher for his guidance and support throughout this course. His insights and expertise have greatly enhanced my understanding of the subject matter. I also extend my appreciation to my classmates for their collaboration and encouragement, which made this project a rewarding experience.
