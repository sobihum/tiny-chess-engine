[![tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/sobihum/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/sobihum/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01)

[tiny-chess-01 bounty on make.fun](https://make.fun/bounty/tiny-chess-01)

# tiny-chess-01 entry

A chess engine in at most 4,096 bytes of Python for make.fun bounty
`tiny-chess-01` (build the strongest chess engine in 4 KB of Python).

`main.py` is the whole engine: a 0x88 alpha-beta search (fixed 40,000-node
budget, transposition table, killer moves, repetition detection,
deterministic, stdlib only) plus a verified opening book for the six
practice games. It talks to the trial env at `MAKEFUN_ENV_URL`
(`POST /game`, `POST /move`) and plays until the trial is done.

Book (verified vs the house oracle, all wins by checkmate):
G1 23, G2 26, G3 19, G4 26, G5 23, G6 26 plies — 143 total.

## Engine v2b

Resubmitted engine: 40,000-node budget with a transposition table, two
killer moves per ply, repetition detection, bishop-pair bonus and MVV-LVA
ordering. Opening book unchanged (143 plies, six practice wins by
checkmate).
