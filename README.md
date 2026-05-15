# VICS-LLM-VulGen

**Exploring and Improving Real-World Vulnerability Data Generation via Prompting Large Language Models**

| | |
|---|---|
| Original artifact | <https://figshare.com/s/20d2cae2cda2142999cb> |
| Imported from | the publications page |
| Tool | `pubs2github` |


---

## Contents

The artifact contains 65 file(s) including Python, Config files, Data files, and Documentation.

```
├── RQ1
│   ├── exam
│   │   ├── case_studies_manual_eval_stats.py
│   │   ├── case_studies_prep.py
│   │   ├── case_studies_split.py
│   │   ├── case_studies_stats.py
│   │   ├── exam-cwe-csv3.py
│   │   ├── file_length_counter.py
│   │   ├── KappaCalculate.py
│   │   ├── remove_non_code.py
│   │   ├── summary_edit_statistics .py
│   │   └── test_persentage.py
│   ├── generated_samples
│   │   ├── claude.zip
│   │   ├── CodeLLaMa.zip
│   │   ├── COT_CVE-LLM_gpt.zip
│   │   ├── COT_dsr.zip
│   │   ├── COT_output_files_codellama_34b-instruct.zip
│   │   ├── COT_output_files_deepseek-coder_33b-instruct.zip
│   │   ├── COT_output_files_llama3_70b.zip
│   │   ├── COT_output_files_qwen2.5_32b-instruct.zip
│   │   ├── COT_output_files_v5.zip
│   │   ├── COT_SARD_gpt.zip
│   │   ├── cve_standard_claude.zip
│   │   ├── CVE_STANDARD_DSC_200.zip
│   │   ├── cve_standard_gpt.zip
│   │   ├── CVE_STANDARD_QWEN_200.zip
│   │   ├── FS_CVE-LLM_gpt.zip
│   │   ├── FS_CVE_output_files_codellama_34b-instruct.zip
│   │   ├── FS_CVE_output_files_deepseek-coder_33b-instruct.zip
│   │   ├── FS_CVE_output_files_deepseek-r1_70b.zip
│   │   ├── FS_CVE_output_files_llama3_70b.zip
│   │   ├── FS_CVE_output_files_qwen2.5_32b-instruct.zip
│   │   ├── FS_output_files_codellama_34b-instruct.zip
│   │   ├── FS_output_files_deepseek-coder_33b-instruct.zip
│   │   ├── FS_output_files_deepseek-r1_70b.zip
│   │   ├── FS_output_files_llama3_70b.zip
│   │   ├── FS_output_files_qwen2.5_32b-instruct.zip
│   │   ├── FS_SARD_gpt.zip
│   │   ├── GPT-4o.zip
│   │   ├── GPT-4o_SARD.zip
│   │   ├── LLaMa.zip
│   │   ├── sard_standard_claude.zip
│   │   ├── sard_standard_gpt.zip
│   │   └── SARD_Standard_QWEN_300.zip
│   ├── vics
│   │   ├── cwe_references.json
│   │   ├── generate_reasoning.py
│   │   ├── preposcess_vics.py
│   │   └── vics_reasoning_example.json
│   ├── generate_sample.py
│   ├── original_datasets.zip
│   └── readme.txt
├── RQ2
│   ├── divide_edit.py
│   ├── divide_sm.py
│   └── readme.txt
├── RQ3
│   ├── readme.txt
│   ├── VGX.zip
│   … (3 more items)
… (73 more items)
```

---

## Original `readme.md` (from the upstream artifact)

# Artifact for "Exploring and Improving Real-World Vulnerability Data Generation via Prompting Large Language Models"

Purpose

This artifact package contains the code, generated samples, and analysis scripts used in the paper "Exploring and Improving Real-World Vulnerability Data Generation via Prompting Large Language Models". The package is intended to (1) enable reviewers to exercise the experiments reported in the paper, (2) provide the generated vulnerability data and supporting scripts for reuse, and (3) support further analysis and comparisons.

Badge(s) claimed

