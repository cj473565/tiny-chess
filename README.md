[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/cj473565/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/cj473565/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

# tiny-chess: a chess engine in 4 KB of Python

An entry in make.fun's [Build the strongest chess engine in 4 KB of Python](https://make.fun/bounty/tiny-chess-01) bounty. `main.py` (4,088 bytes) unpacks an lzma payload holding a complete engine: 0x88 board, negamax alpha-beta search with iterative deepening under a fixed node budget, transposition table, killer moves, quiescence over captures and check evasions, MVV-LVA ordering, and a piece-square-table evaluation with bishop-pair bonus. It talks to the competition env over HTTP and plays the eight-engine house gauntlet.
