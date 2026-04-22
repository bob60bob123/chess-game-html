# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-file chess game (`index.html`) with human vs human and human vs AI modes. Pure vanilla JavaScript, no dependencies.

## Running the Game

Serve the directory with any HTTP server:
```bash
npx serve .
# or
python -m http.server 8080
# or
bunx serve .
```
Then open http://localhost:8080 (or the port shown).

## Code Architecture

### State Variables (lines 619-632)
```javascript
board[][]         // 8x8 array, lowercase=black, uppercase=white
currentPlayer     // 'white' | 'black'
selectedSquare    // {row, col} or null
validMoves        // array of {row, col, type}
moveHistory       // array of move objects for undo/display
capturedWhite     // pieces white captured
capturedBlack     // pieces black captured
castlingRights    // {K, Q, k, q} boolean flags
enPassantSquare   // {row, col} or null
```

### Key Functions
- `initBoard()` - Initialize starting position
- `getLegalMoves(row, col)` - Get legal moves for piece at position (includes pseudo-legal + filtering for check)
- `makeMove(from, to, type, promotion)` - Execute move, update state
- `isInCheck(color)` / `isCheckmate(color)` / `isStalemate(color)` - Game state detection
- `minimax(depth, alpha, beta, isMaximizing, color)` - AI with alpha-beta pruning
- `renderBoard()` - Re-render entire board to DOM
- `handleSquareClick(row, col)` - Main interaction handler

### Piece Representation
Letters: K=King, Q=Queen, R=Rook, B=Bishop, N=Knight, P=Pawn
White pieces are uppercase, black are lowercase.

### CSS Classes for Board Squares
`.light` / `.dark` - Base square color
`.selected` - Currently selected piece's square
`.valid-move` / `.valid-capture` - Move indicator dots
`.last-move` - Highlight of last move squares
`.in-check` - Red highlight on king when in check

## UI Features
- Mode buttons: "人机对弈" (AI) / "双人对弈" (Human)
- "新游戏" (New Game), "悔棋" (Undo), "投降" (Resign)
- Move history in algebraic notation (one move per line)
- Captured pieces display
- Chinese UI text throughout
