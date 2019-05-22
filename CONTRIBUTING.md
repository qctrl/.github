# Contributing

Contributions to this project are released to the public under the project's open source license.

This project is released with a [Code of Conduct](CODE_OF_CONDUCT.md). By contributing to this project you agree to abide by its terms.

## Table of Contents

- [Submitting an Issue](#submitting-an-issue)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Coding Standards](#coding-standards)
- [Resources](#resources)

## Submitting an Issue

Please submit all issues to our [JIRA instance](https://q-ctrl.atlassian.net/secure/CreateIssue.jspa)

## Submitting a Pull Request

1. Clone the repository and create a new branch
1. Configure and install any dependencies
1. Make sure the tests pass on your machine
1. Make your change, add tests, and make sure the tests still pass
1. Push to your branch and submit a pull request
1. Add reviewers
1. Pat yourself on the back and wait for your pull request to be reviewed and merged

Here are a few things you can do that will increase the likelihood of your pull request being accepted:

- Follow our [Coding Standards](#coding-standards)
- Spell variable names out in full using Australian English spelling (e.g. `optimized_pulse`, **NOT** `op`)
- For variable names that are more than three words, use an acronym (e.g. `cpmg`, **NOT** `carr_purcell_meiboom_gill`)
- Write tests and make sure they **all** pass (e.g. `pytest`)
- Lint your code using the file supplied in the project (e.g. `pytlint directoryname --rcfile=.pylintrc`)
- Keep your change as focused as possible - if there are multiple changes you would like to make that are not dependent upon each other - submit them as separate pull requests
- Write a [good commit message](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)

### More Information

- [About pull requests](https://help.github.com/en/articles/about-pull-requests)
- [Understanding the GitHub flow](https://guides.github.com/introduction/flow/)

## Coding Standards

| Language   | Style                                              | Docstrings                                                        | Testing                       | Linting                           |
|------------|----------------------------------------------------|-------------------------------------------------------------------|-------------------------------|-----------------------------------|
| JavaScript | [Prettier](https://prettier.io/)                   | [JSDoc](http://usejsdoc.org/)                                     | [Jest](https://jestjs.io/)    | [ESLint](https://eslint.org/)     |
| Python     | [PEP 8](https://www.python.org/dev/peps/pep-0008/) | [numpydoc](https://numpydoc.readthedocs.io/en/latest/format.html) | [pytest](https://pytest.org/) | [Pylint](https://www.pylint.org/) |

## Resources

- [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [Support](SUPPORT.md)
