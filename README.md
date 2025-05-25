# Book Manuscript Project

This project is a structured book manuscript, organized for easy writing, editing, and exporting using [Pandoc](https://pandoc.org/). The manuscript is divided into chapters, each as a directory containing markdown files. The project is designed for seamless export to DOCX or PDF formats.

## Project Structure

```
book-manuscript/
├── book/
│   ├── chapter-01/
│   │   ├── 01-introduction.md
│   │   └── 02-background.md
│   ├── chapter-02/
│   │   ├── 01-main-topic.md
│   │   └── 02-details.md
│   └── ...
├── README.md
└── ...
```

- Each `chapter-XX` directory contains logically grouped markdown files.
- File names are prefixed with numbers to control order during export.

## Writing Guidelines

- Use standard Markdown syntax.
- For headings, use `#` for chapter titles and `##`, `###`, etc. for sections and subsections.
- To insert page breaks (for export), use:
  ```
  \newpage
  ```
- For images, use relative paths and place image files in an `images/` directory if needed.
- For references, citations, and footnotes, use Pandoc-compatible markdown.

## Exporting the Manuscript

### Prerequisites
- [Pandoc](https://pandoc.org/) must be installed.
- For PDF export: LaTeX distribution (e.g., TeX Live or MikTeX) is required.

### Example Export Commands

To export the entire manuscript, concatenate the markdown files in order and run Pandoc:

```sh
# Example: Export to DOCX
pandoc book/chapter-*/**/*.md -o manuscript.docx

# Example: Export to PDF
pandoc book/chapter-*/**/*.md -o manuscript.pdf
```

- Adjust the glob pattern as needed depending on your shell (e.g., use `cat` to concatenate files if needed).
- You can specify a custom template, cover page, or metadata file with Pandoc options.

### Useful Pandoc Options
- `--toc` : Add a table of contents
- `--metadata title="Book Title"` : Set the document title
- `--template=template.tex` : Use a custom LaTeX template for PDF

## Tips
- Keep chapters and sections in separate files for easier management.
- Use consistent heading levels for best export results.
- Test export early to catch formatting issues.

---

Happy writing! For more details, see the [Pandoc documentation](https://pandoc.org/MANUAL.html).
