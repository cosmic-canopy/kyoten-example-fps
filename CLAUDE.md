# kyoten FPS example

An example game, and its own repository. It normally sits at `games/fps` inside a kyoten checkout, so kyoten's
`CLAUDE.md`, `AGENTS.md` and `AGENTS.kyoten.md` (two directories up) apply here too: read `../../AGENTS.kyoten.md` and
`../../docs/SPIKE.md` first.

- The engine never special-cases this game. When the game needs something the engine lacks, the engine gains a
  pattern every game can use, recorded in kyoten's design docs, and the game uses it from the outside.
- Build: `kama pkg install kama.json`, then `kama run kama.json`.
- A kama gap found here is recorded in kyoten's `docs/KAMA_GAPS.md`.
