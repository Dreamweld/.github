# Dreamweld · Organization profile

Public brand assets and the GitHub organization profile for [Dreamweld](https://github.com/Dreamweld).

- `profile/README.md` — public organization overview, in English and Chinese.
- `assets/banner.svg` / `assets/banner.png` — editable banner and rendered version.
- `assets/avatar.svg` / `assets/avatar.png` — editable organization mark and rendered version.

## Visual identity

Ink `#111820`, warm paper `#f5f1e8`, amber `#ffbd69`.

The joined angular strokes suggest a W; the spark connects imagination with making.

## Updating

Edit the SVG source and regenerate PNGs with Python 3 and CairoSVG:

```sh
python3 -c 'import cairosvg; [cairosvg.svg2png(url=f"assets/{name}.svg", write_to=f"assets/{name}.png") for name in ("avatar", "banner")]'
```

Run the command from the root of the published `Dreamweld/.github` repository. GitHub displays `profile/README.md` on the organization overview. Upload `assets/avatar.png` separately in the organization profile settings.

CairoSVG also requires the Cairo system library. On Apple Silicon macOS with Homebrew Cairo, prefix the command with `DYLD_FALLBACK_LIBRARY_PATH=/opt/homebrew/lib` if Python does not find it automatically.

Brand assets are published for organization identification; no general license is granted by this repository.
