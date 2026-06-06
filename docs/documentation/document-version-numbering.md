---

title: "Document Version Numbering"
slug: "document-version-numbering"
version: "1.0.1"
status: "unpublished"
category: "Documentation"
author: "Scott M. Stolz"
license: "MIT"
copyright: "WisTex TechSero Ltd. Co."

authorship:
  concepts: "Scott M. Stolz"
  structure: "Scott M. Stolz"
  drafting: "AI-assisted"
  editing: "Scott M. Stolz"
  approval: "Scott M. Stolz"

voice_authenticity: "medium-high"

use_for: [voice_modeling, portfolio, ai_guidance, documentation]

disclosure_line: >-
  Drafted with AI assistance. Concepts, structure, and editing by Scott M. Stolz.

tags: ["Documentation", "Versioning", "Standards", "Writing"]

---

# Document Version Numbering

Version: 1.0

## Purpose

Version numbers help readers understand how a document has changed over time.

They provide a simple way to distinguish between major revisions, content updates, and cosmetic corrections. They also help maintainers track the evolution of a document as information is added, clarified, corrected, or reorganized.

This document describes the version numbering system used by documents published by WisTex, Federated Works, and related projects.

## When to Change the Version Number

Version numbers are intended to represent published or distributed revisions of a document.

Routine editing, drafting, research, and work-in-progress changes do not normally require a version change.

The version number should be updated when a new revision of the document is considered complete and ready for publication, distribution, or general use.

A version number does not need to be changed for every edit, save, or Git commit.

<hr>

## Version Structure

Documents use a three-level version numbering system:

```text
1.0
1.1
1.1.1
```

Each number represents a different level of change.

### First Number

Examples:

```text
1.0 → 2.0
2.0 → 3.0
```

Increase the first number when a document undergoes significant changes, such as:

* Major rewrites
* Significant restructuring
* Large additions of content
* Major corrections that substantially change the meaning of the document

### Second Number

Examples:

```text
1.0 → 1.1
1.1 → 1.2
```

Increase the second number for smaller content updates, such as:

* Clarifications
* Additional examples
* Small additions of information
* Minor corrections that do not substantially change the document

### Third Number

Examples:

```text
1.1 → 1.1.1
1.1.1 → 1.1.2
```

Increase the third number for cosmetic updates, such as:

* Typographical corrections
* Grammar fixes
* Formatting improvements
* Minor wording changes that do not affect meaning

<hr>

## Version History

Documents may contain a Version History section that records significant changes over time.

Example:

```markdown
## Version History

| Version | Date       | Notes                              |
| ------- | ---------- | ---------------------------------- |
| 1.1     | 2026-06-10 | Added publishing workflow section. |
| 1.0     | 2026-06-05 | Initial release.                   |
```

The newest version should appear first.

Version History entries should briefly describe significant changes to the document.

Changes that only affect the third number do not normally need to be recorded in the Version History table.

Examples include:

* Typographical corrections
* Grammar fixes
* Formatting adjustments
* Minor wording improvements

However, the version number should still be updated in the document metadata and elsewhere within the document when applicable.

<hr>

## Benefits

Using version numbers provides several benefits:

* Makes document changes easier to understand
* Helps readers identify significant updates
* Creates a simple maintenance history
* Encourages consistent documentation practices
* Makes it easier to track revisions across multiple publications

## Scope

This document describes a version numbering convention used by WisTex, Federated Works, and related projects.

Individual projects may choose to use different versioning systems when appropriate.

<hr>

## Version History

| Version | Date       | Notes            |
| ------- | ---------- | ---------------- |
| 1.0     | 2026-06-05 | Initial release. |
