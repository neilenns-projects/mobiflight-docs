# Deploying the documentation

The documentation can be deployed to any hosting provider as a static website. To build the site run the following command:

```bash
hugo -b <baseUrl>
```

Where `<baseUrl>` is the base URL of the site. For example, the live site is deployed using this command:

```bash
hugo -b https://docs.mobiflight.com/
```

The static pages for deployment are placed in the `./public` folder after the build completes.

## Deploying to CloudFlare Pages: Production

The site is deployed to the CloudFlare Pages production environment with the following settings:

| Setting              | Sub-setting           | Value                               |
| -------------------- | --------------------- | ----------------------------------- |
| Git repository       |                       | `neilenns-projects/mobiflight-docs` |
| Build configuration  | Build command         | `hugo -b $CF_PAGES_URL`             |
| Build configuration  | Output directory      | `public`                            |
| Build configuration  | Root directory        | *leave empty*                       |
| Build configuration  | Build comments        | Enabled                             |
| Build cache          |                       | Disabled                            |
| Branch control       | Production branch     | `main`                              |
| Branch control       | Automatic deployments | Enabled                             |
| Build watch paths    | Include paths         | `*`                                 |
| Build system version |                       | `2`                                 |
| Deploy hooks         |                       | *leave empty*                       |

Use the following variables and secrets:

| Type      | Name         | Value   |
| --------- | ------------ | ------- |
| Plaintext | HUGO_VERSION | 0.140.2 |

Failing to set the `HUGO_VERSION` variable will result in the deployments failing.

## Deploying to CloudFlare Pages: Preview

CloudFlare Pages automatically deploys a preview version of the site for each pull request. The settings are identical to the production environment, with the following exceptions:

| Setting        | Sub-setting    | Value                       |
| -------------- | -------------- | --------------------------- |
| Branch control | Preview branch | All non-production branches |

Remember to set the `HUGO_VERSION` variable on the preview environment as well, otherwise the deployments will fail.
