# GATE DA 2027 | Forensic Intelligence Research System

A rigorously audited, evidence-based research system for the GATE Data Science and Artificial Intelligence (DA) examination. This repository transforms personal "forensic dossier" research into a **reproducible, machine-readable, validation-tracked research infrastructure**.

## 🔬 What's New (Post-Audit)

This repository has undergone a **complete forensic re-audit** against Tier 1 official sources (official GATE question papers and answer keys from IISc Bengaluru, IIT Roorkee, IIT Guwahati, and IIT Madras). 

### Critical Corrections Made

| Claim (Original) | Corrected Value | Evidence |
|-----------------|----------------|----------|
| 2026 ML = 25 marks | **14 marks** | Verified from 65-question database |
| 2026 DBMS = 8 marks | **18 marks** | Verified from 65-question database |
| 2026 Programming & DSA = 10 marks | **14 marks** | Verified from 65-question database |
| 2026 Linear Algebra = 15 marks | **8 marks** | Verified from 65-question database |
| 2026 Calculus = 5 marks | **2 marks** (explicit) | Calculus embedded in ML questions |
| 2025 AI = 3 marks | **5 marks** | Verified from 65-question database |
| 2024 Solutions = "Complete" | **INCOMPLETE** (17/65) | Only 17 questions documented |
| "Examiner deliberately creates panic" | **Notation induces cognitive load** | Intent not evidenced; pattern recognized |

### Validation Summary
- **47 claims audited** against official sources
- **18 CONFIRMED**, 12 PLAUSIBLE, 9 WEAKLY_SUPPORTED, 5 UNSUPPORTED, 3 FALSE
- Full audit trail in `research/validation_report.json`

---

## 📁 Repository Structure

```
gate2027/
├── index_corrected.html          # Home & DNA (with Research System section)
├── solutions_1_corrected.html    # 2026 Intel & 2024 Solutions (marked incomplete)
├── solutions_2_corrected.html    # 2025 & 2026 Complete Forensic Databases
├── strategy_corrected.html       # Strategic Architecture (corrected weightage)
├── battle_plan_corrected.html    # Execution & Battle Plan (corrected targets)
├── data/                         # 📊 MACHINE-READABLE SOURCE OF TRUTH
│   ├── questions_2024.json       # Partial 2024 (17/65 verified)
│   ├── questions_2025.json       # Complete 2025 (65/65)
│   ├── questions_2026.json       # Complete 2026 (65/65)
│   ├── questions_2025_corrected.json  # Standardized subtopic classification
│   ├── questions_2026_corrected.json  # Standardized subtopic classification
│   ├── subtopic_marks_summary.json    # Subtopic-level marks breakdown
│   ├── taxonomy.json             # Classification system (domains, types, difficulty)
│   ├── trends.json               # 3-year longitudinal analysis
│   ├── archetypes.json           # 25 recurring question archetypes
│   ├── concept_network.json      # Prerequisite DAG + bridge concepts
│   ├── trap_taxonomy.json        # 12 psychometric trap categories
│   ├── syllabus_delta_2027.json  # 2027 vs historical syllabus
│   ├── corrected_weightage.json  # Verified marks tables
│   └── source_registry.json      # All sources catalogued by tier
├── research/
│   ├── methodology.md            # Source hierarchy, classification rules, ROI formula
│   └── validation_report.json    # Complete claim-by-claim audit
└── .github/workflows/gh-pages.yml  # GitHub Pages deployment
```

---

## 🎯 Corrected 2027 Strategy Highlights

### Verified Marks Distribution (2025-2026)
| Domain | 2025 | 2026 | Trajectory |
|--------|------|------|------------|
| Probability & Statistics | 19 | 20 | 📈 **Accelerating** |
| Machine Learning | 14 | 14 | ➡️ **Surged then Stable** |
| Database Management | 11 | 18 | 📈 **Accelerating** |
| Linear Algebra | 12 | 8 | 🔄 **Fluctuating** |
| Programming & DSA | 14 | 14 | ➡️ **Stable (post-2024 drop)** |
| Artificial Intelligence | 5 | 8 | 🔄 **Fluctuating** |
| Calculus & Optimization | 9 | 2 | 📉 **Implicit in ML** |
| General Aptitude | 15 | 15 | ➡️ **Constant** |

