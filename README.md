# Real Shot Studio

GitHub repository for the Real Shot Studio website, built with [Next.js](https://nextjs.org) and managed with [pnpm](https://pnpm.io).

## Monorepo structure

This repo is set up as a monorepo so that additional apps can live alongside the frontend. If the client decides they want a backend, it can be added without restructuring anything.

```
realshotstudios/
├── frontend/   # Next.js app (current)
└── backend/    # Planned: added only if the client needs one
```

Each app is self-contained, with its own `package.json`, dependencies and `.gitignore`.

## Getting started

Requirements: [Node.js](https://nodejs.org) and pnpm (`corepack enable` or `npm i -g pnpm`).

```bash
cd frontend
pnpm install
pnpm dev
```

The site runs at [http://localhost:3000](http://localhost:3000).

## Frontend scripts

Run these from `frontend/`:

| Command      | Description                  |
| ------------ | ---------------------------- |
| `pnpm dev`   | Start the development server |
| `pnpm build` | Create a production build    |
| `pnpm start` | Run the production build     |
| `pnpm lint`  | Run ESLint                   |

## Adding a backend later

1. Create a `backend/` folder at the repo root.
2. Initialize it with its own `package.json` (`pnpm init`) or the framework of your choice.
3. If the apps should share dependencies or code, add a root `pnpm-workspace.yaml` listing both folders.
