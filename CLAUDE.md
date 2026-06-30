# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is **not an application codebase**. It is Hussain Shareef's personal coursework archive for **ME03ARM – Certificate III in Automotive Repair & Maintenance** at Maldives Polytechnic. There is no build system, test runner, or executable. The "source" is Markdown/HTML study material plus binary course assets (PPTX, PDF, DOCX, JPG).

Preserve educational material. Do not delete or rename source PDFs/PPTX/DOCX unless explicitly asked; renaming is only acceptable when it improves clarity and preserves meaning.

## Verification (instead of build/lint/test)

```powershell
git status --short                         # confirm which files changed
git diff --cached --stat                   # review staged paths before committing
Get-ChildItem -Recurse -File modules       # confirm module placement of added files
```

There is nothing to compile or run. "Correct" means: files are in the right module folder, and `README.md` + `MATERIALS_INDEX.md` reflect the current structure.

## Module structure

Five modules, each addressed by its **module code** prefix. Always place material under the correct code; folder names are reused consistently across modules:

| Code | Module | Common subfolders |
|---|---|---|
| BBS01 | Basic Business Skills | `learning-materials/` |
| WHS01 | Workplace Health and Safety | `learning-materials/`, `revision-materials/`, `regulations-and-standards/` |
| BWP01 | Basic Workshop Practice | `learning-materials/` |
| AEP01 | Automotive Engine Practice | `learning-materials/`, `assignment-1-qg15de-engine/` |
| VMR01 | Vehicle Maintenance and Repair | `learning-materials/`, `forms/` |

- `course-documents/` — institution-wide docs: `calendars/`, `forms/`, `policies/`.
- `final-exam-prep/` (repo root) — the **single home for all final exam revision**, covering the three examined modules: AEP01, BWP01, VMR01. Do not create parallel per-module `final-exam-prep/` folders; add VMR01/AEP01/BWP01 exam material here. When working on exam prep, prioritize these three modules unless told otherwise.
- Manufacturer manuals/reference PDFs go in the relevant assignment's `references/` folder, not in `learning-materials/` (which is for lecturer slides).
- Keep practical evidence (photos, measurements) inside the relevant assignment folder; do **not** mix it with general course documents.

## Two content conventions to follow

**1. Source-verified exam answers.** `final-exam-prep/Final Exam Source Verified Questions And Answers.md` is derived **only** from the lecturer PowerPoints in each module's `learning-materials/` folder — assignment reports, service manuals, and outside general knowledge are deliberately excluded. Each section cites its source `.pptx`. When editing this file, preserve that constraint: cite the slide source and don't introduce facts that aren't in the lecturer slides. Content is ordered by teaching order (BWP01 → AEP01 → VMR01).

**2. Multi-format assignment deliverables.** The QG15DE engine assignment (`modules/AEP01-automotive-engine-practice/assignment-1-qg15de-engine/`) exists as three parallel artifacts that must stay in sync: `QG15DE Engine Assignment Report.md`, `.html`, and the exported `.pdf`. If you change report content, update the markdown and HTML together (matching cover, headings, and figures) and regenerate the PDF. Photos and measurement scans are numbered (`00`, `01`, …) so they appear in disassembly order.

## When adding or reorganizing material

Update `MATERIALS_INDEX.md` (and `README.md` if the structure changes) in the same change — these are the human index of what exists and where. Use clear, descriptive title-case filenames that include the module/assignment context.

## Commit style

Short, sentence-style messages matching history (e.g. `Add source-verified final exam guide`, `Align QG15DE markdown cover with HTML report`). PRs should say what course material changed, which modules are affected, and note any renamed/reorganized files.