### Top ROI Archetypes (from `data/archetypes.json`)
1. **Bayesian Inference** — Absolute frequency, 5-6 marks/year, ROI 0.625
2. **Relational Algebra & SQL** — Absolute frequency, 5-8 marks/year, ROI 0.500
3. **Python Mutable Scope** — Absolute frequency, 3-4 marks/year, ROI 0.500
4. **PCA / Eigen Properties** — Absolute frequency, 4-5 marks/year, ROI 0.450
5. **SVM Geometric Margins** — High AIR separation, plot-first approach

### Bridge Concepts (Study These First)
- **Eigenvalues/SVD** → Linear Algebra + ML (PCA) + Optimization
- **Conditional Probability/Bayes** → Probability + ML (Naive Bayes) + AI (Bayesian Networks)
- **Projection Matrices** → Linear Algebra + ML (PCA, Regression) + Statistics (Centering)
- **Gradient Descent** → Calculus + ML (Regression, NN) + SVM

---

## 📚 Source Hierarchy (Strict)

**TIER 1** — Official GATE websites, question papers, answer keys
**TIER 2** — Official brochures, mock tests
**TIER 3** — Reputable academic analysis
**TIER 4** — Coaching sites, blogs (corroboration only)

**Never** use Tier 3/4 to override Tier 1/2.

---

## 🔧 How to Use This System

### For Study Planning
1. Read `research/methodology.md` for classification rules and ROI formula
2. Review `data/trends.json` for domain trajectories
3. Focus on `data/archetypes.json` Tier A (ranks 1-10) archetypes
4. Follow `data/concept_network.json` study order: LA → Probability → Calculus → PD → DB → ML → AI

### For Verification
- Every strategic claim in HTML files traces to `data/*.json`
- Every correction logged in `research/validation_report.json` with OLD/NEW/WHY/SOURCE
- HTML should be regenerated from data (future work)

### For Contributing
When GATE 2027 paper releases:
1. Download official paper + answer key (Tier 1)
2. Parse into `data/questions_2027.json` using same schema
3. Run validation against 2027 syllabus (`data/syllabus_delta_2027.json`)
4. Update trends, archetypes, ROI model
5. Append to `research/validation_report.json`

---

## ⚠️ Limitations

1. **Sample Size**: 3 years × 65 questions = 195 data points — statistical significance is LOW
2. **2024 Incomplete**: Only 17/65 questions verified — 2024 trends are speculative
3. **Memory-Based Data**: 2024-2026 data may contain memory-based reconstructions
4. **No Predictive Validity**: ROI scores and trends are preparation aids, NOT mark predictors
5. **Syllabus Revised**: 2027 syllabus changed — historical patterns may not transfer

---

## 📖 Documents (Corrected Versions)

| Document | Title | Status |
|----------|-------|--------|
| `index_corrected.html` | 01. Home, DNA & Research System | ✅ Updated with research section |
| `solutions_1_corrected.html` | 02. 2026 Intel & 2024 Solutions | ⚠️ Marked incomplete (17/65) |
| `solutions_2_corrected.html` | 03. 2025 & 2026 Complete Databases | ✅ 65/65 verified each |
| `strategy_corrected.html` | 04. Strategic Architecture | ✅ Weightage table corrected |
| `battle_plan_corrected.html` | 05. Execution & Battle Plan | ✅ ML target corrected to 12/14 |

---

## 🚀 Deployment

This site auto-deploys to GitHub Pages via GitHub Actions on every push to `main`.

**Live Site**: https://hardik-sankhla.github.io/gate2027/

---

## 📄 License

Personal research repository. Official GATE materials copyright their respective organizing institutes.
