# Digital Rich Technologies – Venue Genius

Marketing site for **Venue Genius**, Digital Rich Technologies’ event staff coordinator and point of management for teams. Built with Nuxt for static export.

**Pages:** Home | Features | Pricing | About Us | Contact

## GitHub Pages

The site is built for static hosting. To deploy to GitHub Pages:

1. Run `pnpm run generate` (or `npm run generate`).
2. Deploy the contents of `.output/public` to your `gh-pages` branch, or enable GitHub Actions with a static export workflow. For a repo named `digitalrichtech.github.io`, the site will be served at **https://digitalrichtech.github.io**.

## Setup

Make sure to install dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
