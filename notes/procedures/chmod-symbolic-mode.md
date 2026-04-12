# chmod symbolic mode

Symbolic mode is an alternative to octal notation for modifying Linux file permissions.

It allows targeted changes without redefining all permissions.

## Why symbolic mode

Octal mode replaces all permissions at once:

```bash
chmod 755 file
```

Symbolic mode modifies only specific parts:

```bash
chmod u+x file
```

This makes it safer for incremental changes.

## Syntax

```bash
chmod [who][operator][permissions] file
```

who

	•	u → user (owner)
	•	g → group
	•	o → others
	•	a → all (u + g + o)

operator

- `+` → add permission
- `-` → remove permission
- `=` → set exact permission

permissions

	•	r → read
	•	w → write
	•	x → execute

## Examples

```bash
chmod u+x script.sh       # add execute to user
chmod g-w file.txt        # remove write from group
chmod o-r file.txt        # remove read from others
chmod a+x script.sh       # add execute for everyone
```

Set exact permissions:

```bash
chmod u=rwx,g=rx,o=rx file   # equivalent to 755
```

## Mental model

symbolic mode = patch existing permissions
octal mode = overwrite permissions

## Related

	•	[[chmod]]
	•	[[linux-file-permissions]]
	•	[[linux-octal-permissions]]