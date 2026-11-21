# sokoban-solver-01

Push-optimal Sokoban solver for the make.fun bounty
[Build the best Sokoban solver, 21 November 2026](https://make.fun/bounty/sokoban-solver-01-run-20261121).

Algorithm: a box pushed through a door into the hallway can never return,
so every box stays in its room and the level optimum is the sum of the
rooms' optima. Each room is solved by BFS over pushes (first solved state
is push-optimal), pruning dead squares and frozen 2x2 blocks; the rooms
are stitched with shortest player walks through the hallway.

Run: `MAKEFUN_INPUT_DIR=<input> MAKEFUN_OUTPUT_DIR=<output> node main.ts`

Referral: https://make.fun/r/cxvrx67h
