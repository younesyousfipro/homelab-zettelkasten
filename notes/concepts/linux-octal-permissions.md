# Linux octal permissions

Permissions can be expressed using octal notation.

## Values

- read (r) = 4
- write (w) = 2
- execute (x) = 1

## Examples

- 7 = rwx
- 6 = rw-
- 5 = r-x
- 4 = r--

## Common combinations

- 755 → rwxr-xr-x
- 644 → rw-r--r--
- 700 → rwx------

## Usage

```bash
chmod 755 script.sh
```
## Related

	•	[[linux-file-permissions]]
	•	[[chmod]]