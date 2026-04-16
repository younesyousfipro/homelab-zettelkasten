# root user

The root user is the superuser in Unix/Linux systems.

It has unrestricted access to all files, commands, and system resources.

## Key characteristics - What can root do

- user ID = 0
- full read/write/execute permissions
- bypasses most security restrictions
- start/stop services
- manage users and permissions
- modify system configs
- (break the system)

## Why root is dangerous

With great power comes great responsibility:

- no safeguards
- no permission checks
- mistakes can affect the entire system

For example:
```bash
rm -rf /
```
run as root -> nothing left.

## Use of sudo

Instead of logging as root and staying root:

- users operate normally
- use sudo only when required

This reduces:

- attack surface
- human errors

## Best practices

- do not use root for daily tasks
- use sudo admin actions
- restrict root access, especially via SSH
- log and audit privileged commandes

## Related

- [[sudo]]
- [[linux-access-control]]

