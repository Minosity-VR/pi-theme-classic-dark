# pi-theme-classic-dark

Pi 0.99.0 made the new `system` theme (colors derived from your terminal's palette) the default, and revised the built-in `dark` and `light` themes. These are the old `dark` and `light` themes from before that change.

Both files are the unmodified built-ins from pi **0.87.1**, with only the `name` field changed (`dark` → `classic-dark`, `light` → `classic-light`) so they install alongside the current built-ins instead of shadowing them.

| File | Original | Accent |
| --- | --- | --- |
| `classic-dark.json` | 0.87.1 `dark` | teal `#8abeb7` |
| `classic-light.json` | 0.87.1 `light` | teal `#5a8080` |

0.99.x replaced every literal hex with `okhsl(...)` and moved the accent from teal to violet, which is the most visible part of the change.

## Install

Download the theme into your pi themes directory:

```bash
curl -fsSL --create-dirs \
  https://raw.githubusercontent.com/Minosity-VR/pi-theme-classic-dark/2e43f5b3739ed12ada90085c51ede6e32a1446f7/classic-dark.json \
  -o ~/.pi/agent/themes/classic-dark.json
```

For the light variant:

```bash
curl -fsSL --create-dirs \
  https://raw.githubusercontent.com/Minosity-VR/pi-theme-classic-dark/main/classic-light.json \
  -o ~/.pi/agent/themes/classic-light.json
```

Or clone this repo and copy the `.json` files to `~/.pi/agent/themes/`.

Then, in your pi session:

1. Run `/reload`.
2. Open `/settings`, select **Theme**, and pick `classic-dark` or `classic-light`.

## Compatibility

The 0.99.x theme schema still requires only `name` and `colors`, and still accepts plain hex values in `vars`, so these files load as-is — no conversion to `okhsl()` needed.

The one field they lack is `appearance` (`"dark"` / `"light"`), which 0.99.x added and treats as optional. Add it if you want the light/dark auto-detection to classify them without guessing.
