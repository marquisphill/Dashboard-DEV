# Dashboard-DEV

A DEV copy of Phill's personal dashboard, used to build the shared Paño (see [PANO-PLAN.md in the Pano repo](https://github.com/marquisphill/Pano/blob/main/PANO-PLAN.md)).

- **DEV site:** https://marquisphill.github.io/Dashboard-DEV/
- **Copied from:** `Personal-Dashboard` at commit `695da67` on 2026-11-23. Only `index.html` was copied. The launcher workflow in `.github/` was left out on purpose.

## How it differs from the real dashboard

| Change | Why |
|---|---|
| Everything saved in the browser uses its own name, starting with `dev-` (for example `dev-pd-gh-token`, `dev-pd-pano-key`) | Every site under `marquisphill.github.io` shares one browser storage. This keeps DEV from ever reading the real GitHub token or Claude key. |
| The **Launch** button is turned off | DEV must never start a real prototype build. The button is greyed out and the form refuses to send. |
| The page asks search engines not to list it | It is a working copy, not a site for visitors. |

Everything else is identical. It still reads Paño's brain and the labs list from the staging portfolio, as the real dashboard does.
