# PlantUML Live Preview

A single-file, browser-based PlantUML live preview tool with no build steps and no dependencies (except pako.js via CDN).

**[Open Live Preview →](https://twominutescoding.github.io/plantUML/)**

---

## Features

- **Live preview** — auto-renders as you type (debounced) or on demand
- **Multi-tab** — open multiple diagrams, rename tabs, middle-click to close
- **Syntax highlighting** — keyword, arrow, comment, string, hex color highlighting
- **Line numbers** — always-visible, scroll-synced with the editor
- **Objects panel** — auto-detects named objects from code with usage count
- **Component palette** — insert participants, arrows, groups, notes, classes and more
- **Pan & zoom** — mouse wheel zoom, drag to pan, fit to screen
- **Diff mode** — side-by-side before/after comparison
- **Theme picker** — default, light, dark, sketch, hacker
- **History** — last 20 rendered diagrams stored in browser
- **Autosave** — all tabs saved to localStorage every 30 seconds
- **Share link** — hash-based URL that works on htmlpreview.github.io
- **Export** — SVG, PNG, PDF (via print), standalone HTML

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl+Enter` | Render diagram |
| `Ctrl+S` | Download SVG |
| `Ctrl+/` | Toggle comment on current line |
| `Ctrl+Shift+F` | Fit diagram to screen |
| `Tab` | Indent (2 spaces) |
| `Esc` | Exit diff mode |
| `Middle click` | Close tab |
| `Double click tab` | Rename tab |

## Usage

Open the [live preview](https://htmlpreview.github.io/?https://github.com/twominutescoding/plantUML/blob/master/index.html) in your browser — no installation needed.

Or clone and open `index.html` directly:

```bash
git clone https://github.com/twominutescoding/plantUML.git
cd plantUML
open index.html
```

## How it works

- PlantUML code is compressed with `pako.deflateRaw` and encoded with a custom base64 alphabet
- The encoded string is sent to the public `plantuml.com` server as an image URL
- Everything runs in the browser — no backend, no server, single HTML file
