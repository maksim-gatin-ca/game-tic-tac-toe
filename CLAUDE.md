# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-file HTML Tic Tac Toe game designed as a first programming project for an 11-year-old. The entire game is contained in `tic-tac-toe.html` with embedded CSS and JavaScript.

## Architecture

The game follows a simple monolithic structure:
- **CSS**: Embedded in `<style>` tags (lines 8-116) - handles all styling and layout
- **HTML**: Game structure (lines 119-157) - contains game board, mode selection, and UI elements
- **JavaScript**: Game logic (lines 160-341) - manages game state, player moves, and AI

### Key Components

**Game State Management**:
- `gameBoard` array (9 elements) represents the 3x3 grid
- `currentPlayer` tracks whose turn it is ("X" or "O")
- `gameMode` switches between "player" (PvP) and "computer" (PvC)
- `gameActive` boolean controls whether moves can be made

**AI Logic**:
- Simple strategy: try to win first, then block player, then random move
- `findWinningMove()` function implements win/block detection
- 500ms delay on computer moves for better UX

**Win Detection**:
- `winningConditions` array defines all possible winning combinations
- Checks horizontal, vertical, and diagonal lines

## Development Commands

Since this is a single HTML file, no build process is required:
- **Run locally**: Open `tic-tac-toe.html` in any web browser
- **Deploy**: Upload `tic-tac-toe.html` to any web server

## Code Conventions

- Inline event handlers (`onclick`) are used throughout
- CSS uses class-based styling with hover effects
- JavaScript uses ES5+ features (arrow functions, const/let)
- Emoji used extensively in UI text for visual appeal
- Functions are organized by purpose (game logic, UI updates, AI)

## File Structure

```
/
├── tic-tac-toe.html    # Complete game in single file
├── README.md           # Project documentation
├── images/             # Screenshots for README
└── instuctions to ai.txt # Original project requirements
```

## Context Notes

This project was created as a learning exercise with requirements for simplicity and single-file deployment. When making changes, maintain the beginner-friendly code style and avoid introducing complex frameworks or build processes.