# Chess Master - 체스

[← 메인 README로 돌아가기](README.md)

단일 HTML 파일로 구현된 완전한 체스 게임. 친구와 로컬에서对战하거나 AI와对战할 수 있습니다.

![체스판](chess-game-initial.png)

## 기능

- **둘이서対戦** - 같은 기기에서 두 명이켜でプレイ
- **AI对战** - AI와対戦 (Minimax 알고리즘 + Alpha-Beta pruning, 深さ3探索)
- **완전한 체스 규칙**:
  - 캐슬링 (롱/숏)
  - 앙파상 ( passant)
  - 폰 프로모션 (Queen, Rook, Bishop, Knight 선택)
- 체크, 체크메이트, 스테일메이트 감지
- 대수 표기법으로 기보 표시
- 항복 기능
- 중국어 UI

## 시작하기

1. `index.html` 을 브라우저에서 열거나
2. `npx serve .` 로 서버를 실행하고 http://localhost:3000 에 접속

## 조작 버튼

| 버튼 | 기능 |
|------|------|
| 人機対弈 | AI와对战 |
| 雙人對弈 | 둘이서对战 |
| 新遊戲 | 새로운 게임 |
| 悔棋 | 한 수 취소 |
| 投降 | 항복 |

## AI 구현

AI 상대는 다음을 사용합니다:
- **Minimax 알고리즘** + Alpha-Beta pruning
- **深さ3 탐색** - 성능과 강함의 균형
- **위치 평가 테이블** - 말의 배치 평가
- **말 가치 테이블** - 각 말의 기본 가치

## 기술 스택

- 순수 바닐라 JavaScript, 의존성 없음
- 단일 HTML 파일 (CSS + JS 포함)
- Unicode 체스 말
- CSS Grid 레이아웃

## 라이선스

MIT 라이선스
