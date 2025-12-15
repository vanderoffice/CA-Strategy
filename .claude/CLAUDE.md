# CA-Strategy — Claude Code Context

This file provides project-specific context for Claude Code when working in this repository.

## Project overview

**CA-Strategy** is a strategic planning framework for California state government modernization, developed in collaboration with the Governor's Office of Operations (GovOps) and the Office of Data and Innovation (ODI).

**Repository purpose:** Define governance models, talent development strategies, funding mechanisms, and procurement guidance for scaling AI and digital innovation across California state agencies.

## Document structure

| Document | Purpose |
|----------|---------|
| 01-executive-summary.md | High-level overview for executive leadership |
| 02-governance-model.md | AI governance framework and organizational structure |
| 03-talent-development.md | Workforce strategy for AI/digital skills |
| 04-funding-implementation.md | Budget and funding mechanisms |
| 05-procurement-guide.md | Contracting and vendor guidance |
| appendices/ | Supporting templates, guides, and technical details |
| readiness-assessment/ | Agency AI readiness evaluation framework |

## Conventions

### File naming
- Numbered prefixes (01-, 02-) indicate reading order
- Use lowercase with hyphens: `funding-implementation.md`
- Appendices use letter prefixes in subdirectory

### Writing voice
| Audience | Voice | Notes |
|----------|-------|-------|
| Secretary / Undersecretary | Formal/Executive | Strategic, concise, decision-focused |
| Department directors | Professional | Analytical, implementation-oriented |
| Technical staff | Technical | Precise, detailed, actionable |
| Public / other agencies | Conversational | Accessible, jargon-free |

### Document format
- ALL CAPS for major section headers in executive documents
- Narrative paragraphs preferred over bullet lists for executive content
- Tables for structured data (timelines, roles, comparisons)
- Cross-references use relative links: `[governance model](02-governance-model.md)`

## Stakeholders

### Primary
- **GovOps** — Governor's Office of Operations (strategic oversight)
- **ODI** — Office of Data and Innovation (implementation lead)
- **Amy Tong** — Senior Counselor to the Governor
- **Jeffrey Marino** — ODI Director

### Secondary
- Department CIOs and CDOs
- Agency undersecretaries
- Governor's Innovation Fellows

## Related context

When drafting or editing documents in this repository:

1. **Check Granola** for recent meeting context about CA-Strategy discussions
2. **Reference global standards** at `~/.claude/docs/writing-standards.md`
3. **Use executive memo format** for leadership communications (TO/FROM/DATE/RE header, narrative sections)

## Google Docs workflow

Final documents are often shared via Google Docs for stakeholder collaboration:

```bash
# Convert markdown to Word/ODT for Google Docs upload
pandoc document.md -o document.odt

# Or use native paste: copy markdown, right-click in Google Docs → "Paste from Markdown"
```

See [google-docs-workflow.md](../docs/google-docs-workflow.md) for detailed instructions.
