# HCV E2 Antibody Orientation & Clustering

Quantifies and clusters HCV **E2-specific antibodies** by binding orientation.

- **Inclination angle (φ)**: angle between lines from E2 COM to Fv COMs of two antibodies. Small φ ⇒ same antigenic region; large φ ⇒ different epitopes.
- **Approach angle (ψ)** (FRLY only): minimal rotation to align one Fab to another; distinguishes approach modes within the same region.

## Figure
![Clustering overview](docs/figure1.png)

## Files & Folders
```
.
├── input.csv
├── pt1_save_pdbs.ipynb
├── pt2_align_E2_regions.ipynb
├── pt3_clustering.ipynb
├── inclination_angle.csv
└── FRLY_Abs/
    ├── input.csv
    ├── pt1_save_pdbs.ipynb
    ├── pt2_align_E2_regions.ipynb
    ├── pt3_clustering.ipynb
    └── approach_angle.csv
```

## Input Format (`input.csv`)
```
pdb_id,antigen_chain,heavy_chain,light_chain,antibody
4mwf,C,H,L,AR3C(4mwf)
4web,E,H,L,2A12(4web)
6bkb,E,H,L,AR3A(6bkb)
...
```

## Usage
1. Run **pt1_save_pdbs.ipynb** to download PDBs from `input.csv`.
2. Run **pt2_align_E2_regions.ipynb** to align on E2 (reference: 4mwf).
3. Run **pt3_clustering.ipynb** to compute pairwise angles and cluster.
4. For FRLY antibodies, repeat steps 1–3 inside `FRLY_Abs/` (ψ).

## Precomputed
- `inclination_angle.csv` (φ)
- `FRLY_Abs/approach_angle.csv` (ψ)

## Contact
rjtpunia@cornell.edu
