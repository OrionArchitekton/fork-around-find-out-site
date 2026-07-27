# AGENTS.md - proctor-site

## Repo Role

`proctor-site` is the Vite/React microsite for the `Proctor` project page at
danmercede.com/works/proctor/. It owns presentation, metadata, static assets,
and cache config for the site surface.

## Boundaries

- Owns site copy, layout, Open Graph metadata, Vercel config, and static assets.
- Does not own the Proctor TypeScript implementation, tests, workflows, or
  UiPath gateway behavior (github.com/OrionArchitekton/proctor).
- Keep product claims grounded in the source project README, docs/submission
  artifacts, and verified behavior. Competition status is finalist until the
  winners announcement says otherwise; never state a placement here first.

## Authority Order

1. `/home/orion/src/orion-estate/platform/orion-estate-audit/AGENTS.md`
2. Source project: the `proctor` repo README.md and docs/
3. This repo's `README.md`, `constants.ts`, `index.html`, and `vercel.json`
4. Vite build output and package scripts

## Validation

```bash
npm install
npm run build
```

For docs-only changes, run `git diff --check` at minimum.
