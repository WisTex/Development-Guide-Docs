---

title: "YAML Metadata Specification"
slug: "yaml-metadata-specification"
summary: "Defines the standard YAML front matter metadata format used by WisTex documentation repositories."

version: "1.8"
status: "active"
type: "reference"

copyright: "WisTex TechSero Ltd. Co."
license: "All Rights Reserved"

classification: "internal"
distribution: "internal"

created: "2026-06-08"
updated: "2026-06-16"

authorship:
  concepts: "Scott M. Stolz"
  structure: "Scott M. Stolz"
  drafting: "AI-assisted"
  editing: "Scott M. Stolz"
  approval: "Scott M. Stolz"

use_for: [metadata, documentation, ai_context, kims_ingestion]

related:
  - "repository-structure.md"
  - "document-types.md"
  - "classification-and-distribution.md"

source: "developer-guide-docs/docs/standards/yaml-metadata-specification.md"

tags: [yaml, metadata, documentation-standards, repository-standards, kims]

disclosure_line: >-
  Drafted with AI assistance. Concepts, structure, and editing by Scott M. Stolz.

---

# YAML Metadata Specification

WisTex documentation repositories use YAML front matter at the beginning of each Markdown document that may be consumed by AI systems, documentation systems, or knowledge management systems such as WisTex KIMS.

## Normative Status

This document is normative.

When using this specification, follow the requirements exactly as stated. Do not infer, extend, simplify, replace, or omit requirements unless explicitly instructed to revise the specification.

Additional requirements or modifications should be made only through explicit revisions to this specification or explicit instructions from the document author or an authorized maintainer.

## YAML Front Matter

All documents should begin with:

```yaml
---
```

and end the metadata block with:

```yaml
---
```

Add one blank line between the closing metadata delimiter and the document title for human readability.

## Standard YAML Template

```yaml
---

# Human-readable document title
title: "Document Title"

# Stable machine-readable identifier
slug: "document-title"

# One-sentence description of the document
summary: "Brief description of the document."

# Document revision number
version: "0.1"

# draft, review, active, superseded, archived
status: "draft"

# context, strategy, decision, plan, brand, product,
# platform, implementation, reference, template, standard
type: "context"

# Rights holder
copyright: "WisTex TechSero Ltd. Co."

# Legal usage rights
license: "All Rights Reserved"

# public, internal, confidential, trade-secret
classification: "trade-secret"

# private, internal, partner, client, customer, public
distribution: "internal"

# Original creation date
created: "2026-06-08"

# Most recent significant update
updated: "2026-06-09"

authorship:
  concepts: "Scott M. Stolz"
  structure: "Scott M. Stolz"
  drafting: "AI-assisted"
  editing: "Scott M. Stolz"
  approval: "Scott M. Stolz"

# Intended usage
use_for: [ai_context, strategy, planning]

# Related documents
related:
  - "related-document.md"

depends_on:
  - "example-foundation-document.md"

supports:
  - "example-supported-document.md"

# Documents replaced by this document
replaces:
  - "older-document.md"

# Identifies the canonical maintenance location for the document.
source: "developer-guide-docs/docs/standards/yaml-metadata-specification.md"

# Search and grouping tags
tags: [tag1, tag2]

disclosure_line: >-
  Drafted with AI assistance. Concepts, structure, and editing by Scott M. Stolz.

---
```

## Field Definitions

### title

Human-readable document title.

### slug

Stable machine-readable identifier. Use lowercase words separated by hyphens.

### summary

One-sentence description of the document.

Used for:

* document indexes
* search results
* AI retrieval
* KIMS previews
* navigation systems

### version

Document revision number.

Suggested format:

```text
0.1 = early draft
1.0 = first stable version
1.1 = minor revision
2.0 = major revision
```

### status

Document lifecycle state.

Suggested values:

```text
draft
review
active
superseded
archived
```

### type

Document category.

Suggested values:

```text
context
strategy
decision
plan
brand
product
platform
implementation
reference
template
standard
```

### copyright

Rights holder.

Default:

```yaml
copyright: "WisTex TechSero Ltd. Co."
```

### license

Legal usage rights.

Default:

```yaml
license: "All Rights Reserved"
```

### classification

Sensitivity level.

Suggested values:

```text
public
internal
confidential
trade-secret
```

### distribution

Intended audience.

Suggested values:

```text
private
internal
partner
client
customer
public
```

### created

Original creation date.

Format:

```text
YYYY-MM-DD
```

### updated

Most recent significant update date.

Format:

```text
YYYY-MM-DD
```

### authorship

Contribution tracking.

