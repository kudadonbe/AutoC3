# Repository Guidelines

## Project Structure & Module Organization

This is a coursework archive for ME03ARM Certificate III in Automotive Repair & Maintenance, not an application codebase.

- `course-documents/`: institution-wide documents, grouped as `calendars/`, `forms/`, and `policies/`.
- `modules/`: module-specific course material.
  - Use module folders such as `AEP01-automotive-engine-practice/`.
  - Store slides, PDFs, and unit material in `learning-materials/`.
  - Store module forms in `forms/`.
  - Store exam notes in `final-exam-prep/` where relevant.
- `final-exam-prep/`: combined AEP01, BWP01, and VMR01 final exam revision files.
- `templates/`: reusable coursework templates.
- `MATERIALS_INDEX.md`: update this when adding or reorganizing material.

## Build, Test, and Development Commands

There is no build system or test runner. Useful verification commands:

```powershell
git status --short
git diff --stat
Get-ChildItem -Recurse -File modules
```

Use these to confirm added files, changed docs, and module placement before committing.

## Style & Naming Conventions

Use clear, descriptive filenames with title case for course assets:

- `Chapter 01 - Understand Automotive Engine Components and Workshop Safety.pptx`
- `Basic Workshop Practice.pptx`
- `FINAL_EXAM_THREE_MODULE_STUDY_GUIDE.md`

Prefer consistent folder names across modules: `learning-materials/`, `forms/`, `revision-materials/`, and `final-exam-prep/`. Keep Markdown concise, with standard headings and bullet lists. Do not rename source PDFs/PPTX/DOCX files unless the new name improves clarity and preserves meaning.

## Testing Guidelines

No automated tests are required. Validate changes manually:

- Confirm every added file is in the correct module or course-document folder.
- Check `README.md` and `MATERIALS_INDEX.md` reflect new structure.
- For exam-prep Markdown, verify module coverage and spelling of module codes.

## Commit & Pull Request Guidelines

Use short sentence-style commit messages matching the repo history, for example:

- `Initial coursework repository setup`
- `Organize course materials and add final exam prep`

Before committing, run `git status --short` and review staged paths with `git diff --cached --stat`. Pull requests should describe what course material changed, list affected modules, and mention any renamed or reorganized files.

## Agent-Specific Instructions

Treat this repository as Hussain Shareef's personal Maldives Polytechnic coursework archive. Preserve educational material, avoid deleting source documents, and keep organization module-code based. When adding final exam prep, prioritize AEP01, BWP01, and VMR01 unless instructed otherwise.
