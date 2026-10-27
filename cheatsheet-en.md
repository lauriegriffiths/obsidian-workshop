# Obsidian & Markdown — quick reference

**Capture first. Add structure when it helps.** A vault is a folder of notes. Start with today's note, link recurring people or projects, and use search to find things again.

## Everyday syntax

| Purpose | Type this |
| --- | --- |
| Heading / subheading | `# Heading` / `## Subheading` |
| Bold / italic | `**bold**` / `*italic*` |
| List / numbered list | `- Item` / `1. Item` |
| Task / completed task | `- [ ] To do` / `- [x] Done` |
| Quote | `> Quoted text` |
| Website | `[Obsidian](https://obsidian.md)` |
| Note link¹ | `[[Maya Chen]]` |
| Link to a heading¹ | `[[Maya Chen#Next steps]]` |
| Image | `![Description](images/photo.jpg)` |
| Embed another note¹ | `![[Maya Chen]]` |
| Inline code | Surround text with one backtick on each side |

Separate paragraphs with a blank line. ¹Obsidian wiki-link syntax. Keep double brackets together, with no spaces between the brackets.

## Handy keyboard shortcuts

Default shortcuts on Mac; use `Ctrl` instead of `Cmd` on Windows/Linux. Customize them in Settings → Hotkeys.

| Action | Shortcut |
| --- | --- |
| Open a note by name (Quick switcher) | `Cmd+O` |
| Find and run a command (Command palette) | `Cmd+P` |
| Create a new note | `Cmd+N` |
| Search across the vault | `Cmd+Shift+F` |
| Bold / italic | `Cmd+B` / `Cmd+I` |

## Properties (YAML frontmatter)

Put this at the **very top** of the file; ordinary note text goes after the closing `---`.

```yaml
---
summary: "Next: send the sketch"
work_time: 2.5
birthday: 1990-11-08
owner: "[[Aki Mori]]"
---
```

Use `key: value` with a space after the colon. Delimiters are three adjacent hyphens. Quote text containing `: ` and wiki links. Numbers stay unquoted; dates use `YYYY-MM-DD`. Daily notes can remain plain text.

## Tables and code blocks

```text
| Name | Next action |
| --- | --- |
| Maya | Send sketch |
```

Fence code with three backticks on separate opening/closing lines. An optional language name follows the opening backticks. Dataview uses this pattern:

````text
```dataview
TABLE summary AS "Summary", work_time AS "Hours"
FROM "Projects"
SORT file.name ASC
```
````

Install and enable **Dataview** via Settings → Community plugins → Browse. Put project notes in `Projects`; field names must match. View results in Reading view. Edit the source notes to update the table. `work_time` here is manually entered total hours.

## Finding and connecting information

**Search:** find words across the vault. **Backlinks:** see which notes link to this one. **Local graph:** explore neighbouring notes. **Daily notes:** record events while fresh. **Kanban:** track next actions. **Map View:** show notes with a `location` such as `"33.58,130.20"`. Graph lines represent links, not typed database relationships.

**First step:** write one useful note, link it, then find it again. Phone access needs sync setup; keep a backup too. Help: https://help.obsidian.md/

<!-- Print: rendered Markdown, A4 portrait, 10 pt body, 12 mm margins; disable browser headers/footers. Raw Markdown and different renderers may paginate differently. -->
