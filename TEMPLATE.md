# Generated Skill Template

Use this structure for each converted book:

```
skills/<slug>/
├── SKILL.md
├── manifest.json
├── glossary.md
├── patterns.md
├── cheatsheet.md
└── chapters/
    ├── ch01-<slug>.md
    ├── ch02-<slug>.md
    └── ...
```

## SKILL.md

Include YAML front matter with `name` and `description`, followed by:
- purpose;
- when to use;
- core mental models;
- concise operating rules;
- chapter index with file paths;
- guidance for selecting the right reference file.

Keep it compact. Detailed knowledge belongs in the chapter/reference files.

## Chapter files

For each chapter or major section include:
- chapter/section title;
- key ideas;
- frameworks and principles;
- procedures/techniques;
- examples expressed concisely;
- anti-patterns/caveats;
- source location when available.

## glossary.md

Alphabetical terms with concise definitions and chapter references.

## patterns.md

Organize reusable knowledge as:
- Framework
- When to use
- Inputs
- Steps
- Decision rules
- Failure modes / anti-patterns
- Related chapters

## cheatsheet.md

Favor compact tables, checklists, triggers, and if/then rules.

## manifest.json

Example:

```json
{
  "schema_version": 1,
  "slug": "example-book",
  "title": "Example Book",
  "authors": ["Author"],
  "source_files": ["example.pdf"],
  "generated_by": "chatgpt-book-to-skill",
  "mode": "chatgpt-github",
  "extraction_status": "complete",
  "limitations": []
}
```

Do not fabricate metadata that cannot be determined from the source.
