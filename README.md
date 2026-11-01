# kyoten FPS example

A first-person shooter built on [kyoten](https://kyotenengine.com), and a starting point for your own: the kyoten
engine manager offers each example as a project you can download and build on. It consumes the engine the way any
game would, so the engine is exercised from the outside and never shaped around one game.

**Status:** seeded. It builds against the engine and prints `fps example, on kyoten`. What it contains first
(movement, shooting, a level, networking) is decided in kyoten's design spike (`docs/design/examples.md` in the
kyoten repository).

## Building it today

**Each kyoten example is its own repository.** The engine is not published yet, so this one depends on it by path
(`"kyoten": { "path": "../../engine" }`) and builds **inside a kyoten checkout, as `games/fps`**. kyoten's
`.gitignore` leaves `games/` out, so examples never weigh on an engine-only checkout.

```sh
git clone <kyoten-url> kyoten
cd kyoten
git clone <kyoten-fps-url> games/fps
kama pkg install games/fps/kama.json
kama run games/fps/kama.json            # prints "fps example, on kyoten"
```

Once the engine is published, an example depends on a released engine version, and the engine manager hands out a
standalone copy (`docs/design/version-manager.md` in kyoten).

Licensed under either of [MIT](LICENSE-MIT) or [Apache-2.0](LICENSE-APACHE), at your option.
