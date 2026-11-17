# samsam-z/tiny-chess-4kb-engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/samsam-z/tiny-chess-4kb-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/samsam-z/tiny-chess-4kb-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A compact, deterministic chess engine in one file (`main.py`, under 4096 bytes, Python 3.13 stdlib only). It reads FEN from the make.fun env at `MAKEFUN_ENV_URL`, generates all legal moves (castling, en passant, all promotions), and chooses a move with negamax alpha-beta, a transposition table, quiescence with check evasions and delta pruning, MVV-LVA ordering, and a material plus piece-square evaluation. Fixed depth and a node cap, no clock and no randomness, so replay matches.

`main.py` is the packed entrypoint produced from the readable `engine_source.py` with `makefun compress`; the source is uploaded as a pack with the transcripts.

## Run it

```sh
python3 main.py
```

- `main.py` — the whole engine (under 4096 bytes, stdlib only)
- `LICENSE` — MIT
- `.makefun/owner.json` — wallet claim

It talks only to the env at `MAKEFUN_ENV_URL` via `/game` and `/move`.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
