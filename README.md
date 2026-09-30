# pi-theme-classic-dark

Pi 0.99.0 made the new `system` theme (colors derived from your terminal's palette) the default, and revised the built-in `dark` theme. This is the old `dark` theme from before that change.

## Install

Download the theme into your pi themes directory:

```bash
curl -fsSL --create-dirs \
  https://raw.githubusercontent.com/Minosity-VR/pi-theme-classic-dark/2e43f5b3739ed12ada90085c51ede6e32a1446f7/classic-dark.json \
  -o ~/.pi/agent/themes/classic-dark.json
```

Or clone this repo and copy `classic-dark.json` to `~/.pi/agent/themes/classic-dark.json`.

Then, in your pi session:

1. Run `/reload`.
2. Open `/settings`, select **Theme**, and pick `classic-dark`.
