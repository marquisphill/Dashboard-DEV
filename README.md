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

| Paño is no longer inside `index.html`. The page loads him from the Pano repo: `/Pano/latest/pano.css` and `/Pano/latest/pano.js` (phase 4, 2026-11-23) | This is the build itself. His words, tours and talks load from his brain there (`/Pano/latest/brain/dashboard.json` and `core.json`), and his abilities from `/Pano/latest/skills/`, including the Claude chat. What stays in the page is how he is dressed here (a few colors), three backgrounds for him to switch between, and a short adapter in the last script that tells him what the page has. Each skill has one line there, and taking a line out turns that skill off. |

Because of that, open the page through a server that also serves the Pano repo at `/Pano/`. GitHub Pages does. On a computer, use `tests/serve.py` from the Pano repo.

Everything else is identical. It still reads the labs list from the staging portfolio, as the real dashboard does.

## What changed for Paño on this copy

He gained, from the shared Paño: **Change the background** (Plain, Sunrise, Ocean, then the colorblind question and four modes), and the newer head mode (he will not tuck away while the pointer rests on him, and his head always starts at the top middle).

He kept: his three tours, his talks and the prompt builder, his stories ("Ask about Phill"), the little chats he starts himself, the ask box, and the Claude chat with a Console key saved on the device (`dev-pd-pano-key`).

Small differences from the real dashboard's Paño, all from sharing one body with the portfolio:
- On a phone he sits at the right of his bubble and the close button is on the left (the real one has him on the left).
- A short goodbye note closes after about 2.6 seconds (4 on the real one).
- The step label reads "Check the weather · 1 of 5" in plain type (small capitals on the real one).
- A dragged head goes back to the top middle after a reload (the real one remembers where it was dropped).
- If his brain cannot be fetched he stays hidden (the real one falls back to the last copy saved on the device).
- Under "Paño’s brain" the ask box now stays visible (the real one hides it there, though the line says to use it).

The tests are in the Pano repo: `tests/dash.py` and `tests/devdash.py`.
