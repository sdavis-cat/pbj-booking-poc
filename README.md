# PBJ Booking Console — POC

An interactive, clickable prototype for a band-booking agency platform. It demonstrates the
core workflow across three roles — **Agency admin**, **Venue**, and **Band** — in a single,
self-contained web page (no build step, no backend).

> ⚠️ **All artist, email, and agent data in this prototype is fictional sample data**
> (`example.com` is a reserved domain). It does not represent any real roster.

## Live demo

If GitHub Pages is enabled for this repo, the demo is here:
**https://stevedavis7.github.io/pbj-booking-poc/**

Or just open `index.html` in any browser.

## What it shows

Switch roles from the left rail; use the "acting as" dropdown to become a specific venue or band.

**The core loop:**
1. **Venue** posts an available date (availability only — no price).
2. **Agency** sets the fee for that date and approves which bands may pitch which venues.
3. **Band** (once approved for that venue) applies to open dates.
4. **Venue** confirms a band — which creates a booked gig.
5. **Payment** is tracked through the lifecycle: unpaid → invoiced → paid.

**Business rules modeled:**
- Bands can only apply to venues that the **agency has approved** them for (access requests
  route to the agency).
- The **agency controls the money** — a venue cannot confirm a booking until the agency has
  priced the date.

## Status

This is a UI/UX proof of concept only. There is **no persistence** (a refresh resets all
state), no authentication, and no database. It exists to validate the flows and the data model
before any real implementation.

## Possible next steps

- Real accounts + roles (agency / venue / band) with permissioned access
- Postgres (or similar) backing store + API
- Full roster import
- Deposits, agency commission %, invoicing and payouts
- Packaging for web + mobile + desktop
