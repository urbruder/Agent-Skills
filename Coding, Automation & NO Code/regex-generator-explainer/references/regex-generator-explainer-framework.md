# Regex Framework

## Engine differences

JavaScript supports lookahead and lookbehind in modern runtimes, but not all environments.
Python uses `re` syntax and raw strings like `r"pattern"`.
Google Sheets supports RE2 and does not support lookbehind.
Many SQL systems use their own regex functions and escaping rules.

## Pattern types

- email-like validation
- URL/domain extraction
- phone number extraction
- SKU/order ID matching
- date matching
- text between delimiters
- remove special characters
- split on delimiters
- negative match
- multiline parsing

## Safety

Avoid overclaiming perfect validation for complex formats like emails, URLs, and international phone numbers. Provide practical validation patterns and limitations.

## Testing checklist

Include:
- expected matches
- expected non-matches
- edge cases
- capture groups
- replacement result if relevant

## Common flags

- `i` case-insensitive
- `g` global in JavaScript
- `m` multiline
- `s` dot matches newline
