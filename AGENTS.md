## Project conventions

- Pages live in `src/pages/` and should wrap their content in the shared
  layout: `import Base from '../layouts/Base.astro'` and pass a `title` prop.
- Shared styles live in `src/styles/global.css` and are loaded by the layout.
  Page-specific styles go in a `<style>` block in the page itself — Astro
  scopes them to that page automatically, so experimenting is safe.
- The site is served at https://icholy.github.io/toptier/ under the `/toptier`
  base path. Never write root-absolute URLs like `/foo`; prefix internal links
  and asset references with `import.meta.env.BASE_URL`.
- Deployment is automatic: every push to `master` builds the site and
  publishes it via the GitHub Actions workflow in `.github/workflows/pages.yml`.

## Development

When starting the dev server, use background mode:

```
astro dev --background
```

Manage the background server with `astro dev stop`, `astro dev status`, and `astro dev logs`.

## Documentation

Full documentation: https://docs.astro.build

Consult these guides before working on related tasks:

- [Adding pages, dynamic routes, or middleware](https://docs.astro.build/en/guides/routing/)
- [Working with Astro components](https://docs.astro.build/en/basics/astro-components/)
- [Using React, Vue, Svelte, or other framework components](https://docs.astro.build/en/guides/framework-components/)
- [Adding or managing content](https://docs.astro.build/en/guides/content-collections/)
- [Adding styles or using Tailwind](https://docs.astro.build/en/guides/styling/)
- [Supporting multiple languages](https://docs.astro.build/en/guides/internationalization/)
