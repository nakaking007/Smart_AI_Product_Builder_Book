# AGENTS.md

## Project identity

This repository is a professional technical book project, not a software application. Markdown manuscript quality, factual accuracy, reader clarity, and reproducibility are the primary goals.

## Current phase rule

Do not write chapter content until the user explicitly authorizes chapter drafting. Empty files in `chapters/` are intentional placeholders.

## Working rules

1. Read `PROJECT_STATE.md`, `BOOK_SPEC.md`, `CONTENT_PLAN.md`, and `STYLE_GUIDE.md` before substantial editorial work.
2. Work only within the requested scope and preserve unrelated user edits.
3. Prefer targeted file searches and small, reviewable changes.
4. Use current authoritative sources for claims about changing products, interfaces, pricing, policy, or platform behavior.
5. Record research and citations under `references/`.
6. Test code, prompts, and procedures before claiming that they work.
7. Never store credentials, tokens, private information, or copyrighted source material without permission.
8. Keep generated publication artifacts in `output/`; do not treat them as manuscript sources.
9. Update `PROJECT_STATE.md` after completing a meaningful project milestone.
10. Report completed work, verification performed, and genuine blockers accurately.

## File placement

- Chapter prose: `chapters/`
- Reusable prompts: `prompts/`
- Runnable examples: `code/`
- Worksheets and reusable frameworks: `templates/`
- Research notes and citations: `references/`
- Visual assets: matching subfolder under `assets/`
- Build and validation tooling: `scripts/`
- Generated deliverables: `output/`

## Editorial quality gate

Before marking chapter work complete, confirm that it:

- Matches the approved scope and reader level.
- Follows `STYLE_GUIDE.md`.
- Uses consistent terms and product names.
- Separates verified facts from assumptions.
- Includes clear success checks for procedures.
- Has no secrets, private data, broken references, or unsupported claims.
- Has been reviewed for accessibility, safety, and version sensitivity.

## Change discipline

Do not rename the chapter files or alter the planned chapter order without explicit authorization. Do not publish, deploy, merge, force-push, delete data, or change access permissions unless the user clearly requests it and all required safeguards are satisfied.
