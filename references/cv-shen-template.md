# CV_Shen.docx Formatting Reference

Use this reference whenever the user asks for the output to follow `CV_Shen.docx`. Content quality matters, but format consistency with `CV_Shen.docx` has the highest priority for the final DOCX.

The bundled template file is:

`assets/CV_Shen.docx`

## Observed Template Style

The reference CV uses a clean academic one-column style:

- Black-and-white only.
- No icons, photos, charts, colors, or decorative elements.
- Times New Roman throughout.
- Compact spacing appropriate for a 1-2 page CV.
- Page size in the inspected file: 8.5 in x 13.19 in.
- Margins: top 1.0 in, bottom 1.0 in, left 0.75 in, right 0.75 in.
- Header distance and footer distance: 0.5 in.
- Student name: centered, bold, approximately 12 pt.
- Contact line: centered, approximately 10 pt.
- Section headings: uppercase, bold, approximately 11 pt, left-aligned, with a thin solid black horizontal line directly underneath each heading.
- Main body: approximately 10 pt.
- Experience titles/organization names: bold, approximately 10 pt.
- Role lines: bold italic, approximately 10 pt.
- Bullet points: compact hanging indent, approximately 10 pt.
- Spacing: single line spacing, 0 pt paragraph spacing for normal lines, and only small spacing before each new section.

## Required Section Order

Use this order by default:

1. EDUCATION
2. PROFESSIONAL EXPERIENCE
3. ACADEMIC EXPERIENCE
4. SKILLS & AWARDS

If the student has no meaningful professional experience but strong research or projects, `ACADEMIC EXPERIENCE` may come before `PROFESSIONAL EXPERIENCE`; keep the same formatting style.

## Header Format

The header should be:

```text
STUDENT NAME
email@example.com | Optional phone | Optional LinkedIn/GitHub/Portfolio
```

Rules:

- Center both lines.
- Use uppercase for the name when it looks natural.
- Keep contact information concise.
- Do not include gender, age, date of birth, marital status, ID number, photo, or unrelated private details.

## Education Format

The reference uses a compact right-aligned education block:

```text
University Name                                      Location
Degree Name                                         Date / Expected Graduation
- GPA: x / x
- Relevant Coursework: Course 1, Course 2, Course 3, Course 4
- Honors: ...
```

Implementation preference:

- Prefer right-aligned tab stops for university/location and degree/date.
- Avoid visible tables. If a table is unavoidable, all table and cell borders must be invisible, with no vertical dividers or gray gridlines.
- University name is bold.
- Degree line is regular unless the reference or user asks otherwise.
- Location and date appear on the right.
- Date should be italic.
- GPA and coursework use compact bullets.
- Relevant Coursework label should be bold if possible.

## Experience Format

Use this structure for both professional and academic entries:

```text
Company / Organization / Project Title              Location
Position / Role                                     Date Range
- Bullet point
- Bullet point
- Bullet point
- Bullet point
```

Formatting:

- First line: organization/project title bold; location right-aligned.
- Second line: position/role italic; date range italic and right-aligned.
- Bullets: compact, hanging indent, consistent with the template.
- Each experience normally has around 4 bullet points and must not exceed 5.
- Sort multiple entries in reverse chronological order using the end date or most recent date.

## Skills & Awards Format

Use compact bullets:

```text
- Technical Skills: Python, SQL, MATLAB, SPSS, Excel
- Data Analysis & Research: Statistical Modeling, Regression Analysis, Survey Design
- Software & Tools: MS Office Suite, Tableau, Power BI
- Language Skills: IELTS 7.5, TOEFL 105
- Certifications: CFA Level I
- Awards: National Scholarship, Dean's List
```

Keep the section concise and relevant to the target application direction.

## Length And Page Balance

Read `page-balance-and-filename.md` before final export. The Shen-style CV should normally be one page for students and recent graduates. Optimize content first, then spacing, and only then minor font-size changes. If underfilled, enlarge all font sizes consistently by 0.5-1 pt while preserving hierarchy.

## Production Requirement

When producing the final CV:

- Use `assets/CV_Shen.docx` directly as a template and replace content while preserving styles, or recreate a new DOCX that visually matches it.
- Prefer `scripts/create_shen_style_cv.py` when structured CV content is available.
- The final output must be a valid `.docx` file.
- Every major section heading must have a thin solid black bottom border.
- Only section headings should show horizontal lines; body alignment tables, if any, must not show gridlines.

## Final Formatting QA

Before delivery, check:

- Header name and contact information are centered.
- Section order matches the required order.
- Headings are uppercase, bold, left-aligned, and have a thin black horizontal line underneath.
- There are no unwanted table borders, gray gridlines, or vertical divider lines.
- Line spacing is compact and visually close to the reference.
- Education entries include school, degree, location, date, GPA/coursework/honors when relevant.
- Experience entries include organization/project, location, role, date, and bullets.
- No experience has more than 5 bullets.
- Bullet indentation is consistent.
- Dates are formatted consistently.
- Multiple entries are sorted from most recent to oldest.
- There are no unreplaced placeholders.
- There are no unnecessary blank lines.
- The CV is suitable for 1-2 pages unless the student has extensive experience.
