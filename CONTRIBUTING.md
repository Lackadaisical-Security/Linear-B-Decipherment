# Contributing to the Linear B Decipherment Project

**By:** Lackadaisical Security
**Website:** https://lackadaisical-security.com

> Read the [Code of Conduct](CODE_OF_CONDUCT.md) first. Evidentiary merit, methodological rigour, and intellectual honesty — nothing else.

The Linear B Decipherment Project resolved 70 years of open questions in the Bronze Age Aegean syllabary — questions left by Michael Ventris and John Chadwick when they cracked the core of the script in 1952. They built the foundation. This project closes the gap they left. Every contribution — whether a new correlation vector, a lexicon correction, a methodology improvement, or a phase log addendum — matters. The research is alive. Make it better.

---

## Getting Started

### Prerequisites

Before contributing, ensure you have:

- Working knowledge of the Linear B signary and Ventris-Chadwick framework (baseline)
- Read at least one Phase log and the UDM20-LB methodology document
- Familiarity with at least one comparison script corpus used in the project (Linear A, Cypro-Minoan, Phoenician, Proto-Sinaitic, etc.)
- Git configured and functional
- Understanding of the evidentiary standard — minimum 3 independent vectors for any definitive claim

### Read First

```
README.md                        ← Project overview and structure
CODE_OF_CONDUCT.md               ← How this project operates
UDM20-LB_v1_0_Linear_B_Methodology.md   ← The framework you're contributing to
LINEAR_B_FINAL_COMPREHENSIVE_REPORT.md  ← Current state of the decipherment
```

If you haven't read all four, stop here and go read them.

---

## Development Workflow

### Fork and Clone

```bash
# Fork via GitHub UI, then clone your fork
git clone https://github.com/YOUR_USERNAME/Linear-B-Decipherment.git
cd Linear-B-Decipherment

# Add upstream remote
git remote add upstream https://github.com/Lackadaisical-Security/Linear-B-Decipherment.git
```

### Branching Strategy

- `main` — stable, reviewed research only
- `feature/your-contribution` — new analysis additions
- `fix/issue-description` — factual corrections with sourcing
- `lexicon/sign-id-description` — lexicon-specific updates

### Standard Workflow

```bash
# Sync with upstream before starting
git fetch upstream
git checkout main
git merge upstream/main

# Create your branch
git checkout -b fix/sign-49-formula-marker-correction

# Make your changes, then commit
git add .
git commit -m "fix(lexicon): correct sign *49 formula marker citation to Bennett 1953"

# Push and open a PR targeting main
git push origin fix/sign-49-formula-marker-correction
```

### Commit Message Format

```
type(scope): short description (max 72 chars)

Longer explanation of WHY the change is needed, not just what it does.
For analysis changes, include the vector basis and confidence impact.

Fixes #123
```

Types: `fix`, `feat`, `docs`, `lexicon`, `phase`, `methodology`, `data`

---

## Research Standards

### What Counts as a Contribution

#### ✅ In Scope
- **Methodology improvements** — demonstrably higher-confidence correlation or more accurate phonetic reconstruction, with full evidence chain
- **Cross-script correlation additions** — new vectors from comparison scripts with sourced corpus entries
- **Error corrections** — factual errors in phase logs with correction and source citation
- **Lexicon refinements** — sign meaning or phonetic value updates backed by comparative linguistic evidence
- **Data format improvements** — the JSON lexicon has a defined schema; schema improvements welcome if backward-compatible
- **Archaeological context additions** — new tablet analyses, palatial context data, or stratigraphic findings affecting sign interpretation
- **Additional validation vectors** — independent confirmations of existing resolutions, cited and sourced

