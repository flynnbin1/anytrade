# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AnyTrade is a single-page marketing and lead generation website for a North Dublin multi-trade service business. The entire site lives in one self-contained file: `index.html`.

## Stack

Vanilla HTML/CSS/JavaScript — no build tools, no frameworks, no dependencies. To preview, open `index.html` directly in a browser or serve it with any static file server (e.g. `npx serve .`).

## Architecture

Everything is in `index.html` (~1080 lines):

- **Lines 1–9**: `<head>`, Google Fonts imports (Syne for headings, DM Sans for body)
- **Lines 10–714**: All CSS in a single `<style>` block
- **Lines 715–1055**: HTML structure — sequential page sections:
  - `#services` — 8 trade service cards
  - `#how` — 4-step process + chat mockup
  - `#reviews` — customer testimonials
  - `#areas` — service area tags + contact info
  - `#quote` — lead generation form
- **Lines 1056–1079**: JavaScript — IntersectionObserver for scroll fade-ins, form submit handler (currently client-side only)

## Design System

CSS custom properties (variables) defined at the top of the `<style>` block:

- **Brand orange**: `#F56E0F` (primary), `#FF8C3B` (hover), `#C95500` (dark)
- **Typography**: Syne (800 weight headings/logo), DM Sans (body)
- **Mobile breakpoint**: 768px

## Known Incomplete Items

- **Form submission** (line ~1060): Currently a placeholder — comment says "connect to Jobber/webhook". No backend is implemented.
- **WhatsApp link**: Floating button and inline links use `https://wa.me/353XXXXXXXXX` — needs real number.
- Phone/email in footer link to `tel:016917151` and `mailto:hello@anytrade.ie`.
