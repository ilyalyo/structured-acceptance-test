# Structured Acceptance Test

**Structured Acceptance Test ("STAT") is a simple and extensible standard for *acceptance testing processes*.** The *target* of the test can be any set of computer files, for example source code, images, audio files and documents. The *process* can be an automated computer program, manual execution of a test plan or even the vote of a committee of approvers. The *outcome* of the process is `pass` or `fail` and may also include helpful *findings* or *recommendations* which can be used to improve the target.

There are two parts to this specification:

 * [STAT Input](Stat-Input.md) -- defines what targets the process should test
 * [STAT Output](Stat-Output.md) -- identifies the test process and expresses the outcome, findings and recommendations

A computer program is said to *support* the Structured Acceptance Test standard if it accepts any valid STAT Input and it produces a valid STAT Output. It is recommended that command-line computer programs use the `--stat-file=<INPUT>` switch to support the STAT standard.

# Who can use it?

This standard is applicable for any automated or manual process that accepts computer files as input and can make a `pass` or `fail` decision. Examples of such processes include:

 * Static code analyzers
  * Code linters
  * Code style checkers
  * Minification checkers
 * Other static analyzers
  * Image metadata checkers
  * Image compression checkers
  * Spelling checkers
  * Grammar checkers
  * Digital signature verification
 * Dynamic code analysis
  * Unit tests (logic tests)
  * Automated UI tests
  * Continuous integration tests
 * Volatile testing
  * Link checkers
  * Package manager version checkers (requirement to use latest upstream versions)
  * Deployment testing (dry run)
 * Manual testing
  * Manual inspection
  * Manual walkthroughs
  * Unstructured customer feedback
  * Committee vote

The acceptance testing *outcome*, *findings* and *recommendations* can be used (*consumed*) by:

 * Interactive file editors (IDEs, text editors, word processors, image editors)
 * Command-line reporting tools (unit test reports)
 * Source code management / content management systems

# Why should I use it? XKCD 927?

**If your acceptance testing process uses a standardized output format then consumers can make better use of it.**

Integrations are amazing. They allow `clang` compilers to show compile errors in your integrated development environment, they allow spelling errors to be underlined in your word processor and they show up as red flags when you review a pull request. But what if *all* of these validations can be shown *everywhere* they are relevant? Standardization supports this.

This is the first widely-applicable standardization of its type so [XKCD 927](https://xkcd.com/927/) does not apply.

Specific features of this specification include:

 * **It is simple**, a few lines of Ruby can translate `gcc`, `clang` or `aspell` output into the required format
 * **The format is extensible**, any acceptance testing process can use this format
 * **Validation output is streamable** and available to the reporting tool incrementally
 * **Repeatability** is specified

# Project Status

This standard is currently version 0.2.0. We follow [Semantic Versioning](http://semver.org/).

**You can start using this standard today.** A few backwards-incompatible changes may be introduced before the 1.0.0. This will be a candidate for 1.0.0 release when all below items are completed.

 - [x] Defines the input format to select computer files
 - [x] Defines the output format for the outcome, findings and recommendations
 - [x] Follows the [Google JSON Style Guide](https://google.github.io/styleguide/jsoncstyleguide.xml)
 - [x] Supports real-time, incremental reporting
 - [ ] An example computer program is produced that supports STAT
 - [ ] An example computer program is produced that reads and reports the above output
 - [ ] Useful computer program is produced (or transformed) to support STAT
 - [x] Compatibility is established with [Code Climate Engine specification](https://github.com/codeclimate/spec)

# Copyright

This specification is copyright 2016 William Entriken and is released under the MIT license.

# Contributing

Development of this specification happens on GitHub. Please use [issues](https://github.com/fulldecent/structured-acceptance-test/issues) and [pull requests](https://github.com/fulldecent/structured-acceptance-test/pulls) to help improve it.

Please help to raise awareness by opening an issue with [your favorite static analysis tool](https://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis) to support this format.

Please open an issue with your favorite integrated development environment or source code sharing tool to request interoperability with this format.

-----

Please add your own projects below!

Supporting acceptance testing programs:

 * YOUR NAME HERE (STAT VERSION NUMBER SUPPORTED)

Supporting consumers:

 * Interactive file editors (IDEs, text editors, word processors, image editors)
   * YOUR NAME HERE
 * Command-line reporting tools (unit test reports)
   * YOUR NAME HERE
 * Source code management / content management systems
   * YOUR NAME HERE
