# 🔬 Contributing to the Linear B Decipherment Project

### *"Prove your worth in the work itself."*

---

## Before You Start

Read the [README.md](./README.md). Read the [Code of Conduct](./CODE_OF_CONDUCT.md). Read at least one Phase log. If you haven't done those three things, stop here and go do them.

This project is not a place to learn what Linear B is. It's a place to contribute to understanding it.

---

## What Contributions Are Accepted

### ✅ In Scope

- **Methodology improvements** — if you can demonstrate a higher-confidence correlation or a more accurate phonetic reconstruction, show your work and submit it
- **Cross-script correlation additions** — new data from comparison scripts with sourced evidence
- **Error corrections** — if a phase log contains a factual error, open an issue with the correction and the source
- **Lexicon refinements** — sign meaning or phonetic value updates backed by archaeological or comparative linguistic evidence
- **Data format improvements** — the JSON lexicon is a living document; schema improvements welcome
- **Archaeological context additions** — new tablet analyses, palatial context data, or stratigraphic findings that affect sign interpretation
- **Vector additions** — additional independent validation vectors for any of the 11 resolved signs, with source citation

### ❌ Out of Scope

- Requests to soften the methodology language for academic audiences
- Requests to add attribution to institutions on the banned list
- "Alternative perspectives" with no evidentiary backing
- Contributions that introduce ideological framing into linguistic analysis
- Reformatting working documents to comply with someone else's style guide
- Issues asking why we haven't submitted to peer review

---

## How to Contribute

### 1. Open an Issue First (For Significant Changes)

Before submitting a pull request for anything beyond a clear factual correction, open an issue. Describe:

- What you found
- Why it matters
- What evidence supports it

If the Operator responds, great. If not, the issue stays open on the record.

### 2. Fork and Branch

```bash
git clone https://github.com/Lackadaisical-Security/Linear-B-Decipherment
git checkout -b your-contribution-name
```

Keep branch names descriptive:

```
phase3-sign47-minoan-substrate-update
lexicon-sign49-formula-marker-correction
phase7-levantine-byblos-additional-vectors
```

### 3. Make Your Changes

Follow the existing document structure. Phase logs are formatted consistently — don't reformat them. The JSON lexicon has a defined schema — don't break it.

If you're adding content:

- Cite your source inline
- State your confidence level explicitly
- Don't assert what you haven't shown

### 4. Submit the Pull Request

Include in the PR description:

- What changed and why
- Evidence supporting the change
- Confidence estimate if applicable
- Any cross-references to existing phases or lexicon entries

PRs with no description get closed immediately.

---

## Evidence Standards

This project applies the same evidentiary standard to contributions that it applies to its own output:

| Claim Type | Required Support |
|------------|-----------------|
| Sign phonetic value | Cross-script comparison + Greek phonotactic compliance |
| Minoan substrate assignment | Linear A / Cypro-Minoan parallel + archaeological context |
| Confidence score | Methodology application + independent vector count |
| Archaeological fact | Published excavation record or tablet provenance |
| Statistical result | Calculation shown, dataset cited |

**"I think" and "it seems" are not evidence.** "The data shows X at Y vectors using Z methodology" is evidence.

---

## File Structure

```
/
├── README.md                                    ← Project overview (do not submit structural rewrites)
├── CODE_OF_CONDUCT.md                           ← This community operates by merit
├── CONTRIBUTING.md                              ← You are here
├── UDM20-LB_v1_0_Linear_B_Methodology.md       ← Core methodology document
├── LINEAR_B_PHASE_[N]_*.md                      ← Phase research logs
├── LINEAR_B_COMPREHENSIVE_FINDINGS.md          ← 22-script analysis synthesis
├── LINEAR_B_FINAL_COMPREHENSIVE_REPORT.md      ← 36-script final report
├── UDM20_LINEAR_B_INDEPENDENT_MANUAL_PASS_LS_2026-05-04.md  ← Independent audit
├── linear_b_MASTER_lexicon_unicode_plus_ls_enhanced_2026-05-03.json  ← Master lexicon
├── Complete Resolution of the Linear B Syllabogram Inventory *.md   ← Academic paper (MD)
├── Complete Resolution of the Linear B Syllabogram Inventory *.pdf  ← Academic paper (PDF)
├── ghost_license_v_1.md                        ← Ghost License v1.0
└── ancient_scripts_attribution_license_v1.md  ← ASAL-1.0
```

---

## Attribution

All accepted contributions will be acknowledged in the relevant document or phase log. There is no contributor leaderboard, no badge system, and no GitHub profile promotion. If your contribution improves the research, the research improves. That is the reward.

If you are contributing on behalf of an institution, check the [banned institutions list](./README.md#-institutionally-banned-entities) before proceeding. Contributions submitted under institutional affiliation from banned entities will be rejected and reported.

---

## Licensing

By submitting a contribution, you agree that your contribution is licensed under the same dual license as this repository:

- **Ghost License v1.0** ([ghost_license_v_1.md](./ghost_license_v_1.md))
- **Ancient Scripts Attribution License v1.0** ([ancient_scripts_attribution_license_v1.md](./ancient_scripts_attribution_license_v1.md))

Both must be followed simultaneously. No exceptions.

You also confirm that your contribution does not contain plagiarized content, does not misattribute existing research, and does not introduce institutional backdoors or ideological framing designed to compromise the integrity of the work.

---

## Contact

For significant research collaborations or methodology discussions outside the GitHub issue tracker:

- **Email:** lackadaisicalresearch@pm.me
- **XMPP+OTR:** thelackadaisicalone@xmpp.jp

Do not email asking for contribution approval before you've done the work. Do the work. Then submit it. If it's good, it gets merged.

---

**Signed,**
**Lackadaisical Security - Linguistics Division**
*Breaking the Unbreakable Since 2025*

> *"The ancient scribes didn't wait for peer review. They just wrote."*
