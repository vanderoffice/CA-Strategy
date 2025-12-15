# Markdown ↔ Google Docs Workflow

This guide covers converting documents between Markdown (for version control in GitHub) and Google Docs (for stakeholder collaboration).

## Markdown → Google Docs

### Option 1: Pandoc (recommended for complex documents)

Convert markdown to ODT or DOCX, then upload to Google Drive:

```bash
# ODT preserves headers better
pandoc document.md -f markdown -t odt -o document.odt

# DOCX for Word compatibility
pandoc document.md -o document.docx
```

Then upload to Google Drive and open as Google Doc.

**Formatting preserved:**
- Headers (H1-H6)
- Bold, italic, links
- Bullet and numbered lists
- Tables
- Code blocks (monospace, no syntax highlighting)

### Option 2: Native Google Docs paste

Google Docs now supports markdown natively:

1. Copy the markdown content from your editor
2. Open a new Google Doc
3. Right-click → **Paste from Markdown**
4. Formatting is automatically converted

**Best for:** Quick, simple documents without complex tables.

### Option 3: n8n automation (advanced)

For automated conversion on git push, see the n8n workflow setup in the [CA-DevStacks repository](https://github.com/vanderoffice/CA-DevStacks).

## Google Docs → Markdown

When stakeholders edit in Google Docs and you need to sync back to GitHub:

### Option 1: Download and convert with Docling

```bash
# Download as .docx from Google Docs (File → Download → Microsoft Word)

# Convert using Docling (in Docker AI container)
python3 << 'EOF'
from docling.document_converter import DocumentConverter

converter = DocumentConverter()
result = converter.convert("document.docx")
print(result.document.export_to_markdown())
EOF
```

### Option 2: Download and convert with Pandoc

```bash
# Download as .docx
pandoc document.docx -t markdown -o document.md
```

**Note:** Some formatting may need manual cleanup after conversion.

### Option 3: Copy as Markdown

In Google Docs: **Edit → Copy as Markdown** (if available), then paste into your editor.

## Best practices

1. **GitHub is source of truth** — Draft and iterate in markdown, use Google Docs only for stakeholder review
2. **Version before converting** — Commit your markdown before converting to Google Docs
3. **Track changes in Docs** — Ask reviewers to use Suggesting mode so changes are visible
4. **Merge carefully** — When syncing back, review diffs to preserve intentional formatting

## Quick reference

| Task | Command |
|------|---------|
| MD → ODT | `pandoc doc.md -o doc.odt` |
| MD → DOCX | `pandoc doc.md -o doc.docx` |
| DOCX → MD | `pandoc doc.docx -t markdown -o doc.md` |
| Check Pandoc version | `pandoc --version` |

## Troubleshooting

**Headers not preserved in DOCX?**
Use ODT format instead: `pandoc doc.md -t odt -o doc.odt`

**Tables look wrong?**
Ensure tables use proper markdown syntax with `|` separators and header row divider `|---|`.

**Code blocks missing background?**
Google Docs doesn't support code block styling. Use monospace font manually if needed.
