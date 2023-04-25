# C++ Style Guide

This document aims to provide a coding style guide for C++ programmers who appreciate simplicity and clarity. The focus is not to participate in the ongoing debates over coding styles, but rather to offer a coherent and practical alternative for those who share similar preferences. Due to the complexity of the C++ language, this guide may not be exhaustive. In cases where the guide doesn't provide explicit direction, prioritize maintaining clean and simple code.

## General Rules

Remember that simplicity and clarity are crucial, as around 80% of programming time is typically spent on maintenance. When faced with a choice between simplicity and clarity, always prioritize clarity.

## Naming

### File Names

File names should be in all lower-case with hyphens '-' as the word separator (kebab case).

### Namespace Names

Namespace names should be short and all-lowercase, typically reflecting the project or module name. If it improves readability, underscores can be used as word separators, although the use of underscores is discouraged.

### Type Names

Type names should be in upper camel case. In UpperCamelCase, acronyms and contractions of compound words are treated as a single word. For example, use Http instead of HTTP, Json instead of JSON, and Stdin instead of StdIn.

```C++
class UpperCamelCase {
    // ...
};
```

### Variable Names

Variable names should be in snake case. This rule also applies to constants and enumerators. In snake_case, acronyms and contractions should be lowercased. For instance, use http_req instead of HTTP_req.

```C++
bool snake_case {true};
```

### Function Names

Function names should be in snake case as well.

```C++
void snake_case() {
    // ...
}
```

### Macro Names

Macro names should be all uppercase with underscores '_' as the word separator (screaming snake case).

```C++
#define UPPERCASE_WITH_UNDERSCORES true
```

## Formatting

### Line Length

Each line of code should be no longer than 80 characters.

### Spaces vs. Tabs

Use only spaces, with a 4-space indent for each level.

### Layout

Adopt the K&R-derived 1TBS style. Functions should have their opening braces on the same line, and braces should not be omitted for a control statement with only a single statement in scope.

```C++
void obts() {
    if (!has_only_one_statement()) {
        has_braces();
    } else {
        also_has_braces();
    }
}
```

## References

* [C++ Core Guidelines](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines)
* [Clang-Format Style Options](https://clang.llvm.org/docs/ClangFormatStyleOptions.html)
* [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html)
* [Indentation Style](https://en.wikipedia.org/wiki/Indentation_style)
* [LLVM Coding Standards](https://llvm.org/docs/CodingStandards.html#llvm-coding-standards)
* [PEP 8 – Style Guide for Python Code](https://peps.python.org/pep-0008/)
* [Rust API Guidelines](https://rust-lang.github.io/api-guidelines/naming.html)
