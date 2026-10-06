# Open World Action RPG

This is the new blank game repository. It targets a single-player third-person 3D PC game and starts with a Godot 4.6.3 greybox foundation.

## Environment

- Engine: Godot 4.6.3 stable (system binary: `godot`)
- Initial target: PC, with headless Linux validation in the cloud environment
- Renderer: Compatibility, to keep editor and CI smoke runs portable; revisit Forward+ after profiling target hardware
- Project entry scene: `scenes/main.tscn`

Run the project from `/workspace/game`:

```bash
mkdir -p .cache/home .cache/godot
HOME="$PWD/.cache/home" XDG_CACHE_HOME="$PWD/.cache/godot" godot --editor project.godot
```

Headless smoke check:

```bash
HOME="$PWD/.cache/home" XDG_CACHE_HOME="$PWD/.cache/godot" \
  godot --headless --path . --editor --quit
```

Export presets and the first playable greybox build will be added as the game systems are implemented. Export templates are an environment prerequisite for a distributable PC package.
