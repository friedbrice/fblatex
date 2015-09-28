fbteach - LaTeX 2e package for styling course documents

# Usage

Invoke as

    \usepackage{fbteach}

There are no options.

# Required Packages

As this is a style package (rather than a structure package), we pull in
many packages.

- `\RequirePackage{lmodern}`
- `\RequirePackage{microtype}`
- `\RequirePackage{fixltx2e}`

- `\RequirePackage{amsmath, amssymb}`
- `\RequirePackage{graphicx}`
- `\RequirePackage{changepage}`
- `\RequirePackage{multicol}`

- `\RequirePackage[margin=0.75in]{geometry}`
- `\RequirePackage{parskip}`
- `\RequirePackage{nopageno}`

# Format and Style

fbteach defaults to lmodern sans for non-math. Math is in lmodern serif,
but notably all math is set to displaystyle. Itemize bullets are changed
to solid squares.

We use 0.75" margins, we do not indent paragraphs but we do skip lines
between them, and we do not number pages.

# Document Globals

A huge list of document global variables are created, used during
header and footer creation.

Each variable is set with the exported `\set<variable>{<value>}`

- `\newcommand{\course}{}
- `\newcommand{\coursename}{}
- `\newcommand{\term}{}

- `\newcommand{\instructor}{}
- `\newcommand{\instructorphone}{}
- `\newcommand{\instructoremail}{}

- `\renewcommand{\title}{}
- `\newcommand{\assessmentvalue}{}
- `\newcommand{\assessmenttime}{}

- `\newcommand{\finalday}{}
- `\newcommand{\finaltime}{}
- `\newcommand{\finalroom}{}

- `\newcommand{\meetingdays}{}
- `\newcommand{\meetingtime}{}
- `\newcommand{\meetingroom}{}

`meeting<num>foo` are ignored if unset by users.

- `\newcommand{\meetingtwodays}{}
- `\newcommand{\meetingtwotime}{}
- `\newcommand{\meetingtworoom}{}

- `\newcommand{\meetingthreedays}{}
- `\newcommand{\meetingthreetime}{}
- `\newcommand{\meetingthreeroom}{}

- `\newcommand{\meetingfourdays}{}
- `\newcommand{\meetingfourtime}{}
- `\newcommand{\meetingfourroom}{}

- `\newcommand{\meetingfivedays}{}
- `\newcommand{\meetingfivetime}{}
- `\newcommand{\meetingfiveroom}{}

- `\newcommand{\officehoursdays}{}
- `\newcommand{\officehourstime}{}
- `\newcommand{\officehoursroom}{}

`officehours<num>foo` are ignored if unset by user.

- `\newcommand{\officehourstwodays}{}
- `\newcommand{\officehourstwotime}{}
- `\newcommand{\officehourstworoom}{}

- `\newcommand{\officehoursthreedays}{}
- `\newcommand{\officehoursthreetime}{}
- `\newcommand{\officehoursthreeroom}{}

# Exported Macros

- `\newcommand{\fbsection}[1]`
  one argument, your content.
  un-numbered sections headings.

- `\newenvironment{definition}`
  no arguments.
  un-numbered block environment for definitions.

- `\newenvironment{theorem}`
  no arguments.
  un-numbered block environment for theorems.

- `\newenvironment{example}`
  no arguments.
  un-numbered block environment for examples.

- `\newcommand{\makeassessmenthead}`
  no "arguments" but reads document globals.
  creates a document heading for assessments.

- `\newcommand{\makehandouthead}`
  no "arguments" but reads document globals.
  creates a document heading for handouts.

- `\newcommand{\makesyllabushead}`
  no "arguments" but reads document globals.
  creates a heading for a course syllabus.
