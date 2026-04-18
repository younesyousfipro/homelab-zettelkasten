# Linux users and groups

Linux manages access using users and groups.

## Users

Each process runs as a user.

Check current user:

```bash
whoami
```

## Groups

Groups allow multiple users to share permissions.

Check groups:

```bash
groups
```

Add user to group:

```bash
sudo usermod -aG dev user
```

## Ownership

Each file has:
• one owner user
• one owner group

Check ownership:

```bash
ls -l
```

## Related

    •	[[linux-access-control]]
    •	[[chown]]