- Available: This package is intended to be made available via a long-term archival repository (Figshare). Please see the `PROVENANCE` section for repository/DOI information. 
- Reusable: The artifact is organized, documented, and includes scripts to reproduce the main results. We believe it meets the ICSE Reusable criteria (careful documentation, structure to facilitate reuse). If reviewers request, we will provide a Docker image to simplify evaluation.

Provenance

- Included in this archive: the accepted paper PDF (see `_ICSE26_submission__Exploring_and_Improving_Real_World_Vulnerability_Data_Generation_via_Prompting_Large_Language_Models.pdf`) and all directories `RQ1/`..`RQ5/`, `codeql-main/`, and `generated_samples/`.
- Archival repository: [PLACEHOLDER - please replace with DOI or permanent link]. Authors will publish a DOI on Zenodo and update this README with the DOI prior to artifact registration.

Inventory of key files and directories

- `RQ1/` — sample generation, preprocessing, case studies, and statistics. Important scripts: `generate_sample.py`, `case_studies_prep.py`, `case_studies_manual_eval_stats.py`, `file_length_counter.py`, and `generated_samples/` (model output archives).
- `RQ2/` — dataset splitting and edit scripts (e.g., `divide_edit.py`, `divide_sm.py`).
- `RQ3/` — generation tool outputs and archives (e.g., `VGX.zip`, `VulGen.zip`).
- `RQ4/` — CVE-related outputs and CodeQL tool bundle (`codeql-main/`), plus `vul_trig_func_loc.csv` mapping files.
- `RQ5/` — baseline and evaluation scripts (e.g., `test_baseline_rag.py`).
- Paper PDF: `_ICSE26_submission__Exploring_and_Improving_Real_World_Vulnerability_Data_Generation_via_Prompting_Large_Language_Models.pdf` (root).
- `readme.txt` files inside each `RQ*` directory contain experiment-specific reproduction instructions and parameters.
- LICENSE: Please refer to `LICENSE` if included. If missing, reviewers should request the license file; authors recommend an Open Data / permissive software license.

Data (provenance and ethics)

- The `generated_samples/` directory contains model-generated code vulnerability samples grouped by source model and experiment. Sizes and formats vary by archive; consult the corresponding `RQ1/readme.txt` for which archive corresponds to which model/experiment.
- No raw human subject data or personally-identifiable information is included. If any third-party datasets or tools are required, the required provenance and retrieval instructions are documented in the relevant `RQ*` subdirectory.
- Ethical statement: generated data are synthetic outputs of LLMs based on public prompts. Use and redistribution should respect the terms of the original models and any third-party dataset licenses.

Setup (executable artifacts)

Hardware

- Typical experiments can be performed on a modern workstation. For model inference experiments using large models, reviewers may require GPU resources — check the `RQ*` README for model-specific hardware guidance.

Software

- Python: Python 3.8 or later is recommended.

- Core (pure-Python) dependencies (can be installed via pip):
  - numpy
  - pandas
  - tqdm
  - scikit-learn
  - matplotlib
  - requests
  - gensim
  - PyYAML (yaml)
  - easydict
  - rank_bm25
  - tokenizers
  - transformers
  - sentencepiece (optional, required by some tokenizers)
  - captum (optional; used by interpretability scripts)
  - python-igraph (may require system packages)
  - py2neo

  Example quick install for most pure-Python packages:

    pip install numpy pandas tqdm scikit-learn matplotlib requests gensim pyyaml easydict rank_bm25 tokenizers transformers sentencepiece captum python-igraph py2neo

- Deep learning / heavy dependencies (optional; required for training or model-based RQ code):
  - torch (PyTorch) — CPU-only or CUDA build depending on availability. Install PyTorch using the official instructions at https://pytorch.org/ to match your CUDA version.
  - torch_geometric (PyG) and its dependencies (torch-scatter, torch-sparse, torch-cluster, torch-spline-conv) — follow the official installation guide: https://pytorch-geometric.readthedocs.io/en/latest/notes/installation.html
  - transformers (already listed above) for model interfaces.

