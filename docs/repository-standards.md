---

title: "Repository Standards"
slug: "repository-standards"
version: "2.0"
status: "draft"
author: "Scott M. Stolz"
license: "MIT"
copyright: "WisTex TechSero Ltd. Co."

authorship:
  concepts: "Scott M. Stolz"
  structure: "Scott M. Stolz"
  drafting: "AI-assisted"
  editing: "Scott M. Stolz"
  approval: "Scott M. Stolz"

voice_authenticity: "medium"

use_for: [documentation, repository_management, ai_guidance]

disclosure_line: >-
  Drafted with AI assistance. Concepts, structure, and editing by Scott M. Stolz.

tags: [repository, standards, development-guide-docs]

---

# Repository Standards

Version 1.0 (Draft)

## Purpose

This document defines repository-specific standards for the Development Guide Docs repository.

These standards govern:

* document organization
* metadata requirements
* file structure
* formatting conventions
* publication workflows
* repository maintenance

This document supplements, but does not replace:

* Scott's Writing Style Guide
* Scott's Documentation Standards
* Scott's Metadata Standards, when available

Repository-specific requirements take precedence within this repository.

## Source Documents

Markdown files stored in this repository are considered source documents.

Published HTML pages, wiki pages, CMS content, PDFs, and other generated formats should be considered derived works generated from these source documents.

Whenever practical:

* edit source documents
* generate published formats from source documents
* avoid maintaining multiple independent versions of the same content

The source document is the authoritative version.

## Metadata Requirements

All source documents should include metadata.

Metadata supports:

* discovery
* organization
* automation
* publishing workflows
* AI-assisted systems

In this repository, metadata is stored using YAML front matter.

YAML is an implementation detail of this repository.

The metadata model is more important than the storage format.

Future systems may store the same metadata using databases, APIs, JSON documents, or other formats.

## Document Template

This repository includes a canonical document template.

Location:

```text
templates/document-template.md
```

When creating new documents, use the document template as the starting point.

The template defines:

* metadata structure
* field order
* indentation requirements
* array formatting
* disclosure formatting
* authorship formatting

The template is the authoritative source for document metadata formatting.

When the template and this document appear to conflict, the template takes precedence.

## Metadata Example

The following example demonstrates the standard metadata structure used within this repository.

```yaml
---
title: "Document Title"
slug: "document-title"
version: "1.0"
status: "draft"
author: "Scott M. Stolz"
license: "MIT"
copyright: "WisTex TechSero Ltd. Co."

authorship:
  concepts: "Scott M. Stolz"
  structure: "Scott M. Stolz"
  drafting: "AI-assisted"
  editing: "Scott M. Stolz"
  approval: "Scott M. Stolz"

voice_authenticity: "medium"

use_for: [documentation, ai_guidance, knowledge_management, voice_modeling]

disclosure_line: >-
  Drafted with AI assistance. Concepts, structure, and editing by Scott M. Stolz.

tags: [documentation]
---
```

The document template contains the authoritative metadata structure.

When creating new documents, start with the template and modify only the values that are specific to the new document.

## voice_authenticity

The `voice_authenticity` field indicates how closely the final document reflects Scott M. Stolz's natural writing voice.

This field is intended to help both humans and AI systems understand the relationship between the published document and Scott's personal communication style.

Common values include:

| Value     | Meaning                                                                                                                     |
| --------- | --------------------------------------------------------------------------------------------------------------------------- |
| low       | Primarily informational or technical. Little effort was made to match Scott's writing voice.                                |
| medium    | Reflects some characteristics of Scott's writing style, but prioritizes clarity, structure, or neutrality.                  |
| high      | Strongly reflects Scott's preferred writing style, tone, and communication patterns.                                        |
| very_high | Intended to closely match Scott's personal voice and writing style. Typically requires significant human editing or review. |

This field describes voice alignment, not factual accuracy, authorship, or quality.

## YAML Formatting Rules

### Indentation

Nested fields must be indented using two spaces.

Example:

```yaml
authorship:
  concepts: "Scott M. Stolz"
  structure: "Scott M. Stolz"
  drafting: "AI-assisted"
  editing: "Scott M. Stolz"
  approval: "Scott M. Stolz"
```

Continuation lines following `>-` must also be indented using two spaces.

Example:

```yaml
disclosure_line: >-
  Drafted with AI assistance. Concepts, structure, and editing by Scott M. Stolz.
```

Improper indentation may cause parsing failures.

### Arrays

Use flow-style arrays.

Example:

```yaml
use_for: [documentation, ai_guidance, knowledge_management, voice_modeling]
```

Example:

```yaml
tags: [documentation, standards]
```

Do not use block-style arrays.

```yaml
tags:
  - documentation
  - standards
```

Although block-style arrays are valid YAML, this repository standardizes on flow-style arrays for consistency and compatibility.

### Field Order

Maintain the field order defined by the document template.

Consistency improves:

* readability
* maintenance
* automation
* AI processing

Avoid unnecessary variation.

## Repository Organization

Repository content should be organized according to purpose.

Examples include:

* articles
* style guides
* reference materials
* repository documentation
* templates

Documents should be placed in the most appropriate location based on their purpose.

## Style Guides

Documents within the `style-guides` directory define preferred standards and methodologies.

Examples include:

* writing standards
* documentation standards
* metadata standards
* voice guides

These documents define guidance rather than repository structure.

## Repository Documentation

Documents within the `docs` directory describe repository-specific requirements and workflows.

Examples include:

* repository standards
* publishing workflows
* repository structure
* contributor information

These documents explain how the repository operates.

## Source Readability

Source documents should remain easy for humans to read and maintain.

Prefer:

* readable Markdown
* consistent spacing
* descriptive headings
* logical organization

The source document is part of the documentation experience.

## AI Usage

AI-assisted drafting is permitted and encouraged.

However:

* human review remains important
* factual accuracy should be verified
* repository standards should be followed
* style guides should be respected

AI should assist authors rather than replace editorial judgment.

## Preferred Outcome

This repository should serve as a high-quality source of documentation that is:

* easy to maintain
* easy to publish
* easy to discover
* easy for humans to understand
* easy for AI systems to process

The repository should function as a long-term knowledge asset rather than a collection of unrelated documents.
