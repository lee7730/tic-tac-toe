# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A simple, browser-based tic tac toe game for two players. The entire application is a self-contained HTML file with embedded CSS and JavaScript—no build process or dependencies required.

## Running the Game

Open `tictactoe.html` directly in any modern web browser. The game is immediately playable.

## Code Structure

**tictactoe.html** contains three sections:

1. **HTML (lines 1-111)**: DOM structure with a 3×3 grid of cells, status display, and reset button
2. **CSS (lines 7-92)**: Styling with flexbox layout, gradient background, and hover/active animations
3. **JavaScript (lines 113-187)**: Game logic

### Game Logic Architecture

- **Game State**: `gameBoard` array (indices 0-8 representing the 3×3 grid), `currentPlayer` (X or O), `gameActive` (boolean flag)
- **Win Detection**: `checkWin()` iterates through 8 win conditions (3 rows, 3 columns, 2 diagonals)
- **Draw Detection**: `checkDraw()` checks if all cells are filled
- **Turn Flow**: Click handler updates board state, calls `updateStatus()`, toggles player

Key functions:
- `handleCellClick()`: Processes player moves and updates the board
- `updateStatus()`: Checks win/draw conditions and updates the status display
- `resetGame()`: Clears the board and resets game state

## Potential Enhancements

- AI opponent (minimax algorithm)
- Score tracking across multiple games
- Difficulty levels
- Mobile responsiveness refinements
- Sound effects
