# Discretionary Access Control (DAC)

DAC is the access control model used by Linux.

## Principle

The owner of a resource controls its permissions.

## Model

subject → ownership → permissions → resource

## Characteristics

- simple and flexible
- permissions managed per file
- based on user ownership

## Limitations

- not centralized
- harder to manage at scale compared to RBAC

## Related

- [[linux-access-control]]
- [[rbac]]