Authorship values are attribution references and labels. They may represent individuals, organizations, teams, working groups, or other entities responsible for a particular contribution. Future systems may replace or supplement these labels with structured identity references.

Default:

```yaml
authorship:
  concepts: "Scott M. Stolz"
  structure: "Scott M. Stolz"
  drafting: "AI-assisted"
  editing: "Scott M. Stolz"
  approval: "Scott M. Stolz"
```

### use_for

Machine-readable list of intended uses.

Example:

```yaml
use_for: [ai_context, strategy, planning]
```

### related

Related Markdown documents.

Use `.md` extensions.

Example:

```yaml
related:
  - "wistex-ecosystem-overview.md"
  - "system-layers-authority-model.md"
```

### replaces

Documents superseded or replaced by this document. Optional.

Example:

```yaml
replaces:
  - "legacy-brand-architecture.md"
```

### tags

Search and grouping tags.

Example:

```yaml
tags: [wistex, kims, strategy]
```

### disclosure_line

Human-readable disclosure statement.

Default:

```yaml
disclosure_line: >-
  Drafted with AI assistance. Concepts, structure, and editing by Scott M. Stolz.
```

## Dependency Metadata Fields

The following fields may be used when a document has explicit architectural dependencies.

### `depends_on`

Optional.

A list of documents that this document conceptually depends upon.

Use `depends_on` when understanding the current document requires or strongly benefits from understanding another document first.

Example:

```yaml
depends_on:
  - "mission-model.md"
  - "strategy-model.md"
```

### `supports`

Optional.

A list of documents that are directly supported, enabled, clarified, or extended by this document.

Use `supports` when the current document provides conceptual foundation for another document.

Example:

```yaml
supports:
  - "mission-brief-model.md"
  - "daily-planning-architecture-model.md"
```

### Difference from `related`

The `related` field identifies documents with a general relationship.

The `depends_on` and `supports` fields identify directional architectural relationships.

Use:

```yaml
related:
```

for general association.

Use:

```yaml
depends_on:
```

for prerequisite or foundation documents.

Use:

```yaml
supports:
```

for documents that build upon the current document.

These fields should be used selectively. They are most useful for architectural hub documents and documents with clear dependency relationships.

## source

Optional.

Identifies the canonical maintenance location for the document.

Use this when a document may be mirrored, published, copied, indexed, or distributed in multiple places.

The source value should remain the same in copied or mirrored versions to identify where the document is maintained.

## Example

```yaml
---

title: "WisTex KIMS Strategy"
slug: "wistex-kims-strategy"
summary: "Defines the long-term architecture and strategic direction of WisTex KIMS."

version: "0.1"
status: "draft"
type: "strategy"

copyright: "WisTex TechSero Ltd. Co."
license: "All Rights Reserved"

classification: "trade-secret"
distribution: "internal"

created: "2026-06-08"
updated: "2026-06-09"

authorship:
  concepts: "Scott M. Stolz"
  structure: "Scott M. Stolz"
  drafting: "AI-assisted"
  editing: "Scott M. Stolz"
  approval: "Scott M. Stolz"

use_for: [ai_context, strategy, planning]

related:
  - "wistex-ecosystem-overview.md"
  - "wistex-catalyst-overview.md"
  - "system-layers-authority-model.md"

depends_on:
  - "example-foundation-document.md"

supports:
  - "example-supported-document.md"

replaces:
  - "legacy-kims-strategy.md"

source: "developer-guide-docs/docs/standards/yaml-metadata-specification.md"

tags: [wistex, kims, strategy, knowledge-management]

disclosure_line: >-
  Drafted with AI assistance. Concepts, structure, and editing by Scott M. Stolz.

---

# WisTex KIMS Strategy

Document content begins here.
```

## Design Principles

* Prefer many focused documents over large monolithic documents.
* Each document should answer one primary question whenever practical.
* Use metadata that is useful to both humans and AI systems.
* Preserve compatibility with existing WisTex documentation standards.
* Use `.md` filenames when referencing documents.
* Keep metadata concise but sufficient for future KIMS ingestion and relationship mapping.
* Omit optional metadata fields when they are not used.
* Document filenames should normally match their slug and use the .md extension.
* Related entries use Markdown filenames, not paths. Each filename should normally match the target document slug plus .md. Slugs should be unique across the repository.

## YAML Formatting Requirements

The examples in this document are normative.

Generated documents should follow the examples exactly, including:

- Two-space indentation for nested YAML structures.
- Proper indentation of list items.
- Proper indentation of folded text blocks such as `disclosure_line`.
- Blank lines between metadata sections for readability.

Improper indentation may cause YAML parsing errors in GitHub, KIMS, AI tools, and other systems.
