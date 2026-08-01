# Cocogo

Bilingual side-by-side reading. The original on one line, the translation on the next — so you can finish a book in its original language.

Works on web pages, selected text, and video subtitles. Bring your own OpenAI, Claude, Gemini, or DeepL key.

---

## What this repository is

This repository holds Cocogo's **public assets**, fetched by the extension at runtime:

| File | Purpose |
| --- | --- |
| `cocogo-rules_v2.json` | Site adaptation rules (stable) |
| `cocogo-rules-on_v2.json` | Site adaptation rules (translation on by default) |
| `cocogo-rules-off_v2.json` | Site adaptation rules (translation off by default) |
| `version.txt` | Version manifest used for update checks |
| `README*.md` | Content rendered on the extension's About page |

---

## Site adaptation rules

Every site is laid out differently. Adaptation rules tell Cocogo which elements hold the **body text**, and which regions — navigation, buttons, code blocks — should be **left alone**.

Rules are delivered by subscription, so they update without reinstalling the extension.

### Reporting a rule problem

Translations landing in the wrong place, paragraphs skipped, or menus getting translated? Please [open an issue](https://github.com/gaopei0924/cocogo-rules/issues/new) with the URL and a screenshot.

### A note on safety

When Cocogo loads remote subscription rules, it **strips every executable script field** (`injectJs`, `transStartHook`, `transEndHook`) before use.

In practice: even if this rule source were compromised, it could not run code on any page you visit. Only rules you enter locally yourself may carry scripts.

---

## License

### The Cocogo extension

Cocogo is licensed under the **GNU General Public License v3.0 (GPL-3.0-only)**.

Cocogo is a derivative work of **[KISS Translator](https://github.com/fishjar/kiss-translator)** by **Gabe**, also licensed under GPL-3.0. The original copyright notices are preserved in full in this project's `LICENSE` and `NOTICE` files, as required by section 4 of the GPL-3.0.

Under section 6 of the GPL-3.0, anyone who receives Cocogo is entitled to the complete corresponding source code.

> **Obtaining the source**: Cocogo's code repository is currently private and will be made public before the first public release. Until then, please open an issue in this repository to request the source.

### Site adaptation rules

The `cocogo-rules*.json` files in this repository are derived from **[kiss-rules](https://github.com/fishjar/kiss-rules)** by Gabe, licensed under the **MIT License**. With thanks.

### Disclaimer of warranty

This program is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability and fitness for a particular purpose. The entire risk as to the quality and performance of the program is with you. See sections 15 and 16 of the GPL-3.0.
