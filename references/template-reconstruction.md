# Template Reconstruction Guide

Use this guide whenever the user supplies a CV template in DOCX, PDF, screenshot, image, or plain text. For this skill's default formatting workflow, `assets/CV_Shen.docx` is the primary reference template.

## Priority Order

1. DOCX template with editable structure.
2. PDF template with selectable text.
3. Screenshot or scanned image.
4. Text-only sample layout.

When multiple versions are provided, use the user's stated preferred version. If no preference is stated, use the most editable file as the source of truth and cross-check visual appearance against screenshots/PDFs.

## What To Extract

Capture these details before drafting into the template:

- Page size, margins, columns, header/footer, page count expectation.
- Fonts, font sizes, bold/italic/small caps, line spacing, paragraph spacing.
- Section names and order.
- Date placement and format, such as `Sep 2024 - Present`, `2024.09-present`, or right-aligned dates.
- Whether entries use tables, tab stops, two-column layouts, hanging indents, or bullet lists.
- Bullet symbols, indentation, punctuation style, and whether bullets end with periods.
- Treatment of GPA/ranking/coursework.
- Whether the template is academic, business, minimalist, dense, or design-heavy.

## DOCX Template Handling

For a DOCX template, preserve its native structure whenever possible:

- Copy the template to a new output file rather than rebuilding from a blank document.
- Reuse existing styles instead of creating new ones.
- Replace placeholder text if placeholders exist.
- If the template contains example entries but no placeholders, use the existing paragraphs/tables as structural patterns.
- Keep table widths, cell margins, borders, and paragraph styles stable.

If the source template is an example CV with someone else's content, remove their personal content and keep only the format. Do not accidentally retain names, schools, phone numbers, emails, awards, or experience details from the sample.

For `CV_Shen.docx`, pay special attention to:

- Centered name and email header.
- Section order: EDUCATION, PROFESSIONAL EXPERIENCE, ACADEMIC EXPERIENCE, SKILLS & AWARDS.
- Times New Roman styling, compact spacing, and black-and-white academic layout.
- Education block using a compact two-column structure.
- Experience entries using organization/project and location on the first line, role and date on the second line, followed by compact bullets.

## PDF Or Image Template Handling

For non-editable templates, recreate the layout in DOCX:

- Start from page setup: size, margins, and approximate columns.
- Rebuild headers, section dividers, tables, and bullet indentation.
- Match the visual hierarchy rather than tracing every pixel.
- If the layout is complex, create a first-page reconstruction and compare visually before filling all content.

## Template Fidelity Checks

Before final delivery, compare the output against the template:

- Same section order unless user-approved changes were needed.
- Similar density and whitespace.
- Matching heading weight, casing, and separators.
- Dates and organization names aligned like the template.
- No unexpected page spillover.
- No leftover placeholder or sample-person content.
