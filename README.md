# awyiss/phpcs-sniffs

PHPCS standard with custom rules for Awyiss projects.

## Installation

```bash
composer require fabian-mcfly/awyiss-phpcs-sniffs
```

## Usage

```bash
vendor/bin/phpcs --standard=Awyiss src
```

## What the sniffs do

### Arrays

- `NoInlineCommentedArrayItemSniff`: Comments cannot be on the same line as an array item. The comment must be on its own line.

### Classes

- `ClassMemberSpacingSniff`: Enforces blank lines between class members. Same groups have no blank line,
 different groups have two blank lines, methods have one or two blank lines.

### Commenting

- `SeeUsesTagSpacingSniff`: Requires exactly one space after `@see` and `@uses`.
- `VariableCommentSniff`: Validates property docblocks. Special case: missing `@var` is allowed when `@inheritdoc` is present.

### Functions

- `ArrowFunctionDeclarationSniff`: Validates arrow function (`fn`) formatting. No space before `(`, exactly one space around `=>`,
 and clean indentation for wrapped lines.

### Operators

- `MethodChainingSniff`: Validates method chains. Long or multiline chains must be wrapped and indented consistently,
 including semicolon placement.

### WhiteSpace

- `ArrayUnionIndentationSniff`: Aligns the closing `]` correctly in specific multiline array union cases.
- `ConstantDeclarationSpacingSniff`: In typed `const` declarations, requires exactly one space between the type and constant name.
- `SemicolonSpacingSniff`: Disallows whitespace before `;`. Also applies rules for method chains and multiline string concatenation.
- `SingleArgumentNotMultilineSniff`: Prevents simple single argument calls from being split across multiple lines without need.
