<div align="center">

# 🧬 HemoPI-MOD2

**Prediction of Hemolytic Potency (HC50) & Design of Chemically Modified Peptides**

[![Web Server](https://img.shields.io/badge/Web%20Server-IIIT--Delhi-blue?style=for-the-badge&logo=google-chrome)](https://webs.iiitd.edu.in/raghava/hemopimod2)
[![Open In Colab](https://img.shields.io/badge/Colab-Open%20Demo-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/github/raghavagps/HemoPImod2/blob/main/HemoPIMOD2_Demo.ipynb)
[![PyPI](https://img.shields.io/badge/PyPI-hemopimod2-3775A9?style=for-the-badge&logo=pypi&logoColor=white)](https://pypi.org/project/hemopimod2/)
[![Anaconda](https://img.shields.io/badge/Anaconda-drv01%2Fhemopimod2-44A833?style=for-the-badge&logo=anaconda&logoColor=white)](https://anaconda.org/channels/drv01/packages/hemopimod2/overview)
[![Docker](https://img.shields.io/badge/Docker-drv01%2Fhemopimod2-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/repository/docker/drv01/hemopimod2/general)
[![Zenodo](https://img.shields.io/badge/Zenodo-Archive%20(Coming%20Soon)-024CAD?style=for-the-badge&logo=zenodo&logoColor=white)](#zenodo)

</div>

---

## 📚 Reference
> **Rathore AS et al.** *HemoPI-MOD2: Prediction of Hemolytic Potency (HC50) of Chemically Modified Peptides.* **#Coming Soon#**

---

## 📌 Introduction

**HemoPI-MOD2** is developed to help researchers estimate the hemolytic activity of peptides before synthesis. It predicts **$\text{HC}_{50}$**, the concentration causing 50% hemolysis, as a continuous regression value rather than a bare hemolytic/non-hemolytic call, so analogues can be quantitatively ranked against each other.

Modified peptides are first-class input: N-terminal acetylation, C-terminal amidation, head-to-tail cyclization, D-amino acids, and non-natural residues are all expressed in **MAP notation** and directly utilized by the models.

Three complementary models are offered—each taking a distinct view of the peptide—alongside a **Design** module that enumerates and scores every single-residue analogue of a lead candidate.

- 🔗 **Web Server:** [https://webs.iiitd.edu.in/raghava/hemopimod2](https://webs.iiitd.edu.in/raghava/hemopimod2)
- 📖 **Citation:** Please cite the publication above for complete details, including the underlying algorithms.

### Zenodo
[![Zenodo](https://img.shields.io/badge/Zenodo-Coming%20Soon-024CAD?style=flat-square&logo=zenodo&logoColor=white)](#zenodo) *Coming soon...*

---

## 🌐 Available Platforms & Distribution Channels

Access **HemoPI-MOD2** across multiple platforms depending on your workflow:

| Platform | Best For | Link / Quick Command |
| :--- | :--- | :--- |
| 🌐 **Web Server** | Interactive browser-based prediction & design (no installation) | [webs.iiitd.edu.in/raghava/hemopimod2](https://webs.iiitd.edu.in/raghava/hemopimod2) |
| ☁️ **Google Colab** | Zero-setup cloud notebook demo & batch execution | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/raghavagps/HemoPImod2/blob/main/HemoPIMOD2_Demo.ipynb) |
| 📦 **PyPI Package** | Fast command-line installation (`hemopimod2`) | [`pip install hemopimod2`](https://pypi.org/project/hemopimod2/) |
| 🐍 **Anaconda** | Conda-based environment & package management | [`conda install drv01::hemopimod2`](https://anaconda.org/channels/drv01/packages/hemopimod2/overview) |
| 🐳 **Docker Hub** | Containerized execution on Linux / macOS / Windows | [`docker pull drv01/hemopimod2:latest`](https://hub.docker.com/repository/docker/drv01/hemopimod2/general) |
| 🏛️ **Zenodo** | Permanent archival release & dataset snapshot | *Coming soon...* |

---

### 🖼️ HemoPI-MOD2 Workflow Representation

<div align="center">
  <img src="data/Figure1.jpg" alt="HemoPI-MOD2 Workflow" width="85%">
</div>

---

## 🧪 Quick Start

```bash
# 1. Clone or unpack the standalone repository
git clone https://github.com/raghavagps/HemoPImod2.git
cd hemopimod2

# 2. Set up the environment (conda recommended)
conda env create -f environment.yml
conda activate HemoPI-MOD2

# 3. View all available CLI options
python HemoPI_MOD2.py -h

# 4. Run prediction on the sample input
python HemoPI_MOD2.py -i example_sequence.fasta -o output.csv -j 1 -m 1

# 5. Design all single-residue analogues of a lead peptide
python HemoPI_MOD2.py -i example_design.fasta -o design.csv -j 2 -m 1
```

> The three pre-trained model files are already included in `models/`; no external weight downloads are required.

---

## 🛠️ Installation Options

### 🧰 Pip Installation <img src="data/PyPI_logo.svg.png" alt="PyPI Logo" width="24" align="absmiddle">

Install **HemoPI-MOD2** directly from PyPI:
```bash
pip install hemopimod2
```
Verify the installation and view available flags:
```bash
hemopimod2 -h
```

---

### 🐍 Anaconda Installation

Install **HemoPI-MOD2** via Conda from Anaconda Cloud:
```bash
conda install drv01::hemopimod2
```
Or create an isolated environment using the repository's `environment.yml`:
```bash
conda env create -f environment.yml
conda activate HemoPI-MOD2
```

---

### 🐳 Docker Installation

Pull and run the pre-built container image from Docker Hub:
```bash
docker pull drv01/hemopimod2:latest

docker run --rm -v $(pwd):/data drv01/hemopimod2:latest -i /data/example_sequence.fasta -o /data/output.csv -j 1 -m 1
```

---

### ☁️ Google Colab (No Local Installation)

Run the complete **HemoPI-MOD2** interactive demo notebook directly in your browser on free cloud compute:
- 👉 **[Open HemoPI-MOD2 Demo in Google Colab](https://colab.research.google.com/github/raghavagps/HemoPImod2/blob/main/HemoPIMOD2_Demo.ipynb)**

---

### 🔹 Standalone Installation (via `pip`)

**HemoPI-MOD2** is written in **Python 3** (`>=3.9`) and requires the following core libraries:

```bash
pip install scikit-learn==1.6.1
pip install xgboost==3.2.0
pip install "numpy>=1.23,<2.0"
pip install pandas
pip install joblib
```

Additional dependencies required **only** for the Chemical (`-m 2`) and Structure (`-m 3`) models:

```bash
pip install rdkit
pip install mordred==1.2.0
pip install "networkx>=2.8,<3.0"
```

Or install all dependencies at once:

```bash
pip install -r requirements.txt
```

---

## ⚠️ Important Notes

- **Pinned Versions:** `scikit-learn` (`1.6.1`) and `xgboost` (`3.2.0`) are pinned intentionally. The serialized models in `models/` were trained with these exact versions; newer or older releases may load, but are not guaranteed to reproduce published predictions.
- **Lightweight Sequence Mode:** The Sequence (`-m 1`) and Design (`-j 2`) modules run **without** RDKit or Mordred. You only need those libraries if running Chemical (`-m 2`) or Structure (`-m 3`) predictions.

---

## 🔬 Prediction Overview

**HemoPI-MOD2** predicts **$\text{pHC}_{50}$** and reports **$\text{HC}_{50}$ in $\mu\text{M}$**, where:

$$\text{HC}_{50} = 10^{-\text{pHC}_{50}}$$

- **Higher $\text{HC}_{50}$** $\rightarrow$ **Less hemolytic** (safer therapeutic profile).
- **Cut-off:** By established convention, peptides with $\text{HC}_{50} > 100\ \mu\text{M}$ are classified as **Non-hemolytic**.

🔹 **Available Models**
- **Model 1 — Sequence (MAP):** Amino acid composition + modification tags + D/L stereochemistry counts.
- **Model 2 — Chemical (SMILES):** 2D molecular descriptors computed via Mordred.
- **Model 3 — Structure (PDB):** 2D molecular descriptors extracted from 3D PDB structures.

---

## 🚀 Usage

### 🔹 Minimum Usage

```bash
python HemoPI_MOD2.py -h
```

Run a default prediction:

```bash
python HemoPI_MOD2.py -i example_sequence.fasta
```

### 🔹 Full Usage

```text
usage: HemoPI_MOD2.py [-h]
                      -i INPUT
                      [-o OUTPUT]
                      [-j {1,2}]
                      [-m {1,2,3}]
                      [-d {1,2}]
                      [-wd WORKING_DIRECTORY]
```

#### CLI Arguments

| Argument | Description |
| :--- | :--- |
| **`-i INPUT`** | Input file: peptide sequence in MAP/FASTA format (or one sequence per line); SMILES file for Chemical model (`-m 2`); a `.pdb` file or directory of `.pdb` files for Structure model (`-m 3`). |
| **`-o OUTPUT`** | Output CSV filename (default: `output.csv`). |
| **`-j {1,2}`** | Job type: `1` = Prediction (default), `2` = Design all possible single-residue mutants. |
| **`-m {1,2,3}`** | Model selection: `1` = Sequence (MAP), `2` = Chemical (SMILES), `3` = Structure (PDB). |
| **`-d {1,2}`** | Screen display filter: `1` = Hemolytic peptides only, `2` = All peptides (default: `2`). |
| **`-wd WORKING`** | Custom working directory for saving results. |

> **Note:** Job type `1` (Prediction) works with all three models (`-m 1, 2, 3`). Job type `2` (Design) operates exclusively with the Sequence model (`-m 1`). The `-d` flag controls terminal output only—the saved CSV file always contains all input entries.

---

## 📂 Input & Output Files

### ✅ Input File Format

**1. FASTA / MAP Format** (e.g., `example_sequence.fasta`)  
Chemical modifications are written in **MAP notation** using curly braces alongside standard single-letter amino acid codes:

| Tag | Meaning |
| :--- | :--- |
| **`{nt:Acet}`** | N-terminal acetylation (placed before the first residue) |
| **`{ct:Amid}`** | C-terminal amidation (placed after the last residue) |
| **`{cyc:N-C}`** | Head-to-tail backbone cyclization (placed at the start) |
| **`{d}`** | Indicates the preceding residue is a D-enantiomer |
| **`{nnr:orn}`** | Non-natural residue occupying one chain position |

```fasta
>example
{nt:Acet}KWKLFKKIL{ct:Amid}
```

**2. SMILES Format** (`-m 2`, e.g., `example_smiles.txt`)  
One SMILES string per line (or FASTA/MAP sequences, which are automatically converted via `stitch.py`).

**3. Structure Format** (`-m 3`, e.g., `example_structure.pdb`)  
Provide either a single `.pdb` file or a directory containing multiple `.pdb` files; each entry's ID is derived from its filename.

---

### ✅ Output File Format

Results are saved in **CSV format** (`output.csv` by default).

#### Prediction Output (`-j 1`)

| Column | Meaning |
| :--- | :--- |
| **`ID`** | FASTA header, or the PDB filename for `-m 3` |
| **`Sequence`** | Input peptide sequence (when supplied as sequence) |
| **`SMILES`** | Chemical SMILES representation (`-m 2` only) |
| **`pHC50`** | Predicted $\text{pHC}_{50}$ value |
| **`Prediction`** | Predicted **$\text{HC}_{50}$ in $\mu\text{M}$** |
| **`Hemolytic_Activity`** | `Hemolytic` or `Non-hemolytic` (at the $100\ \mu\text{M}$ cut-off) |

> Under the Chemical model (`-m 2`), entries supplied as peptide sequences report both `Sequence` and `SMILES`, whereas raw SMILES inputs report `SMILES` only. Long SMILES strings are truncated in terminal previews for readability, while full strings are always preserved in the CSV file.

#### Design Output (`-j 2`)

| Column | Meaning |
| :--- | :--- |
| **`SeqID`** | Identifier of the parent lead peptide |
| **`Mutant_ID`** | `Original_Seq1` for the wild type, or `Mutant_<WT><Pos><Mut>` (e.g., `Mutant_K1A`) |
| **`Sequence`** | Full variant sequence with original modifications preserved |
| **`Position`**, **`Wild_Residue`**, **`Mutant_Residue`** | Mutation site and residue substitution details |
| **`pHC50`**, **`Prediction`** | Predicted $\text{pHC}_{50}$ and $\text{HC}_{50}$ ($\mu\text{M}$) |
| **`Fold_Change_vs_WT`** | Ratio of variant $\text{HC}_{50}$ relative to its parent wild-type $\text{HC}_{50}$ |
| **`Direction`** | `More hemolytic` / `Less hemolytic` / `No change` |
| **`Hemolytic_Activity`** | `Hemolytic` or `Non-hemolytic` |

---

## 🔍 Jobs & Features

### 🔹 Job Types

| Job | Description |
| :--- | :--- |
| 1️⃣ **Prediction** | Predicts $\text{pHC}_{50}$ and $\text{HC}_{50}$ ($\mu\text{M}$) for every input peptide. |
| 2️⃣ **Design** | Enumerates and scores **all possible single-residue mutants** for each input lead peptide. |

### 🔹 How the Design Module Works

- Every standard residue position in each input peptide is systematically substituted with each of the other 19 canonical amino acids and scored using the Sequence model (`-m 1`).
- **Modification Preservation:** Terminal tags (`{nt:Acet}`, `{ct:Amid}`, `{cyc:N-C}`), stereochemistry tags (`{d}`), and non-natural residues (`{nnr:...}`) remain untouched across all generated variants. Non-natural residue positions are preserved as-is without substitution.
- **Batch Lead Support:** Multiple lead sequences can be submitted in a single FASTA file; `Fold_Change_vs_WT` is calculated independently against each lead's respective wild-type score.
- **Limits:** Maximum 50 residues per lead peptide ($50 \times 19 = 950$ variants) using the Sequence model (`-m 1`) only.

---

## 🧠 Model Architecture Summary

| Model | Input | Features | Estimator | Training Samples |
| :--- | :--- | :--- | :--- | :--- |
| **Sequence (`-m 1`)** | MAP / FASTA | 28 features (20 AAC + 5 mod tags + 3 D/L counts) | ExtraTrees (tuned) | 1,924 |
| **Chemical (`-m 2`)** | SMILES | 100 Mordred 2D descriptors | XGBoost (tuned) | 1,924 |
| **Structure (`-m 3`)** | PDB | 100 Mordred 2D descriptors | ExtraTrees | 1,100 |

---

## 📑 Package Contents

| File / Folder | Description |
| :--- | :--- |
| **`INSTALLATION.txt`** | Detailed installation instructions |
| **`LICENSE.txt`** | Software license information |
| **`README.md`** | Documentation & usage guide |
| **`HemoPI_MOD2.py`** | Main Python CLI script for prediction and design |
| **`stitch.py`** | MAP sequence $\rightarrow$ SMILES builder used by Model 2 |
| **`models/`** | Pre-trained regression model weights |
| **`data/`** | Modification/NNR database and documentation figures |
| **`example_sequence.fasta`** | Sample MAP/FASTA input file |
| **`example_smiles.txt`** | Sample SMILES input file (for `-m 2`) |
| **`example_structure.pdb`** | Sample 3D structure file (for `-m 3`) |
| **`example_design.fasta`** | Sample lead peptide file (for `-j 2`) |
| **`environment.yml`** | Conda environment specification |
| **`requirements.txt`** | Pip dependency list |

---

<div align="center">

🚀 **Start predicting and designing hemolytic peptides with HemoPI-MOD2 today!**

[![Web Server](https://img.shields.io/badge/Web%20Server-Launch-blue?style=flat-square)](https://webs.iiitd.edu.in/raghava/hemopimod2)
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Open%20Demo-orange?style=flat-square)](https://colab.research.google.com/github/raghavagps/HemoPImod2/blob/main/HemoPIMOD2_Demo.ipynb)
[![PyPI](https://img.shields.io/badge/PyPI-Package-blue?style=flat-square)](https://pypi.org/project/hemopimod2/)
[![Anaconda](https://img.shields.io/badge/Anaconda-Package-brightgreen?style=flat-square)](https://anaconda.org/channels/drv01/packages/hemopimod2/overview)
[![Docker](https://img.shields.io/badge/Docker-Hub-blue?style=flat-square)](https://hub.docker.com/repository/docker/drv01/hemopimod2/general)
[![Raghava Lab](https://img.shields.io/badge/Raghava%20Lab-IIIT--Delhi-green?style=flat-square)](https://webs.iiitd.edu.in/raghava/)

© 2026 **Dr. G.P.S. Raghava**, IIIT-Delhi

</div>
