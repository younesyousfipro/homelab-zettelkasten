# Zettelkasten best practices

Guidelines to maintain a clean, consistent, and usable Zettelkasten over time.

## Naming

- use lowercase only
- use kebab-case (e.g. `rbac-in-kubernetes.md`)
- avoid underscores `_`
- keep names concise but explicit

## Renaming

- always rename files using Obsidian
- never rename files directly via CLI or Finder

Why:

- prevents broken links
- keeps the graph consistent

## Linking

- always link related concepts
- prefer meaningful links over many links
- avoid linking just for the sake of linking

Good:

- [[rbac-in-kubernetes]] → [[role-kubernetes]]

Bad:

- random or irrelevant links

## Atomic notes

- one main idea per note
- include enough context to understand the note alone
- avoid overly short notes with no value

## Structure

- folders are for organization, not logic
- logic comes from links, not hierarchy

## Consistency

- use the same naming conventions everywhere
- avoid mixing formats (e.g. `k8s_verbs` vs `kubernetes-verbs`)
- keep terminology consistent

## Common mistakes

- renaming files outside Obsidian
- mixing `_` and `-`
- creating duplicate notes for the same concept
- writing large notes mixing multiple topics
- creating notes without linking them

## Rule of thumb

If a note is:

- unclear → rewrite it
- isolated → link it
- too big → split it

## Related

- [[zettelkasten]]
- [[atomic-note]]
- [[note-linking]]
- [[zettelkasten-workflow]]
