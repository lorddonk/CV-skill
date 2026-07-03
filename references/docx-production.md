# DOCX Production And QA Guide

Use this guide when creating the final Word document. When `CV_Shen.docx` is provided or requested, final format consistency with `CV_Shen.docx` has the highest priority.

## Preferred Production Path For Shen-Style CVs

1. Finalize or stabilize the English CV content.
2. Read `references/cv-shen-template.md`.
3. Use `assets/CV_Shen.docx` as the primary visual reference.
4. Prefer one of these approaches:
   - **Option A:** Use `CV_Shen.docx` directly as a template and replace its original content while preserving paragraph styles, font, font size, margins, alignment, bullets, and spacing.
   - **Option B:** Recreate a new DOCX that visually matches `CV_Shen.docx`, using `python-docx` or another reliable DOCX-generation method.
5. If structured CV content is available, use `scripts/create_shen_style_cv.py <cv_content.json> <output.docx-or-dir>`. When passing a directory, the script saves as `CV-[Student English Name].docx`.
6. Render or visually inspect the final DOCX before delivery whenever tools allow.

## Required Visual Style

Replicate the reference CV style:

- Clean, simple academic CV.
- One-column layout.
- Compact spacing suitable for a 1-2 page CV.
- Professional black-and-white formatting.
- Times New Roman or the same font used in the reference file.
- Consistent font sizes across headings, titles, dates, and bullet points.
- Narrow/compact margins similar to the reference file.
- No decorative colors, icons, photos, charts, or unnecessary design elements.
- Every major section heading has a thin solid black horizontal line underneath it.
- Only section headings should have visible horizontal rules.

## Required Section Order

Use this order by default:

1. EDUCATION
2. PROFESSIONAL EXPERIENCE
3. ACADEMIC EXPERIENCE
4. SKILLS & AWARDS

If the student has no professional experience but has strong academic/research experience, `ACADEMIC EXPERIENCE` may appear before `PROFESSIONAL EXPERIENCE`, while preserving the same heading and entry format.

## Stable DOCX Constructs

Use stable DOCX constructs:

- Center-aligned paragraphs for name and contact header.
- Right-aligned tab stops for education school/location and degree/date.
- Right-aligned tab stops for organization/location and role/date lines.
- Named styles copied from the template when using the original file.
- Explicit paragraph spacing and line spacing.
- List bullet paragraphs with consistent hanging indentation.
- Paragraph bottom borders for section heading horizontal lines.

Avoid fragile hacks:

- Do not flatten the CV into an image.
- Do not use decorative text boxes or icons.
- Do not silently change the template's margins, font family, or section order.
- Avoid repeated spaces for alignment when right-aligned tabs are possible.
- Avoid tables for normal alignment. If a table is unavoidable, remove all table and cell borders so no gridlines or vertical divider lines appear.

## One-Page And File Naming

Read `references/page-balance-and-filename.md` before final export. Prefer one page whenever reasonably possible. Reduce content before reducing font size. If the page is underfilled, use consistent font enlargement of about 0.5 pt, up to 1 pt total. If it slightly exceeds one page, shorten content and spacing before any minor font reduction.

The required filename is:

- `CV-[Student English Name].docx`
- For multiple program-specific versions: `CV-[Student English Name]-[University or Program].docx`

## Final QA Checklist

Check these before final response:

- The file is a valid `.docx`.
- The document visually follows `CV_Shen.docx`.
- Name and contact information are centered.
- The section order is correct.
- Section headings are uppercase, bold, simple, and consistent.
- Every major section heading has a thin black horizontal line underneath.
- There are no unwanted table borders, visible gridlines, or vertical divider lines.
- Education entries include school, degree, location, date, and GPA/coursework/honors when relevant.
- Experience entries include organization/project name, location, role, date, and bullet points.
- Each experience has no more than 5 bullet points.
- Bullet points are written in strong professional English.
- Dates are formatted consistently.
- Bullet indentation is consistent.
- Paragraph spacing is compact, with no large gaps between heading, title lines, role lines, and bullets.
- Entries in Education, Professional Experience, and Academic Experience are sorted reverse chronologically.
- There are no unreplaced placeholders.
- There are no unnecessary blank lines.
- The CV is suitable for 1-2 pages unless the student has extensive experience.
- The CV is one page whenever reasonably possible, or a second page is clearly justified and balanced.
- Low-relevance content was reduced before font-size reduction.
- The final filename follows `CV-[Student English Name].docx`.
- No template sample person's private information remains.

## User-Facing Summary

Keep the final message short:

- Link the DOCX.
- State that it follows the `CV_Shen.docx` reference style.
- Mention any assumptions, uncertain facts, or content that was omitted because of space or relevance.
