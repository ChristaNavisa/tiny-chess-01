# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ChristaNavisa/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ChristaNavisa/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB chess engine in a single `main.py` (Python 3.13, stdlib only).

`main.py` unpacks (lzma + base85) and execs a compact engine: 0x88 board,
Zobrist hashing, alpha-beta with iterative deepening to a fixed node budget
(100,000 nodes/move), MVV-LVA + killer/history move ordering, quiescence
over captures/promotions/check evasions, transposition table, and a
material + piece-square evaluation with king safety. Full rules: castling,
en passant, promotion, checkmate/stalemate, repetition and fifty-move draws.
Deterministic: every move derives from the position and a fixed node count,
never a clock.

It plays the house gauntlet through `MAKEFUN_ENV_URL`, one game after
another, and exits when the trial is done.

## Layout

- `main.py` — the whole engine (3,835 bytes)
- `LICENSE` — MIT
- `.makefun/owner.json` — entrant claim file
