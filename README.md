# OHA Team Coding Convention Manifesto

"OHA Team Coding Convention Manifesto" contains a set of rules and requirements that dictate why and how OHA Team follow coding convention standards in company. You can find full document in [OHA-Team-Coding-Convention-Manifesto.md](./README.md) or visit our official website [ohateam.com/coding-convention-manifesto](https://ohateam.org/coding-convention-manifesto.com) to find previous versions and localized specifications.

All projects, apps, files, classes, functions, variable, etc. MUST apply rule of OHA Team coding convention.

The goal of this manifesto is to produce safe, secure, fast and easy understandable code by using manifesto standard. 

Changes to the document and open an issue by a [GitHub Open Issue](https://github.com/oha-organization/OHA-Team-Coding-Convention-Manifesto/issues) which you can use.


OHA Team Coding Convention Declaration 0.0.1
============================================

Summary
-------

There is no exact coding style for programming languages but known the best practice is keep consistent.
Unless there is a generally acceptable logical reason, follow the rules.

Folowed standarts:

1. [Semantic Versioning](https://semver.org/)
1. [Conventional Commit](https://www.conventionalcommits.org/)
1. [PEP 8 – Style Guide for Python Code](https://peps.python.org/pep-0008/)
1. [PEP 20 – The Zen of Python](https://peps.python.org/pep-0020/)
1. [GitHub Workflow for Committing](https://docs.github.com/en/actions/using-workflows)

Followed standarts will be added.

Introduction
------------

In the world of software management standarts are important.
In this document we make another standart for OHA Team Company.
We call this system "OHA Team Coding Convention." Under this scheme,
you will use concrate declations for easily and safely moving your project forward.

OHA Team Coding Convention Specification (SemVer)
-------------------------------------------------

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD",
"SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be
interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).

1. There is no exact coding style for programming languages but keep consistent.

1. Unless there is a generally acceptable logical reason, follow the rules.

1. For version number use "Semantic Version" (SEMVER) MAJOR.MINOR.PATCH style numbering.

1. For coding style use [PEP 8 – Style Guide for Python](https://peps.python.org/pep-0008/),
unless there is an acceptable logical reason. Brief examples as follows:

      1. Identifier(variable): All small letters, if two or more word use snake case style.
      Examples: person, height, first_name

      1. Collection(list, tuple, array, vs.): Plural names or name_list.
      Examples: colors, user_list, question_list, questions

      1. Function(method): All small letters, snake case, concise imperative sentences.
      Context + Verb + How (user_get_by_id)
      Examples: user_add(), user_delete(), user_delete_by_name()
      
      1. If function name is too general like [Python builtin functions](https://docs.python.org/3/library/functions.html)
      use only verb or Verb + Context + How. As The Zen of Python -> Although practicality beats purity.
      Example: len, isinstance(), getattr() settattr, get_elements_by_id(), get_elements_by_class_name()
      
      1. Class: Pascal case and noun.
      Examples: Color, Animal, IndexView
      
      1. Module(file): All small letters, single word, if two or more word use flat case style.
      Examples: calender, collections, configparser
      
      1. All other detail(comment, white spaces, conditional, expression, statement, etc.) use
      [PEP 8 – Style Guide for Python](https://peps.python.org/pep-0008/)


1. For database design:

      1. Identifier(variable): All small letters, if two or more word use snake case style.
      Examples: person, height, first_name

      1. Collection(list, tuple, array, vs.): Plural names or name_list.
      Examples: colors, user_list, question_list, questions

      1. Function(method): All small letters, snake case, concise imperative sentences.
      Context + Verb + How (user_get_by_id)
      Examples: user_add(), user_delete(), user_delete_by_name()

1. Unless there is a generally acceptable logical reason, follow the rules.

1. Precedence refers to how versions are compared to each other when ordered.

   1. Precedence MUST be calculated by separating the version into major,
      minor, patch and pre-release identifiers in that order (Build metadata
      does not figure into precedence).

   1. Precedence is determined by the first difference when comparing each of
      these identifiers from left to right as follows: Major, minor, and patch
      versions are always compared numerically.

      Example: 1.0.0 < 2.0.0 < 2.1.0 < 2.1.1.
