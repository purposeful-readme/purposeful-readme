<!--
resource: readme
spec: purposeful-readme/0.1.0
version: 0.1.0
type: documentation
language: markdown
status: experimental
visibility: public
docs: null
-->

# Purposeful Readme

***A principled, purposeful standard for READMEs.***

***

A specification and style guide for README.md files that defines an ordered, structured format enabling fast human comprehension and reliable machine parsing.

[![License](https://img.shields.io/github/license/purposeful-readme/purposeful-readme)](LICENSE)
![Version](https://img.shields.io/github/v/release/purposeful-readme/purposeful-readme)
![Status](https://img.shields.io/badge/status-experimental-orange)

## Table of Contents

- [Overview](#overview)
- [Design Principles](#design-principles)
- [Usage](#usage)
- [Security](#security)
- [Roadmap](#roadmap)
- [FAQ](#faq)
- [Contributing](#contributing)
- [Acknowledgements](#acknowledgements)
- [License](#license)

## Overview

Purposeful Readme defines a structure, vocabulary, and set of governing principles for `README.md` files across repository-centred projects, addressing the widespread inconsistency, stale content, and uneconomical verbosity that characterise top-level project documentation. It treats the README as the primary entry point into a project's documentation ecosystem — helping readers understand *what a project is*, *how to begin*, and *where to go next*, without forcing every detail into one file. By defining stable section names, a mandatory ordering, and an embedded machine-readable metadata block, it enables reliable automation and AI-native tooling integration while guarding against the drift and overreach that make READMEs go stale.

The specification governs section architecture and writing discipline; it does not prescribe visual styling, Markdown formatting conventions, or toolchain-specific workflows beyond those boundaries.

This repository is the canonical home of the specification.

## Design Principles

- **Readers come first**; structure, language, and length exist to serve comprehension, not to demonstrate completeness.
- **The README is an entry point and a map, not a destination**; it orients and links outward rather than absorbing content that belongs in companion documents.
- **Section ordering is functional** and follows the natural progression of questions a first-time reader brings to an unfamiliar project.
- **Human readability and machine parseability are complementary, equally important goals** that must improve together.
- **Conditional minimalism**: every section must earn its place, remain maintainable, and be warranted by the project's actual nature and needs.
- **Opinionated structure and non-restrictive scope coexist**; the specification mandates form while remaining agnostic about technology, domain, and project size.
- **The specification evolves incrementally** through community-driven, RFC-style change proposals under semantic versioning.

## Usage

### Adopting

Read the current specification at [`spec/spec_v0_1_0.md`](spec/spec_v0_1_0.md).

To write a conformant `README.md` for your own project:

1. Open your `README.md` file, or create one at the repository root.
2. Begin the file with the [Machine Metadata Block](spec/spec_v0_1_0.md#22-machine-metadata-block), populated with your project's values.
3. Follow it immediately with the [Header Block](spec/spec_v0_1_0.md#23-header-block).
4. Add [sections](spec/spec_v0_1_0.md#26-section-scaffolding-reference) in the prescribed order, including only those whose conditions are met.
5. Vet the file to determine if it needs a [Table of Contents](spec/spec_v0_1_0.md#24-table-of-contents), and if so create one in the proper place.

> [!IMPORTANT]
> Begin with a concise `README.md`, keeping only the sections whose conditions apply to your project. Add companion files such as `INSTALL.md`, `CONFIG.md`, and `USAGE.md` only when the corresponding topics grow too substantial to keep concise within the README itself.

### Validating

To validate that a README conforms to the specification, see the [validation](spec/spec_v0_1_0.md#51-validation-and-ci) chapter within the specification itself.

### Citing

If you reference Purposeful Readme in a project or publication, a [`CITATION.cff`](CITATION.cff) file is provided at the repository root for machine-readable citation.

## Security

Purposeful Readme is primarily a documentation and standards project; its repository (this repository) contains specification text, governance documents, and an embedded validation script. Security-relevant concerns are therefore limited to the repository, website, automation, and related project infrastructure.

Vulnerability reports should follow the coordinated disclosure process described in [`SECURITY.md`](SECURITY.md).

## Roadmap

- [ ] Publish the initial `0.1.0` draft specification ***[IN PROGRESS]***
- [ ] Publish the project website
- [ ] Extract and publish the validator as a standalone reference implementation
- [ ] Add adoption examples and starter templates
- [ ] Define the RFC-style change proposal and governance process for post-`1.0.0` revisions

See the [issue tracker](https://github.com/purposeful-readme/purposeful-readme/issues) for the full backlog and any ongoing discussions.

## FAQ

**Q: Why are section names and ordering defined so strictly?**  
A: Predictable, stable headings make READMEs easier to scan for human readers and easier to parse reliably for automated tools, validators, and agentic systems — without requiring heuristics or guesswork.

**Q: Can I add custom sections to a conformant README?**  
A: No. Purposeful Readme restricts top-level structure to the prescribed sections to ensure predictable navigation. Content that does not fit an existing section likely belongs in a companion document — or may represent a gap worth raising as a contribution.

**Q: Does adopting this standard mean I have to delete my detailed tutorials?**  
A: No, it simply means moving them — gradually if need be. Lengthy tutorials, API references, and architecture essays belong in dedicated companion files (e.g., `INSTALL.md`, `USAGE.md`, `ARCHITECTURE.md`), which your README will then link to.

**Q: Is this standard compatible with standard Markdown linters?**  
A: Yes. Purposeful Readme only imposes rules on structural ordering and section naming, not stylistic Markdown choices, ensuring compatibility with most formatting tools.

## Contributing

All contributions are welcome (*post-`v1.0.0` release*). Contributions should be focused, well-explained, and aligned with the goal of developing a clear, useful, and stable README standard. For substantial changes, open an issue first so scope and direction can be discussed before work begins.

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for the full contribution guidelines.

## Acknowledgements

Purposeful Readme was shaped by earlier work on documentation structure, conventions, and metadata discipline, including:

- [Standard Readme](https://github.com/RichardLitt/standard-readme)
- [Keep a Changelog](https://keepachangelog.com/)
- [Common Changelog](https://common-changelog.org)
- [jlevy/frontmatter-format](https://github.com/jlevy/frontmatter-format)

## License

[CC-BY-4.0](LICENSE) © 2026 Purposeful Readme.
