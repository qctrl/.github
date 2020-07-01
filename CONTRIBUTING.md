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

When contributing code, bear in mind that Q-CTRL values the [Three Virtues](http://threevirtues.com/). Standards for coding style SHOULD be obtained from the following hierarchy in the order specified.

1. [Third-party](#third-party)
1. [Language](#language)
1. [First-party](#first-party)

### Third-party

"Third-party" refers to the third-party software you are using. For example, if you are using [Django](https://www.djangoproject.com/), you SHOULD use the [Django coding style](https://docs.djangoproject.com/en/dev/internals/contributing/writing-code/coding-style/). If:

1. you are not using third-party software, or
1. the third-party software does not specify a coding standard, or
1. the coding standard does not specify a rule (e.g. how to name variables)

then, you SHOULD move to [Language](#language).

### Language

"Language" refers to the language you are using and the corresponding [language standards](#language-standards). For example, if you are using [Python](https://www.python.org/), you SHOULD use the [PEP 8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/). If:

1. the language does not specify a coding standard, or
1. the coding standard does not specify a rule (e.g. how to name variables)

then, you SHOULD move to [First-party](#first-party).

### First-party

"First-party" refers to the [Q-CTRL coding standards](#q-ctrl-coding-standards). The Q-CTRL coding standards exist to specify standards that are not defined in the coding standards of the third-party software or language you are using.

## Language standards

| Language   | Style                                              | Docstrings                                                        | Testing                                                    | Linting                                                       |
| ---------- | -------------------------------------------------- | ----------------------------------------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------- |
| HTML       | [Prettier](https://prettier.io/)                   | N/A                                                               | [HTMLProofer](https://github.com/gjtorikian/html-proofer/) | N/A                                                           |
| JavaScript | [Prettier](https://prettier.io/)                   | [JSDoc](http://usejsdoc.org/)                                     | [Jest](https://jestjs.io/)                                 | [ESLint](https://eslint.org/)                                 |
| Markdown   | [Prettier](https://prettier.io/)                   | N/A                                                               | N/A                                                        | [Markdownlint](https://github.com/markdownlint/markdownlint/) |
| Python     | [PEP 8](https://www.python.org/dev/peps/pep-0008/) | [numpydoc](https://numpydoc.readthedocs.io/en/latest/format.html) | [pytest](https://pytest.org/)                              | [Pylint](https://www.pylint.org/)                             |

## Q-CTRL coding standards

### Variable naming

- Spell variable names out in full using American English spelling (e.g. `optimized_pulse` or `optimizedPulse` and **NOT** `op`)
- For variable names that are more than three words, use an acronym (e.g. `cpmg` and **NOT** `carr_purcell_meiboom_gill` or `carrPurcellMeiboomGill`)

### API design
The standards here are written in the context of GraphQL APIs, but the same concepts apply to any
other API, especially those with hard backwards-compatibility requirements.

#### Favour type safety
Type safety means that the data are structured in such a way that invalid data either cannot be
detected by the type system or cannot be represented at all. Striving for type safety wherever
possible ensures that the API is harder to misuse (errors can be detected before the code is
executed, or even before it’s written), and often leads to a more accurate representation of the
data (since implicit relationships are made explicit). Some examples of things to watch out for:
- Documentation specifying that certain data must be consistent in some way (e.g. "`X` must have the
same length as `Y`"): instead can we restructure the data so that consistency is enforced (e.g. so
that `X` and `Y` are specified in the same single list)? (Note that the answer will often be "no",
since the type system isn’t expressive enough to model all constraints.)
- Structured objects represented as unstructured objects (e.g. string representations of some
non-string object): instead can we represent the original structured object using native types?

#### When in doubt, use an enum instead of a boolean
Unless you can be highly confident that your value can only ever have two states, it's better to err
on the side of using an enum (to which we can add new states later) instead of a boolean. For
example, instead of a `use_gpu` boolean, use something like a `device` enum with values `CPU` and
`GPU`.

#### When in doubt, wrap list arguments in a type
If you're adding a new field consisting of a list of built-in types (e.g. scalars or lists),
consider whether the list entries might ever need more data associated with them. If so, or if in
doubt, create a new type to wrap the list entries. This adds a minor usability burden (one more
layer of classes) but can avoid extensibility headaches in the future if we want to add new data to
the entries.
```
# Hard to extend if we want to add data to each field.
matrices: [EncodedNumpyArray]

# Easy to extend if we want to add data to each field.
input FooItem {
    matrix: EncodedNumpyArray
}
items: [FooItem]
```
Note that for non-lists this isn’t so important, because additional fields can just be added to the
containing type if necessary.

#### When in doubt, use feature-specific types
Creating types focused on each feature allows us to be more specific, prescriptive and type-safe
with our data.
```
# Less specific, type only makes sense in context.
input GenericData {
    optional_field_1: Float
    optional_field_2: Float
}
input Feature1 {
    """Must have optional_field_1 set."""
    data: GenericData
}
input Feature2 {
    """Must have optional_field_2 set."""
    data: GenericData
}

# More specific, types make sense on their own.
input Feature1Data {
    field: Float!
}
input Feature2Data {
    field: Float!
}
input Feature1 {
    data: Feature1Data
}
input Feature2 {
    data: Feature2Data
}
```

#### Don't factor client syntax into decisions about data representation
Every client is affected by the data representation the same way, but the syntax is
client/language-dependent. Therefore the API, which is shared by all clients, should focus on a good
representation of the data, while the client should be responsible for adding idiomatic syntactic
sugar.

## Resources

- [How to contribute to open source](https://opensource.guide/how-to-contribute/)
- [Code of conduct](CODE_OF_CONDUCT.md)
- [Support](SUPPORT.md)
