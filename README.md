# Development Guide Documentation

This repository contains source documentation for Hubzilla, Neuhub, OpenWebAuth, WisTex projects, and related technologies.

The repository serves as the canonical source for documentation that may be published on one or more websites, including development.guide, neuhub.org, federatedhub.org, and future platforms.

## Why This Repository Exists

Technical knowledge is often discovered while working on a project, solving a problem, or researching a topic. If that information is not captured while it is fresh, it can be forgotten, lost in chat logs, buried in forum discussions, or require rediscovery later.

This repository provides a central place to capture and maintain that knowledge as it is discovered.

The documents in this repository are maintained independently of any specific publishing platform. Documentation can be written, updated, and reviewed without first deciding where it will eventually be published.

## Source of Truth

The Markdown documents stored in this repository are the authoritative versions of the documentation.

Published HTML pages, wiki pages, CMS content, and other generated formats should be considered published versions generated from these source documents.

## Reuse and Redistribution

The repository uses the MIT License to encourage sharing, reuse, adaptation, and redistribution.

Documentation may be incorporated into websites, knowledge bases, project documentation, educational materials, and other resources, subject to the terms of the applicable license.

## Repository Structure

```text
docs/
    Documentation source files

style-guides/
    Site-specific styling and conversion guidance

publishing-targets/
    Site-specific publishing instructions
```

## Publishing Workflow

The general workflow used by this repository is:

1. Create or update a Markdown document.
2. Commit changes to Git.
3. Convert the document to the desired output format if needed.
4. Publish to one or more destinations.
5. Continue maintaining the source document in this repository.

This workflow separates documentation from publication and allows documents to be maintained in a single location.

## Publishing

Documents may be published to one or more destinations while continuing to be maintained in a single location.

This approach allows documentation to be written and updated once, then reused wherever it is useful.

Potential publishing targets include:

* development.guide
* neuhub.org
* federatedhub.org
* project websites
* knowledge bases
* future publishing systems

## Licensing

Unless otherwise specified, documentation in this repository is licensed under the MIT License.

Individual documents may contain metadata describing authorship, copyright ownership, licensing information, version numbers, and related details.

## Contributing

Contributions, corrections, and improvements are welcome.

Please submit changes through pull requests when possible.
