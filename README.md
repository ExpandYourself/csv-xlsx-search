# CSV & XLSX Search

Browser-based search tools for CSV and Excel files. No server, no upload — everything runs locally in your browser.

<!-- ![CSV Search](screenshots/csv-search.png) -->
<!-- ![XLSX Search](screenshots/xlsx-search.png) -->

## Tools

### CSV Search
Search across multiple CSV files simultaneously.

- **Configurable delimiter** — comma or semicolon, switchable at any time (useful for European CSV formats that use `;` as separator)
- Reload files on-the-fly when switching delimiters

### XLSX Search
Search across Excel files (.xlsx, .xls, .xlsm, .xlsb, .ods). Powered by [SheetJS](https://sheetjs.com/).

- Automatically parses **all sheets** in each workbook
- Each sheet appears as a separate entry in the search scope

## Features

Both tools share the same feature set:

- **Multi-file support** — load and search across multiple files at once
- **File/sheet selection** — choose which files or sheets to include in the search
- **Match types** — partial match, exact match, or wildcard patterns
- **Wildcard syntax** — asterisk style (`*`, `?`) or SQL style (`%`, `_`)
- **Multiple search terms** — comma-separated, combined with AND or OR
- **Row-wide search** — search terms can match across different columns in the same row, with all matched columns shown in the results
- **Case sensitivity** — toggle case-sensitive matching
- **Auto-search** — results update as you type (with debounce)
- **Pagination** — configurable rows per page (100 / 250 / 500 / 1000)
- **CSV export** — export search results with selectable columns
- **Privacy** — all processing happens in the browser, no data leaves your machine

## Usage

### Option 1: GitHub Pages
Visit the hosted version: **https://expandyourself.github.io/csv-xlsx-search/**

### Option 2: Download
1. Download the HTML file you need (`csv-search.html` or `xlsx-search.html`)
2. Open it in any modern browser
3. Load your files and search

That's it. No install, no dependencies, no build step.

## Row-Wide Search

The **Search Scope** dropdown lets you switch between two modes:

- **Cell** (default) — each search term is matched per cell. With AND, all terms must appear in the same cell.
- **Row** — search terms are matched across the entire row. With AND, each term must appear somewhere in the row, but they can be in different columns. The results show which columns matched.

This is useful for queries like "find rows where Name contains 'Smith' AND Department contains 'Engineering'" — the terms don't need to be in the same cell.

## License

[MIT](LICENSE)
