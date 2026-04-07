# pdfonlytext, a simpler pdftext

Forked from [this repo](https://github.com/datalab-to/pdftext) because of a dependency conflict with the other projects.

Modified and simplified to fit our needs.

## Summary of modifications:

- Removed `scripts` folder.
- Removed all table functionality, since they only have table extraction, but not detection. Not useful for us.
- Removed some plain text output functionality from `extraction.py` to further simplify.
- Removed replacement of ligatures in postprocessing, it does not do anything.
- Removed settings.py, the only relevant value is `WORKER_PAGE_THRESHOLD`, so copied over to `extraction.py`.
- Integrated better font size extraction in `chars.py` suggested from [pdftext issue #24.](https://github.com/datalab-to/pdftext/issues/24)
- Used purely vertical distance in `pages.py` when checking if a line is close for block grouping, this improves block grouping and gets rid of unecessary gaps.