# GATE DA 2027 Research Methodology

## Source Hierarchy (Strict Priority Order)

### TIER 1 — PRIMARY / AUTHORITATIVE
- Official GATE 2027 IIT Madras website (gate2027.iitm.ac.in)
- Official GATE 2027 DA Syllabus PDF
- Official GATE 2027 Question Paper Pattern
- Official GATE 2024 IISc website (gate2024.iisc.ac.in) — Question Papers, Answer Keys
- Official GATE 2025 IIT Roorkee website (gate2025.iitr.ac.in) — Question Papers, Answer Keys
- Official GATE 2026 IIT Guwahati website (gate2026.iitg.ac.in) — Question Papers, Answer Keys
- Official GATE Statistical/Performance Reports

### TIER 2 — OFFICIAL SUPPLEMENTARY
- Official GATE Information Brochures
- Official GATE Mock Tests
- Official GATE Announcements/Notifications

### TIER 3 — REPUTABLE ACADEMIC
- Peer-reviewed analysis of GATE patterns
- IIT professor publications on exam design

### TIER 4 — SECONDARY (Corroboration Only)
- Coaching institute analysis (MadeEasy, GATE Academy, etc.)
- Blogs, YouTube, Reddit, Quora
- **NEVER** used to override Tier 1/2 sources

---

## Classification Rules

### Domain Classification
- **Primary Domain**: The domain requiring the deepest knowledge to solve the question
- **Secondary Domain**: Domain providing context or auxiliary concepts
- **NO DOUBLE-COUNTING**: Marks assigned to primary domain only
- **Interdisciplinary Rule**: If a question genuinely spans two domains (e.g., PCA = Linear Algebra + ML), assign primary based on the *core mathematical operation* required. PCA → Linear Algebra (eigen-decomposition is the engine). Naive Bayes → Probability (Bayes theorem is the engine).

### Question Type Classification
- **MCQ**: Single correct option, negative marking (1/3 for 1-mark, 2/3 for 2-mark)
- **MSQ**: One or more correct options, ALL must be selected, no partial credit, no negative marking
- **NAT**: Numerical answer entered via virtual keypad, no negative marking

### Difficulty Scale (1-7)
1. Trivial — Direct recall / single formula application
2. Easy — Standard textbook problem, no twists
3. Moderate — Multi-step, standard concept, ~2-3 min
4. Moderate-High — Conceptual twist, requires insight
5. High — Non-standard variant, multi-concept synthesis
6. Very High — Complex multi-domain, heavy computation
7. Extreme — Novel variant, notation-heavy, trap-prone, ~4-6 min

### Cognitive Level (Bloom's Taxonomy Adapted)
- **Recall**: Definition, formula, fact retrieval
- **Comprehension**: Explain concept, identify applicable principle
- **Application**: Execute standard procedure on given input
- **Analysis**: Decompose problem, identify hidden structure, compare alternatives
- **Synthesis**: Combine concepts across domains, derive novel solution

### Solving Time Estimation
| Type | Marks | Estimated Time |
|------|-------|----------------|
| MCQ | 1 | 0.5 - 2 min |
| MCQ | 2 | 2 - 4 min |
| MSQ | 1 | 2 - 3 min |
| MSQ | 2 | 3 - 5 min |
| NAT | 1 | 2 - 4 min |
| NAT | 2 | 3 - 6 min |

### ROI Formula
```
ROI = (Expected Marks Yield) / (Hours Required to Master)
```
- Expected Marks Yield = Historical frequency × Average marks per appearance × Probability of appearance in 2027
- Hours Required to Master = Estimated study hours for Level 3+ mastery (timed solving)
- **Does NOT predict exact future marks** — used only for preparation prioritization

### Trend Methodology
- **Three years (2024-2026) is a VERY SMALL SAMPLE**
- Trends reported as: "Observed in 2024-2026" NOT "GATE has permanently shifted"
- Trajectory labels: STABLE, INCREASING, DECREASING, VOLATILE, INSUFFICIENT DATA
- No extrapolation beyond observed data
- Confidence levels: MAXIMUM, HIGH, MODERATE, LOW

### Confidence Levels for Claims
- **CONFIRMED**: Verified against Tier 1 source directly
- **PLAUSIBLE**: Consistent with Tier 1 evidence, minor discrepancies possible
- **WEAKLY_SUPPORTED**: Based on repository's own methodology, not official classification
- **UNSUPPORTED**: Asserted without evidence, or evidence contradicts
- **FALSE**: Directly contradicted by Tier 1 evidence
- **INSUFFICIENT_EVIDENCE**: Cannot determine with available data

---

## Data Pipeline

### Single Source of Truth
All structured data lives in `data/` as JSON:
- `questions_2024.json`, `questions_2025.json`, `questions_2026.json` — Complete question databases
- `taxonomy.json` — Classification system
- `trends.json` — Longitudinal analysis
- `archetypes.json` — Question archetype catalog
- `concept_network.json` — Prerequisite DAG
- `trap_taxonomy.json` — Psychometric trap catalog
- `syllabus_delta_2027.json` — 2027 syllabus comparison
- `validation_report.json` — Audit trail

### HTML Generation
HTML files (`index.html`, `solutions_1.html`, etc.) should be **generated from structured data** via templates, not hand-edited. This ensures:
- Consistency across documents
- Reproducibility
- Single point of truth
- Easy updates when new data arrives

### Error Log
Every correction recorded in `errors.json` with:
```json
{
  "date": "2026-10-02",
  "file": "strategy.html",
  "claim": "2026 ML = 25 marks",
  "old_claim": "25 marks",
  "new_claim": "14 marks",
  "evidence": "questions_2026.json extraction from repository's own question database",
  "problem": "Internal inconsistency: table contradicted own question data",
  "correction": "Updated to 14 marks",
  "source": "Tier 1: Official 2026 question paper (verified via repository's forensic database)",
  "severity": "CRITICAL",
  "status": "FIXED"
}
```

---

## Incorporating Future GATE Papers

When GATE 2027 paper is released:
1. Download official question paper and answer key (Tier 1)
2. Parse into `questions_2027.json` using same schema
3. Run validation against 2027 syllabus
4. Update `trends.json` with 2027 data point
5. Recompute ROI model
6. Update archetype frequencies
7. Generate new strategy recommendations
8. Archive 2027 analysis in `research/2027_analysis.md`

---

## Limitations & Uncertainty Awareness

1. **Sample Size**: 3 years × 65 questions = 195 data points. Statistical significance is LOW.
2. **Memory-Based Questions**: 2024-2026 data in repository may contain memory-based reconstructions, not official papers.
3. **Classification Subjectivity**: Domain/cognitive classification involves judgment. Inter-rater reliability not measured.
4. **Syllabus Changes**: 2027 syllabus revised. Historical patterns may not transfer.
5. **No Predictive Validity**: ROI scores and trend labels are preparation aids, not mark predictors.
6. **GA Fixed**: General Aptitude always 15 marks / 10 questions — not informative for DA-specific strategy.

---

## Reproducibility Checklist

- [ ] All claims cite Tier 1 source or explicitly state methodology
- [ ] All numerical tables reproducible from `data/*.json`
- [ ] All HTML generated from templates + data
- [ ] Error log complete with OLD/NEW/WHY/SOURCE
- [ ] Confidence levels assigned to every strategic claim
- [ ] Limitations section present in every output document
