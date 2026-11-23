# Development notes

`main.py` (4,083 bytes) is the packed form of the engine: an lzma payload that
unpacks to a complete chess engine in Python — 0x88 board, negamax alpha-beta
with iterative deepening under a fixed node budget (no clock, so a trial's
replay makes the same moves), a transposition table, null-move pruning,
late-move reductions, MVV-LVA ordering, and a quiescence search over captures
and check evasions. Evaluation is material plus piece-square tables and the
bishop pair. The driver talks to the competition env over HTTP and tracks the
game's position history for repetition scoring.

## Validation

- Move generation: perft matches the known counts on six standard positions
  (start position, Kiwipete, two endgame/ep-pin positions, two promotion
  positions) at depths 3–4.
- The packed file round-trips byte-for-byte to the readable source it was
  built from, and plays legal moves against a stub env.
- Local practice trials run with the kit's own env and scorer; results are
  recorded here as they are measured.
