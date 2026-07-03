# CV-skill

A Codex skill for generating polished English study-abroad CVs with applicant positioning, Shen-style DOCX formatting, one-page preference, and quality checks.

## Contents

- `SKILL.md` - skill entrypoint
- `references/` - workflow, positioning, content, formatting, and page-balance rules
- `scripts/` - DOCX generation and QA helpers
- `assets/CV_Shen.docx` - reference CV template
- `study-abroad-cv-generator.skill` - packaged skill artifact

## Quick smoke test

```powershell
python scripts/create_shen_style_cv.py examples/example-content.json outputs
python scripts/check_cv_docx.py "outputs/CV-Chen Yiran.docx"
```
