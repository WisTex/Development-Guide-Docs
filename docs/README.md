# Documentation Standards

This directory contains source documentation files.

Each document should be self-contained and suitable for publication on multiple websites.

## Document Format

Documents should be written in Markdown and begin with YAML front matter.

Example:

```yaml
---

title: "Document Title"
slug: "document-slug"
version: "1.0"
status: "unpublished"
category: "Category"
author: "Author Name"
license: "MIT"
copyright: "Organization Name or Author Name"
tags: ["Tag1", "Tag2"]

---
```

The metadata fields should appear in the order shown above for consistency.

## Required Metadata

| Field      | Description                                       |
| ---------- | ------------------------------------------------- |
| title      | Human-readable document title                     |
| slug       | URL-friendly identifier                           |
| version    | Current document version                          |
| status     | Publication status                                |
| category   | Primary document category                         |
| author     | Primary document author                           |
| license    | Document license                                  |
| copyright  | Copyright owner (organization or individual)      |
| tags       | Search and classification tags                    |

## Source Readability

Documentation should be formatted for readability in both rendered form and source form.

When multiple Markdown formats produce the same rendered output, prefer the format that is easier for humans to read and maintain in the raw Markdown source.

Examples include:

- Aligning table columns for readability
- Using consistent spacing
- Favoring clear formatting over compact formatting
- Organizing content to make editing and review easier

Git repositories, pull requests, and code reviews often involve reading the Markdown source directly. Source readability is therefore considered part of the documentation quality.

## Headings

Use a single H1 heading for the document title.

Use H2 headings for major sections.

Additional heading levels may be used when appropriate.

## Horizontal Rules

Use:

```html
<hr>
```

to separate major sections of a document.

Do not place horizontal rules between every heading. Horizontal rules should be reserved for major transitions within the document.


## Version History

Documents should contain a Version History section near the end of the document.

The YAML version field represents the current version.

The Version History section provides the historical record of document changes.

### Example

```markdown
## Version History

| Version | Date       | Notes                              |
| ------- | ---------- | ---------------------------------- |
| 1.1     | 2026-06-10 | Added publishing workflow section. |
| 1.0     | 2026-06-05 | Initial release.                   |
```

The newest version should appear first.

Version History entries should briefly describe significant changes to the document.

## Source of Truth

The Markdown files in this directory are the authoritative versions of all documentation.

Published HTML pages, wiki pages, CMS content, and generated formats should be considered derived works generated from these source documents.
