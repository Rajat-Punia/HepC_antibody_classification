# 🧬 Antigen–Antibody Complex Alignment and Clustering Pipeline

This repository provides a complete structural analysis workflow for **antigen–antibody complexes** (e.g., HCV E2–Fab).  
It automates **PDB download, chain filtering, structure alignment, orientation angle computation, and clustering** based on antibody approach geometry.

---

## 📂 Overview of Pipeline

### 1️⃣ Download and Preprocess PDBs
**Script:** `download_and_filter_structures.py`

- Reads `input.csv` with columns:  
  `pdb_id, antigen_chain, heavy_chain, light_chain, antibody`
- Downloads PDBs using Biopython’s `PDBList`
- Extracts only specified chains (Ag, heavy, light) and removes heteroatoms/water
- Renumbers residues using **ANARCI’s ImmunoPDB** for consistent numbering
- **Output:**  
