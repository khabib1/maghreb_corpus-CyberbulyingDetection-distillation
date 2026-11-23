# maghreb_corpus-CyberbulyingDetection-distillation
Official implementation for reproducing the unified Maghrebi dataset and distilling the student model from five Arabic/Maghrebi teacher transformers (**DziriBERT**, **DarijaBERT**, **TunBERT**, **MARBERT**, **AraBERT**).

## 1. Data Reconstruction
To comply with upstream dataset licenses, raw merged text files are not hosted here. Download the three original datasets directly from their official sources:
- **AlgD** (Algerian): [Zenodo](https://zenodo.org/records/10937445) *(CC BY 4.0)*
- **OMCD** (Moroccan): [GitHub](https://github.com/kabilessefar/OMCD-Offensive-Moroccan-Comments-Dataset) *(CC BY 4.0)*
- **T-HSAB** (Tunisian): [GitHub](https://github.com/Hala-Mulki/T-HSAB-A-Tunisian-Hate-Speech-and-Abusive-Dataset) *(Academic/Research use)*

Place the downloaded files in `data/raw/` and run:
```bash
python merge_datasets.py --input_dir data/raw --output_dir data/processed
