# Contributing to ralph-codex

Contributions improve the specification-driven execution controller while preserving its immutable product requirements, isolated Git changes, append-only learnings, and test-based acceptance.

## Before you start

Read the [README](README.md), [product requirements](prd.json), and [verification entry point](verify.py). Describe how a controller change affects allowed metadata updates, failure recovery, subprocess execution, and preservation of existing work.

Search existing issues and pull requests to avoid duplicating work. Describe substantial proposals before implementation, and use repository issue or pull request templates when available. Small corrections can go directly into a focused pull request.

For bug reports, include the affected version or commit, environment, minimal reproduction, expected and actual behavior, and sanitized diagnostics. For feature requests, explain the use case and intended outcome.

## Development and validation

The canonical verification command is:

```sh
python verify.py
```

It compiles `ralph.py` and runs the Python test suite. Record the Python environment, command result, and any unavailable dependencies. Add focused regression tests for changes to specification enforcement, selected-story updates, retry behavior, or Git recovery.

Use disposable repositories and synthetic stories for controller tests. Preserve all existing PRD fields except the narrowly permitted execution metadata, and preserve the append-only learning history. A failed verifier remains a failure; do not weaken checks to permit a commit. Ordinary repository contributions do not require launching unrestricted agent runs or changing trust settings.

Update affected documentation and examples alongside behavior changes. Add a focused regression case for a bug fix where executable tests are appropriate. Record checks that were not run and the reason.

## Submitting a pull request

Create a focused branch from the current `main` branch and open a pull request back to it. Keep unrelated formatting, refactoring, and dependency changes separate.

Include:

- The problem, proposed change, and resulting behavior.
- Related issues or existing track references.
- Exact validation commands or inspection steps, results, and limitations.
- Compatibility implications and any data or dependency provenance.

Inspect the complete diff before submission. Required automated checks must pass before merge. Follow the existing repository and account policies; this guide does not introduce a second-person approval requirement or relax existing checks.

## Security and sensitive information

Follow the [account security policy](https://github.com/edithatogo/.github/blob/main/SECURITY.md). Report vulnerabilities privately through GitHub's **Report a vulnerability** option if available. Otherwise request a private reporting contact without disclosing the vulnerability publicly. Keep credentials, personal data, and unredacted logs out of commits, issues, and examples.

## Licensing and conduct

Preserve existing attribution and applicable source or package terms. This guide does not grant a new license. Submit only material you are entitled to contribute, and document unclear permissions before adding third-party content. Follow the [account code of conduct](https://github.com/edithatogo/.github/blob/main/CODE_OF_CONDUCT.md). This guide adds no CLA, mandatory sign-off, or relicensing condition.

## Reference guidance

- [GitHub contributor guidelines](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors)
- [OpenSSF Best Practices criteria](https://www.bestpractices.dev/en/criteria)
