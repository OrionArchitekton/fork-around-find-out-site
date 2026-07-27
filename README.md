# proctor-site

Vite/React microsite for the `Proctor` project page at
`https://www.danmercede.com/works/proctor/`.

## Role

This repo owns the marketing/presentation surface for `Proctor` (behavioral
regression testing for AI agents; UiPath AgentHack 2026 finalist, Track 3:
UiPath Test Cloud): layout, copy, metadata, static assets, and Vercel
routing/cache config. The source project owns the TypeScript engine, tests,
workflows, dashboard, and UiPath gateway behavior.

## Source Of Truth

- Product repo: github.com/OrionArchitekton/proctor
- Site copy: `constants.ts`
- Metadata: `index.html`
- Routing/cache: `vercel.json`

## Local Development

```bash
npm install
npm run dev
npm run build
npm run preview
```

## Boundaries

Keep claims grounded in the source project README, docs/submission artifacts,
and verified behavior. Competition status is finalist until winners are
announced; never state a placement the announcement has not made. Do not change
the Proctor engine from this repo.
