# Book Manuscript Repository

Welcome! This repository is for collaborative book manuscript projects, organized for easy writing, editing, and exporting using [Pandoc](https://pandoc.org/). Each book is kept in its own directory and follows a clear folder structure for chapters, images, and documentation.

## Repository Structure

```
book-manuscript/
├── righteousness-is-a-strategy/
│   ├── chapter-01/
│   │   └── 01-introduction.md
│   ├── images/
│   │   └── .gitkeep
│   ├── docs/
│   │   └── README.md
│   └── metadata.yaml
├── README.md
└── ...
```

- Each book has its own folder (e.g., `righteousness-is-a-strategy/`).
- Chapters are organized in numbered subfolders (e.g., `chapter-01/`).
- Images for each book go in the `images/` folder.
- Documentation, plans, and notes for each book go in the `docs/` folder.
- Metadata for Pandoc export is in `metadata.yaml`.

## How to Add a New Book

1. Create a new folder at the root with your book's name (use dashes, e.g., `my-new-book`).
2. Inside your book folder, create:
   - `chapter-01/` (and more as needed)
   - `images/` (for figures, cover art, etc.)
   - `docs/` (for plans, ideas, issues, etc.)
   - `metadata.yaml` (set `title`, `author`, and `date`)
3. Start your first chapter as `chapter-01/01-introduction.md`.

## Writing Guidelines

- Use standard Markdown syntax.
- For headings, use `#` for chapter titles and `##`, `###`, etc. for sections and subsections.
- To insert page breaks (for export), use:
  ```
  \newpage
  ```
- For images, use relative paths and place image files in the `images/` directory.
- For references, citations, and footnotes, use Pandoc-compatible markdown.

## Exporting a Book

From inside the book's folder, run:

```sh
pandoc chapter-*/**/*.md -o manuscript.docx --metadata-file=metadata.yaml
```

Or for PDF:

```sh
pandoc chapter-*/**/*.md -o manuscript.pdf --metadata-file=metadata.yaml
```

- Requires [Pandoc](https://pandoc.org/) and (for PDF) a LaTeX distribution.
- You can add options like `--toc` for a table of contents, or use a custom template.

## About the `docs/` Folder

Each book has a `docs/` folder for:
- `plans.md` — Outline your writing plan, chapter goals, and timeline.
- `ideas.md` — Collect new ideas and inspiration.
- `issues.md` — Track open questions or problems.

## Collaboration Guidelines

- Use branches or pull requests for major changes.
- Document your ideas, plans, and issues in the `docs/` folder.
- Keep chapters and sections in separate files for easy review.
- Test Pandoc exports early to catch formatting issues.

---

Happy writing! For more details, see the [Pandoc documentation](https://pandoc.org/MANUAL.html).

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
