# Chess Master / 国际象棋 /  Chess / エ шахматы / Schach

[English](README_en.md) | [中文](README_zh.md) | [日本語](README_ja.md) | [한국어](README_ko.md)

---

A complete chess game in a single HTML file. Play against a friend locally or challenge the AI opponent.



## Features

- Human vs Human (local two-player)
- Human vs AI (with Minimax algorithm, alpha-beta pruning)
- Full chess rules: castling, en passant, pawn promotion
- Check, checkmate, and stalemate detection
- Move history in algebraic notation
- Resign functionality
- Chinese UI

## Quick Start

Simply open `index.html` in your browser, or serve with any HTTP server:

```bash
# Using npx
npx serve .

# Using Python
python -m http.server 8080

# Using Bun
bunx serve .
```

Then open http://localhost:8080

## Controls

- Click to select a piece, click again to move
- **人机对弈** - Play against AI
- **双人对弈** - Play against another person
- **新游戏** - Start a new game
- **悔棋** - Undo last move
- **投降** - Resign current game

## Tech Stack

Pure vanilla JavaScript, no dependencies. Single HTML file with embedded CSS and JS.

## License

MIT License - see [LICENSE](LICENSE) for details.
