# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Project Is

Momentum Tracking is a SaaS practice management app built specifically for **solo personal trainers in Australia**. It replaces spreadsheets and generic invoicing tools with a single purpose-built system.

**Founder:** David Coyne — Melbourne-based PT with 12+ years running his own practice (Momentum Health & Fitness).
**Target user:** Solo Australian PTs, sole traders, 5–40 active clients, needing GST/BAS compliance.
**Tagline:** "Stop guessing, start knowing."

## Intended Tech Stack

- **Frontend:** Progressive Web App (PWA) — runs in any browser, installable on mobile, no app store
- **Backend/Database:** Supabase
- **Payments:** Stripe
- **Market:** Australia only — all figures in AUD, GST-registered sole traders

## Current Repo State

This repo currently holds SEO and AI-discovery files only. No application code exists here yet:

| File | Purpose |
|---|---|
| `index.md` | Product description / landing page content |
| `llms.txt` | AI-readable product summary for LLM discovery |
| `sitemap.xml` | Sitemap for momentumtracking.com.au |

The live domain is **momentumtracking.com.au**.

## Core Feature Domains

When building features, these are the main domains to model:

- **Clients** — profiles, health history, contact details, session notes
- **Sessions** — logged against a client, full history view
- **Packages** — prepaid session packs with automatic credit deduction
- **Revenue** — income by client, by period, by package type
- **Invoicing** — create and send invoices to clients
- **Expenses** — business expenses with category and GST fields
- **BAS/Tax Reporting** — quarterly GST summaries aligned with ATO requirements
- **Leads** — pipeline tracking from enquiry to sign-up
- **Payments** — Stripe card payments integration

## Australian Tax Context

This is critical domain knowledge for any financial feature:

- Users are **Australian sole traders registered for GST**
- GST is **10%** — must be tracked separately on income and expenses
- **BAS (Business Activity Statement)** is filed quarterly with the ATO
- Reports must surface: G1 (total sales), 1A (GST collected), 1B (GST paid on expenses)
- All monetary values in **AUD**

## Business Model

Subscription SaaS. Free 30-day trial. No lock-in. Cancel anytime via Stripe.

## Prompt Templates

Reusable templates are in `.claude/templates/`. Use them to start tasks cleanly:

| Template | Use when |
|---|---|
| `new-feature.md` | Planning any new feature before writing code |
| `supabase-schema.md` | Designing or modifying database tables |
| `bug-report.md` | Reporting something broken |
| `marketing-copy.md` | Writing Instagram, email, or landing page content |
| `stripe-integration.md` | Building any Stripe payment or webhook flow |

**How to use:** Copy the relevant template into your message, fill in the blanks, then send.
