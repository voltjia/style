# C++ Style Guide

The point of this document is not to join the holy war of coding styles, but simply provides one of the many possibilities, so that if you have the same taste, you may simply follow this guide instead of writing one.

## General Rules

When coding, always keep in mind that simplicity and clarity are important, because about 80% of the time are actually spent on maintaining. If there is a conflict between simplicity and clarity, choose clarity. This document may never be complete as C++ is a so complex language, so whenever you meet something not mentioned in this guide, just remember to keep everything clean and simple.

## Naming

### File Names

File names should be all lower-case with underscore '_' as the word separator.

### Namespace Names

Namespace names should be all lower-case with underscore '_' as the word separator.

### Type Names

Type names should be in upper camel case.

```C++
class CamelCase {
    ...
};
```

### Variable Names

Variable names should be in lower camel case. Constants and enumerators follow the same rule.

```C++
int camelCase {0};
```

### Function Names

Function names should be in lower camel case.

```C++
void camelCase() {
    ...
}
```

### Macro Names

Macro names should be all upper-case with underscores '_'  as the word separator.

```C++
#define UPPER_CASE_WITH_UNDERSCORES true
```

## Formatting

### Line Length

Each line of code should be at most 80 characters long.

### Spaces vs. Tabs

Use only spaces, and indent 4 spaces for each level.

### Layout

Use K&R derived style 1TBS. Functions should have their opening braces on the same line, and the braces are not omitted for a control statement with only a single statement in scope.

```C++
void obts() {
    if (!hasOnlyOneStatement()) {
        hasBraces();
    } else {
        alsoHasBraces();
    }
}
```

## References

* [C++ Core Guidelines](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines)
* [Google C++ Style Guide](https://google.github.io/styleguide/cppguide.html)
* [Indentation Style](https://en.wikipedia.org/wiki/Indentation_style)
* [Clang-Format Style Options](https://clang.llvm.org/docs/ClangFormatStyleOptions.html)