# kyoten FPS example

A first-person shooter built on [kyoten](https://kyotenengine.com), and a starting point for your own: the kyoten
engine manager offers each example as a project you can download and build on. It consumes the engine the way any
game would, so the engine is exercised from the outside and never shaped around one game.

**Status:** seeded. It builds against the engine and prints `fps example, on kyoten`. What it contains first
(movement, shooting, a level, networking) is decided in kyoten's design spike (`docs/design/examples.md` in the
kyoten repository).

## Building it today

**Each kyoten example is its own repository.** The engine is not published yet, so this one depends on it by path
(`"kyoten": { "path": "../../../engine" }`) and builds **inside a kyoten checkout, as `examples/games/fps`**. kyoten's
`.gitignore` leaves `examples/games/` out, so examples never weigh on an engine-only checkout.

```sh
git clone https://github.com/cosmic-canopy/kyoten.git kyoten
cd kyoten
git clone https://github.com/cosmic-canopy/kyoten-example-fps.git examples/games/fps
kama pkg install examples/games/fps/kama.json
kama run examples/games/fps/kama.json           # prints "fps example, on kyoten"
```

Once the engine is published, an example depends on a released engine version, and the engine manager hands out a
standalone copy (`docs/design/version-manager.md` in kyoten).

Licensed under either of [MIT](LICENSE-MIT) or [Apache-2.0](LICENSE-APACHE), at your option.
