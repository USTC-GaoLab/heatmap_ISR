# Repository structure audit

Repository:

`heatmap_ISR`

Current structure:

- One extensionless R workflow (`GY-HH`) was stored at repository root.
- Review and structure documents were stored at root.
- No notebooks, raw data, generated results, or files larger than 50 MB were found.

Problems:

- The scientific script was not identifiable by extension and was outside a code directory.
- The script contains a hard-coded source-machine working directory.
- Environment and license files were missing.

Recommended structure:

```text
R/
examples/
docs/
```

Migration actions:

- Moved `GY-HH` to `R/GY-HH` with `git mv`; scientific contents were not edited.
- Moved review documents to `docs/` with `git mv`.
- Added an examples placeholder, environment record, license and audit.
- Kept raw data and generated results outside the repository.
