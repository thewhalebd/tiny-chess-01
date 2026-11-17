# tiny-chess-01 — 4 KB Python chess engine

Original engine (MIT) for make.fun tiny-chess-01.

`main.py` (4,093 bytes) is an LZMA-packed engine: 0x88 board,
negamax alpha-beta with a transposition table, killer moves and
MVV-LVA ordering, quiescence on captures, piece-square eval
(material + pawn/knight tables + formula bishop/rook/queen/king
terms + bishop pair), iterative deepening to a fixed budget of
60,000 nodes a move. Deterministic: no clock, no randomness.

It talks to the env at `MAKEFUN_ENV_URL` only (`/game`, `/move`),
no model calls, Python 3.13 standard library only.
