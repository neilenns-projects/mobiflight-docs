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

## Deploying to CloudFlare workers

The site deploys to CloudFlare workers using the `./build.sh` script. When updating the Go or Hugo
versions make sure to update the respective values in that script.

The deployment command is simply the default, `npx wrangler deploy`. The deployment method is copied
directly from the [Hugo documentation](https://gohugo.io/host-and-deploy/host-on-cloudflare/) with no
modifications other than version numbers.
