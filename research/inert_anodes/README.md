# Condensed research archive

## Contents
- DIGEST.md and digests/: extractive abstracts, summaries and conclusions with source page numbers. Verbatim source-page excerpts selected automatically, not independently verified analytical summaries.
- text/: full extractable text from every source PDF, separated by original PDF page number. Equations, columns and tables may have extraction artifacts.
- figures/: digital visual-region crops in WebP format, with an HTML gallery for each document. Open index.html in a browser.
- figure_table_index.csv: automatic caption candidates and links to document galleries. May contain in-text mentions and miss scanned captions.
- visual_regions.json: original PDF page and bounding box for every image crop.
- manifest.json: original filenames, page counts, checksums, and low-text pages.

## Scope and limitations
Original PDFs are omitted to meet the size limit; original archives remain unchanged. All source documents have text files. Figures are automatically detected from raster images and vector drawing regions, with padding to capture adjacent labels. Crops may contain tables, equations or text; detection and grouping are not guaranteed complete. Sparse-text pages are preserved as full-page images, without OCR. Text-only tables remain in the text extracts; formatting may be lost.

Figures are preserved as digital images, NOT converted to validated numeric x-y datasets. No chart values have been invented. Use original PDFs for exact typography, high-resolution microscopy, uncertain symbols, missing labels, or quantitative curve digitization. Digests retain source wording and may include surrounding page text.
