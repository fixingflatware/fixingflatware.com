# Fixing Flatware — umbrella site (v1)

**What:** the manifesto/portfolio "front door" above the products. CUTLR is
product #1; a dedicated Events, File-transfer, Link-shortener and a cheap AI
chat are on the roadmap. Same house pattern as the sibling sites (static in
`public/`, `dev.sh`, GitHub Pages), same **Cold Steel** design system as CUTLR
for family cohesion.

**Brand:** Fixing Flatware (flat**ware** = cutlery — matches CUTLR's "we fix bent
flatware"). NOT flatwire.

**Decisions (confirmed with user):**
- Canonical domain **fixingflatware.com** (buy `.com` + `.xyz`; 301 `.xyz` → `.com`). Not bought yet.
- GitHub org **`fixingflatware`** (no hyphen); org rename `cutlr` → `fixingflatware` is UI-only, pending.
- Future products shown **by function + "coming soon"**, **no invented names** (only CUTLR is named — it's live).
- AI chat positioned as **"affordable AI chat"** (cheaper conversations), NOT the "MCP brain" story.

## M1 — Scaffolding
- [x] `public/`, `.gitignore`, `dev.sh`, `README.md`, `.github/workflows/deploy.yml` (same as cutlr).
- [ ] `public/CNAME` = `fixingflatware.com` — **deferred** until the domain is bought.

## M2 — `public/index.html` (single file, Cold Steel)
- [x] No-FOUC theme script; dark/light toggle in **footer** (consistent w/ cutlr).
- [x] Header: brand "Fixing Flatware" + nav (Manifesto · Tools · Principles) + CTA "Open CUTLR ↗".
- [x] Hero: manifesto one-liner ("We fix bent flatware"), sub, CTAs.
- [x] Manifesto / the problem (software inflation — lifted from cutlr `landing.md`).
- [x] Principles grid: no bloat · fair price, no lock-in · one account · MCP-native · open-source (MIT).
- [x] Products grid: **CUTLR (LIVE, → cutlr.xyz)** + Events / File transfer / Link shortener / AI chat (SOON, **by function only — NO explicit competitor references anywhere**, per user).
- [x] Closing CTA + honest building-in-public (GitHub org link).
- [x] Footer: Guidance Srl credit + legal (same block as cutlr) + theme toggle.

## M3 — Deploy (deferred)
- [ ] Create repo under the org, enable Pages (Actions), deploy preview to `*.github.io`.
- [ ] Once `fixingflatware.com` DNS is set: add `public/CNAME`, attach domain, enforce HTTPS, 301 `.xyz`→`.com`.
- [ ] Wire CUTLR footer "Fixing Flatware" reference → live umbrella URL.

## Revision v1.1 — mirror cutlr's `cal` addition (2026-07-11)

CUTLR gained a 6th tool `cal` (Calendly-shaped booking; see cutlr devplan v1.5).
`cal` is an **internal CUTLR module, not an umbrella product** → the roadmap grid is
**unchanged** (no new "coming soon" card). Only the CUTLR product card's function list
is re-synced with cutlr.xyz for consistency.

- [x] CUTLR product card (line 251): added **`bookings`** to the function list →
      "notes, to-dos, time tracking, scheduling, **bookings** and saved links."
      (mirrors cutlr's meta-description edit; `bookings` is a function, not a name — fits the umbrella rule.)
- [x] Commit + push (Pages auto-deploys).

## Revision v1.2 — add "Spreadsheet database" to the roadmap grid (2026-08-06) ✅

**Trigger:** Bending Spoons agreed to acquire Airtable (announced 2026-08-04, $1.285B cash,
$2.25B implied equity value; closing expected later this year, pending regulatory approval).
Three roadmap items already shadow that portfolio — Events (Eventbrite, acquired Mar 2026),
File transfer (WeTransfer), CUTLR's notes (Evernote). This card covers the highest-ARR
product of the group (~$480M ARR, +20% YoY, per-seat pricing).

**Scope call:** umbrella product, NOT a CUTLR module (unlike `cal` in v1.1). CUTLR is
single-user €2.99/mo everyday apps; a shared team database is a different buyer and a
different price shape. Function-named, no competitor reference, per the v1 rule.

**Naming call:** the market category term is **`no-code database`** (Baserow, NocoDB, Teable,
SeaTable all self-describe that way). Plain `Database` was rejected: in technical usage it
means DBaaS (Postgres/Supabase/Neon), a different market. Airtable's own current framing
(`app platform`, Gartner's LCAP) is enterprise positioning, not the function. Split adopted:
visible copy carries the plain-English **`Spreadsheet database`** (house style, cf. "File
transfer", "Site builder"); the searchable category term goes in `<meta name="description">`.
"Airtable alternative" stays out everywhere, meta included.

- [x] `public/index.html`: 6th "Coming soon" card between Site builder and More
- [x] `public/index.html`: `<meta name="description">` gains the roadmap clause with `no-code database`
- [x] `public/index.html`: footer "Tools" column gains `Spreadsheet database — soon`
      (not in the original plan — caught on the render check; the footer lists every product)
- [x] Render check at 1280px and 390px: title + `fn` fit on one line on desktop; on mobile the
      h3 flex wraps to two lines, same as the existing "Link shortener" / "Site builder" cards.
      No overflow. Grid is now 8 cards, 4 even rows of 2.
- [x] Commit + push (Pages auto-deploys)

### Deferred
- Grid ratio: 1 live vs 6 coming-soon weakens principle [06] "Honest by default". Later
  revision: split into "Next up" (the 2 actually being built) and a compact "On the bench" list.

### Out of scope (v1)
The actual future products; auth/one-account backend; per-product subpages.
