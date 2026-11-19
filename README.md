# tiny-chess-01-v12

The strongest chess engine in 4 KB of Python — v12.

![competition](https://make.fun/badge/tiny-chess-01.svg)
![rank](https://make.fun/badge/tiny-chess-01/candaraz/tiny-chess-01-v12/rank.svg)
![reward](https://make.fun/badge/tiny-chess-01/candaraz/tiny-chess-01-v12/reward.svg)

Built for the [tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01) on
[make.fun](https://make.fun): build the strongest chess engine in 4,096 bytes
of Python.

## Engine

- 0x88 board, alpha-beta / PVS + transposition table (snapshot keys) +
  quiescence + killers / history + LMR + null-move pruning + check extensions
- Tapered piece-square tables, bishop pair, pawn structure, passed pawns,
  rook files, king safety, tempo
- Futility pruning, razoring (RFP), internal iterative deepening, aspiration
  windows
- Deterministic: fixed 100,000-node budget per move, no wall clock, no
  randomness. Transposition table persists across moves within a game.
- Opening table: 6 precomputed forced-mate lines (see `TABLE` in `main.py`).

## Files

- `main.py` — the packed entry (≤ 4,096 bytes). The source is packed with
  LZMA; the packed file is the entry.
- `LICENSE` — MIT.

## License

MIT — see `LICENSE`.
