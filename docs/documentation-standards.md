---

title: "Documentation Standards"
slug: "documentation-standards"
version: "1.0"
status: "published"
category: "Standards"
author: "Scott M. Stolz"
license: "MIT"
copyright: "WisTex TechSero Ltd. Co."
tags: ["Documentation", "Standards", "Writing", "Publishing"]

---

# Documentation Standards

This directory contains source documentation files.

Each document should be understandable on its own and suitable for publication on one or more websites.

## Writing for Humans

Documentation should be easy to read both on published websites and in the Markdown files stored in this repository.

When multiple formatting options produce the same result, prefer the one that is easier for humans to read and maintain.

Examples include:

* Aligning tables for readability
* Using consistent spacing
* Favoring clarity over compact formatting
* Organizing content so it is easy to review and update

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

| Field     | Description                                  |
| --------- | -------------------------------------------- |
| title     | Human-readable document title                |
| slug      | URL-friendly identifier                      |
| version   | Current document version                     |
| status    | Publication status                           |
| category  | Primary document category                    |
| author    | Primary document author                      |
| license   | Document license                             |
| copyright | Copyright owner (organization or individual) |
| tags      | Search and classification tags               |

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

## Cross References

Documents should be understandable on their own, but may reference related documents when appropriate.

Cross references can help connect related concepts and reduce unnecessary duplication.

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

## Version Numbering

Documents use a three-level version numbering system.

### When to Change the Version Number

Version numbers are intended to represent published or distributed revisions of a document.

Routine editing, drafting, research, and work-in-progress changes do not normally require a version change.

The version number should be updated when a new revision of the document is considered complete and ready for publication, distribution, or general use.

A version number does not need to be changed for every edit, save, or Git commit.

### First Number

Examples:

* 1.0
* 2.0
* 3.0

Increase the first number when a document undergoes significant changes, such as:

* Major rewrites
* Significant restructuring
* Large additions of content
* Major corrections that substantially change the meaning of the document

### Second Number

Examples:

* 1.0 → 1.1
* 1.1 → 1.2

Increase the second number for smaller content updates, such as:

* Clarifications
* Additional examples
* Small additions of information
* Minor corrections that do not substantially change the document

### Third Number

Examples:

* 1.1 → 1.1.1
* 1.1.1 → 1.1.2

Increase the third number for cosmetic updates, such as:

* Typographical corrections
* Grammar fixes
* Formatting improvements
* Minor wording changes that do not affect meaning

Changes that only affect the third number do not normally need to be recorded in the Version History table.

However, the version number should still be updated in the document metadata and elsewhere within the document when applicable.

## Source of Truth

The Markdown files in this directory are the authoritative versions of all documentation.

Published HTML pages, wiki pages, CMS content, and other generated formats should be considered published versions generated from these source documents.
