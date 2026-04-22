# Chess Master

[← Back to Main README](README.md)

A complete chess game in a single HTML file. Play against a friend locally or challenge the AI opponent.

![Chess Board](chess-game-initial.png)

## Features

- Human vs Human (local two-player mode)
- Human vs AI (with Minimax algorithm and alpha-beta pruning, depth-3 search)
- Full chess rules implementation:
  - Castling (kingside and queenside)
  - En passant
  - Pawn promotion (Queen, Rook, Bishop, or Knight)
- Check, checkmate, and stalemate detection
- Move history displayed in algebraic notation
- Resign functionality
- Responsive design for desktop and tablet

## How to Play

1. Open `index.html` in any modern web browser
2. Or serve with `npx serve .` and open http://localhost:3000

## Game Controls

| Button | Function |
|--------|----------|
| 人机对弈 | Play against AI |
| 双人对弈 | Two players on same device |
| 新游戏 | Start new game |
| 悔棋 | Undo last move |
| 投降 | Resign current game |

## AI Implementation

The computer opponent uses:
- **Minimax algorithm** with alpha-beta pruning
- **Depth-3 search** for balanced performance
- **Position tables** for better move evaluation
- **Piece-square tables** for positional play

## Technical Details

- Pure vanilla JavaScript, no frameworks or libraries
- Single HTML file with embedded CSS and JavaScript
- Unicode chess pieces for clean rendering
- CSS Grid-based board layout

## License

MIT License
