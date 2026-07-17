# TOP TIER

An [Astro](https://astro.build) static site published to GitHub Pages at
**https://icholy.github.io/toptier/**.

## Getting started

This project uses [mise](https://mise.jdx.dev) to pin the Node and pnpm
versions (see `mise.toml`) and [pnpm](https://pnpm.io) to manage dependencies.

```sh
mise install        # install the pinned Node and pnpm toolchain
pnpm install        # install dependencies
pnpm dev            # start the local dev server
```

## Scripts

| Command        | Description                            |
| -------------- | -------------------------------------- |
| `pnpm dev`     | Start the local dev server.            |
| `pnpm build`   | Build the production site to `dist/`.  |
| `pnpm preview` | Preview the production build locally.  |

## Project structure

```
src/
  pages/     # one file per route; wrap content in the Base layout
  layouts/   # Base.astro — shared HTML shell, loads global styles
  styles/    # global.css — site-wide styles
public/       # static assets copied verbatim (favicon, etc.)
```

The site is served under the `/toptier` base path, so internal links and asset
references must be prefixed with `import.meta.env.BASE_URL` rather than using
root-absolute URLs.

## Deployment

Deployment is automatic. Every push to `master` builds the site and publishes
it via the GitHub Actions workflow in `.github/workflows/pages.yml`.

## Contributing

See [AGENTS.md](AGENTS.md) for project conventions and links to the relevant
Astro documentation.
