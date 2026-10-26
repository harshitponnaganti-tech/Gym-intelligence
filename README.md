# Gym Intelligence PWA — MVP Starter

A mobile-first fitness tracking PWA starter with custom exercise definitions, custom splits/days, set-level workout logging, subjective recovery logs, manual nutrition/body entries, basic analytics, IndexedDB persistence and JSON backup/restore.

## Run locally
1. Install Node.js 20+.
2. Extract this ZIP and open a terminal in the folder.
3. Run `npm install`.
4. Run `npm run dev`.
5. Open the local URL printed by Vite.

Build: `npm run build`; preview: `npm run preview`.

## Install as a PWA
Deploy the built `dist/` directory to HTTPS hosting. Configure Vite's `base` for a subpath deployment such as GitHub Pages. The included service worker provides a basic cache. App data is in IndexedDB and is not cleared by service-worker updates.

## Data safety
Use Data & Backup → Export JSON regularly. Imports validate the schema version and merge by stable IDs. Browser data clearing can remove local data.

## Cloud status — read this
This ZIP is a **local-first MVP starter**, not a finished cloud-synced service. It includes a Supabase SQL schema with per-user RLS policies and an `.env.example`, but authentication, queued bidirectional sync, conflict resolution and managed backup automation are not implemented. Do not assume cloud persistence until those pieces are built and tested. Never put a Supabase service-role key in frontend code.

## Current MVP scope
- Custom exercise definitions and muscle labels
- Custom split creation, days, exercise assignment
- Start a planned day, log load/reps, finish session
- Recovery self-report logs
- Manual food entries and weight logs
- Basic volume/working-set analytics and chart
- JSON backup/restore

## Not implemented yet
- Full generic custom-field editor/UI (starter creates an RIR field definition but doesn't render all field types)
- Superset/drop-set and detailed cardio/boxing logging
- Food database/search, recipes, micronutrients and serving-based calculations
- Advanced filters, configurable dashboards, correlations and report builder
- Cloud authentication, offline sync queue, conflict handling, wearable imports
- Automated cloud backups, photo attachments, full audit/revision history

This is an honest MVP foundation, not a claim that all items in the finalized specification are complete.
