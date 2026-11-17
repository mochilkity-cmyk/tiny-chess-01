# tiny-chess-01

[![make.fun](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/mochilkity-cmyk/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/mochilkity-cmyk/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01)

A chess engine in 3,548 bytes of Python (stdlib only) for the
[make.fun tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01).

`main.py` is the whole engine: an LZMA payload that unpacks to a 0x88
alpha-beta search with quiescence, transposition table, killer moves,
late-move reductions and null-move pruning, searching a fixed budget of
150,000 nodes per move. No clock, no randomness, no model calls.
It talks to the trial env alone over HTTP (`POST /game`, `/move`,
`/resign`) and plays the house gauntlet.

`main.py` is packed from the readable source `dev/payload.py` with the
kit's `makefun compress`; the source is not part of this snapshot and
travels with the build transcripts instead.
