# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/thewhalebd/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/thewhalebd/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Original engine (MIT) for make.fun tiny-chess-01.

`main.py` (3,756 bytes) is an LZMA-packed engine: 0x88 board,
negamax alpha-beta with a transposition table, killer moves and
MVV-LVA ordering, PVS, null-move pruning and late-move reductions,
quiescence on captures with check evasions, piece-square eval,
repetition avoidance, iterative deepening to a fixed budget of
60,000 nodes a move. Deterministic: no clock, no randomness.

It talks to the env at `MAKEFUN_ENV_URL` only (`/game`, `/move`),
no model calls, Python 3.13 standard library only.

## Run it

```sh
MAKEFUN_ENV_URL=<env url> python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
