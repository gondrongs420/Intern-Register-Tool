# Development environment

The cloud machine provides Godot 4.6.3, Node.js 24, Python 3.12, GCC 14, and Git. The project uses Godot because it is already installed, supports 3D scenes and desktop export without a paid service, and can run headlessly for repeatable checks.

Create writable engine caches before invoking Godot:

```bash
mkdir -p .cache/home .cache/godot
export HOME="$PWD/.cache/home"
export XDG_CACHE_HOME="$PWD/.cache/godot"
```

The first milestone is a real third-person greybox: one controllable character, a camera, movement, one attack, one target enemy, and a measurable headless smoke test. Keep gameplay data in resources or configuration files as systems grow. Add `export_presets.cfg` and install the matching Godot export templates before claiming a distributable PC build.
