# How to run a reproducible PDF compression test

[Back to the README](../README.md)

This guide is a test method, not a published benchmark. It contains no measured compression results or claims that one product outperforms another.

## Select representative documents

Use PDFs that you created or are allowed to redistribute. A useful small set includes:

- A mostly text-based report.
- A scanned document with high-resolution page images.
- A presentation or brochure with photographs and diagrams.
- A PDF that has already been optimized.

If you publish the samples, include their source and redistribution terms. Use synthetic content rather than real application forms, invoices, contracts, or identity documents.

## Record the environment

Record the test date, tool URL, browser version, operating system, device model, and available memory where known. Record each sample's page count, original byte size, and SHA-256 hash so another person can identify the same input.

For timing, say whether you included the initial loading of the compression engine. An initial run and a run with assets already loaded measure different things.

## Run each mode from the original

Run Light, Balanced, and Strong independently from the same original PDF. Do not feed one mode's output into another mode.

For a timing comparison, run each case three times under the same conditions and report the median. Record failures, unchanged outputs, and files preserved because of a digital signature; do not silently remove them from the results.

If comparing multiple tools, state the settings used for each. Similarly named modes are not necessarily equivalent. Check whether the output preserves the document features needed for your use case before comparing size alone.

## Check both size and usability

Calculate size reduction as:

```text
reduction_percent = (original_bytes - output_bytes) / original_bytes * 100
```

Use the same units throughout. Byte counts avoid ambiguity between decimal MB and binary MiB.

Inspect the same pages and regions at the same zoom level. Include small scanned text, image detail, line charts, and any forms or links. Check text search where the input already has searchable text. Do not use compression percentage as a substitute for visual or functional review.

## Suggested result columns

```text
sample_id, input_sha256, pages, original_bytes, tool, mode,
output_bytes, reduction_percent, median_elapsed_ms, status,
text_search_check, visual_notes, feature_notes, browser, os, test_date
```

Describe how each check was performed. If you did not check a feature, mark it as not tested. Avoid presenting a small sample set as a guarantee for all PDFs.

For results you want other people to cite, publish the method, sample sources, settings, failures, and limitations alongside the numbers. Link to the exact report rather than only to a product homepage.
