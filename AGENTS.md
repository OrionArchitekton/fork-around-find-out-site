# AGENTS.md - fork-around-find-out-site

## Repo Role

`fork-around-find-out-site` is the Vite/React microsite for the
`Fork Around & Find Out` project page at
danmercede.com/works/fork-around-find-out/. It owns presentation, metadata,
static assets, and cache config for the site surface.

## Boundaries

- Owns site copy, layout, Open Graph metadata, Vercel config, and static assets.
- Does not own the Fork Around & Find Out gateway: the Daytona sandbox runner,
  policy engine, Braintrust scoring, attack suite, or tests
  (github.com/OrionArchitekton/fork-around-find-out).
- Keep product claims grounded in the source project README and verified
  behavior. The project won no prize at Daytona HackSprint #5; never state a
  placement.
- `constants.ts` (`PRODUCT_DATA`) feeds both the React app and the build-time
  body-bake; edit copy there. Keep `base` in `vite.config.ts` equal to
  `/works/fork-around-find-out/` so it matches the hub rewrite.

## Authority Order

1. `/home/orion/src/orion-estate/platform/orion-estate-audit/AGENTS.md`
2. Source project: the `fork-around-find-out` repo README.md and docs/
3. This repo's `README.md`, `constants.ts`, `index.html`, and `vercel.json`
4. Vite build output and package scripts

## Validation

```bash
npm install
npm run build
```

For docs-only changes, run `git diff --check` at minimum.
