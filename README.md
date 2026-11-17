# tiny-chess-01 entry

A compact chess engine in one file (`main.py`). The readable source is
compressed with lzma and base85 at build time; `main.py` unpacks and execs it.
The engine uses a 0..64 board, full legal move generation (castling, en
passant, all promotions), negamax alpha-beta with a transposition table,
quiescence with check evasions and delta pruning, MVV-LVA ordering, and a
material plus piece-square evaluation. It is fully deterministic: fixed
depth 4 with a node cap, no clock and no randomness, so a replay matches.

- `main.py` — the whole engine (under 4096 bytes, stdlib only)
- `LICENSE` — MIT
- `.makefun/owner.json` — wallet claim

It talks only to the env at `MAKEFUN_ENV_URL` via `/game` and `/move`.
