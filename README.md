# chatgpt-book-skills

A GitHub-backed library of reusable skills generated from books and documents with ChatGPT.

## ChatGPT/GitHub mode

This repository contains a ChatGPT-oriented adaptation of the workflow inspired by [virgiliojr94/book-to-skill](https://github.com/virgiliojr94/book-to-skill).

Instead of requiring ChatGPT to write to a local `~/.agents/skills/` directory, GitHub acts as the persistent skill store:

```
Book/document -> ChatGPT -> structured extraction -> skills/<book-slug>/ -> GitHub
```

Generated skills use a compact `SKILL.md`, chapter files, glossary, patterns, cheatsheet, and provenance manifest. See [SKILL.md](SKILL.md) and [TEMPLATE.md](TEMPLATE.md).

## Important distinction

Publishing a skill here makes it persistent and retrievable through an authorized GitHub connection. It does not by itself install that skill into ChatGPT's internal runtime or onto a local computer.

## Credits

The design is based on concepts from the MIT-licensed [book-to-skill](https://github.com/virgiliojr94/book-to-skill) project by Virgilio Jr. This repository's ChatGPT/GitHub mode is an adaptation, not the upstream project.
