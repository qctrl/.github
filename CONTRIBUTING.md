# Contributing

This guide to contributing to [Q-CTRL](https://q-ctrl.com/) projects is intended for all contributors - from external open source developers, outside collaborators, and even members of the [@qctrl](https://github.com/qctrl) team.

As a contributor, you agree to abide by the terms of the projects specific license and our [code of conduct](CODE_OF_CONDUCT.md).

## Table of contents

- [Submitting an issue](#submitting-an-issue)
- [Submitting a pull request](#submitting-a-pull-request)
- [Documentation standards](#documentation-standards)
- [Licensing standards](#licensing-standards)
- [Coding standards](#coding-standards)
- [Resources](#resources)

## Submitting an issue

1. In the repository navigation, click "Issues"
1. Click "New issue"
1. Choose "Bug report" to create a report to help us improve or "Feature request" to suggest an idea for the project
1. Use the provided template to create your issue

### More information on submitting an issue

- [Creating an issue](https://help.github.com/en/articles/creating-an-issue)

## Submitting a pull request

1. Fork and clone the repository
1. Configure and install any dependencies
1. Make sure the tests pass on your machine
1. Create a new branch
1. Make your change, add tests, and make sure the tests still pass
1. Push to your fork and submit a pull request
1. Pat yourself on the back and wait for your pull request to be reviewed and merged

Here are a few things you can do that will increase the likelihood of your pull request being accepted:

- Follow the [coding standards](#coding-standards)
- Write tests and make sure they **all** pass (e.g. `pytest`)
- Lint your code using the file supplied in the project (e.g. `pylint directoryname --rcfile=.pylintrc`)
- Keep your change as focused as possible (if there are multiple changes you would like to make that are not dependent upon each other, submit them as separate pull requests)
- Write a [good commit message](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)

Note:

- We prefer squash merges from short-lived branches (e.g. `feature/ABC-123`) to long-lived branches (e.g. `master`)
- If a project has both `development` and `master` branches, we prefer the default merge commit option for merges between them
- When squashing commits, lines that add little meaning to the overall commit message (e.g. "Oops missed another instance") should be removed

### More information on pull requests

- [About pull requests](https://help.github.com/en/articles/about-pull-requests)
- [Understanding the GitHub flow](https://guides.github.com/introduction/flow/)

## Documentation standards

Q-CTRL projects have two types of documentation:

1. [Contributor documentation](#contributor-documentation)
1. [User documentation](#user-documentation)

### Contributor documentation

Contributor documentation is found in the README file and contains only the necessary information for a developer to get started contributing to the project. Q-CTRL follows the standard specified in the [Formatting your README](https://guides.github.com/features/wikis/#Formatting-a-readme) GitHub guide. The README file in the [Q-CTRL template repository](https://github.com/qctrl/template) contains the prescribed structure and instructions on how to apply this standard.

### User documentation

User documentation is found on the [Q-CTRL Documentation](https://docs.q-ctrl.com/) website. Any means by which a user accesses the platform is supported by user documentation with the aim of making it easy and intuitive to use the software.

### More information on documentation standards

- [Formatting your README](https://guides.github.com/features/wikis/#Formatting-a-readme)
- [Q-CTRL template repository](https://github.com/qctrl/template)

## Licensing standards

Q-CTRL projects have one of three types of licensing applied:

1. Commercial
1. Open source
1. Unlicensed

| Type        | Description                                                                                        | License                                                                                                                               |
|-------------|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Commercial  | The software is developed and distributed by Q-CTRL and is commercial in nature                    | Q-CTRL Terms of service [HTML](https://q-ctrl.com/terms) [Text](https://q-ctrl.com/terms.txt)                                         |
| Open source | The software is developed and distributed by Q-CTRL, is open source, and contributions are welcome | Apache License, Version 2.0 [HTML](http://www.apache.org/licenses/LICENSE-2.0) [Text](http://www.apache.org/licenses/LICENSE-2.0.txt) |
| Unlicensed  | The software is developed by Q-CTRL and is not distributed                                         | N/A                                                                                                                                   |

## Coding standards

In general, coding standards should be obtained from the following hierarchy:
1. Framework
1. Language
1. Q-CTRL

When looking for a standard to follow for a design/syntax decision, start at the
top and work down: if the relevant framework specifies a standard, use that;
otherwise, if the language specifies a standard (see below), use that;
otherwise, fall back to the Q-CTRL standard (see below).

### Language standards

| Language   | Style                                              | Docstrings                                                        | Testing                                                    | Linting                                                       |
| ---------- | -------------------------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------- |
| HTML       | [Prettier](https://prettier.io/)                   | N/A                                                               | [HTMLProofer](https://github.com/gjtorikian/html-proofer/) | N/A                                                           |
| JavaScript | [Prettier](https://prettier.io/)                   | [JSDoc](http://usejsdoc.org/)                                     | [Jest](https://jestjs.io/)                                 | [ESLint](https://eslint.org/)                                 |
| Markdown   | [Prettier](https://prettier.io/)                   | N/A                                                               | N/A                                                        | [Markdownlint](https://github.com/markdownlint/markdownlint/) |
| Python     | [PEP 8](https://www.python.org/dev/peps/pep-0008/) | [numpydoc](https://numpydoc.readthedocs.io/en/latest/format.html) | [pytest](https://pytest.org/)                              | [Pylint](https://www.pylint.org/)                             |

### Q-CTRL standards

#### Variable naming
- Spell variable names out in full using American English spelling (e.g. `optimized_pulse`, **NOT** `op`).
- For variable names that are more than three words, use an acronym (e.g. `cpmg`, **NOT** `carr_purcell_meiboom_gill`).

## Resources

- [How to contribute to open source](https://opensource.guide/how-to-contribute/)
- [Code of conduct](CODE_OF_CONDUCT.md)
- [Support](SUPPORT.md)
