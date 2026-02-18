# Digital Rich Technologies – Venue Genius

Marketing site for **Venue Genius**, Digital Rich Technologies’ event staff coordinator and point of management for teams. Built with Nuxt for static export.

**Pages:** Home | Features | Pricing | About Us | Contact

## GitHub Pages

The site is set up for **GitHub Pages** and will be available at **https://digitalrichtech.github.io** once deployed.

**One-time setup in the repo:**
1. In GitHub: **Settings → Pages**
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.

**Deploy:** Push to `main`; the workflow builds the static site and deploys it. No manual steps.

**Local build:** Run `pnpm run generate`; output is in `.output/public`. You can preview with `pnpm run preview` (or `npx serve .output/public`).

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
