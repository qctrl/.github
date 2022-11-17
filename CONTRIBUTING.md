# Contributing

## Overview

This guide to contributing to [Q-CTRL](https://q-ctrl.com/) projects is intended for all contributors - from external open source developers, to outside collaborators and, of course, members of the [@qctrl](https://github.com/qctrl) team.

When contributing to Q-CTRL projects, always bear in mind that Q-CTRL values the [Three Virtues](https://thethreevirtues.com/).

As a contributor, you agree to abide by the terms of the projects specific license and our [code of conduct](https://github.com/qctrl/.github/blob/master/CODE_OF_CONDUCT.md).

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this section are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).

## Submitting an issue

To submit an issue against one of the Q-CTRL GitHub repositories:

1. In the repository navigation, click "Issues".
1. Click "New issue".
1. Choose "Bug report" to create a report to help us improve or "Feature request" to suggest an idea for the project.
1. Use the provided template to create your issue.

More information on [creating an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue).

## Submitting a pull request

To a submit a pull request to one of the Q-CTRL GitHub repositories:

1. Fork and/or clone the repository.
1. Follow the installation instructions in the README.
1. Create a new branch.
1. Make your changes.
1. Push your changes and submit a pull request.
1. Ensure a pull request title follows the [Conventional Commits](https://www.conventionalcommits.org/) standard and uses one of the [supported pull request types](#supported-pull-request-types).
1. Address any reviews.

Here are a few things you can do that will increase the likelihood of your pull request being accepted/approved:

- Follow the [coding standards](https://code.q-ctrl.com/).
- Write tests and make sure they **all** pass (for example `pytest`).
- Lint your code using the file supplied in the project (for example `pylint directoryname --rcfile=.pylintrc`).
- Keep your change as focused as possible (if there are multiple changes you would like to make that are not dependent upon each other, submit them as separate pull requests).
- Write a [good commit message](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html).

After a pull request has been approved, if you squash merge it, its commit message to the `master` branch MUST follow the [Conventional Commits](https://www.conventionalcommits.org/) standard. Since GitHub defaults a squashed commit message to a pull request title, a title MUST also follow that standard.

Note that:

- We prefer squash merges from short-lived branches (for example `feature/ABC-123`) to long-lived branches (for example `master`).
- If you're a member of the Q-CTRL team, you're responsible for merging your own pull requests once reviewed and approved.
- The following table (extracted from [commitlint](https://github.com/conventional-changelog/commitlint/blob/c936401be64dfc82b2efb69e4e17060f4c9cc3a3/%40commitlint/config-conventional/index.js#L39) ) is a guide on how to choose a proper type for your pull requests/commit messages.

### Supported pull request types

| Type       | Purpose                                                                                                    |
| ---------- | ---------------------------------------------------------------------------------------------------------- |
| `feat`     | A new feature                                                                                              |
| `fix`      | A bug fix                                                                                                  |
| `perf`     | A code change that improves performance                                                                    |
| `refactor` | A code change that neither fixes a bug nor adds a feature                                                  |
| `chore`    | Other changes that don't modify src or test files                                                          |
| `revert`   | Reverts a previous commit                                                                                  |
| `build`    | Changes that affect the build system or external dependencies (example scopes: gulp, broccoli, npm)        |
| `ci`       | Changes to our CI configuration files and scripts (example scopes: Travis, Circle, BrowserStack, SauceLabs)|
| `docs`     | Documentation only changes                                                                                 |
| `style`    | Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)     |
| `test`     | Adding missing tests or correcting existing tests                                                          |

More information [about pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).
