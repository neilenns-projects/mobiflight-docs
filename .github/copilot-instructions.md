# MobiFlight Documentation

MobiFlight documentation is a Hugo-based static site that uses the Hextra theme to document MobiFlight hardware and software. The site is deployed to CloudFlare Pages at https://docs.mobiflight.com/.

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

### Bootstrap the repository

- Install Hugo 0.140.2 extended: `wget -O /tmp/hugo.deb https://github.com/gohugoio/hugo/releases/download/v0.140.2/hugo_extended_0.140.2_linux-amd64.deb && sudo dpkg -i /tmp/hugo.deb`
- Install npm dependencies: `npm install` -- takes 5-10 seconds
- Install global markdown linter: `npm install -g markdownlint-cli2` -- takes 5-10 seconds

### Build the site

- Production build: `hugo --gc --minify` -- takes 3-15 seconds. NEVER CANCEL. Set timeout to 60+ seconds.
- Development build: `hugo` -- takes 3-10 seconds
- Output directory: `public/`

### Run the development server

- Start dev server: `hugo server --buildDrafts --disableFastRender --baseURL http://localhost:1313/` -- starts in 4-8 seconds
- Server runs on http://localhost:1313/
- Includes live reload for development
- Press Ctrl+C to stop

### Lint and format

- Lint markdown: `markdownlint-cli2 --config .markdownlint.json "content/**/*.md"` -- takes 1-3 seconds
- Check specific file formatting: `npx prettier --check README.md` -- takes 1-2 seconds
- Format specific files: `npx prettier --write <file>` -- takes 1-2 seconds
- Note: Some Hugo template files may have prettier formatting issues due to go-template plugin limitations

## Validation

- ALWAYS manually validate the dev server works by starting it with `hugo server` and curling `http://localhost:1313/` to verify HTML content is served.
- ALWAYS run through at least one complete build and test cycle after making changes: `hugo --gc --minify && markdownlint-cli2 --config .markdownlint.json "README.md"`
- Always run `npx prettier --check README.md` and `markdownlint-cli2` before you are done or the CI (.github/workflows/lint.yaml and .github/workflows/ci.yaml) will fail.
- Test scenarios include: building the site, starting dev server, accessing documentation pages, and validating that image assets load properly.

## Key Project Structure

### Repository root

```txt
.github/             # CI workflows and GitHub configuration
.devcontainer/       # VS Code dev container setup
.vscode/             # VS Code configuration including launch.json for F5 debugging
assets/              # Hugo assets (card-images/, css/)
content/             # All documentation content in Markdown
  boards/            # Hardware board documentation
  devices/           # Device-specific guides
  features/          # MobiFlight software features
  game-controllers/  # Game controller integrations
  guides/            # Step-by-step guides and workshops
  midi-devices/      # MIDI device documentation
data/                # Hugo data files
layouts/             # Custom Hugo layouts and shortcodes
static/              # Static assets (favicons, images)
hugo.yaml            # Hugo configuration
package.json         # npm dependencies (prettier, prettier-plugin-go-template)
.markdownlint.json   # Markdown linting rules
.prettierrc.json     # Prettier formatting configuration
```

### Content organization

- All documentation is in `/content/` as Markdown files with front matter
- Use Hugo shortcodes like `{{< screenshot >}}`, `{{< card >}}`, `{{< schematic >}}` for rich content
- Images stored in `assets/card-images/` or as page bundles
- Navigation defined in `hugo.yaml` and page front matter weights

### Theme and styling

- Uses Hextra Hugo theme via Go modules (`github.com/imfing/hextra`)
- Custom CSS in `assets/css/`
- Responsive design with dark/light mode support
- Custom shortcodes in `layouts/shortcodes/`

## Development Workflows

### Making content changes

1. Start dev server: `hugo server --buildDrafts --disableFastRender --baseURL http://localhost:1313/`
2. Edit Markdown files in `/content/`
3. View changes at http://localhost:1313/ (auto-refreshes)
4. Stop server and run validation commands before committing

### Adding new documentation

1. Create new `.md` files in appropriate `/content/` subdirectory
2. Add proper front matter with title, description, weight
3. Use existing shortcodes for consistency
4. Add images to `assets/card-images/` or page bundles
5. Validate with build and lint commands

### Deployment process

- CloudFlare Pages automatically deploys from `main` branch
- Uses Hugo version 0.140.2 (set via `HUGO_VERSION` environment variable)
- Build command: `hugo -b $CF_PAGES_URL`
- Output directory: `public`

## Common Tasks

### Testing a documentation change

```bash
# Start dev server
hugo server --buildDrafts --disableFastRender --baseURL http://localhost:1313/

# In another terminal, verify site loads
curl -s http://localhost:1313/ | head -10

# Make changes to content files, view in browser
# Stop server with Ctrl+C

# Validate before committing
hugo --gc --minify
markdownlint-cli2 --config .markdownlint.json "content/**/*.md"
npx prettier --check README.md
```

### Adding a new device guide

1. Create directory: `content/devices/new-device/`
2. Add `index.md` with front matter and content
3. Add images to `assets/card-images/devices/`
4. Reference images using `{{< card >}}` shortcode
5. Test with dev server and validate build

### VS Code F5 debugging

- Press F5 to launch Hugo dev server and open in Edge browser
- Select "Launch Chrome" in debug panel for Chrome instead
- Uses `.vscode/launch.json` configuration with pre-launch task

## Build Times and Timeouts

- **Hugo build**: 3-15 seconds normally. NEVER CANCEL. Set timeout to 60+ seconds.
- **Dev server start**: 4-8 seconds to build and start serving
- **npm install**: 5-10 seconds for dependencies
- **Markdown linting**: 1-3 seconds for all content files
- **Prettier formatting**: 1-2 seconds per file

## CI/CD Information

### GitHub Actions workflows

- `.github/workflows/ci.yaml` - Builds site on PRs (takes ~30 seconds)
- `.github/workflows/lint.yaml` - Lints changed markdown files on PRs

### CloudFlare Pages deployment

- Production: Deploys from `main` branch automatically
- Preview: Deploys from all non-production branches
- Build command: `hugo -b $CF_PAGES_URL`
- Hugo version: 0.140.2 (critical environment variable)

## Troubleshooting

### Hugo modules issues

- Run `hugo mod tidy` to clean up module dependencies
- Check `go.mod` and `go.sum` for theme version

### Build failures

- Verify Hugo version: `hugo version` (should be 0.140.2+extended)
- Check for markdown syntax errors: `markdownlint-cli2 --config .markdownlint.json "content/**/*.md"`
- Validate front matter syntax in new content files

### Dev server not starting

- Check if port 1313 is in use: `lsof -i :1313`
- Verify Hugo is installed: `which hugo`
- Check for configuration errors in `hugo.yaml`
