# Start Here · Mainline AP Biology Units 1–5 · Unit 5 F6

This is the clean repository-root package for the current `memory-palace-v2` mainline.

## Included

Units 1 through 5 are student-ready. Units 3, 4, and 5 have completed F6 functional browser-facing/classroom validation. Units 6–8 remain source-ready placeholders.

Combined Units 1–5 contain **889 canonical records, 38 guided journeys, 282 permanent scenes/loci, and 67 Challenge Lab items**.

Unit 5 contains **152 canonical records with zero loss, 131 runtime Memory Objects, 8 journeys, 50 scenes, 18 optional first-exposure recalls, 16 Challenge Lab tasks, 5 non-runtime scope guards, 130 delayed exact-name Review targets, and 32 mixed-discrimination sets with 79 questions**.

## Update GitHub

Unzip the release, open the included `memory-palace-v2` folder, and copy **the contents of that folder** into the root of the existing private `memory-palace-v2` repository, replacing matching files. Do not upload the ZIP itself, source PDFs, SQLite files, `.env`, caches, or historical work folders.

A suitable commit message is

```text
Release AP Biology Unit 5 F6 and validated Units 1–5 mainline
```

## Run before committing

```bash
python scripts/qa_unit4_f6.py
python scripts/qa_unit5_f1.py
python scripts/qa_unit5_f2.py
python scripts/qa_unit5_f3.py
python scripts/qa_unit5_f4a.py
python scripts/qa_unit5_f4b.py
python scripts/qa_unit5_f4c.py
python scripts/qa_unit5_f4d.py
python scripts/qa_unit5_f4e.py
python scripts/qa_unit5_f4f.py
python scripts/qa_unit5_f4g.py
python scripts/qa_unit5_f4h.py
python scripts/build_unit5_f5.py
python scripts/qa_unit5_f5.py
python scripts/build_unit5_f6.py
python scripts/qa_unit5_f6.py
python scripts/qa_mainline_u1_u5.py
node scripts/qa_unit3_f6_ui.mjs
node scripts/qa_unit4_f6_ui.mjs
node scripts/qa_unit5_f6_ui.mjs
python -m pytest -q
```

## Preview

```bash
python -m uvicorn backend.main:app --host 0.0.0.0 --port 8000 --reload
```

The public student runtime exposes Units 1–5.

## Current runtime

```text
v2-apbio-0.24.0-u5-f6
```

## Validation boundary

Unit 5 has completed functional browser-facing/classroom validation. All 50 production scenes and 18 hidden Quick Recall states were exercised through the production rendering functions, together with Review, mixed-discrimination, Challenge Lab, persistence, unit switching, responsive CSS contracts, and live HTTP/API checks.

The sandbox Chromium executable times out even on a blank headless page. This package therefore does not claim screenshot-level or pixel-level browser validation.

## Next branch

Begin **Unit 6 scientific locking**. Complete source inventory, scientific atomization, AP-scope mapping, conflict/misconception audit, and the canonical lock before writing any Unit 6 palace or narrative.

See `docs/UNIT5_F6_RELEASE.md`, `docs/UNIT5_F6_CLASSROOM_BROWSER_QA.md`, `docs/UNIT5_F6_INTEGRATION_AUDIT.md`, `docs/UNIT5_F6_PACKAGE_QA.md`, and `docs/MAINLINE_RELEASE_U1_U5.md`.
