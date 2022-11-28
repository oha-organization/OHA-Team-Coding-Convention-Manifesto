# OHA Team Coding Convention Manifesto

[![OHA Team Coding Convention](https://img.shields.io/badge/OHA%20Team%20Coding%20Convention-0.1.0-green)](https://github.com/oha-organization/OHA-Team-Coding-Convention-Manifesto/)

"OHA Team Coding Convention Manifesto" contains a set of rules and requirements that dictate why and how OHA Team follow coding convention standards in company. You can find full document in [OHA-Team-Coding-Convention-Manifesto.md](./README.md) or visit our official website [OHA Team Coding Convention Manifesto](https://ohateam.org/coding-convention-manifesto.com) to find previous versions and localized specifications.

All projects, libraries, modules, apps, files, classes, functions, methods, variables, etc. MUST apply rule of OHA Team coding convention. Except that the current project already has a certain standard. This manifesto is specifically focused on the python programming language. For PHP language use this conventions -> https://www.php-fig.org/

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
        
        Examples: 
        
        ```person, height, first_name```

    1. Collection(list, tuple, array, vs.): Plural names or name_list. Remember to keep consistent.
    
        Examples: 
        
        ```colors, color_list, users, user_list, questions, question_list```

    1. Function(method): All small letters, snake case, concise imperative sentences.
    Context + Verb + How (user_get_by_id)
    
        Examples: 
        
        ```user_add(), user_delete(), user_delete_by_name()```
      
    1. If function name is too general like [Python builtin functions](https://docs.python.org/3/library/functions.html)
    use only verb or Verb + Context + How. As The Zen of Python -> Although practicality beats purity.
    
        Example:
        
        ```len, isinstance, getattr, settattr, get_elements_by_id, get_elements_by_class_name```
      
    1. Class: Pascal case and noun.
    
        Examples:
        
        ```Color, Animal, ClassName, IndexView```
      
    1. Module(file): All small letters, single word, if two or more word use flat case style.
    
        Example:
        
        ```calender, collections, configparser```
      
    1. All other detail(comment, white spaces, conditional, expression, statement, etc.) use
    [PEP 8 – Style Guide for Python](https://peps.python.org/pep-0008/)


1. For database naming Convention:

    1. Database, table, column, view, constraint, etc. all these names should be small ASCII letters.
    Except SQL keyword like SELECT, FROM, ORDER etc. for readiblity.
    
        Example:
        
        ```sql
        'SELECT * FROM person WHERE name="Alice" ORDER BY last_name'
        ```
      
    1. Avoid quotes(white spaces): Don't use white spaces or quotes table, column, etc. names.
    
        Examples: Don't do these ~"User Table", "First name", "SchoolTable"~
      
    1. Avoid reserved words(user, delete, select, lock, etc.).
      
    1. Avoid using type names(text, date, integer, timestamp, etc.).

    1. Use singlular names for tables, views, and other relations NOT plural. If you are not aggree keep consitent.
    
        Examples:
        
        ```person, student, member, question```

    1. Use underscores separate words.
    
        Examples:
        
        ```first_name, last_name, middle_name```
      
    1. Primary key fields should be named ```id```, NOT ~userid, userID, userId or user_id~
      
    1. Foreign Key fields should be named ```foo_id```(foo is table name)

    1. Use Explicit name NOT abbreviated forms (Except common abbreviations like i18n).
    
        Example:
        
        ```first_name, middle_name, primary_address```, NOT f_name, l_name or mid_name
      
    1. Index(idx_) : Indexes should be explicitly named and include both the table name and the column names indexed.
    Use idx_ prefix to show that is index.
    
        Examples:
        
        ```sql
        'CREATE INDEX idx_first_name_last_name ON person (first_name, last_name)';
        ```
      
    1. Constraint: Use pk_, uc_, fk_, chk_, etc. prefix for naming constrain.
        
        Examples:
        
        ```sql
        'CONSTRAINT uc_person UNIQUE (id, last_name)'
        
        'CONSTRAINT pk_person UNIQUE (id, last_name)'
        
        'CONSTRAINT fk_order_person FOREIGN KEY (person_id) REFERENCES person(id)'
        
        'CONSTRAINT chk_person_age CHECK (age>=18 AND city="Sandnes")'
        
        'CONSTRAINT fk_note_task FOREIGN KEY (task_id) REFERENCES task(id)'
        
        'CONSTRAINT fk_task_user FOREIGN KEY (user_id) REFERENCES user(id)'
        ```
      
    1. Use short table names
    
        Examples:
        
        ```site``` is better than ```site_detail```
      
    1. Date type column names: Suffix your date-type column names with _on or _date.
    
        Example:
        
        ```updated_on, updated_date or pub_date```
      
    1. Date-Time type column names: If your column name has time with it, then suffix them with _at or _time.
    
        Examples:
        
        ```ordered_at, order_time or created_time```
      
    1. Boolean type column Names: If you have boolean type column names, then prefix them with is_ or has_.
    
        Examples:
        
        ```is_admin or has_membership```

1. Only things worse than a bad convention are multiple conventions or no conventions. 
