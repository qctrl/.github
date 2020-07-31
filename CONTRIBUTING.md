# Contributing

This guide to contributing to [Q-CTRL](https://q-ctrl.com/) projects is intended for all contributors - from external open source developers, to outside collaborators and, of course, members of the [@qctrl](https://github.com/qctrl) team.

As a contributor, you agree to abide by the terms of the projects specific license and our [code of conduct](CODE_OF_CONDUCT.md).

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).

## Table of contents

- [Submitting an issue](#submitting-an-issue)
- [Submitting a pull request](#submitting-a-pull-request)
- [Documentation standards](#documentation-standards)
- [Licensing standards](#licensing-standards)
- [Coding standards](#coding-standards)
- [Naming conventions](#naming-conventions)
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
| Commercial  | The software is developed and distributed by Q-CTRL and is commercial in nature                    | Q-CTRL Terms of service<br>[HTML](https://q-ctrl.com/terms) / [Text](https://q-ctrl.com/terms.txt)                                         |
| Open source | The software is developed and distributed by Q-CTRL, is open source, and contributions are welcome | Apache License, Version 2.0<br>[HTML](http://www.apache.org/licenses/LICENSE-2.0) / [Text](http://www.apache.org/licenses/LICENSE-2.0.txt) |
| Unlicensed  | The software is developed by Q-CTRL and is not distributed                                         | N/A                                                                                                                                   |

## Coding standards

When contributing code, bear in mind that Q-CTRL values the [Three Virtues](http://threevirtues.com/). Standards for coding style SHOULD be obtained from the following hierarchy in the order specified.

1. [Third-party](#third-party)
1. [Language](#language)
1. [First-party](#first-party)

### Third-party

"Third-party" refers to the third-party software you are using and the corresponding [Third-party standards](#third-party-standards). For example, if you are using [Django](https://www.djangoproject.com/), you MUST use the [Django coding style](https://docs.djangoproject.com/en/dev/internals/contributing/writing-code/coding-style/). If:

1. you are not using third-party software, or
1. the third-party software does not specify a coding standard, or
1. the coding standard does not specify a rule (e.g. how to name variables)

then, you MUST move to [Language](#language).

### Language

"Language" refers to the language you are using and the corresponding [language standards](#language-standards). For example, if you are using [Python](https://www.python.org/), you MUST use the [PEP 8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/). If:

1. the language does not specify a coding standard, or
1. the coding standard does not specify a rule (e.g. how to name variables)

then, you MUST move to [First-party](#first-party).

### First-party

"First-party" refers to the [Q-CTRL coding standards](#q-ctrl-coding-standards). The Q-CTRL coding standards exist to specify standards that are not defined in the coding standards of the third-party software or language you are using.

## Third-party standards

| Third-party | Style                                                                                                          | Docstrings                                                        | Testing                       | Linting                           |
|-------------|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------|-----------------------------------|
| Django      | [Django coding style](https://docs.djangoproject.com/en/dev/internals/contributing/writing-code/coding-style/) | [numpydoc](https://numpydoc.readthedocs.io/en/latest/format.html)[[++](#numpydoc-docstrings)] | [pytest](https://pytest.org/) | [Pylint](https://www.pylint.org/) |
| React       | [Prettier](https://prettier.io/)                                                                               | [JSDoc](http://usejsdoc.org/)                                     | [Jest](https://jestjs.io/)    | [ESLint](https://eslint.org/)     |

## Language standards

| Language   | Style                                              | Docstrings                                                        | Testing                                                    | Linting                                                                    |
|------------|----------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------|----------------------------------------------------------------------------|
| GraphQL    | [GraphQL Rules](https://graphql-rules.com/)        | N/A                                                               | N/A                                                        | [graphql-schema-linter](https://github.com/cjoudrey/graphql-schema-linter) |
| HTML       | [Prettier](https://prettier.io/)                   | N/A                                                               | [HTMLProofer](https://github.com/gjtorikian/html-proofer/) | N/A                                                                        |
| JavaScript | [Prettier](https://prettier.io/)                   | [JSDoc](http://usejsdoc.org/)                                     | [Jest](https://jestjs.io/)                                 | [ESLint](https://eslint.org/)                                              |
| Markdown   | [Prettier](https://prettier.io/)                   | N/A                                                               | N/A                                                        | [Markdownlint](https://github.com/markdownlint/markdownlint/)              |
| Python     | [PEP 8](https://www.python.org/dev/peps/pep-0008/) | [numpydoc](https://numpydoc.readthedocs.io/en/latest/format.html)[[++](#numpydoc-docstrings)] | [pytest](https://pytest.org/)                              | [Pylint](https://www.pylint.org/)                                          |

## Q-CTRL coding standards

### Variable naming

- Spell variable names out in full using American English spelling (e.g. `optimized_pulse` or `optimizedPulse` and **NOT** `op`)
- For variable names that are more than three words, use an acronym (e.g. `cpmg` and **NOT** `carr_purcell_meiboom_gill` or `carrPurcellMeiboomGill`)
- For variable names that describe how many of an object there are, use `<object>_count` or `<object>Count` (e.g. `pulse_count` or `pulseCount` and **NOT** `number_of_pulses`, `numberOfPulses`, `pulses_count` or `pulsesCount`)

### numpydoc docstrings

The [numpydoc](https://numpydoc.readthedocs.io/en/latest/format.html) standard is unopinionated and/or inconsistent in a small number of cases. We therefore adopt the following additional standards:

- Place the leading and final triple quotes of each docstring on their own lines, with no blank lines separating them from the contents, as follows:
  ```
  """
  <contents>
  """
  ```
- Use single backticks when referring to a module, function, class, method, parameter, variable, or attribute thereof; otherwise use double backticks (for example `` `np.array` ``, `` `int` ``, `` `parameter_1` ``, `` `CustomClass.attribute` ``, `` `CustomClass.method` ``, ` ``value_1*value_2`` `, ` ``function().result`` `, or ` ``List[int]`` `).

## Naming conventions

- **Repository** specifies the framework or language (in that order)
- **Install** implies the language (e.g. `pip` = Python, `npm` = JavaScript, `gem` = Ruby, etc.)
- **Import** MAY negates the `-` (e.g. see [PEP 8 -- Style Guide for Python Code: Package and Module Names](https://www.python.org/dev/peps/pep-0008/#package-and-module-names))

### Python examples

| Type       | Example             |
|------------|---------------------|
| Repository | `qctrl/python`      |
| Install    | `pip install qctrl` |
| Import     | `import qctrl`      |

| Type       | Example                        |
|------------|--------------------------------|
| Repository | `qctrl/python-api-client`      |
| Install    | `pip install qctrl-api-client` |
| Import     | `import qctrlapiclient`        |

| Type       | Example                        |
|------------|--------------------------------|
| Repository | `qctrl/python-visualizer`      |
| Install    | `pip install qctrl-visualizer` |
| Import     | `import qctrlvisualizer`       |

| Type       | Example                               |
|------------|---------------------------------------|
| Repository | `qctrl/django-visualizer`             |
| Install    | `pip install qctrl-django-visualizer` |
| Import     | `import qctrldjangovisualizer`        |

### JavaScript examples

| Type       | Example                    |
|------------|----------------------------|
| Repository | `qctrl/javascript`         |
| Install    | `npm install @qctrl/qctrl` |
| Import     | `import @qctrl/qctrl;`     |

| Type       | Example                         |
|------------|---------------------------------|
| Repository | `qctrl/javascript-api-client`   |
| Install    | `npm install @qctrl/api-client` |
| Import     | `import @qctrl/api-client;`     |

| Type       | Example                         |
|------------|---------------------------------|
| Repository | `qctrl/javascript-visualizer`   |
| Install    | `npm install @qctrl/visualizer` |
| Import     | `import @qctrl/visualizer;`     |

| Type       | Example                               |
|------------|---------------------------------------|
| Repository | `qctrl/react-visualizer`              |
| Install    | `npm install @qctrl/react-visualizer` |
| Import     | `import @qctrl/react-visualizer;`     |

## Resources

- [How to contribute to open source](https://opensource.guide/how-to-contribute/)
- [Code of conduct](CODE_OF_CONDUCT.md)
- [Support](SUPPORT.md)
