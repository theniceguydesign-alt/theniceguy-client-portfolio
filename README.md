# Theniceguy.Design — Client Website Portfolio

Central repository for all client websites, pitch decks, and agency projects built by Theniceguy.Design LLC.

## Project Structure

### `/paul-williams-insurance/`
**Status:** ✅ LIVE at paul-williams-insurance.pages.dev

Complete fullstack insurance agency website with:
- Cinematic landing page (6 sections)
- 10-section intake form (Acrisure replica)
- Admin dashboard with OAuth authentication
- MySQL database backend
- tRPC API

**Deployment:** Cloudflare Pages + GitHub Actions auto-deploy

---

### `/client-pitches/`
**Status:** ✅ Ready for Presentation

10 professional 5-page static pitch decks (PDF-ready):

1. **Cafe Gianni** — Italian restaurant (dark red branding)
2. **Kings Donuts** — Donut shop (warm brown branding)
3. **Bavaria Haus** — German cafe (vintage aesthetic)
4. **Blow Hair Studio** — Hair salon (elegant luxury)
5. **Auto Detailing Fabian** — Car detailing (professional blue)
6. **Donnelly House** — Residential (classic white)
7. **Faden Builders** — Construction (industrial gray)
8. **Lemon Drop Market** — Grocery store (fresh yellow)
9. **MJS Home Improvements** — Contractor (earth tones)
10. **Moonlit Acre Carriages** — Luxury transport (midnight blue)

Each pitch includes: Problem statement, solution, business impact, and CTA.

**Format:** Static HTML, responsive, print-optimized

---

### `/theniceguy-design-agency/`
**Status:** ✅ LIVE at theniceguy-design.com

Agency hub with three sections:
- `/agency/` — Core services & portfolio
- `/disputes/` — Dispute resolution services
- `/loadless/` — LOADLESS™ cognitive load reduction platform

---

### `/docs/`
**Status:** ✅ Complete

Documentation and proposals:
- `DEPLOYMENT_GUIDE_AND_PRICING.md` — Full pricing breakdown
- `Paul_Williams_Complete_Proposal.docx` — Client deliverables
- `SITE_AUDIT_AND_FEATURE_COMPARISON.md` — Technical audit
- Implementation guides for all features

---

## Deployment

All projects deploy via **Cloudflare Pages** with GitHub Actions auto-deploy.

### Paul Williams Insurance
```bash
git push origin main
# Automatically deploys to: https://paul-williams-insurance.pages.dev
```

### Client Pitches (Static HTML)
Each pitch can be deployed independently or as a collection.

### Agency Website
```bash
git push origin main
# Automatically deploys to connected Cloudflare Pages domain
```

---

## Quick Setup

1. **Clone the repo:**
   ```bash
   git clone https://github.com/theniceguydesign-alt/theniceguy-client-portfolio.git
   cd theniceguy-client-portfolio
   ```

2. **For Paul Williams Insurance:**
   ```bash
   cd paul-williams-insurance
   npm install
   npm run build
   ```

3. **For client pitches:**
   Open any `/client-pitches/*/index.html` in browser or deploy as static site.

4. **For agency website:**
   ```bash
   cd theniceguy-design-agency
   npm install
   npm run build
   ```

---

## File Inventory

- **Paul Williams Insurance:** 90 hours, $16,400 market value
- **10 Client Pitches:** Static HTML, 5 pages each, presentation-ready
- **Agency Website:** Full responsive multi-section hub
- **Documentation:** Deployment guides, proposals, audit reports

---

## Status Dashboard

| Project | Status | Deployed | Last Update |
|---------|--------|----------|-------------|
| Paul Williams Insurance | ✅ Complete | paul-williams-insurance.pages.dev | Jun 2026 |
| Client Pitches (10) | ✅ Complete | Ready for download | Jun 2026 |
| Theniceguy Agency | ✅ Complete | In deployment | Jun 2026 |

---

## Support & Maintenance

Zero maintenance required for static sites (client pitches).

Paul Williams Insurance requires monitoring of:
- Database backups
- Admin dashboard security
- Form submissions processing

---

**Last Updated:** June 22, 2026  
**Maintained By:** Theniceguy.Design LLC  
**Contact:** theniceguy.design@gmail.com
