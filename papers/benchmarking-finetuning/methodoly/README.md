# Methodology revision package

## Purpose

This package provides a source-controlled English LaTeX replacement for the Methodology section of the benchmark manuscript. The methodology is grounded in the current source code, Engram records, retained evaluation outputs, and dataset artifacts.

## Integration steps

1. Replace the manuscript's current Methodology section with the contents of `methodology.tex`.
2. Merge the entries in `references.bib` into the manuscript bibliography, preserving the citation keys used by the fragment.
3. Compile the target manuscript with its existing LaTeX and bibliography workflow.
4. For any future rerun, record the exact source revisions, dataset or model revisions, configuration, and commands used so that the resulting outputs and evaluations remain reproducible.

## Evidence boundaries

The fragment reports the four retained fine-tuning evaluation conditions, each with 328 test outputs, using the grounded `sft_grounded` test variant and the documented inference and evaluation protocol. The reported evaluation-error counts are metric-evaluation records in retained summaries, not missing model predictions. The benchmark is an offline descriptive comparison, not clinical validation, expert validation, patient-outcome assessment, deployment evidence, or decision-support evidence.

Auxiliary retrieval augmentation is distinct from grounded supervised fine-tuning. The repository's `no_rag`, Hybrid BM25+dense retrieval with reciprocal-rank fusion, and independent HyDE protocols should be reported only when their corresponding artifacts are available. The four retained fine-tuning summaries are not RAG results. No unsubstantiated lexical metrics, exact-match metrics, or auxiliary RAG results are reported.
