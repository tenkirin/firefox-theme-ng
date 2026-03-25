# Firefox Theme NG for VS Code

![banner](./images/banner.png)

A VS Code color theme inspired by Firefox's [browser chrome](https://developer.mozilla.org/en-US/docs/Glossary/Chrome) — not just DevTools, but the full UI palette you see every day. Colors are extracted directly from Firefox's built-in theme definitions.

## Themes

- **Firefox Dark NG** — The signature Firefox dark palette: deep purples, cool grays, and vivid accent blues
- **Firefox Light NG** — A clean, airy counterpart with Firefox's native light-mode tones

## Installation

### From Marketplace

Search for "Firefox Theme NG" in the VS Code Extensions view (`Ctrl+Shift+X`).

## Development / Preview

1. Open this repository in VS Code
2. Press `F5` to launch the Extension Development Host
3. In the new window, press `Ctrl+K Ctrl+T` to open the Color Theme picker
4. Select "Firefox Dark NG" or "Firefox Light NG"

## Color Sources

All workbench/UI colors are derived from Firefox's `omni.ja` assets:

| VS Code Element                 | Firefox Source                                       |
| ------------------------------- | ---------------------------------------------------- |
| Editor background (dark)        | `--tabpanel-background-color: #2B2A33`               |
| Sidebar background (dark)       | `--sidebar-background-color: #1C1B22`                |
| Tab bar / Status bar (dark)     | Derived from Firefox gray-100: `#15141A`             |
| Input / Popup background (dark) | `--input-bgcolor / --arrowpanel-background: #42414D` |
| Borders (dark)                  | `--arrowpanel-border-color: #52525E`                 |
| Primary text (dark)             | `--button-text-color: #FBFBFE`                       |
| Accent (dark)                   | `--tab-loading-fill: #0A84FF`                        |
| Links (dark)                    | `--link-color: #00DDFF`                              |
| Attention (dark)                | `--attention-dot-color: #54FFBD`                     |
| Warning (dark)                  | `--warning-icon-bgcolor: #FFBD4F`                    |
| Editor background (light)       | White (Firefox default)                              |
| Sidebar background (light)      | `--tabpanel-background-color: #F9F9FB`               |
| Accent (light)                  | `--color-accent-primary: #0061E0`                    |
| Primary text (light)            | `--button-text-color: #15141A`                       |
| Borders (light)                 | `--arrowpanel-border-color: #F0F0F4`                 |
| Attention (light)               | `--attention-dot-color: #2AC3A2`                     |
| Warning (light)                 | `--warning-icon-bgcolor: #FFA436`                    |

## Credits

- Original [Firefox Theme](https://github.com/firefox-theme/visual-studio-code) (MIT License)
- Color values derived from Firefox (MPL 2.0). No MPL-licensed source code is included in this distribution.

## License

[MIT](LICENSE)
