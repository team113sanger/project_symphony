# Uncovering RNA Dependencies in Lung Cancer through CRISPR–Cas13d Functional Genomics

[![DOI](https://zenodo.org/badge/1034340540.svg)](https://doi.org/10.5281/zenodo.24337798)

This repository is the central landing page for the sub-analyses supporting the manuscript:

> **_Arriaga-González, F.G., Joseph, N.A., Peidli, S. et al 2026 - Uncovering RNA Dependencies in Lung Cancer through CRISPR–Cas13d Functional Genomics_**

<details>
<summary>Full author list</summary>

Fernanda G. Arriaga-González\*, Nithila A. Joseph\*, Stefan Peidli\*, Demetrios Aspris, Josephine Ilott, Jamie Billington, Eliza Yankova, Maria Eleftheriou, Siân Evans, Victoria Harle, Rebeca Olvera-León, Rafaela Fagundes, Larissa Satiko Alcantara Sekimoto Matsuyama, Wolfgang Huber, Sunay Usluer†, David J. Adams†, Konstantinos Tzelepis†

\*equal contribution · †corresponding authors
</details>

## Study summary

We established CRISPR–Cas13d as an RNA-targeting platform for systematic loss-of-function screening of both
protein-coding and non-coding transcripts in lung cancer. The work combines:

- a **pooled dropout screen** with the lung-cancer-focused *Symphony* library (6,225 gRNAs; 627 protein-coding
  and 91 lncRNA targets) in three genetically distinct lines (A549, NCI-H1299, NCI-H1975);
- **benchmarking against Cas9** (DepMap), showing comparable essential-gene recovery (ROC AUC > 0.9) without
  the copy-number bias of Cas9 screens;
- **arrayed Cas13d validation** with Incucyte live-cell imaging, colony formation, siRNA knock-down, western
  blot and cell cycle assays;
- **single-cell CaRPool-Seq** perturbation profiling across the three cancer lines plus the KOLF2.1S hiPSC line.

The screens recover known lncRNA dependencies (MALAT1, NEAT1, GAS5) and identify **SNHG15** and **SNHG16** as
oncogenic lncRNAs converging on MYC signalling: their depletion lowers c-MYC protein, arrests cells in G1 and
suppresses proliferation in lung cancer lines but not in non-malignant hiPSCs.

The analyses were conducted by several authors in the Adams, Huber, and Tzelepis groups (Wellcome Sanger Institute, EMBL,
University of Cambridge). Each sub-analysis repository linked below carries its own **README.md** with the methods, code and data needed to reproduce its results.

## Project overview

The sub-analyses of the project, the authors who performed them, and the repositories they correspond to are:

- Pooled Cas13d screen (SYM101) [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/stefanpeidli/symphony-101)[![DOI](https://zenodo.org/badge/TBC.svg)](TBC) (sp41@sanger.ac.uk)
  - Guide count generation and screen QC — Figure 1c, Supplementary Figure 2
  - MAGeCK MLE essentiality calling — Figures 1d–1f, Supplementary Figures 2b–2c, 3a
  - Cas9/DepMap benchmarking and copy-number analysis — Figure 2
  - Submodule `SYM_101_Stefan_Peidli_Screen_Analysis`

- Single-cell CaRPool-Seq screen (SYM10X1) [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/stefanpeidli/symphony-10x1)[![DOI](https://zenodo.org/badge/TBC.svg)](TBC) (sp41@sanger.ac.uk)
  - cellranger processing, guide assignment and SNP demultiplexing — Supplementary Figures 4a, 4b, 4d, 4f
  - Differential expression, GSEA and clustering — Figures 4a–4b, 5b, Supplementary Figure 4g
  - Submodule `SYM_101_Stefan_Peidli_10X_Analysis`

- Arrayed live-cell growth assays [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/team113sanger/SYM_101_Incucyte_data_analysis_FerArriaga)[![DOI](https://zenodo.org/badge/1105434607.svg)](https://doi.org/10.5281/zenodo.24338160) (fa15@sanger.ac.uk)
  - Incucyte green-object and confluence analysis in A549, NCI-H1299 and NCI-H1975 — Figures 3b–3d, Supplementary Figures 3b–3c
  - Essential vs non-essential comparisons and guide-level barplots — Figure 3b
  - Submodule `SYM_101_Fernanda_Arriaga_González`

- Symphony library design and Cas13d validation [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/team113sanger/SYM_101_Sunay_Usluer)[![DOI](https://zenodo.org/badge/1018557085.svg)](https://doi.org/10.5281/zenodo.24338199) (su1@sanger.ac.uk)
  - Library design and Cas13d activity tests — Figures 1a, 3a, Supplementary Figure 1
  - TRACERx tumour vs normal expression analysis — Figures 3e, 5a, Supplementary Figure 3d
  - CellTrace proliferation and cell cycle assays — Figures 5e–5f, Supplementary Figures 5b–5d
  - Submodule `SYM_101_Sunay_Usluer`

- Cas13d collateral activity (SYM10X0) [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/team113sanger/sym101_cas13_collateral_activity_analysis)[![DOI](https://zenodo.org/badge/1461365821.svg)](https://doi.org/10.5281/zenodo.24310447) (jb63@sanger.ac.uk)
  - Perturb-seq in A549 and NCI-H1299 testing for target-independent transcriptional effects
  - Pseudobulk guide correlations, cell-cycle-stratified DE, GSEA and RP-module controls — Supplementary Figure 4c
  - Submodule `SYM_101_Cas13_Collateral_Activity`

Clone everything, including the sub-analyses, with:

```
git clone --recurse-submodules https://github.com/team113sanger/project_symphony.git
```

## Data availability

Raw sequencing data are deposited with the ENA:

| Dataset | Accession |
| --- | --- |
| SYM101 — pooled Cas13d dropout screen | [PRJEB82598](https://www.ebi.ac.uk/ena/browser/view/PRJEB82598) |
| SYM10X1 — CaRPool-Seq single-cell screen | [ERP165591](https://www.ebi.ac.uk/ena/browser/view/ERP165591) |

Processed and raw count matrices, plus large files and figures from the paper, are on FigShare:

| Dataset | DOI |
| --- | --- |
| SYM101 — pooled screen counts | [10.6084/m9.figshare.29557898](https://doi.org/10.6084/m9.figshare.29557898) |
| SYM10X1 — CaRPool-Seq matrices | [10.6084/m9.figshare.29557997](https://doi.org/10.6084/m9.figshare.29557997) |

Download a FigShare bundle with:

```
# SYM101 pooled screen
curl -k -o sym101_bundle.zip https://figshare.com/ndownloader/articles/29557898/versions/1
unzip sym101_bundle.zip

# SYM10X1 CaRPool-Seq
curl -k -o sym10x1_bundle.zip https://figshare.com/ndownloader/articles/29557997/versions/1
unzip sym10x1_bundle.zip
```

## Contact

- Konstantinos Tzelepis (<kt404@cam.ac.uk>) †
- David J. Adams (<da1@sanger.ac.uk>) †
- Sunay Usluer (<su1@sanger.ac.uk>) †
- Fernanda G. Arriaga-González (<fa15@sanger.ac.uk>)
- Stefan Peidli (<sp41@sanger.ac.uk>)
- Jamie Billington (<jb63@sanger.ac.uk>)

† corresponding authors

## Acknowledgements

K.T., E.Y. and S.E. were supported by Wellcome Trust (grants 203151/A/16/Z, 306752/A/23/Z and 306752/Z/23/Z)
and UKRI Medical Research Council (grant 203151/Z/16/Z). K.T. and M.E. were supported by Leukaemia UK
(2022/FuF/001). E.Y. was supported by a Leukaemia UK John Goldman Fellowship (2024/JGF/009). This research was
funded in part by Wellcome, who supported the Cambridge Stem Cell Institute (203151/Z/16/Z). D.J.A., J.B.,
R.F. and L.S.A.S.M. were supported by Cancer Research UK (C20510/A21717), Wellcome Trust (220540/Z20/A) and the
Medical Research Council. S.U., F.G.A-G., S.P., D.A., J.I. and N.A.J. were supported by Open Targets (OTAR3083).
Computations were in part run on EMBL IT Services HPC resources. The authors thank Cath Ennis (Wordomics
Editing) for assistance with editing the manuscript prior to submission, and Petr Smirnov, Sarah Linker,
Panos Zalmas and the Open Targets pharma partners for useful discussions.
