TASK 1 : Orientation and Configuration Management

Project: Polar Vault Verification and Validation Study (PSVS)

1.1 Project Overview

The Polar Seed Vault stores sealed boxes of crop seeds deposited by registered institutions, including gene banks, universities, and governments. Each box contains seed samples of one species. Depositors retain ownership of their boxes, while the vault acts as a custodian.

The purpose of this project is to inspect the system requirements, identify defects, maintain configuration control, and document verification activities using Git and GitHub.

1.2 Repository Structure

The repository contains the following folders and files:

│
├── README.md
├── TASK-1.md
├── TASK-2.md
├── requirements/
├── defect-logs/
├── abstractions/
├── models/
├── operations/
├── constraints/
├── proofs/
└── reports/

The folders are organized as follows:

requirements/ — Requirements baseline and change requests.

defect-logs/ — Defect identification and peer-review records.

abstractions/ — Abstract representation of system requirements.

models/ — Relationships between requirements.

operations/ — Verification procedures.

constraints/ — System constraints and limits.

proofs/ — Verification arguments.

reports/ — Taxonomy, summary, and chart information.

Note: Git does not track empty folders. Add a .gitkeep file to any folder that does not contain another file.

1.3 Original Requirements Baseline

Artifact ID: PSVS-REQ-v1.0
Version: 1.0
Status: Baseline
Git Tag: baseline-1

ID

Original Requirement

S1

The system shall accept seed boxes only from registered depositors.

S2

Each chamber can hold a large number of boxes.

S3

Chambers 1-3 hold at most 50,000 boxes each; Chamber 4 holds at most 20,000.

S4

A box belongs to exactly one depositor, and only that depositor may withdraw it.

S5

In an emergency, the vault authority may release any box to any requesting party.

S6

Boxes shall be stored at a safe temperature.

S7

Chamber temperature shall never rise above -18°C.

S8

During maintenance, a chamber may be warmed to 0°C.

S9

Seed samples with low viability shall be flagged promptly for regeneration.

S10

A depositor may withdraw at most 20% of its boxes of a species per year.

S11

A withdrawn box may be redeposited only after re-inspection.

S12

The system shall keep a good audit trail of all actions.

The original requirements must remain unchanged in the baseline. Any correction must be documented through a change request.

1.4 README.md Contents

The root README.md describes the project, its objectives, repository structure, verification approach, and expected deliverables.

Project Objectives

Identify defects in informal requirements.

Classify defects using a defined taxonomy.

Record evidence, severity, and suggested fixes.

Identify conflicts between requirements.

Maintain requirements using version control.

Perform peer review and calculate the detection rate.

1.5 Configuration Management Using Git

Step 1: Create the GitHub Repository

Create a repository named:

VV-Lab-<RollNo>-PSVS

Replace <RollNo> with your actual roll number.

Step 2: Clone the Repository

git clone https://github.com/YOUR-USERNAME/VV-Lab-<RollNo>-PSVS.git
cd VV-Lab-<RollNo>-PSVS

Step 3: Add the Requirements Baseline

Create requirements/PSVS-REQ-v1.0.md and enter the original requirements from Section 1.3.

Commit the baseline:

git add README.md TASK-1.md requirements/
git commit -m "PSVS-REQ-v1.0: establish requirements baseline"
git tag -a baseline-1 -m "Original requirements baseline"

Step 4: Create a Defect-Analysis Branch

git switch -c defect-analysis

Step 5: Make Three Commits

After creating and filling the relevant files, use three separate commits.

Commit 1 — Defect Analysis

git add TASK-2.md defect-logs/
git commit -m "Add defect analysis and verification logging"

Commit 2 — Taxonomy and Reports

git add reports/
git commit -m "Add defect taxonomy and summary reports"

Commit 3 — Supporting Artifacts

git add abstractions/ models/ operations/ constraints/ proofs/ requirements/
git commit -m "Add verification artifacts and change management"

These commits require actual file changes. If the files have not been created yet, finish them before running the commands.

Step 6: Merge into Main

git switch main
git merge --no-ff defect-analysis -m "Merge defect analysis into main"

If your default branch is named master, use master instead of main.

Step 7: Display the Git History

git log --oneline --graph --decorate --all

Take a screenshot of the terminal showing the baseline commit, three defect-analysis commits, branch merge, and baseline-1 tag.

1.6 Change-Request Template

A change request is used to propose, assess, approve, and document a modification to an existing requirement or project artifact.

Change Request Form

Field

Description

Change Request ID

Unique identifier, e.g. CR-001

Artifact

Requirement or document being changed

Reason

Explanation of the defect or need for change

Proposed Change

Exact correction or addition

Impact

Effects on functionality, safety, testing, and documentation

Approver

Authorized person who approves or rejects the change

Status

Proposed, Approved, Rejected, or Implemented

Commit ID

Git commit associated with the implemented change

