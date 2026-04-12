# Linux permission patterns

Common permission patterns used in real-world Linux systems.

These patterns reflect security best practices and typical use cases.

## Files

### Sensitive / private data

```text
600 → rw-------
400 → r--------
```

- secrets
- SSH private keys
- private configs

Rule: only the owner should access

---

### Team shared (read-only)

```text
640 → rw-r-----
```

- configs
- shared documentation

Rule: owner writes, group reads

---

### Team shared (read/write)

```text
660 → rw-rw----
```

- collaborative files

Rule: group collaboration without exposing to others

---

### Standard files

```text
644 → rw-r--r--
```

- text files
- configs readable by all

---

## Executables / scripts

```text
700 → rwx------
750 → rwxr-x---
755 → rwxr-xr-x
```

- 700 → personal script
- 750 → team script
- 755 → public executable

Rule: only executables should have `x`

---

## Directories

```text
700  → private directory
750  → team directory
770  → collaborative directory
755  → public directory
```

### Important

- `x` = traverse (enter directory)
- without `x`, directory cannot be accessed

---

## Mental rules

- not executable → no `x`
- secrets → 600 or 400
- team work → use groups
- directories → always consider `x`
- avoid `777` (almost always wrong)

---

## Ultra-short summary

```text
600 → secret
640 → team read-only
660 → team read-write
644 → standard file
755 → executable
```

## Related

- [[linux-file-permissions]]
- [[linux-octal-permissions]]
- [[linux-users-and-groups]]
- [[chmod]]