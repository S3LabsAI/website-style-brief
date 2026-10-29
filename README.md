# Website Style Brief Skill

A Claude skill that turns one web page into a compact, evidence-based design brief that another person or agent can use without visiting the site. It describes the page as it exists today, not a proposed redesign.

## How it works

`SKILL.md` walks through four steps:

1. **Resolve the target** from a supplied URL or the active browser tab, and record the final URL after redirects.
2. **Read the content**: offer, navigation, calls to action, service areas & audience signals.
3. **Inspect the rendering** with screenshots of the hero, a middle section & the footer.
4. **Synthesize** the most distinctive supported facts into a fixed six-field brief.

## Output

One `txt` code block with exactly six fields:

```txt
Brief:

- Page kind: template gallery
- Product: insurepages.com, a gallery of insurance agency website templates for agency owners and insurance professionals, with preview cards and an option to open each template as a full site
- Audience: Insurance agency owners, insurance industry professionals
- Vibe words: Playful, Neo-Brutalist, Bold, Warm
- References: https://insurepages.com
- Avoid: em dashes, insurance jargon-heavy copy, competing calls to action
```

When the page can't be rendered or read, the skill follows the exception rules in `SKILL.md` instead of guessing.

## Structure

```
website-style-brief/
├── SKILL.md     # Skill instructions, output contract & examples
└── CLAUDE.md    # Copy of SKILL.md, so Claude Code uses the skill in this folder
```

## Source

Maintained in Notion (TP HQ / Anthropic Library / AI Library). The Notion page ID is in the `SKILL.md` frontmatter.

## Installing

Copy `SKILL.md` into a folder named `website-style-brief` in your skills directory, or upload the folder as a skill in Claude.
