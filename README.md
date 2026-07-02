# pdf2any

![python-version](https://img.shields.io/badge/python-%3E=3.10-green.svg)

**PDF to DOCX, HTML, and Markdown converter — extract text, tables, and images from PDFs.**

## Features

- Convert PDF to **DOCX** (Word documents with full formatting)
- Convert PDF to **HTML** (preserves layout, tables and images)
- Convert PDF to **Markdown** (clean, readable text with tables)
- Preserve document structure: paragraphs, tables, images, text styling
- Extract tables from PDFs
- Multi-processing support for large documents
- Command-line and Python API interfaces

## Installation

```bash
pip install pdf2any
```

## Quick Start

### Command Line

```bash
# Convert PDF to DOCX
pdf2any convert input.pdf output.docx

# Convert PDF to HTML
pdf2any convert-html input.pdf output.html

# Convert PDF to Markdown (no page breaks)
pdf2any convert-md input.pdf output.md --nopage_break

# Convert specific pages
pdf2any convert input.pdf output.docx --pages=1,3,5
```

### Python API

```python
from pdf2any import Converter

# Convert to DOCX
cv = Converter("input.pdf")
cv.convert("output.docx")

# Convert to HTML (no page breaks)
cv.convert_html("output.html", page_break=False)

# Convert to Markdown
cv.convert_md("output.md", page_break=False)

# Extract tables
tables = cv.extract_tables()
cv.close()
```

### Key Options

| Option | Description | Default |
|--------|-------------|---------|
| `--pages` | Specific pages to convert (e.g. `1,3,5`) | All |
| `--nopage_break` | Remove page separators in output | `False` |
| `--remove_header_footer` | Remove headers and footers | `False` |
| `--multi_processing` | Enable parallel processing | `False` |

## Documentation

- [Installation](https://pdf2any.readthedocs.io/en/latest/installation.html)
- [Quickstart](https://pdf2any.readthedocs.io/en/latest/quickstart.html)
  - [Convert PDF](https://pdf2any.readthedocs.io/en/latest/quickstart.convert.html)
  - [Extract table](https://pdf2any.readthedocs.io/en/latest/quickstart.table.html)
  - [Command Line Interface](https://pdf2any.readthedocs.io/en/latest/quickstart.cli.html)
- [API Documentation](https://pdf2any.readthedocs.io/en/latest/modules.html)

## License

MIT License — see [LICENSE](LICENSE) for details.
