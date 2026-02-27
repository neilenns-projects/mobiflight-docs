# MobiFlight documentation copilot instructions

This is a documentation website for MobiFlight, written in [Hugo](https://gohugo.io/) with the [Hextra theme](https://imfing.github.io/hextra/docs/getting-started/).

## General conventions

- File and directory names must be in lowercase, use dashes (`-`) instead of spaces, and use lowercase file extensions.
- All Markdown files must pass markdownlint.
- Unordered lists use hyphens (`-`).
- Unordered list items that are complete sentences end with a period.
- Use GitHub alerts instead of Hextra `{{< callout >}}` shortcodes.
- Reference board and device images using `{{% card %}}` shortcodes.
- Reference UI elements that users should click or interact with in **bold**.
- Links to other documentation pages should be absolute, not relative.
- Headings are in sentence case.
- Table headers are in sentence case.
- Page descriptions are in sentence case and end in a period.
- Page titles are in sentence case and do not end in a period.
- Spelling and grammar must be correct.
- Voltages that aren't whole numbers use a decimal point, e.g. `3.3V` instead of `3V3`.
- All leaf pages should be in their own folder as a page bundle.
- Device and board intro pages should always have an opening descriptive paragraph before a card with an image of the device or board.
- Ohms use the `Ω` symbol.
- Microfarads use the `µF` symbol (not `uF`).
- "Arduino Pro Micro" and "SparkFun Pro Micro" should always be called "Pro Micro".
- "Arduino Mega 2560 Pro Mini" should always be called "Mega 2560 Pro Mini".
- "WINWING" should be written as "WinCtrl".
- All files under the `boards/` and `devices/` folders must have an `ogimage` specified in the front matter.

## Screenshots

- Use `.png` format for all screenshots.
- Set width to 800px.
- Store in a `screenshots` folder in the page bundle, or in the `static/screenshots` folder if the screenshot is used across multiple pages.
- Reference using the `{{< screenshot >}}` shortcode with a `title` attribute that ends in a period.
- Do not use Markdown image syntax for screenshots.

## Board and device images

- Use `.png` format for all board and device images.
- Set dimensions to 800×600px.
- Store in the `assets/card-images` folder.
- Reference using the `{{% card %}}` shortcode.
- Do not use Markdown image syntax for board and device images.

## SVG files

- All SVG files must be minified using [svgomg](https://svgomg.net/) with the default options plus `Prefer viewBox to width/height` enabled.

## Pinout diagrams

- Use `.svg` format.
- Store in the page bundle for the associated board and name the file `pinout.svg`.
- Reference using the `{{< pinout >}}` shortcode.
- Do not use Markdown image syntax for pinout diagrams.

## Schematics

- Use `.svg` format.
- Prefer net labels over global labels.
- Store in the page bundle for the associated board.
- Reference using the `{{< schematic >}}` shortcode.
- Do not use Markdown image syntax for schematics.
