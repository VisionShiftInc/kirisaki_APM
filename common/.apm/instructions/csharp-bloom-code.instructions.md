---
description: C# Bloom Code Style Guide
applyTo: "**/*.cs"
metadata:
  version: 1.1
---
# C# "Bloom Code" Style Guide
This is a strict style guide meant for code legibility, maintainability, and verifiability of C# code.
Its principal objective is maximizing reading speed and quick understanding for someone unfamiliar with the codebase.
The main ideas are:
* organize all code in a predictable manner, for example by grouping declarations based on a common characteristic
    and then alphabetically within each group
* avoid abbreviations, acronyms, aliases, and mnemonics
* use line breaks judiciously to separate logical concepts within a statement and reduce visual clutter


## Basic Guidelines
Do not add UTF-8 BOM markers to the beginning of files.

Use Allman bracing for namespaces (if necessary), classes, functions, and methods.
Use One True Brace Style for any other blocks.
Expression-bodied members are an acceptable alternative to braces.

Always use meaningful variable names, and avoid any variable names with less than 3 characters.
Avoid reassigning new values to existing variables, as each variable models a distinct concept, and preserving the full
trace of intermediate objects simplifies debugging.

Any construct necessarily or optionally delimited by parentheses, brackets, or braces, which includes 2 or more items
separated by commas, logical operators, or arithmetic operators must have each item on a separate line with the
appropriate indent. Examples of this construct type include: iterables, function arguments and parameters, and
conditional structures.
Break before a binary operator, not after.

Strive to do at most one function/method/operator call per line. Nested calls are perfectly fine, but with each call
on its own line with the appropriate indent, as shown in the following example:
```csharp
var myVar = MyFunc(
    MyOtherFunc(
        MyThirdFunc(
            myArg,
            myOtherArg
        )
    )
);
```


## Structure
Each file should contain one primary type, which should share the filename.
Any additional helper types must be organized before the primary type, in blocks in this order:
1. Public types
2. Internal types

The same ordering applies to types declared directly within a namespace.

Methods in classes must be organized in blocks in this order:
1. Abstract methods
2. Constructors and finalizers
3. Public methods
4. Internal methods
5. Protected methods
6. Private methods

Within each block, any types and methods should be ordered alphabetically by their name.
