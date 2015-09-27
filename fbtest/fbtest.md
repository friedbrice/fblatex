fbtest - LaTeX 2e package for creating quizzes, tests, exams...

# Usage

Invoke as

    \usepackage{fbtest}

or

    \usepackage[key]{fbtest}

The presence of the `key` option alters the behavior of the `\solution`
and the `\inlinesolution` commands.

# Required Packages

Requires the `color` package, available with most TeX distributions and
on CTAN.

# Format and Style

Notably, `fbtest` does not overwrite any document formatting or style.

# Exported Macros

- `\newcounter{ProblemCounter}`
  counter incremented by the `problem` environment.

- `\newcounter{SubproblemCounter}[ProblemCounter]`
  counter incremented by the `subproblem` command.
  reset whenever `ProblemCounter` changes.

- `\newcounter{StatementCounter}[ProblemCounter]`
  counter incremented by the `statement` command.
  reset whenever `ProblemCounter` changes.

- `\newcounter{ChoiceCounter}[ProblemCounter]`
  counter incremented by the `choice` command.
  reset whenever `ProblemCounter` changes.

- `\newenvironment{problem}[1]`
  one argument, number of points. leave blank for no points.

- `\newcommand{\subproblem}[2]`
  two arguments, number of points and your content.

- `\newenvironment{choices}`
  no arguments.
  must occur within the `problem` environment.

- `\newcommand{\choice}[1]`
  one argument, your content.
  must occur within the `choices` environment.

- `\newenvironment{statements}`
  no arguments.
  must occur within the `problem` environment.

- `\newcommand{\statement}[1]`
  one argument, your content.
  must occur within the `statements` environment.

- `\newcommand{\solution}[1]`
  one argument, your content.
  ignored by default. prints if package is invoked with `key` option.

- `\newcommand{\inlinesolution}[1]`
  one argument, your content.
  ignored by default. prints if package is invoked with `key` option.
  useful if you have, say, a table that you want to fill in.

- `\newcommand{\llabel}[1]`
  one argument, a label name.
  creates a label whose name is scoped to the current problem.

- `\newcommand{\lref}[1]`
  one argument, a label name.
  references a label whose name is scoped to the current problem.

# Internal Macros

- `\newcommand{\@inenvir}{}`
- `\newcommand{\@wantenvir}{}`
- `\newcommand{\@savedenvir}{}`
  internal global variables.
  used to check that the document is stucturally sound.

- `\newcommand{\@updateenvir}[1]`
  internal function.
  one argument, a string.
  used to check that the document is stucturally sound.
  updates `\@inenvir` to #1, saving the old envir.

- `\newcommand{\@restoreenvir}`
  internal function.
  used to check that the document is stucturally sound.
  restores the old `\@inenvir`.

- `\newcommand{\@envircheck}[1]`
  internal function.
  one argument, a string.
  used to check that the document is stucturally sound.
  compares the last `\@inenvir` with #1, halts if they don't match.
