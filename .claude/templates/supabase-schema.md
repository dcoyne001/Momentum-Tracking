# Template: Supabase Schema Design

## Feature / domain
[e.g. "Package management" or "BAS reporting"]

## What I need the schema to support
[Describe the behaviour, not the tables — let Claude design the tables]

## Relationships to existing tables
[e.g. "Each session belongs to a client and optionally a package"]

## Australian tax requirements (if financial)
- GST applies: yes / no
- Needs to appear in BAS report: yes / no
- Fields needed: amount_ex_gst, gst_amount, amount_inc_gst

## Constraints / rules
- [e.g. "A package credit cannot go below zero"]
- [e.g. "Sessions must have a date, client, and duration"]

## Ask Claude to
- [ ] Design the table schema with RLS policies
- [ ] Generate the SQL migration
- [ ] Generate TypeScript types
- [ ] Suggest indexes
