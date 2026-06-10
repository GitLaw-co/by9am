# by9am.com

Landing site for **by9am** — the ambient personal assistant. Hand off your tasks at night; wake up to them done by 9am.

- **Live:** https://by9am.com
- Static site, no build step. Single-file pages, Inter + Instrument Serif via Google Fonts, hand-rolled CSS.
- Hosted on GitHub Pages (`main` branch root, `CNAME` → by9am.com).

## Pages

- `index.html` — landing (hero · value props · life-areas bento · access · waitlist)
- `faq.html` — how it works (vision diagrams + FAQ)
- `family-hub.html` — Family Hub product page
- `components.html` — UX block-kit gallery
- `architecture.html`, `spaces-lab.html`, `surfaces-lab.html`, `gallery-lab.html` — labs (unlisted, rough working notes)
- `demo.html` / `demo-app.html` — narrated interactive walkthrough (illustrative dummy data)
- `blog.html` + `blog/` — notes; copy `blog/_template.html` to add a post, then add an entry to `POSTS` in `blog.html`

## Waitlist

Forms POST to FormSubmit; the endpoint is assembled at runtime in `index.html` (`hello@by9am.com`). Entries also persist client-side in `localStorage` so the flow never dead-ends. The optional AI review gate lives in `gate/` (Cloudflare Worker) — deploy it and set `AGENT_ENDPOINT` in `index.html` to enable.