#### ❌ Out of Scope
- Requests to soften methodology language for academic audiences
- Contributions from [banned institutions](./README.md#-institutionally-banned-entities)
- "Alternative perspectives" with no evidentiary backing
- Reformatting working documents to match someone else's style guide
- Submissions introducing ideological framing into linguistic analysis
- Issues asking why the project hasn't submitted to peer review

---

## Evidence Standards

This project applies the same evidentiary standard to contributions that it applies to its own output. No exceptions.

| Claim Type | Required Support |
|------------|-----------------|
| Sign phonetic value | Cross-script comparison + Greek phonotactic compliance + minimum 3 independent vectors |
| Minoan substrate assignment | Linear A / Cypro-Minoan parallel + archaeological or palatial context |
| Confidence score | Methodology application + independent vector count shown explicitly |
| Archaeological fact | Published excavation record or tablet provenance citation |
| Statistical result | Calculation shown, dataset cited, method documented |
| New correlation hit | Source corpus identified, entry count stated, overlap explained |

**"I think" and "it seems" are not evidence.**
**"The data shows X at Y vectors via Z corpus with W% Greek phonotactic compliance" is evidence.**

### The Rule of Independent Vectors

Minimum thresholds under UDM20-LB:

- **3+ vectors** → minimum for consideration
- **5+ vectors** → DEFINITIVE — publication-ready
- **4 vectors** → HIGH CONFIDENCE — flag for additional validation
- **1–2 vectors** → not accepted without exceptional justification

Vectors must be *independent* — from distinct scripts, corpora, or methodological approaches. Repeating the same source in different forms is not multiple vectors.

---

## Documentation Style

### Phase Logs

Phase logs are formatted consistently. Do not restructure them. If adding to a phase log:

- Maintain the existing header block (date, analyst, methodology, status)
- Add numbered sub-sections inline with existing numbering
- State confidence levels explicitly in every new finding block
- Cite sources inline, not in a separate bibliography

### Lexicon JSON

The master lexicon has a defined schema. Additions must conform:

```json
{
  "sign_id": "*49",
  "unicode_codepoint": "U+10083",
  "standard_transliteration": null,
  "ls_enhanced_resolution": {
    "functional_class": "formula_delimiter",
    "confidence": "DEFINITIVE",
    "vector_count": 13,
    "primary_corpus": ["Egyptian_administrative", "Demotic", "Hieratic"],
    "notes": "Non-phonetic clause boundary marker confirmed via 13-vector convergence"
  }
}
```

Do not delete or overwrite the standard Unicode layer. The LS-enhanced layer is additive.

### Commit and PR Descriptions

Include in every PR description:

- What changed and why
- Evidence supporting the change (vector count, corpus cited)
- Confidence estimate if applicable
- Cross-references to existing phases or lexicon entries
- Any flags for further validation

**PRs with no description get closed immediately.**

---

## Submission Process

### 1. Open an Issue First (For Significant Changes)

Before submitting a PR for anything beyond a clear factual correction, open an issue:

- What you found
- Why it matters
- What evidence supports it
- Which existing phase or lexicon entry it affects

If the Operator responds, great. If not, the issue stays on record.

### 2. Submit the Pull Request

```bash
git push origin your-branch-name
```

Open the PR on GitHub targeting `main`. Fill in the description template completely.

### 3. Review Process

PRs are reviewed for:

| Criterion | What We Check |
|-----------|--------------|
| **Accuracy** | Does the claim hold under the existing methodology? |
| **Evidence** | Are the vectors real, sourced, and independent? |
| **Methodology compliance** | Does it follow UDM20-LB standards? |
| **Document integrity** | Does it maintain existing formatting and schema? |
| **Reproducibility** | Can the finding be independently verified? |

**Review timeline:**
- Factual corrections: 1–3 days
- Lexicon updates: 3–7 days
- Phase log additions: 7–14 days
- Methodology changes: 14+ days (significant review required)

---

## File Structure

```
/
├── README.md                                    ← Project overview (no structural rewrites)
├── CODE_OF_CONDUCT.md                           ← How this community operates
├── CONTRIBUTING.md                              ← You are here
├── UDM20-LB_v1_0_Linear_B_Methodology.md       ← Core methodology — read before contributing
├── LINEAR_B_PHASE_[N]_*.md                      ← Phase research logs
├── LINEAR_B_COMPREHENSIVE_FINDINGS.md           ← 22-script analysis synthesis
├── LINEAR_B_FINAL_COMPREHENSIVE_REPORT.md       ← 36-script final report
├── UDM20_LINEAR_B_INDEPENDENT_MANUAL_PASS_LS_2026-05-04.md  ← Independent audit
├── linear_b_MASTER_lexicon_unicode_plus_ls_enhanced_2026-05-03.json  ← Master lexicon
├── Complete Resolution of the Linear B Syllabogram Inventory *.md    ← Academic paper (MD)
├── Complete Resolution of the Linear B Syllabogram Inventory *.pdf   ← Academic paper (PDF)
├── ghost_license_v_1.md                         ← Ghost License v1.0
└── ancient_scripts_attribution_license_v1.md   ← ASAL-1.0
```

---

## Licensing

By submitting a contribution, you agree your work is licensed under the same dual license as this repository:

- **Ghost License v1.0** ([ghost_license_v_1.md](./ghost_license_v_1.md))
- **Ancient Scripts Attribution License v1.0** ([ancient_scripts_attribution_license_v1.md](./ancient_scripts_attribution_license_v1.md))

Both must be followed simultaneously. No exceptions.

You confirm your contribution does not contain plagiarised content, does not misattribute existing research, and does not introduce institutional framing designed to compromise research integrity.

If you are contributing on behalf of an institution, check the [banned institutions list](./README.md#-institutionally-banned-entities) first. Submissions from banned entities are rejected and reported.

---

## Recognition

Accepted contributions are acknowledged in the relevant phase log or document. There is no leaderboard, badge system, or GitHub profile promotion. If your contribution improves the research, the research improves. That is the reward.

---

## Community & Contact

- **Email**: lackadaisicalresearch@pm.me
- **XMPP+OTR**: thelackadaisicalone@xmpp.jp
- **Website**: https://lackadaisical-security.com
- **Decipherment updates**: https://lackadaisical-security.com/decipherment-drops.html

Do not email asking for contribution approval before you've done the work. Do the work. Submit it. If it's good, it gets merged.

---

**TL;DR**: Read the methodology. Show your vectors. Cite your sources. Don't fake it. Don't steal it. If your analysis holds up, it gets in.

**Copyright © 2025–2026 Lackadaisical Security. All rights reserved.**
