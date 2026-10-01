# CHANGELOG — GATE DA 2027 Forensic Re-Audit

## 2026-10-02 — Forensic Re-Audit & Research System Build

### Critical Data Corrections
- **FIXED**: 2026 Machine Learning marks: 25 → 14 (verified from 65-question forensic database)
- **FIXED**: 2026 Database Management marks: 8 → 18 (major correction from question database)
- **FIXED**: 2026 Programming & DSA marks: 10 → 14
- **FIXED**: 2026 Linear Algebra marks: 15 → 8
- **FIXED**: 2026 Calculus & Optimization marks: 5 → 2 (explicit; calculus concepts embedded in ML)
- **FIXED**: 2025 Artificial Intelligence marks: 3 → 5
- **FIXED**: 2025 DBMS marks: 9 → 11 (from verified data)
- **FIXED**: 2025 Calculus marks: 8 → 9 (from verified data)
- **FIXED**: 2025 Linear Algebra marks: 17 → 12 (from verified data)
- **FIXED**: 2025 Programming & DSA marks: 16 → 14 (from verified data)
- **FIXED**: Question count: "55 Questions" → "65 Questions (10 GA + 55 Subject)" in all headers
- **FIXED**: 2024 Solutions Database: Marked INCOMPLETE (17/65 questions documented)
- **FIXED**: 2024 Q2 solution: Added disclaimer that independent solution pending figure retrieval

### Examiner Psychology Claims Qualified
- "IIT Guwahati deliberately created notation panic" → "Notation induces cognitive load; recognition yields shortcuts"
- "Examiner punished students who..." → "Question rewards candidates who recognize X over those who apply Y"
- "IIT Guwahati prioritizes First Principles" → "2026 patterns consistent with emphasis on mathematical derivation"

### New Research Infrastructure (Machine-Readable)
Added `data/` directory with 14 JSON datasets:
- `questions_2024.json`, `questions_2025.json`, `questions_2026.json` — Raw extracted data
- `questions_2025_corrected.json`, `questions_2026_corrected.json` — Standardized subtopic classification
- `taxonomy.json` — Complete classification system (domains, types, difficulty, cognitive levels, ROI formula)
- `trends.json` — 3-year longitudinal analysis with confidence levels and caveats
- `archetypes.json` — 25 recurring question archetypes with frequency, marks, traps, fastest methods
- `concept_network.json` — Prerequisite DAG with 70+ nodes and 7 bridge concepts
- `trap_taxonomy.json` — 12 psychometric trap categories with countermeasures
- `syllabus_delta_2027.json` — Official 2027 syllabus vs historical coverage
- `corrected_weightage.json` — Verified marks tables with 2024 caveats
- `subtopic_marks_summary.json` — Subtopic-level marks breakdown
- `source_registry.json` — All sources catalogued by tier (14 Tier 1, 1 Tier 2, 4 Tier 4)

### Validation & Methodology
Added `research/` directory:
- `validation_report.json` — 47-claim audit with CONFIRMED/PLAUSIBLE/WEAKLY_SUPPORTED/UNSUPPORTED/FALSE classifications
- `methodology.md` — Complete methodology: source hierarchy, classification rules, ROI formula, trend methodology, confidence levels, error log format, reproducibility checklist

### Updated HTML Documents (Corrected Versions)
- `index_corrected.html` — Added Research System section (Phase 6), updated navigation
- `solutions_1_corrected.html` — Marked 2024 DB incomplete, fixed Q2 disclaimer
- `solutions_2_corrected.html` — Fixed question count headers (65 questions)
- `strategy_corrected.html` — Corrected weightage table, narrative text, Pareto analysis
- `battle_plan_corrected.html` — Corrected ML target from 20/25 to 12/14

### Original Files Preserved
All original HTML files retained (`index.html`, `solutions_1.html`, `solutions_2.html`, `strategy.html`, `battle_plan.html`) for comparison.

---

## Next Steps (When GATE 2027 Paper Released)
1. Download official 2027 question paper + answer key (Tier 1)
2. Parse into `data/questions_2027.json` using existing schema
3. Validate against `data/syllabus_delta_2027.json` 2027 syllabus
4. Update `data/trends.json` with 2027 data point
5. Recompute `data/archetypes.json` frequencies
6. Update ROI model in `data/taxonomy.json`
7. Append audit entries to `research/validation_report.json`
8. Regenerate HTML from data (future: template system)
