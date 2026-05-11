# Raeleen Cleaning Co.

Marketing website for **Raeleen Cleaning Co.**, a residential and commercial
cleaning service serving the greater San Antonio, TX area (inside the Loop 410).

Built with [SvelteKit](https://svelte.dev/docs/kit) (Svelte 5, runes mode) +
[Tailwind CSS](https://tailwindcss.com/) v4. The site is statically generated
via `@sveltejs/adapter-static` and deployed to GitHub Pages.

## Developing

```sh
npm install
npm run dev
```

## Building

```sh
npm run build
npm run preview
```

The production build is written to `build/`.

If the site is deployed to a non-root URL (e.g. GitHub Pages at
`https://<user>.github.io/<repo>/`), set `BASE_PATH` to the sub-path before
building:

```sh
BASE_PATH=/raeleencleaningco npm run build
```

## Deployment

A GitHub Actions workflow (`.github/workflows/deploy.yml`) builds the site and
publishes it to GitHub Pages on every push to `main`. To enable it:

1. In the repo's **Settings → Pages**, set **Source** to **GitHub Actions**.
2. Push to `main`. The workflow uses the repo name as the base path.
   - For a project site (`https://<user>.github.io/<repo>/`) this is correct.
   - For a user/organization root site (`<user>.github.io`) edit the workflow's
     `BASE_PATH` env var to an empty string.

## Content

- Static assets (favicon, photos, map) live in `static/`.
- The site is a single page (`src/routes/+page.svelte`) with hero, services,
  pricing, service area, about, and contact sections.
- Brand styling lives in `src/routes/layout.css` (`@theme` tokens for the blue
  palette and Lalezar / Nunito fonts).
