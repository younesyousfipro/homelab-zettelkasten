# Linux octal permissions

Permissions in Linux can be expressed using octal notation.

Octal notation provides a compact and efficient way to represent permissions for user, group, and others.

## Why octal notation

Symbolic permissions (`rwxr-xr-x`) are readable but not always practical.

Octal notation:

- is shorter and faster to type
- is commonly used in CLI tools like `chmod`
- makes permission changes predictable and reproducible

Example:

```bash
chmod 755 script.sh
```

## How it works

Permissions are encoded using numbers based on binary addition:
	•	read (r) = 4
	•	write (w) = 2
	•	execute (x) = 1

Each digit is the sum of these values.

## Octal values (single digit)

```bash
0  ---  no permissions
1  --x  execute only
2  -w-  write only
3  -wx  write + execute
4  r--  read only
5  r-x  read + execute
6  rw-  read + write
7  rwx  read + write + execute
```

Each digit = r(4) + w(2) + x(1)

## Structure

An octal permission is composed of three digits:

```bash
user | group | others
```
Example:
```bash
755
```

Means:
	•	user → 7 → rwx
	•	group → 5 → r-x
	•	others → 5 → r-x

Equivalent symbolic form:
```bash
rwxr-xr-x
```
Common combinations
	•	755 → executable files (scripts, binaries)
	•	644 → standard files (readable by all, writable by owner)
	•	700 → private files (owner only)

Mental model

Each digit defines permissions for a category:

```bash
[ user ][ group ][ others ]
```

Each value is the sum of allowed actions.

Related
	•	[[linux-file-permissions]]
	•	[[chmod]]