---
order: 3
title: "The Right Prior for the Right Deformation"
headline: "The Right Prior for the Right Deformation"
supportingTitle: "Continuous Deformable Image Registration"
supportingTitleEmphasis: "Rethinking"
supportingTitleEmphasisPosition: "before"
venue: "MICCAI 2026 Off-Grid Workshop — Oral"
image: "https://raw.githubusercontent.com/HengjieLiu/RightPriorDIR/main/figures/fig1.png"
imageAlt: "Overview of continuous deformable image registration methods and deformation priors"
secondaryImage: "https://raw.githubusercontent.com/HengjieLiu/RightPriorDIR/main/figures/fig2.png"
secondaryImageAlt: "Comparison of continuous deformable registration performance across motion regimes"
imageSide: "left"
paper: "https://arxiv.org/abs/2608.16146"
code: "https://github.com/HengjieLiu/RightPriorDIR"
codeLabel: "Code coming soon"
---

This work studies continuous deformable image registration from a prior-matching perspective: registration performance depends not simply on using an off-grid or neural representation, but on whether the deformation prior induced by the parameterization and optimization matches the target motion.

- We compare INR-Dense, INR-BSCP, D-BSCP, and MR-D-BSCP across two distinct regimes: inter-subject brain MRI on OASIS, with moderate but locally complex anatomical deformation, and intra-subject exhale-to-inhale lung CT on DIR-LAB 4DCT, with larger, smoother, and more directionally coherent respiratory motion.
- On OASIS, directly optimized B-Spline control points closely match INR-BSCP, indicating that much of INR-BSCP's effectiveness comes from the locality, smoothness, and scale of the B-Spline parameterization, rather than the INR alone. INR-Dense instead favors a smoother deformation regime and is less effective at capturing complex local variation.
- On DIR-LAB, single-scale B-Spline methods are less robust to large respiratory motion. INR-Dense benefits from its smooth, coherent INR prior, while MR-D-BSCP uses coarse-to-fine optimization to capture large displacement before local refinement, achieving the strongest performance among the tested continuous parameterizations.
- We evaluate methods across the alignment–regularity trade-off, rather than at a single regularization setting, to enable fairer comparisons across deformation models.
