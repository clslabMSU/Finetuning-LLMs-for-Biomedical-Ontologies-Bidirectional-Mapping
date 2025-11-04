**From Memorization to Generalization: Fine-Tuning Large Language Models for Biomedical Term-to-Identifier Normalization**

Large language models (LLMs) show promise in biomedical term normalization, but their performance varies significantly across different terminologies. Understanding when fine-tuning leads to memorization versus generalization is crucial for effective biomedical knowledge acquisition.

In this project, we investigate fine-tuning effectiveness across three biomedical terminologies: Human Phenotype Ontology (HPO), Gene Ontology (GO), and protein-gene symbol mappings (GENE). We reveal that success depends on two key factors: **identifier popularity** (frequency in biomedical literature) and **identifier lexicalization** (semantic meaningfulness of identifiers).

When tested on frequency-balanced datasets, we observed that GO achieved substantial memorization gains (up to **77%** for term→identifier mappings), while GENE demonstrated both memorization and generalization to unseen terms (**13.9%** improvement on validation terms). HPO showed minimal gains due to low identifier popularity.

Our findings provide a predictive framework for understanding when fine-tuning will enhance factual recall and when it will fail due to low popularity or non-lexicalized identifiers.

---

## 📦 Setup

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Set up your API keys for model access:

```bash
export OPENAI_API_KEY="your-openai-api-key-here"
export TOGETHER_API_KEY="your-together-api-key-here"
```

For local fine-tuning (optional):

```bash
# Ensure CUDA is available for GPU acceleration
python -c "import torch; print(torch.cuda.is_available())"
```

---

## 📁 Repository Structure

```
datasets/    # Biomedical term-identifier datasets (HPO, GO, GENE)
notebooks/   # Jupyter notebooks for baseline evaluation and fine-tuning
results/     # Output files from baseline and fine-tuning experiments
```

---

## 📂 Scripts

"Analysisofbaseline and ft.ipynb",
"comparision graphs.ipynb",
"FT-GN-PN-8b.ipynb",
"FT-PN-GN-8b.ipynb",
"GO-CC-8B-Term-ID-FT.ipynb",
"GO-CC-70B-Term-ID-FT.ipynb",
"Gpt4.ipynb",
"HPO-8B-Term-id.ipynb",
"Llama 3.1 70b.ipynb",
"llama 8B terms to id.ipynb",
"Llama 8B.ipynb",
"Llama 70B.ipynb",
"Llama 70Bterm-id.ipynb"

---

## 📂 Data

"datasets/go_terms.csv",
"datasets/go_terms_sampled_10_per_bin_20bins.csv",
"datasets/hpo_terms.csv",
"datasets/hpo_terms_sampled_10_per_bin_20bins.csv",
"datasets/protein_name_GN.csv",
"datasets/protein_name_GN_sampled_10_per_bin_20bins.csv"

## ✅ Outputs

Example output folders:

"results/FT Llama 3.1 8b ID - term/",
"results/FT Llama 3.1 8B term - ID/",
"results/FT Llama 3.1 70 B term- ID/",
"results/Gpt Id to terms/",
"results/Gpt term to id/",
"results/Llama 3.1 8B Id to terms/",
"results/Llama 3.1 8B terms to Id/",
"results/Llama 3.1 70 B Id to terms/",
"results/Llama 3.1 70B terms to ID/"

---

## 🧠 Citation

This repository supports the findings of the published manuscript:

Pericharla S, Hier DB, Obafemi-Ajayi T. 
From Memorization to Generalization: Fine-Tuning Large Language Models for Biomedical Term-to-Identifier Normalization. 
arXiv preprint arXiv:2510.19036. 2024.
https://arxiv.org/abs/2510.19036
