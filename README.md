# Homelab Zettelkasten

Version-controlled Zettelkasten knowledge base using Obsidian, focused on DevOps, homelab, and infrastructure concepts.

---

## Overview

This repository contains a personal knowledge system built with the Zettelkasten method.

The goal is to:
- understand systems (not just memorize commands)
- connect concepts across DevOps domains
- document real learning from homelab practice

Notes are written in Markdown and designed to be used with Obsidian.

---

## Structure

The repository is intentionally kept simple.  
Folders are used for clarity in GitHub, not to enforce strict hierarchy.

notes/
├── concepts/
├── tools/
├── procedures/
├── incidents/
└── maps/

---

### concepts/

Core ideas and explanations.

Examples:
- `zettelkasten.md`
- `atomic-note.md`
- `ssh.md`
- `infrastructure-as-code.md`

→ Focus: understanding

---

### tools/

Concrete tools or system components.

Examples:
- `terraform.md`
- `k3s.md`
- `ansible.md`

→ Focus: usage and role in the system

---

### procedures/

Step-by-step actions and setups.

Examples:
- `setup-ssh-access-homelab.md`
- `install-k3s-server.md`

→ Focus: execution

---

### incidents/

Real problems and debugging notes.

Examples:
- `ssh-permission-denied.md`
- `k3s-agent-not-joining.md`

→ Focus: troubleshooting and experience

---

### maps/

Entry points into the knowledge graph.

Examples:
- `homelab-map.md`
- `kubernetes-map.md`

→ Focus: navigation and overview

---

## How to use

This is not a traditional documentation repository.

- Notes are **atomic** (one idea per note)
- Notes are **linked together** using `[[...]]`
- Navigation is done through:
  - search
  - links
  - backlinks (in Obsidian)

You are not supposed to read everything linearly.  
You explore the knowledge graph depending on your needs.

---

## Workflow

Typical usage:

1. Learn something (concept, tool, issue)
2. Create or update a note
3. Link it to existing notes
4. Reuse notes to produce structured documentation (README, projects, etc.)

---

## Why Zettelkasten

- avoids large, unstructured notes
- improves long-term understanding
- builds a connected mental model of systems

---

## Tech

- Markdown
- Obsidian (recommended)
- Git / GitHub for versioning

---

## Scope

This knowledge base focuses on:

- DevOps fundamentals
- Kubernetes (k3s)
- Infrastructure as Code (Terraform, Ansible)
- Homelab architecture and experimentation

---

## Author

Younes Yousfi