---
name: study-abroad-cv-generator
description: Generate polished, professional English CVs in DOCX format for international education consulting and overseas university applications. Use this skill whenever the user provides a student's raw background information and asks to create, organize, rewrite, polish, translate, structure, format, tailor, position, or export an application CV/resume/academic CV for master's, PhD, exchange, scholarship, or other study-abroad applications. Before final DOCX generation, analyze the target program, propose authentic applicant positioning, and tailor evidence to that direction. When CV_Shen.docx or a similar reference CV is provided, prioritize visual format consistency.
compatibility: Requires filesystem access for final DOCX output. Prefer python-docx and the bundled assets/CV_Shen.docx reference template when the user requests the Shen-style CV format.
---

# Study Abroad CV Generator

This skill helps an international education consultant turn a student's raw background information into a polished English CV for overseas university applications. It handles target-program analysis, applicant positioning, evidence selection, English rewriting, section logic, and final DOCX production.

When the user provides or references `CV_Shen.docx`, format consistency with that reference file has the highest priority. Content quality remains important, but the final Word document should visually match the clean academic style of the reference CV.

The bundled formatting reference is `assets/CV_Shen.docx`.

## Default CV Structure

Use this structure by default:

1. Personal Information
2. EDUCATION
3. PROFESSIONAL EXPERIENCE
4. ACADEMIC EXPERIENCE
5. SKILLS & AWARDS

If the student has no meaningful professional experience but has strong academic/research experience, `ACADEMIC EXPERIENCE` may appear before `PROFESSIONAL EXPERIENCE`. Otherwise, follow the `CV_Shen.docx` order.

Keep the CV suitable for overseas university applications, usually 1-2 pages unless the student has substantial research, publications, or professional experience.

## Inputs To Collect

Collect or infer the following from the user's message and files:

- Target application direction: degree level, country, intended major/program, schools if known, academic vs career-oriented application angle.
- Personal information: full name, phone, email, address if provided, LinkedIn/GitHub/portfolio/personal website if relevant.
- Education: universities, degrees, majors, study periods, expected graduation, GPA, ranking, honors, scholarships, relevant coursework.
- Professional evidence: internships, full-time work, part-time professional roles, consulting or industry projects, RA/TA roles when they function more like work experience.
- Academic evidence: research projects, academic projects, course projects, competitions, thesis/dissertation, independent research, lab experience.
- Skills and awards: technical tools, research skills, languages and test scores, certifications, scholarships, competition awards.
- Constraints: target page length, required sections, language, anonymization, items the user wants emphasized or omitted.
- Formatting reference: use `assets/CV_Shen.docx` by default when the user requests Shen-style output or provides that file.

If important information is missing, either ask a concise follow-up question before finalizing or use a clear placeholder such as `[GPA if available]`. Do not invent experiences, results, awards, dates, rankings, publications, institutions, certificates, or scores.

## Generation Workflow

