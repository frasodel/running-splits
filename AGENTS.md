# Repository Guidelines

## Project Structure & Module Organization

This is a Next.js 16 application using the App Router, React 19, TypeScript, and Tailwind CSS 4.

- `app/` contains routes, layouts, and global styles. `app/page.tsx` defines the home route, `app/layout.tsx` provides shared metadata and layout, and `app/globals.css` holds Tailwind imports and theme variables.
- `public/` stores static assets referenced from the site root, such as `/next.svg`.
- Root configuration lives in `next.config.ts`, `tsconfig.json`, and `eslint.config.mjs`.

Keep route-specific components near their route. Add shared UI under `app/components/` and reusable non-UI utilities under `lib/` as the project grows.

## Build, Test, and Development Commands

Install dependencies with `npm install`, then use:

- `npm run dev` — start the local development server at `http://localhost:3000` with hot reload.
- `npm run build` — create a production build and catch Next.js compilation or type errors.
- `npm run start` — serve the previously built production bundle.
- `npm run lint` — run ESLint with Next.js Core Web Vitals and TypeScript rules.

Run `npm run lint` and `npm run build` before submitting changes.

## Coding Style & Naming Conventions

Use TypeScript for application code and keep strict type checking enabled. Follow the existing two-space indentation, double quotes, semicolons, and trailing commas. Name React components in `PascalCase`, functions and variables in `camelCase`, and route folders in lowercase. Prefer the `@/` alias for imports from the repository root. Use Tailwind utility classes for component styling; reserve `app/globals.css` for global rules and shared theme tokens. Use `next/image` for local images when optimization is appropriate.

## Testing Guidelines

No automated test framework or coverage threshold is configured yet. Until one is added, lint and production-build checks are required. Manually verify affected routes in both light and dark color schemes and at mobile and desktop widths. When introducing a test runner, colocate tests as `*.test.ts` or `*.test.tsx` beside the code they cover and add the command to `package.json`.

## Commit & Pull Request Guidelines

Git history is not available in this checkout. Use short, imperative commit subjects, optionally with Conventional Commit prefixes, for example `feat: add split calculator` or `fix: preserve pace input`. Keep commits focused. Pull requests should explain the user-visible change, list validation performed, link relevant issues, and include screenshots for visual changes. Call out new dependencies, configuration changes, or follow-up work explicitly.
