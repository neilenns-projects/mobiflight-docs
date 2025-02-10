# MobiFlight Documentation

Documentation website for MobiFlight, written in [Hugo](https://gohugo.io/) with the [Hextra theme](https://imfing.github.io/hextra/docs/getting-started/). This documentation is deployed using CloudFlare Pages to the [MobiFlight documentation site](https://docs.mobiflight.com/). See the [deployment guide](DEPLOYMENT.md) for information on how to deploy.

## Editing the documentation

The documentation is set up for editing using Visual Studio Code dev containers:

1. [Install VSCode](https://code.visualstudio.com/)
2. [Install Docker Desktop](https://docs.docker.com/get-started/introduction/get-docker-desktop/)
3. Install the [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension
4. Run VSCode
5. Hit `CTRL-SHIFT-P` and type `clone repo` to find the dev container command and select it: ![Screenshot of the clone repository command selected](clone-repo.png)

6. Enter this repo's URL (https://github.com/neilenns/mobiflight-docs)
7. Wait for the dev container to build

To view the documentation press `F5` and it will automatically build and open in Edge. To use Chrome instead select `Launch Chrome` in the run and debug tab.

## Style guidelines

### General conventions

- Filenames are in lowercase, spaces are replaced with hyphens (-).
- All Markdown files must pass markdownlint.
- Unordered lists use hyphens (-).
- Unordered lists have a period at the end of each sentence.
- Use GitHub alerts instead of Hextra callout shortcodes.
- Reference board and device images using cards (see the `boards/` and `devices/` pages for examples).
- Reference UI elements that users should click or interact with in **bold**.
- Links to other documentation pages should be absolute, not relative.
- Headings are in sentence case.
- Table headers are in sentence case.
- Page descriptions are in sentence case and end in a period.
- Page titles are in sentence case and do not end in a period.

### Screenshots

- Use `.png` format for all screenshots.
- Set width to 800px.
- Store in a `screenshots` folder in the page bundle, or in the `static/screenshots` folder if the screenshot is used across multiple pages.
- Reference using the `{{< screenshot >}}` shortcode.
- The shortcode must have a title specified, and the title must end in a period.
- Take screenshots using the [Windows Snipping Tool](https://support.microsoft.com/en-us/windows/use-snipping-tool-to-capture-screenshots-00246869-1843-655f-f220-97299b865f6b) in `Window` mode, not `Freeform` mode.
- Take all screenshots against a white background.
- Highlight rectangles should be use a 6px red stroke and should be applied after screenshots are resized to 800px wide.
- When taking screenshots of the main window:
  - Resize the window width so the right edge is next to the Exit button.
  - Resize the window height so it is shorter. There's no specific size requirement, but make it look nice :)
  - Ensure the .mcc file is called `Cessna 172 G1000 (MSFS2024)` for consistency with other screenshots unless the tutorial is for a specific other aircraft.
  - Only show input and output configs that are directly relevant to the tutorial.
- When taking screenshots of a dialog, stretch the main MobiFlight window vertically to provide a clean white background behind the dialog.

### Board and device images

- Use `.png` format for all board and device images.
- Set dimensions to 800x600.
- Store in the `assets/card-images` folder.
- Reference using the `{{% card %}}` shortcode, accessible using the VSCode `board` and `device` snippets.

### Pinout diagrams

- Use `.svg` format for all pinout diagrams.
- Process the files using [svgomg](https://svgomg.net/) with the default options plus `Prefer viewBox to width/height` enabled.
- Store in the page bundle for the associated board and name the file `pinout.svg`.
- Reference using the `{{< pinout >}}` shortcode, accessible using the VSCode snippet `pinout`.

### Schematics

- Use `.svg` format for all schematics.
- Prefer net labels over global labels.
- Process the files using [svgomg](https://svgomg.net/) with the default options plus `Prefer viewBox to width/height` enabled.
- Store in the page bundle for the associated board.
- Reference using the `{{< schematic >}}` shortcode, accessible using the VSCode snippet `schematic`.
