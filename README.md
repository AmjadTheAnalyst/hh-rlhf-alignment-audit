# HH-RLHF Alignment Audit

**What Binary Preference Labels Leave Out in AI Alignment** is a secondary-data research project by Muhammad Amjad. It examines value trade-offs, factual confidence, stakeholder context, and review triage in Anthropic HH-RLHF preference pairs.

**Repository status:** Initial implementation. The notebook is unexecuted. Study results and the archival release are pending completion of the independent annotations and the final run.

## Quick start

1. Open `HH_RLHF_Alignment_Audit.ipynb` in Kaggle or Jupyter with Python 3.11 or later. Install `requirements.txt` if the runtime lacks these dependencies.
2. Enable Internet access or attach the four public [HH-RLHF archives](https://huggingface.co/datasets/Anthropic/hh-rlhf). For offline access, point `RAW` to a folder containing `helpful-base/{train,test}.jsonl.gz` and `harmless-base/{train,test}.jsonl.gz`. Pin `REVISION` to the source commit for the final run.
3. Run a private preparation session to create the seeded sample, blinded reviewer packets, and CSV templates. Complete the independent annotations according to the notebook schema and point `ANNOTATIONS` to the private input folder.
4. Run the notebook from top to bottom. The final cell creates `hh_rlhf_results.zip` with aggregate figures, tables, provenance, and the run status. With complete inputs, the planned outputs are 10 PDF figures and 10 CSV tables. For local Jupyter, set `WORK` to a dedicated writable directory.

## Research context

- Target journal: [Ethics and Information Technology](https://link.springer.com/journal/10676)
- Reference study: [Dahlgren Lindström et al. (2025)](https://doi.org/10.1007/s10676-025-09837-2)
- Cite the software using `CITATION.cff`. Final study artifacts can be added to a versioned release after validation.

Keep raw dialogues, blinded reviewer packets, annotation inputs, and credentials in private working directories. The public release is intended for aggregate results and reproducibility materials.
