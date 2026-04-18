# sudo

`sudo` (superuser do) allows a user to execute commands with elevated privileges,
usually as the root user.

It is the standard mechanism for controlled privilege escalation on Unix/Linux systems.

## Historical context

Originally, system administration required logging in directly as `root`.

This was risky:

- full access at all times
- no traceability
- high risk of mistakes

`sudo` was introduced to:

- avoid direct root login
- allow temporary privilege escalation
- track administrative actions

## Key idea

Instead of being root all the time:

````text
user → sudo → root (temporary)
## Example

```bash
sudo systemctl restart nginx
````

Privileges are granted per command, not per session.

# How it works

- user authenticates (usually with password)
- system checks etc/sudoers
- if allow -> command runs with elevated privileges

# Why it matters

- limit risk (least privilege)
- improves auditability (who did what?)

# Risks

- misuse can lead to full system compromise
- poorly configured sudo -> too much access

# Best practices

- grant minimal privileges
- avoid giving full sudo access when not needed
- avoid running full shells as root unless necessary

# Mental model

sudo = controlled bridge to root

## Related

• [[linux-access-control]]
• [[least-privilege-principle]]
• [[root-user]]
