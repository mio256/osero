# README

## Overview

This project is a simple implementation of the game Othello (also known as Reversi) in C. The game features basic functionality, including placing pieces on the board, flipping opponent pieces, and an optional "emperor" mode for manual board manipulation.

## Files

- `main.c`: The main source file containing the game logic and functions.

## Compilation

To compile the program, use the following command:

```sh
gcc main.c -o othello
```

## Usage

Run the compiled program:

```sh
./othello
```

## Game Rules

1. The game is played on an 8x8 board.
2. Players take turns placing pieces on the board. One player uses black pieces (represented by "○") and the other uses white pieces (represented by "●").
3. A move consists of placing a piece on the board such that there is at least one straight (horizontal, vertical, or diagonal) occupied line between the new piece and another piece of the same color, with one or more contiguous pieces of the opponent's color in between.
4. All of the opponent's pieces lying on a straight line between the new piece and any anchoring pieces of the current player's color are flipped to the current player's color.
5. The game ends when neither player can make a valid move, typically when the board is full.
6. The player with the most pieces of their color on the board at the end of the game wins.

## Special Features

### Emperor Mode

The emperor mode allows manual manipulation of the board. To enter emperor mode:

1. Input `X=11` and `Y=11` when prompted for coordinates.
2. In emperor mode, you can set any piece at any position on the board by specifying the coordinates and the piece's color (512 for black, 256 for white, or 0 to clear a space).

## Functions

### `int main()`

The main function initializes the game board, handles user input, and controls the game loop.

### `void table()`

Prints the current state of the game board.

### `void conturn()`

Handles the turn switching between players and sets the current player color.

### `void riversi(int meat)`

Handles the logic for flipping the opponent's pieces according to the game rules.

### `void emperor()`

Allows manual manipulation of the board in emperor mode.

## Variables

- `int i, j`: Loop counters for board iteration.
- `int x, y, data[9][9]`: Coordinates and board data.
- `int fish`: Flag for valid moves.
- `int ancolor, color`: Variables for opponent and current player colors.
- `int turn`: Counter for the number of turns taken.
- `int count, wcount, bcount`: Counters for pieces on the board.
- `int emp`: Flag for emperor mode.

## Example Gameplay

1. Run the program.
2. Follow the prompts to enter coordinates for your move.
3. The program will display the updated board after each move.
4. Continue taking turns until the game ends.
5. The final score and the winner will be displayed.

Enjoy playing Othello!
