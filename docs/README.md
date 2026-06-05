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

## Required Metadata

## Required Metadata

| Field | Description |
|----------|----------|
| title | Human-readable document title |
| slug | URL-friendly identifier |
| version | Current document version |
| status | Publication status |
| category | Primary document category |
| author | Primary document author |
| license | Document license |
| copyright | Copyright owner (organization or individual) |
| tags | Search and classification tags |

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

## Source of Truth

The Markdown files in this directory are the authoritative versions of all documentation.

Published HTML pages, wiki pages, CMS content, and generated formats should be considered derived works generated from these source documents.
