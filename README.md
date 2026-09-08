# Memory Palace V2 · AP Biology

## Mainline Units 1–5

This repository is the consolidated student-ready mainline for **AP Biology Units 1–5**. Together they contain **889 canonical records, 38 guided journeys, 282 permanent scenes/loci, and 67 Challenge Lab items**. Units 3, 4, and 5 have completed F6 functional browser-facing/classroom validation. Units 6–8 remain registered source-ready placeholders.

See `docs/MAINLINE_RELEASE_U1_U5.md` for the integrated release audit.

## Current course state

- **Unit 1 · Chemistry of Life** — student-ready, 229 canonical records, 9 journeys, 78 loci, 16 Challenge Lab items.
- **Unit 2 · Cells** — student-ready, 142 canonical records, 7 journeys, 49 loci, 9 Challenge Lab items.
- **Unit 3 · Cellular Energetics** — student-ready and F6 validated, 186 canonical records, 7 journeys, 54 loci, 11 Challenge Lab items, 4 scope guards.
- **Unit 4 · Cell Communication and Cell Cycle** — student-ready and F6 validated, 180 canonical records, 162 runtime Memory Objects, 7 journeys, 51 loci, 15 Challenge Lab items, 3 scope guards, 162 exact-name Review targets, and 33 mixed-discrimination sets with 99 questions.
- **Unit 5 · Heredity** — student-ready and F6 validated, 152 canonical records, 131 runtime Memory Objects, 8 journeys, 50 loci, 18 optional first-exposure recalls, 16 Challenge Lab items, 5 scope guards, 130 exact-name Review targets, and 32 mixed-discrimination sets with 79 questions.

The learner interface remains **Home · Learn · Review**. Challenge Lab is launched from Home. Mixed discrimination appears inside Review only after every associated science record has been encountered and the delay has elapsed.

## Development server

```bash
pip install -r requirements.txt
python -m uvicorn backend.main:app --host 0.0.0.0 --port 8000 --reload
```

Open a released unit with `/?unit=unit-1`, `/?unit=unit-2`, `/?unit=unit-3`, `/?unit=unit-4`, or `/?unit=unit-5`.

## QA

GitHub Actions rebuilds Unit 1, Unit 2 through F5, Unit 3 through F6, Unit 4 through F6, and Unit 5 through F6. It verifies every frozen Unit 5 gate from F1 through F6, both historical and current mainline gates, the full Python suite, Unit 3 through Unit 5 UI-logic QA, JavaScript syntax, and deterministic repository cleanliness with `git diff --exit-code`.

For the current mainline

```bash
python scripts/build_unit5_f5.py
python scripts/qa_unit5_f5.py
python scripts/build_unit5_f6.py
python scripts/qa_unit5_f6.py
python scripts/qa_mainline_u1_u5.py
python -m pytest -q
```

## Validation boundary

Unit 5 F6 has completed functional browser-facing/classroom validation across production scene rendering, hidden Quick Recall states, persistence, Review behavior, Challenge Lab behavior, unit switching, responsive contracts, and live HTTP/API behavior. The sandbox Chromium limitation prevents a screenshot-level or pixel-level claim.

## Current runtime

```text
v2-apbio-0.24.0-u5-f6
```

## Next curriculum stage

Unit 5 is complete through F6. The next curriculum gate is **Unit 6 scientific locking**. Complete source inventory, scientific atomization, AP-scope mapping, conflict/misconception audit, and canonical locking before writing Unit 6 narratives.
