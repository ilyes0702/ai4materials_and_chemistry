---
task_categories:
- tabular-regression
language:
- en
tags:
- physics
- chemistry
- materials
- ASE
- Perovskites
pretty_name: AI4Materials Demo FAIR Perovskites
license: mit
---

# AI4Materials Demo FAIR Perovskites

This is a **teaching** dataset demonstrating F.A.I.R. hosting on the Hugging Face Hub.  
It contains a small table of oxide perovskites with band gaps and toy EXTXYZ structures.

## Contents
- `data/table.csv` — main tabular data  
- `data/records.jsonl` — line-delimited JSON mirror  
- `data/structures/*.xyz` — example structures (EXTXYZ)  
- `metadata/schema.json` — JSON Schema for validation  
- `CITATION.cff`, `LICENSE` — citation & reuse terms

## Provenance
Synthetic examples generated for classroom demonstration on {datetime.utcnow().date()}.

## How to load
```python
from datasets import load_dataset
ds = load_dataset("cparidaAI/fair_dataset_demo", data_files={"train": "data/table.csv"})
print(ds)
```
Or download a structure file:
```python
from huggingface_hub import hf_hub_download
path = hf_hub_download(repo_id="cparidaAI/fair_dataset_demo", filename="data/structures/ABO3_0001.xyz")
```

## License
MIT. Please cite using `CITATION.cff`.

## F.A.I.R. checklist
- **F**indable: metadata, tags, README, (add DOI later via Zenodo)  
- **A**ccessible: public repo, open formats  
- **I**nteroperable: CSV/JSON/EXTXYZ, schema describes fields/units  
- **R**eusable: license, clear citation, validation, examples
