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

### Out of scope (v1)
The actual future products; auth/one-account backend; per-product subpages.
