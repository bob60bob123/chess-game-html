# 国际象棋 Chess Master

[← 返回主 README](README.md)

一款完整的单文件国际象棋游戏。支持双人本地对弈和人机对战。

![棋盘](chess-game-initial.png)

## 功能特点

- **双人对弈** - 两人在同一设备上对弈
- **人机对战** - 与 AI 对战（使用 Minimax 算法 + Alpha-Beta 剪枝，搜索深度3）
- **完整国际象棋规则**：
  - 王车易位（长短易位）
  - 吃过路兵
  - 兵升变（可选择后、车、象、马）
- 将军、将死、僵局检测
- 代数记谱法走棋记录
- 投降功能
- 简洁的中文界面

## 快速开始

直接在浏览器中打开 `index.html`，或使用 HTTP 服务器：

```bash
# 使用 npx
npx serve .

# 使用 Python
python -m http.server 8080

# 使用 Bun
bunx serve .
```

然后访问 http://localhost:8080

## 操作说明

| 按钮 | 功能 |
|------|------|
| 人机对弈 | 与电脑对战 |
| 双人对弈 | 双人同机对战 |
| 新游戏 | 开始新游戏 |
| 悔棋 | 撤销最后一步 |
| 投降 | 认输 |

## AI 实现

电脑对手使用：
- **Minimax 算法** + Alpha-Beta 剪枝
- **深度3搜索** 保证平衡的性能
- **位置评估表** 优化棋子位置
- **棋子价值表** 基础棋子价值评估

## 技术栈

- 纯原生 JavaScript，无任何依赖
- 单个 HTML 文件包含所有 CSS 和 JS
- Unicode 国际象棋棋子
- CSS Grid 布局棋盘

## 开源协议

MIT 协议 - 详见 [LICENSE](LICENSE)
