# Linux file permissions

Linux permissions define what actions can be performed on a file or directory.

## Permission types

- read (r)
- write (w)
- execute (x)

## Structure

Permissions are defined for:

- user (owner)
- group
- others

Example:

```bash
-rwxr-x---
```
## Interpretation

	•	user → rwx
	•	group → r-x
	•	others → no access

## File vs directory

Permissions behave differently:
	•	file:
	•	r → read content
	•	w → modify content
	•	x → execute
	•	directory:
	•	r → list files
	•	w → create/delete files
	•	x → traverse directory

## Related

	•	[[linux-access-control]]
	•	[[linux-octal-permissions]]
	•	[[chmod]]