1. **Analyze the target program first.** Read `references/applicant-positioning.md`. Use official program pages or user-provided program text when available. Distinguish explicit requirements, reasonable curriculum-based inferences, and general discipline advice.
2. **Create the pre-draft positioning report.** Before final DOCX generation, show: Program Analysis, Recommended Applicant Positioning, Content Selection Plan, and Missing Information. Wait for user approval unless the user explicitly requests a one-step workflow.
3. **Normalize raw information.** Convert Chinese or messy notes into a clean evidence inventory: date, organization, role, objective, methods/tools, personal contribution, outcome, relevance, and uncertainty.
4. **Select and prioritize content.** Read `references/content-selection.md` and `references/field-prioritization.md`. Match program needs to real evidence, classify materials as Priority A/B/C, and reduce low-relevance content with a brief reason.
5. **Build the section structure.** Read `references/cv-structure.md`. Place education in reverse chronological order. Put internships/work/industry evidence under `PROFESSIONAL EXPERIENCE`; put academic/research/project evidence under `ACADEMIC EXPERIENCE`; group skills and awards logically.
6. **Rewrite in professional English.** Read `references/writing-rules.md`. Translate Chinese source material into natural English CV language, using concise, achievement-oriented bullets that start with strong action verbs and support the approved positioning.
7. **Limit bullet density.** Each academic or professional experience should normally have about 4 bullet points and must not exceed 5 bullet points. Use fewer bullets for weaker or less relevant experiences.
8. **Generate Shen-style DOCX.** After positioning approval, read `references/cv-shen-template.md`, `references/docx-production.md`, and `references/template-reconstruction.md`. Use `assets/CV_Shen.docx` directly as the reference template or recreate a new DOCX that visually matches it. The final output must be `.docx`.
9. **Optimize length and page balance.** Read `references/page-balance-and-filename.md`. Prefer one page whenever reasonable. Reduce weak/duplicated/low-relevance content before changing font size. Use two pages only when essential relevant content cannot fit cleanly.
10. **Run a final quality check.** Check both positioning/content and formatting: target program analyzed, positioning supported by real evidence, no invented claims, one-page length whenever reasonable, page balance, relevance, missing information, vague bullets, natural keyword use, correct section order, centered header, thin black horizontal line under every major section heading, no visible table gridlines or vertical dividers, compact spacing, right-aligned locations/dates, italic roles/dates, reverse chronological ordering, consistent bullet indentation, no more than 5 bullets per experience, no placeholders, no unnecessary blank lines, correct `CV-[Student English Name].docx` filename, and valid DOCX output.

## Output Contract

When the user provides raw student information and requests a final CV, first produce the pre-draft report unless they explicitly request a one-step workflow:

1. Program Analysis
2. Recommended Applicant Positioning
3. Content Selection Plan
4. Missing Information

After approval, produce:

1. A final `.docx` CV following the `CV_Shen.docx` visual style whenever that template is supplied or requested.
2. Polished bullet points for academic, research, project, internship, and work experiences.
3. A short content and formatting quality check with clear, practical notes.

If the user asks for a draft before DOCX production, use this text format:

```markdown
# [STUDENT FULL NAME]
[Email] | [Phone if provided] | [LinkedIn/GitHub/Portfolio if relevant]

## EDUCATION
...

## PROFESSIONAL EXPERIENCE
...

## ACADEMIC EXPERIENCE
...

## SKILLS & AWARDS
...

## Content And Formatting Quality Check
- Relevance to target direction:
- Missing or uncertain information:
- Bullets that need stronger evidence or quantification:
- English/style issues:
- Format readiness for CV_Shen.docx:
- Length and section balance:
```

Do not include irrelevant personal details such as gender, age, date of birth, marital status, nationality, or ID number unless explicitly required by the application context.

## Reference Routing

- For exact section requirements, read `references/cv-structure.md`.
- For program analysis, applicant positioning, and pre-draft approval workflow, read `references/applicant-positioning.md`.
- For one-page preference, adaptive font sizing, page balance, and final file naming, read `references/page-balance-and-filename.md`.
- For Shen-style formatting, read `references/cv-shen-template.md`.
- For content filtering and evidence ranking, read `references/content-selection.md`.
- For target-field emphasis, read `references/field-prioritization.md`.
- For English bullet writing and Chinese-to-English rewriting, read `references/writing-rules.md`.
- For DOCX/template production, read `references/docx-production.md` and `references/template-reconstruction.md`.

## Examples

- Read `examples/example-input.md` for a representative raw student background.
- Read `examples/example-output.md` for the expected English CV draft style and quality-check format.
- Use `scripts/create_shen_style_cv.py` to convert structured CV content into a Shen-style DOCX.

## Helper Scripts

- `scripts/inspect_docx_template.py <template.docx> --out template_report.json` extracts styles, sections, paragraphs, tables, margins, and header/footer signals.
- `scripts/create_shen_style_cv.py <cv_content.json> <output.docx-or-dir> [--font-delta 0.5]` creates a Shen-style DOCX from structured CV content. If an output directory is passed, it names the file `CV-[Student English Name].docx`.
- `scripts/check_cv_docx.py <final.docx>` performs lightweight checks for empty paragraphs, repeated whitespace, missing sections, and basic document structure.
