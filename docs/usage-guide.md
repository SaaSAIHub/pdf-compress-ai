# Using PDF-Compress.ai

[Back to the README](../README.md)

## Start with a copy of your PDF

Open [PDF-Compress.ai](https://pdf-compress.ai/) in a modern browser. Keep the original document so you can compare it with the compressed result.

Select or drop up to 10 PDFs. The selection limit is 1GB per file. This is a file-selection limit: successful processing also depends on your browser, available device memory, and the contents of each PDF.

## Pick the mode that fits your document

- **Light:** choose this when preserving image detail is the priority. It optimizes PDF structure without re-encoding images, so the size reduction can be small.
- **Balanced:** start here for everyday reports, attachments, and application documents. It can reduce image quality to save space.
- **Strong:** try this for large image-heavy files when Balanced is not small enough. Review small text in scans, charts, and photographs for lost detail.

Run each comparison from the original PDF. Repeatedly compressing an already compressed result makes it harder to judge the trade-off and may reduce image quality further.

## Process and download

Start compression and leave the page open. Processing runs locally, so larger files can use substantial CPU time and memory. Download the result when it is ready.

Open the downloaded PDF and check:

- Page count, orientation, and layout.
- Small text, diagrams, and image detail.
- Existing text search and selection.
- Any links, forms, bookmarks, or annotations you rely on.
- The final file size against the destination's attachment or upload limit.

An image-only scan remains image-only unless it already has an OCR text layer. This tool does not add OCR.

## Work with batches and large files

Batch selection accepts up to 10 PDFs, but a smaller batch may be more practical on a phone or a device with limited memory. For a large document, start with one file, close unneeded tabs, and keep the browser in the foreground.

If processing runs out of memory, retry with a smaller file or a device with more available memory. Light may reduce image-processing work, but even Light is not guaranteed to handle every large PDF.

## Troubleshooting

| What you see | What it can mean | What to try |
| --- | --- | --- |
| No smaller result was found | The document may already be optimized, or its contents offer little room for reduction. | Keep the original. If you used Light, compare Balanced or Strong against the original. |
| Images look less clear | Image optimization traded detail for a smaller file. | Start again from the original and choose Light or Balanced. |
| Processing fails on a large file | Browser memory or PDF complexity may be a constraint. | Try a single file, fewer open tabs, or a device with more memory. |
| A password-related error appears | The PDF requires a password to open. | If you are authorized to do so, create an unlocked copy in your PDF editor and compress that copy. |
| The original is preserved for a digital signature | The tool detected a signature and returned the original instead of rewriting it. | Keep the signed original. For a smaller version, compress an unsigned copy before it is signed. |
| The result still exceeds an upload limit | A compression level cannot guarantee a particular output size. | Try Strong and review the result, or reduce source images and export a new PDF from the original application. |
| The compression engine cannot load | A network problem or content filter may have blocked a required website asset. | Reload and check whether the required assets are available on your network. |

The tool does not promise compatibility with every PDF feature. For documents where signatures, forms, accessibility data, or archival requirements matter, review the output in the software used by the recipient.

## Report a reproducible problem

Use the [bug report form](https://github.com/SaaSAIHub/pdf-compress-ai/issues/new?template=bug_report.yml). Include the compression mode, browser and operating system, approximate file size and page count, steps to reproduce, and the message shown by the tool.

Do not post confidential documents. A synthetic sample that reproduces the same behavior is more useful than a screenshot containing private information. See [contributing](../CONTRIBUTING.md).
