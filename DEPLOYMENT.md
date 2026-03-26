# Deploying the documentation

The documentation can be deployed to any hosting provider as a static website. To build the site run the following command:

```bash
hugo -b <baseUrl>
```

Where `<baseUrl>` is the base URL of the site. For example, the live site is built using this command:

```bash
hugo -b https://docs.mobiflight.com/
```

The static pages for deployment are placed in the `./public` folder after the build completes.

## Deploying to Cloudflare Workers

The site is deployed to Cloudflare Workers using [Wrangler](https://developers.cloudflare.com/workers/wrangler/). The deployment configuration is stored in `wrangler.toml` at the root of the repository.

### Prerequisites

- [Node.js](https://nodejs.org/) installed
- A Cloudflare account with Workers enabled
- A Cloudflare API token with `Workers Scripts:Edit` and `Workers Assets:Edit` permissions

### GitHub Actions deployment

The site is deployed automatically via GitHub Actions on every push to `main`. The workflow requires the following repository secrets:

| Secret                  | Description                                    |
| ----------------------- | ---------------------------------------------- |
| `CLOUDFLARE_API_TOKEN`  | A Cloudflare API token with deploy permissions |
| `CLOUDFLARE_ACCOUNT_ID` | The Cloudflare account ID                      |

### Manual deployment

To deploy manually, run the following commands from the repository root:

```bash
hugo --gc --minify -b https://docs.mobiflight.com/
npx wrangler deploy
```
