---
name: chatgpt-book-to-skill
description: "Convert books and documents supplied to ChatGPT into reusable Agent Skills stored in GitHub. Produces a compact SKILL.md plus chapters, glossary, patterns, and cheatsheet. Designed for ChatGPT + GitHub and compatible with Agent Skills hosts such as Codex and GitHub Copilot CLI."
---

# ChatGPT Book-to-Skill

Turn a user-provided book or document into a reusable knowledge skill and publish the generated text files to a GitHub repository the user has authorized.

## When to use

Use this workflow when the user asks to turn a PDF, EPUB, DOCX, Markdown, text document, or collection of documents into a reusable skill or knowledge base.

## Core rule

Extract structure, not merely a summary. Preserve named frameworks, definitions, decision rules, procedures, techniques, caveats, examples, and anti-patterns. Do not invent material absent from the source.

## ChatGPT/GitHub mode

This mode does not require ChatGPT to access the user's local ~/.agents/skills directory.

Flow:

1. Receive the source document in the ChatGPT conversation or Library.
2. Read the document with available file/document tools.
3. Identify title, author, table of contents, sections, frameworks, terminology, techniques, examples, warnings, and decision rules.
4. Create a stable lowercase-hyphenated skill slug.
5. Generate the files defined in TEMPLATE.md.
6. Store them under skills/<slug>/ in the configured GitHub repository.
7. Verify every generated file can be read back from GitHub.
8. Report the repository path and any extraction limitations.
9. Never claim the skill is locally installed merely because it exists in GitHub.

## Output contract

Every generated skill should contain:

- SKILL.md — compact operating instructions and index.
- chapters/ — source-grounded chapter or major-section knowledge.
- glossary.md — important terms and definitions.
- patterns.md — reusable frameworks, methods, techniques, and anti-patterns.
- cheatsheet.md — concise decision rules and quick reference.
- manifest.json — provenance and generation metadata.

Large books should use multiple chapter files so an agent can retrieve only the relevant material.

## Source fidelity

Separate source-derived claims from added organizational wording. Keep chapter references or page references when available. If extraction is incomplete, scanned, ambiguous, or missing pages, record that limitation in manifest.json and do not silently fill gaps.

## Updating an existing skill

If skills/<slug>/ already exists, inspect the existing manifest and skill before changing it. Merge new source material deliberately. Preserve useful existing content unless the new source supersedes it. Never overwrite an existing skill blindly.

## GitHub publishing

Default repository for this installation: alabieri/chatgpt-book-skills.

Generated skills live at:

skills/<slug>/

GitHub is the persistence and interchange layer. ChatGPT can retrieve these files through the connected GitHub integration when authorized. Compatible local agents can clone or otherwise install the repository/skill separately.

## Safety and copyright

Transform user-provided or otherwise authorized source material into structured notes and operating knowledge. Avoid reproducing large portions verbatim. Prefer concise paraphrase, short necessary quotations, and source references.
