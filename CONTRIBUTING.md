# Contributing to QBCore UEFN

Thank you for helping improve QBCore UEFN. These guidelines apply across the
organization unless a repository documents a more specific requirement.

## Choose the right channel

- Use a bug form for a reproducible defect in an official QBCore UEFN project.
- Use a feature form to propose new behavior or a meaningful improvement.
- Use a documentation form for missing, incorrect, or unclear documentation.
- Use the [QBCore UEFN projects](https://github.com/qbcore-uefn) and
  [official Discord](https://discord.gg/qbcore) for installation,
  configuration, and usage support.
- Follow the [QBCore UEFN Code of Conduct](CODE_OF_CONDUCT.md) whenever you
  participate in project or community spaces.
- Follow the [security policy](SECURITY.md) to report vulnerabilities privately.
  Never disclose vulnerability details in a public issue, pull request, or
  Discord channel.

Search open and closed issues and pull requests before starting work. For a
large feature, breaking change, or architectural change, open a proposal and
wait for maintainer direction before investing significant effort.

## Development workflow

1. Fork the affected repository and branch from its current default branch.
2. Keep each branch and pull request focused on one logical change.
3. Follow the surrounding code style and repository-specific instructions.
4. Avoid unrelated formatting, generated-file churn, dependency updates, or
   refactoring.
5. Update documentation, configuration examples, persistence or project
   migrations, and translations affected by the change.
6. Test the change and open a draft pull request early when maintainer feedback
   would reduce rework.

## Testing expectations

There is no single test command shared across QBCore UEFN repositories. At
minimum:

- Run every check or lint workflow provided by the repository.
- Test with current UEFN and Fortnite ecosystem versions and compatible official
  dependencies.
- Record the exact project or module commit and the UEFN and Fortnite versions.
- Verify UEFN, Verse, and play-session logs for new warnings or errors.
- Test edit-session startup, project reload behavior, and the smallest reliable
  reproduction for the changed behavior.
- Test fresh installation and upgrade paths when changing project settings or
  persistence.
- Test relevant resolutions and interaction states for user-interface changes,
  and include screenshots or video.

Never include production credentials, webhook URLs, license keys, database
contents, player identifiers, or other private information in tests, issues,
commits, or pull requests.

## Pull requests

Use a Conventional Commit-style pull request title. Maintainers may use the
title as the final squash commit:

```text
fix(inventory): prevent duplicate item transfer
feat(core): add configurable player metadata
docs: clarify project startup order
feat(core)!: replace the legacy callback signature
```

Use `fix` for bug fixes, `feat` for new functionality, and an exclamation mark
or `BREAKING CHANGE:` description for incompatible changes. Other useful types
include `docs`, `refactor`, `perf`, `test`, `build`, `ci`, and `chore`.

Complete the pull request template, link the relevant issue, explain migration
requirements, and provide enough testing evidence for a maintainer to reproduce
your result. Passing automation is necessary but does not replace relevant
manual UEFN edit-session and uploaded-island testing.

## Code, assets, and generated material

Only submit code, media, translations, and other assets that you have the right
to contribute under the repository's license. Do not copy leaked, escrowed,
decompiled, purchased, or incompatibly licensed material.

AI-assisted contributions are held to the same standards as any other work.
Contributors must understand, review, test, and accept responsibility for every
submitted change, including its security and licensing.

## Review and acceptance

Maintainers may request changes, additional testing, a smaller scope, or a
different design. A contribution may be declined when it conflicts with the
project direction, duplicates existing behavior, adds disproportionate
maintenance cost, lacks adequate testing, or cannot be distributed under the
repository's license.

Be patient and professional during review. Opening a pull request does not
guarantee that the change will be merged.
