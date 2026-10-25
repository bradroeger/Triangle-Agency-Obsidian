# Repository guidance

This repository is an Obsidian vault for a tabletop role-playing campaign. Its primary content is Markdown notes; it is not a software project.

## Working with notes

- Keep campaign information in Markdown and preserve Obsidian wikilinks (`[[Note]]`) and embeds (`![[File]]`) when editing.
- Treat established campaign facts as canon. Do not invent or silently alter names, events, relationships, or rules; mark uncertain details as unresolved or ask for clarification.
- Preserve existing filenames and spelling unless a rename is requested. Update links when a requested rename requires it.
- Keep notes readable in Obsidian and use concise headings and lists where they improve navigation.
- Follow the structure and metadata conventions of nearby notes or templates when they exist. Do not add frontmatter or template fields without a reason.
- Avoid editing `.obsidian` settings, plugin code, or theme files unless the task specifically concerns vault configuration.

## Validation

- There is no build or test suite to run for ordinary note changes.
- Before finishing, review the diff for unintended changes and verify that edited wikilinks and Markdown structure are intact.