- External tools / system-level requirements:
  - Joern: some FVD-DPM / graph-based preprocessing scripts call Joern (joern-all). Install Joern separately (https://joern.io/) and ensure it is available in PATH or configured as required by the scripts.
  - CodeQL: the `codeql-main/` bundle requires the CodeQL CLI/toolchain for some analyses. Install CodeQL separately following GitHub / CodeQL documentation.

Notes

- Some packages (e.g., python-igraph, PyTorch Geometric, or PyG dependencies) require system libraries or specific wheel builds; follow package-specific installation instructions if pip install fails.
- If you plan to run large-model inference, use the corresponding GPU-enabled PyTorch build and ensure sufficient GPU memory.
- If a subdirectory provides a `requirements.txt`, prefer installing that (e.g., `pip install -r RQ1/requirements.txt`)

Quick installation test (basic smoke test)

1. Create a Python environment and install dependencies (see `RQ*/requirements.txt` where present).
2. From the repository root, run a basic script to confirm installation and the environment. Example (smoke test):

  - python RQ1/generate_sample.py --help

Expected result: the script prints usage information and exits without error.

Usage — reproduce core results

Follow the per-RQ instructions in `RQ*/readme.txt` to reproduce experiments. High-level steps to reproduce the major results in the paper:

1. RQ1 (Sample generation and analysis):
   - Unpack the relevant archive in `RQ1/generated_samples/` for the model(s) you want to analyze.
   - Run preprocessing scripts (for example `RQ1/remove_non_code.py`) and then the evaluation/statistics scripts (e.g., `RQ1/case_studies_manual_eval_stats.py`) as described in `RQ1/readme.txt`.
2. RQ2 (Dataset splitting / edits):
   - Use `RQ2/divide_edit.py` and `RQ2/divide_sm.py` to generate train/test splits consistent with the paper.
3. RQ3–RQ5: run the scripts listed in each folder to obtain the results corresponding to each research question. Each `readme.txt` contains detailed commands and expected outputs.

Verification and expected outputs

- Each `RQ*` README includes sample commands and expected output artifacts (CSV summaries, statistics, or zip files). Reviewers should compare produced summary statistics (e.g., vulnerability counts, length distributions) with the numbers in the paper.

Time-to-install

- The artifact is organized so that basic verification (smoke tests and running small-scale scripts) should complete within 30 minutes on a standard machine. Full-scale experiments involving large model inference may take longer and may require GPU access or pre-generated outputs included in `generated_samples/`.

How to obtain the artifact (download information)

- Archival repository: The full artifact archive (code, generated samples, paper PDF, and supporting scripts) will be published to a long-term archival repository (Figshare/Zenodo). DOI: DOI_PLACEHOLDER. The archive contains the files present in this working copy and the included paper PDF `_ICSE26_submission__Exploring_and_Improving_Real_World_Vulnerability_Data_Generation_via_Prompting_Large_Language_Models.pdf`.



Package checklist (recommended for quick evaluation)

1. Confirm you can download and unpack the archive from the DOI link.
2. Verify the included paper PDF is present and matches the repository contents.
3. Follow the per-RQ `readme.txt` commands for a smoke test (e.g., `python RQ1/generate_sample.py --help`) and confirm expected outputs described in each `RQ*` README.
4. For heavy-model experiments, use the provided pre-generated outputs in `generated_samples/` to validate analysis scripts if GPU resources are restricted.
5. If requested, the authors will provide a Docker image containing a validated runtime environment to speed evaluation.

Contact and support during review

- For general inquiries, contact the authors listed in the paper.

License

- This artifact is released under the MIT License. See the included `LICENSE` file for the full text.

Citation

ACM Reference Format:
Guangbei Yi, Yu Nong, Minzhang Li, and Haipeng Cai. 2026. Exploring and Improving Real-World Vulnerability Data Generation via Prompting Large Language Models. In 2026 IEEE/ACM 48th International Conference on Software Engineering (ICSE ’26), April 12–18, 2026, Rio de Janeiro, Brazil. ACM, New York, NY, USA, 13 pages. https://doi.org/10.1145/3744916.3773176

Acknowledgments

- This README and artifact structure follow the ICSE 2026 Artifact Evaluation guidelines. We thank the artifact reviewers in advance; please consult per-RQ `readme.txt` files for precise commands and dependency details. The authors will provide additional materials (Docker image, updated requirements, or license) on request during the review window.
