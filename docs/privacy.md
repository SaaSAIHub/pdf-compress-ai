# Local PDF processing and privacy

[Back to the README](../README.md)

## Where your PDF is processed

When you select a PDF in [PDF-Compress.ai](https://pdf-compress.ai/), the browser reads the file on your device. The compression workflow processes the PDF locally and creates the downloadable output in the browser.

The current workflow does not upload selected PDFs to PDF-Compress.ai servers for compression or create a server-side PDF task history.

Selected files and results can remain in browser memory while the page is open. Downloaded files are saved wherever your browser and operating system normally save downloads. Local processing does not control copies made by your operating system, browser extensions, backups, or cloud-synced download folders.

## Why the website still uses the network

The browser needs to load the website and its processing code and assets. The production site also uses Google Analytics 4, and hosting or CDN services may keep ordinary technical request logs.

The published Privacy Policy distinguishes these requests from PDF processing:

- PDF contents and filenames are not sent to Google Analytics by the compression workflow.
- Usage events can include the chosen compression mode, file count, completion count, download action, and error category.
- Standard website analytics and technical logs can include device or browser information, referring pages, and request metadata.

For the full description of data practices, choices, and contact information, read the website's [Privacy Policy](https://pdf-compress.ai/privacy-policy). This guide explains the workflow and does not replace that policy.

## Inspect the workflow yourself

If you want to inspect the browser's network activity, use a synthetic PDF containing no private information:

1. Open the browser's developer tools and select the Network panel before loading the website.
2. Load the page, select the test PDF, and run compression.
3. Inspect the requests, their destinations, and their request payloads. Distinguish website assets and usage events from any transmission of document data.
4. Record the browser version and date if you report an unexpected request.

A single network inspection covers that session and is not an independent security audit. Do not publish raw network logs without reviewing them for identifiers or other sensitive information.

## Keep public feedback separate from private documents

Use the [FeedLog feedback portal](https://pdf-compress-ai.feedlog.ai/) for product questions and bug reports. Do not include confidential PDFs or personal information in feedback posts or attachments. Describing a file's general structure, approximate size, and page count is usually enough to start a report. Share a synthetic example when possible.

For privacy questions, use the contact method in the website's Privacy Policy rather than posting personal information in a feedback request.
