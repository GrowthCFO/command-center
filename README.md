# Command Center

Static host for CFOLogic Command Center demos — `commandcenter.cfologic.com`.

| Path | Demo |
| --- | --- |
| `/compliancedemo` | Compliance Command Center — multi-country statutory compliance calendar (Meridian Advanced Engineering, demo data) |

Each demo is a single self-contained HTML file (React, fonts and data inlined;
no external requests) at `<name>/index.html`. To add one, drop a new folder with
an `index.html` and push to `main`.

`.nojekyll` disables Jekyll processing — without it the `{{ }}` sequences inside
the bundled script islands get mangled at build time.

The export ships with no `<title>` in its inner template (the loader replaces
`document.documentElement`, so the outer `<head>` is discarded). A `<title>`,
`robots: noindex, nofollow` and a description are injected into that inner head
before publishing. Reapply those when replacing a bundle with a fresh export.

Same pattern as `GrowthCFO/p2p-control-tower`.
