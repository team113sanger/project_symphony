# Uncovering RNA Dependencies in Lung Cancer through CRISPR–Cas13d Functional Genomics

This repository is the central landing page for the sub-analyses supporting the manuscript:

> **_Arriaga-González F.G.\*, Joseph N.A.\*, Peidli S.\*, Aspri D., Ilott J., Billington J., Yankova E., Eleftheriou M., Evans S., Harle V., Olvera-León R., Fagundes R., Sekimoto Matsuyama L.S.A., Huber W., Usluer S.†, Adams D.J.†, Tzelepis K.† — "CRISPR–Cas13d Functional Genomics Reveals RNA Dependencies in Lung Cancer"_**
>
> \*equal contribution · †corresponding authors

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

The sub-analyses, the authors who performed them, and the repositories they correspond to are:

- **Pooled Cas13d screen (SYM101): guide count generation, QC, MAGeCK MLE, Cas9/DepMap benchmarking and
  copy-number analysis** — Figures 1–2, Supplementary Figures 2–3.
  [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/stefanpeidli/symphony-101)[![DOI](https://zenodo.org/badge/932059905.svg)](TBC)
  (Stefan Peidli, sp41@sanger.ac.uk — submodule `SYM_101_Stefan_Peidli_Screen_Analysis`)

- **Single-cell CaRPool-Seq screen (SYM10X1): cellranger processing, guide assignment, SNP demultiplexing,
  differential expression, GSEA and clustering** — Figures 4–5b, Supplementary Figure 4.
  [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/stefanpeidli/symphony-10x1)[![DOI](https://zenodo.org/badge/TBC.svg)](TBC)
  (Stefan Peidli, sp41@sanger.ac.uk — submodule `SYM_101_Stefan_Peidli_10X_Analysis`)

- **Arrayed live-cell growth assays: Incucyte green-object and confluence analysis across A549, NCI-H1299 and
  NCI-H1975, including essential vs non-essential comparisons and guide-level barplots** — Figure 3,
  Supplementary Figure 3.
  [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/team113sanger/SYM_101_Incucyte_data_analysis_FerArriaga)[![DOI](https://zenodo.org/badge/971292322.svg)](https://doi.org/10.5281/zenodo.15304185)
  (Fernanda Arriaga González, fa15@sanger.ac.uk — submodule `SYM_101_Fernanda_Arriaga_González`)

- **Symphony library design, Cas13d activity tests, TRACERx tumour vs normal expression analysis, and cell
  cycle / CellTrace assays** — Figures 1a, 3e, 5a, 5f, Supplementary Figures 1 and 5.
  [![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/team113sanger/SYM_101_Sunay_Usluer)[![DOI](https://zenodo.org/badge/TBC.svg)](TBC)
  (Sunay Usluer, su1@sanger.ac.uk — submodule `SYM_101_Sunay_Usluer`)

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

Corresponding authors:

- Konstantinos Tzelepis (<kt404@cam.ac.uk>)
- David J. Adams (<da1@sanger.ac.uk>)
- Sunay Usluer (<su1@sanger.ac.uk>)

Analysis contacts:

- Stefan Peidli (<sp41@sanger.ac.uk>)
- Fernanda Arriaga González (<fa15@sanger.ac.uk>)
