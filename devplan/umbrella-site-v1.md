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

## Revision v1.3 — state the AI business model (2026-08-06) ✅

**What:** the "bring your own AI" idea currently lives only as half a line in principle [04],
and says how (MCP) but not who pays for what. It gets a manifesto paragraph — the AI surcharge
is the second wave of the software inflation the manifesto already attacks — and a sharpened [04].

**Honesty call:** "we don't resell you tokens" as an absolute contradicts the AI chat card
(cheaper conversations = resold inference). Scoped to "…to use our tools": true, and the AI chat
stays coherent as a product where conversations are what you're openly buying. Rejected:
switching AI chat to bring-your-own-key (reverses the v1 positioning decision, l.16) and
dropping the card.

**Copy constraints applied:** no invented price figures (a made-up "€10 → €30" in a manifesto
about pricing honesty argues against itself) and no competitor named, per the v1 rule.

- [x] `public/index.html`: third manifesto paragraph
- [x] `public/index.html`: principle [04] body rewritten
- [x] Render check at 1280px and 390px — [04] is 4 lines against 2–3 for the others; the row
      ([04][05][06]) stays aligned because the grid row takes the tallest cell. No overflow at
      either width; on mobile the principles stack single-column as before.
- [x] Commit + push

### Deferred
- `og:description` still reads "Honest prices, no lock-in, MCP-native" and does not carry the
  no-token-resale claim. Left alone: the social card has room for one idea, and the roadmap
  clause added in v1.2 already lengthened `meta name="description"`.

## Revision v1.4 — principle [04] carries the free-plan fact (2026-08-06) ✅

**Why:** cutlr v1.6 (`07b1788`) surfaced a house rule from the locked app plan
(`software/cutlr/ARCHITECTURE.md` §API & MCP): "gate throughput, never access" — MCP is on the
free plan, paying lifts the rate limit only. That is a rule for every tool, so it belongs in the
principles grid, and it is more concrete than the generic claim it replaces.

**Correction:** the plan predicted [04] would drop back to two lines. It doesn't — the new body
is 152 characters against 141, so it renders at the same four lines and stays the tallest of the
six cells. The swap is concrete-for-generic, not shorter-for-longer. Layout is unaffected (the
grid row takes the tallest cell), so the copy stands as approved.

- [x] `public/index.html`: [04] body → "…can drive it. It's there on the free plan too — paid
      plans lift the rate limit." (drops "We don't add an AI surcharge or meter you in credits" —
      the manifesto paragraph above already carries the token claim)
- [x] Render check at 1280px and 390px — row ([04][05][06]) aligned, no overflow at either width;
      see the Correction above for what the check disproved
- [x] Commit + push

**Not bringing over:** the 20 req/min figure and the tier names — the umbrella has no pricing
section and names future products by function only.

**Checked, no conflict:** the app plan says "CUTLR ships no chat — bring your own AI" while the
roadmap grid has an "AI chat" card. Consistent: that card is a separate umbrella product, not a
CUTLR module — the same distinction that scoped the token claim in v1.3.

### Out of scope (v1)
The actual future products; auth/one-account backend; per-product subpages.
