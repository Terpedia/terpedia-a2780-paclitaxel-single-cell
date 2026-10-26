# A2780 paclitaxel single-cell report

This public Terpedia research project analyzes [GEO GSE162256](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE162256), a chemical-exposure single-cell study of A2780 cells. Paclitaxel is a taxane diterpenoid. The analysis is descriptive: cells are not independent biological replicates, and this study is not genetic Perturb-seq.

- [Executed Jupyter notebook](notebooks/terputer-gse162256-single-cell.ipynb)
- [Claim-linked white paper](research/a2780-paclitaxel-single-cell/generated/white-paper.md)
- [Claim ledger](research/a2780-paclitaxel-single-cell/generated/claim-ledger.tsv)
- [Pinned input and methods](research/transcriptomics/gse162256/README.md)
- [Marker results](research/transcriptomics/gse162256/results/marker_descriptive.tsv)
- [Feature-wide background](research/transcriptomics/gse162256/results/background_descriptive.tsv)

The notebook downloads the 5.8 MB GEO processed matrix on demand and verifies its SHA-256. Run it from the repository root using a Jupyter Python kernel with pandas, or use Terputer's `notebook-runner.py`. The recorded run used Python 3.11, pandas 2.3.3, nbformat 5.10.4, and nbclient 0.10.2. After a fresh run, regenerate the evidence brief with:

```sh
node report-generator.mjs research/transcriptomics/gse162256/report-spec.json
```

To attach this example to your own `terpedia-report` Codespace, fork this repository into your GitHub account with the same repository name, then call `add_research_project_submodule` with slug `a2780-paclitaxel-single-cell`. Terputer's attachment tools require the project repository to belong to the linked account.

A fresh run updates notebook and artifact hashes, so regenerate the report only after producing a matching execution receipt. The current report, ledger, and receipts refer to the committed notebook and result files. Most baseline-detected features also shift lower after paclitaxel in this matrix, so lower cell-cycle marker medians alone do not establish a specific program. The result does not establish a replicated pathway, a controlled cell-context interaction, or a paclitaxel target dependency.
