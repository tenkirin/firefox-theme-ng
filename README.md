# Firefox Theme NG for VS Code

[![Release](https://vsmarketplacebadges.dev/version/tenkirin.firefox-theme-ng.avif?label=Release&style=flat-square&colorA=2B2A33&colorB=0A84FF)](https://marketplace.visualstudio.com/items?itemName=tenkirin.firefox-theme-ng)
[![Installs](https://vsmarketplacebadges.dev/installs/tenkirin.firefox-theme-ng.avif?label=Installs&style=flat-square&colorA=2B2A33&colorB=058B00)](https://marketplace.visualstudio.com/items?itemName=tenkirin.firefox-theme-ng)
[![Rating](https://vsmarketplacebadges.dev/rating/tenkirin.firefox-theme-ng.avif?label=Rating&style=flat-square&colorA=2B2A33&colorB=DD00A9)](https://marketplace.visualstudio.com/items?itemName=tenkirin.firefox-theme-ng#review-details)

![banner](./images/banner.png)

A next-generation VS Code color theme inspired by Firefox's [browser chrome](https://developer.mozilla.org/en-US/docs/Glossary/Chrome) — not just DevTools, but the full UI palette you see every day. Colors are extracted directly from Firefox's built-in theme definitions.

## Highlights

- **Firefox-native palette**: UI and token colors are taken directly from Firefox source files in `omni.ja`, so every major color choice stays anchored to the browser's real theme definitions.
- **Split source model**: browser chrome CSS drives workbench surfaces such as sidebars, tabs, inputs, and status bars, while DevTools CSS drives syntax tokens such as keywords, strings, types, comments, and links.
- **Balanced dark and light themes**: Firefox Dark NG and Firefox Light NG are built as equal first-class variants with the same structure and Firefox-matched palette counterparts.
- **Consistent coverage**: each variant ships with `113` token color rules, `311` mapped scopes, and `312` workbench colors for broad editor coverage without uneven gaps between modes.
- **Semantic token mapping**: syntax colors follow Firefox DevTools semantic categories, including body text, comments, keywords, definitions, properties, variables, strings, numbers, and links.
- **Traceable color system**: workbench and token layers remain separate, making the theme easier to maintain and keeping UI colors from drifting away from syntax colors.

## Themes

- **Firefox Dark NG** — The signature Firefox dark palette: deep purples, cool grays, and vivid accent blues
- **Firefox Light NG** — A clean, airy counterpart with Firefox's native light-mode tones

## Installation

### From [Marketplace](https://marketplace.visualstudio.com/items?itemName=tenkirin.firefox-theme-ng)

Search for "Firefox Theme NG" in the VS Code Extensions view (`Ctrl+Shift+X`).

## Development / Preview

1. Open this repository in VS Code
2. Press `F5` to launch the Extension Development Host
3. In the new window, press `Ctrl+K Ctrl+T` to open the Color Theme picker
4. Select "Firefox Dark NG" or "Firefox Light NG"

## Color Sources

Firefox Theme NG uses two source layers from Firefox's `omni.ja` assets:

| Theme Layer           | Firefox Source                                                                     |
| --------------------- | ---------------------------------------------------------------------------------- |
| Workbench / UI colors | `omni/chrome/browser/skin/classic/browser/browser-colors.css` and `browser.css`    |
| Syntax / token colors | `omni/chrome/devtools/skin/variables.css`, `light-theme.css`, and `dark-theme.css` |

## Credits

- Color values derived from Firefox (MPL 2.0). No MPL-licensed source code is included in this distribution
- [Firefox Theme](https://marketplace.visualstudio.com/items?itemName=Heron.firefox-devtools-theme) (MIT License)
- [C/C++ Themes](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-themes) (MIT License)
- [Night Owl](https://marketplace.visualstudio.com/items?itemName=sdras.night-owl) (MIT License)
- [Atom One Light Theme](https://marketplace.visualstudio.com/items?itemName=akamud.vscode-theme-onelight) (MIT License)

## License

[MIT](LICENSE)
