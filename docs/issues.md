# Known Issues
This probably does not cover all issues; only known ones.

### Error in `defconf()` showing `{content}` placeholder.
When inputting a file that does not exist in `defconf()`, it outputs:
```plaintext
[ERROR]: defconf: File '{content}' does not exist.
```
as an error, with the `{content}` placeholder.
