---

title: "Documentation Standards"
slug: "documentation-standards"
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

voice_authenticity: "high"

use_for: [documentation, ai_guidance, knowledge_management]

disclosure_line: >-
  Drafted with AI assistance. Concepts, structure, and editing by Scott M. Stolz.

tags: [documentation, standards, formatting]

---

# Test

# Documentation Standards

Version 1.0 (Draft)

## Purpose

This document defines standards for organizing, formatting, publishing, and maintaining documentation.

The goal is to create documentation that is:

* easy to read
* easy to navigate
* easy to maintain
* easy to update
* useful to both humans and AI systems

These standards are platform-independent and may be applied to repositories, websites, wikis, knowledge bases, applications, and other documentation systems.

## Human Readability Comes First

Documentation exists to communicate information.

Source documents should be optimized for human readability and maintainability.

Prefer:

* clear formatting
* predictable structure
* consistent organization
* readable source files

Avoid:

* compressed formatting
* unnecessary complexity
* structures that are difficult to edit manually

Documentation is often maintained for years. Future maintainers should be able to understand and modify it efficiently.

## Skimmability Matters

Most readers scan before they read.

Documentation should allow readers to:

* determine relevance quickly
* locate specific information
* understand document structure
* return later and find information efficiently

Support skimmability through:

* descriptive headings
* logical organization
* concise introductions
* short paragraphs
* lists where appropriate
* tables when beneficial
* clear section boundaries

Readers should be able to understand the structure of a document before reading every word.

## Headings

Headings are navigation tools.

Headings should describe content rather than create curiosity.

Prefer:

> Identity Cloning and Redundancy

Over:

> A Powerful Feature You May Not Know About

A reader should be able to skim headings and understand the overall structure of the document.

## Logical Organization

Group related information together.

Arrange sections in a logical sequence.

A common pattern is:

1. Overview
2. Definitions
3. Core Concepts
4. Details
5. Examples
6. Related Information

Exact structures may vary, but information should flow naturally.

## One Topic Per Section

Each section should have a clear purpose.

Avoid combining unrelated topics within the same section.

If the discussion shifts significantly, create a new section.

Smaller focused sections are generally easier to maintain and navigate than larger mixed sections.

## Lists

Use lists when they improve readability.

Lists are particularly useful for:

* requirements
* options
* features
* procedures
* summaries
* comparisons

Use numbered lists when sequence matters.

Use bullet lists when sequence does not matter.

Do not convert ordinary prose into lists unnecessarily.

## Tables

Use tables when information is being compared or referenced.

Examples include:

* feature comparisons
* configuration references
* compatibility information
* definitions
* status information

Avoid tables when prose communicates the information more clearly.

## Examples

Place examples near the concepts they illustrate.

Examples should:

* reinforce understanding
* demonstrate usage
* reduce ambiguity
* clarify abstract concepts

Readers should not need to search elsewhere for clarification.

## Paragraph Length

Prefer shorter paragraphs.

Large blocks of text are more difficult to read and scan.

Whenever practical:

* one idea per paragraph
* concise explanations
* clear transitions

Paragraph structure should support understanding rather than satisfy arbitrary formatting rules.

## Consistency Matters

Use consistent formatting throughout a document.

Consistency should apply to:

* headings
* terminology
* capitalization
* lists
* tables
* examples
* metadata

Readers should not need to learn new formatting conventions while reading the same document.

## Source Documents vs Published Documents

Documentation often exists in multiple forms.

Examples include:

* Markdown source files
* HTML articles
* wiki pages
* CMS content
* PDFs
* generated documentation

The source document is the authoritative version.

Published versions should preserve:

* meaning
* structure
* terminology
* organization

Formatting may differ.

Content should not.

## Metadata

Metadata is optional.

Use metadata only when it provides meaningful value.

Common uses include:

* content management
* static site generation
* knowledge management
* publishing workflows
* AI-assisted systems

Not all documentation requires metadata.

When metadata is used:

* use a consistent schema
* use consistent field names
* use consistent formatting
* avoid unnecessary variation

## YAML Front Matter

YAML front matter is a source-document convention.

It is commonly used in:

* Markdown repositories
* documentation systems
* publishing workflows
* static site generators

Do not assume all documentation requires YAML front matter.

When YAML front matter is used:

* maintain a consistent schema
* maintain consistent field names
* prioritize readability
* prioritize compatibility

### Arrays

Use flow-style arrays.

Preferred:

```yaml
tags: [documentation, standards, formatting]
```

Preferred:

```yaml
use_for: [documentation, ai_guidance]
```

Avoid block-style arrays.

```yaml
tags:
  - documentation
  - standards
  - formatting
```

While block-style arrays are valid YAML, some tooling and publishing workflows may not process them consistently.

For compatibility and consistency, use flow-style arrays throughout documentation metadata.

## HTML Publishing Standards

Published HTML documents should remain structurally similar to their source documents.

Preserve:

* heading hierarchy
* organization
* terminology
* overall document flow

HTML should enhance readability, not change the meaning of the content.

### Bootstrap Usage

Bootstrap may be used to improve presentation and readability.

Appropriate uses include:

* alerts
* responsive tables
* typography improvements
* spacing utilities
* responsive images

Examples:

* Warnings may use warning alerts.
* Important notes may use informational alerts.
* Tables may use Bootstrap table classes.
* Images may use responsive image classes.

### Use Styling Sparingly

Styling should support content, not compete with it.

Avoid:

* excessive colors
* decorative effects
* excessive nesting
* unnecessary visual complexity

Readers should focus on the information being presented.

The content is more important than the styling.

## AI-Friendly Documentation

Documentation may be consumed by both humans and AI systems.

Well-structured documentation benefits both.

Practices that improve AI interpretation often improve human readability:

* clear headings
* consistent terminology
* logical organization
* descriptive section names
* structured metadata

Documentation should not be written exclusively for AI systems, but it should not unnecessarily hinder them.

## Preferred Outcome

A successful document allows readers to:

* find information quickly
* understand information accurately
* return to information later
* maintain the document efficiently

Good documentation reduces effort for both readers and maintainers.
