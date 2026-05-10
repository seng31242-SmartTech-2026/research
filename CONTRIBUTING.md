# Contributing to `research`

This guide defines the branching strategy and commit conventions for the `research` repository. All team members must follow these rules before making any contribution.

---

## Branching Strategy

| Branch Pattern | Purpose | Example |
|---|---|---|
| `main` | Latest approved, reviewed work. Merges via PR only. | `main` |
| `draft/<topic>` | Active working branch for a research area in progress. | `draft/competitive-analysis` |
| `fix/<issue-number>` | Corrective changes addressing review feedback. | `fix/17` |

**Rules:**
- Never commit directly to `main`.
- Branch off the latest `main` when starting new work.
- Delete your branch after it is merged.

```bash
git checkout main
git pull origin main
git checkout -b draft/client-interview-02
```

---

## Commit Message Convention

Follow the **Conventional Commits** specification adapted for a research repository.

```
<type>(<scope>): <short imperative summary>

[Optional body: explain WHY, not WHAT]

[Optional footer: Closes #<issue-number>]
```

### Allowed Types

| Type | When to Use |
|---|---|
| `docs` | Adding or updating a research note, interview transcript, or summary |
| `feat` | Adding a new research artefact (new interview, new survey instrument, etc.) |
| `fix` | Correcting an error or incorporating review feedback |
| `refactor` | Restructuring a document without changing its content |
| `chore` | Repository housekeeping (README, .gitignore, folder structure) |
| `style` | Formatting-only changes |

### Allowed Scopes

`interviews` · `surveys` · `competitive-analysis` · `literature` · `observation` · `workshops` · `readme`

### Good Examples ✅

```
feat(interviews): add transcript and key findings for client interview #2

Interview conducted 2026-03-10 with the owner of PeakTech Repairs.
Key pain points: manual invoicing, no job tracking, 3-day password reset.
See: client-interviews/interview-02-2026-03-10.md

Closes #12
```

```
docs(competitive-analysis): add feature comparison matrix for 3 SaaS alternatives

Covers RepairDesk, Orderry, and ServiceM8. Summary of gaps added.

Refs #8
```

### Bad Examples ❌

```
added interview / research stuff / update / new file
```

---

## Privacy Reminder Before Every Commit

Before committing any file to this repository, confirm:

- [ ] No full names or contact details of interviewees are included (unless written consent is on record)
- [ ] Survey response files are anonymised
- [ ] Observation photographs have consent documented in the protocol
- [ ] No personally identifiable information (PII) is present in any committed file

---

## Pull Request Checklist

- [ ] Content is accurate and faithfully represents what was gathered
- [ ] Anonymisation / privacy requirements are met
- [ ] File is placed in the correct folder following the structure in README.md
- [ ] Committed within 24 hours of the activity
- [ ] PR description links to the related GitHub Issue (`Closes #N`)
- [ ] At least one team member is assigned as reviewer

---

*© Software Engineering Teaching Unit, University of Kelaniya — SENG 31242, 2026*
