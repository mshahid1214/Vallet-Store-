
# Task 1: Orientation and Configuration Management


## 2. README.md

### Project Overview
This project verifies and analyzes the requirements of a Polar Seed Vault system. The vault stores seed boxes owned by registered institutions. The project identifies requirement defects, analyzes conflicts, and documents verification activities using Git and GitHub.

### Objectives
- Identify defects in requirements.
- Classify defects using a taxonomy.
- Record evidence and suggested fixes.
- Maintain version control.
- Perform peer review.
- Prepare defect summaries and charts.

### Repository Contents
- `requirements/`: Requirements baseline and change requests.
- `defect-logs/`: Defect log and peer-review records.
- `abstractions/`: Requirement abstractions.
- `models/`: Requirement relationships.
- `operations/`: Verification procedures.
- `constraints/`: System constraints.
- `proofs/`: Verification arguments.
- `reports/`: Taxonomy, summaries, and charts.

## 3. Requirements Baseline: PSVS-REQ-v1.0

| ID | Requirement |
|---|---|
| S1 | The system shall accept seed boxes only from registered depositors. |
| S2 | Each chamber can hold a large number of boxes. |
| S3 | Chambers 1-3 hold at most 50,000 boxes each; Chamber 4 holds at most 20,000. |
| S4 | A box belongs to exactly one depositor, and only that depositor may withdraw it. |
| S5 | In an emergency, the vault authority may release any box to any requesting party. |
| S6 | Boxes shall be stored at a safe temperature. |
| S7 | Chamber temperature shall never rise above -18°C. |
| S8 | During maintenance, a chamber may be warmed to 0°C. |
| S9 | Seed samples with low viability shall be flagged promptly for regeneration. |
| S10 | A depositor may withdraw at most 20% of its boxes of a species per year. |
| S11 | A withdrawn box may be redeposited only after re-inspection. |
| S12 | The system shall keep a good audit trail of all actions. |

## 4. Git Configuration Management

Create the repository on GitHub and clone it:

```bash
git clone https://github.com/Vallet Store.git
cd Vallet Store.git
```

Create the required folders:

```bash
mkdir requirements defect-logs abstractions models operations constraints proofs reports
```

Commit the baseline:

```bash
git add README.md TASK-1.md requirements/
git commit -m "PSVS-REQ-v1.0: establish requirements baseline"
git tag -a baseline-1 -m "Original requirements baseline"
```

Create the defect-analysis branch:

```bash
git switch -c defect-analysis
```

Make three commits:

```bash
git add TASK-2.md defect-logs/
git commit -m "Add defect analysis and verification logging"

git add reports/
git commit -m "Add defect taxonomy and summary reports"

git add abstractions/ models/ operations/ constraints/ proofs/ requirements/
git commit -m "Add verification artifacts and change management"
```

Merge the branch:

```bash
git switch main
git merge --no-ff defect-analysis -m "Merge defect analysis into main"
```

Display the Git history:

```bash
git log --oneline --graph --decorate --all
```

Take a screenshot of the Git history for submission.

## 5. Change Request Template

| Field | Description |
|---|---|
| Change Request ID | CR-001 |
| Artifact | S7 and S8 |
| Reason | Temperature requirements conflict during maintenance. |
| Impact | Temperature monitoring, maintenance procedures, and testing. |
| Approver | Course Instructor / Authorized Reviewer |

**Proposed Change:** Define an explicit maintenance exception, authorization conditions, duration, and safety controls.

**Status:** Proposed
