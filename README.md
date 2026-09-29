# fork-around-find-out-site

Vite/React microsite for the `Fork Around & Find Out` project page at
`https://www.danmercede.com/works/fork-around-find-out/`.

## Role

This repo owns the marketing/presentation surface for `Fork Around & Find Out`
(a fail-closed decision gateway for AI agent tool-calls, built solo at Daytona
HackSprint #5): layout, copy, metadata, static assets, and Vercel cache config.
The source project owns the gateway itself: the Daytona sandbox runner, the
policy engine, Braintrust scoring, the labeled attack suite, and tests.

## Source Of Truth

- Product repo: github.com/OrionArchitekton/fork-around-find-out
- Site copy: `constants.ts` (`PRODUCT_DATA`)
- Metadata: `index.html`
- Cache headers: `vercel.json`

## Local Development

```bash
npm install
npm run dev
npm run build
npm run preview
```

## Build And Deploy

- `vite.config.ts` sets `base: '/works/fork-around-find-out/'` so emitted
  asset URLs resolve under the hub path.
- The danmercede.com hub (`danmercede-com` repo, `vercel.json`) rewrites
  `/works/fork-around-find-out/` to this project's Vercel deployment,
  `fork-around-find-out-site.vercel.app`.
- `vite-plugin-bodybake.ts` bakes a static, crawlable HTML body from
  `PRODUCT_DATA` into `#root` at build time, for answer-engine crawlers that
  do not run JavaScript. React replaces it on mount. The build fails if the
  baked body lacks an `<h1>` or `<p>`, or if the `#root` anchor is missing.

## Boundaries

Keep claims grounded in the source project README and verified behavior. The
project was submitted to Daytona HackSprint #5 and won no prize; never state a
placement. Do not change the gateway from this repo.
