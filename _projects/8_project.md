---
layout: page
title: Genomic prediction for metabolites in rice
description: Role of genomics on regulating rice grain metabolic variability under warmer nights, A statistical and image-based deep learning approach
img: /assets/img/GP4Met/DL_Results.png
importance: 1
category: Quantitative Genetics
---

Preprint: [GitHub linke for more details with figures](https://github.com/yebigithub/GBLUP4Met/tree/main?tab=readme-ov-file)

## Abstract
It has been argued that metabolites can be used to accelerate crop improvement because metabolic profiles in crops are generally under genetic control. Evaluating the role of genetics in metabolic variation is a longstanding challenge. Rice, one of the world's most important staple crops, is known to be sensitive to recent increases in nighttime temperatures. Quantification of metabolic levels can help measure rice responses to high nighttime temperature (HNT) stress. However, the extent of metabolic variation that can be explained by regression on whole-genome molecular markers remains to be answered. In the current study, primary metabolites of a rice diversity panel generated from grains using gas chromatography-mass spectrometry were used. The metabolites obtained were low to moderately heritable, and the genomic prediction accuracies of the metabolites were within the expected upper limit set by their genomic heritability estimates. Genomic heritability estimates were slightly higher in the control group than in the HNT group. Genomic correlation estimates for the same metabolites between the control and HNT conditions indicated the presence of genotype by environment interactions. Reproducing kernel Hilbert spaces regression and deep learning, which treat markers as images, improved prediction accuracy, suggesting that some metabolites are under non-additive genetic control. Joint analysis of multiple metabolites simultaneously was effective in improving prediction accuracy by exploiting correlations among metabolites. The current study serves as an important first step in evaluating the cumulative effects of the genome in regulating metabolic variation under control and HNT conditions. 


## 0. Data Preprocessing
- [.Rmd file](https://github.com/yebigithub/GBLUP4Met/blob/main/PreProcessing/DataPreprocessing.Rmd) Including metabolite and genotype data cleaning

## 1. Genomic heritability of metabolites
- [.R file](https://github.com/yebigithub/GBLUP4Met/blob/main/heritability/h2_calculate.R) Using sommer package to calculate heritability for metabolites.
- [.Rmd file](https://github.com/yebigithub/GBLUP4Met/blob/main/heritability/h2_plot_drawing.Rmd) Drawing heritability plots.


## 2. Single-trait genomic prediction of metabolites
- [.R file](https://github.com/yebigithub/GBLUP4Met/blob/main/SingleTraitGBLUP/GBLUP_whole.R) Running Single trait GBLUP in cluster.
- [.Rmd file](https://github.com/yebigithub/GBLUP4Met/blob/main/SingleTraitGBLUP/SingleTraitGBLUP.Rmd) Drawing Single trait GBLUP plots.
- [.Rmd file](https://github.com/yebigithub/GBLUP4Met/blob/main/SingleTraitGBLUP/GK.Rmd) Selecting suitable bandwidth for RKHS.
- [.R file](https://github.com/yebigithub/GBLUP4Met/blob/main/SingleTraitGBLUP/GK.R) Runing Single trait RKHS in cluster.


## 3. Genomic correlation between the same metabolite in different treatments
- [.R file](./GenoCorrSameMet/GenoCorrSameMet.R) Running multi-trait genomic correlation.
- [.Rmd file](./GenoCorrSameMet/GenoCorrSameMet.Rmd) Drawing multi-trait genomic correlation plots.

## 4. Exporatory factor analysis
- [.Rmd file](./FactorAnalysis/FA4Met.Rmd) Factorial analysis to identify underlying latent factors controlling metabolites.

## 5. Simultaneous regression modeling of metabolites
- [.R file](./SimultaneousRegression/MegaLLM.R) Running MegaLMM for genomic prediction.
- [.R file](./SimultaneousRegression/MegaLLM_GK.R) Running MegaLMM for RKHS.
- [.Rmd file](./SimultaneousRegression/MegaLMM_drawing.Rmd) Drawing barplot, density plots for MegaLMM genomic prediction model.
- [.Rmd file](./SimultaneousRegression/GenomicCorr.Rmd) Drawing genomic correlation density plot.


## 6. Deep learning models
- [.ipynb](./DL/ConvertSNP2Image.ipynb) Shows examples about how to convert SNP tabular data into SNP images.
- [.py file](./DL/ConvertSNP2Image.py) Loop converting for SNPs in all chromosomes.
- [.py file](./DL/FeatureExtractorMulti.py) Convolutional neural network with multiple branches.
- [.Rmd file](./DL/DL_drawing.Rmd) Drawing barplot to compare performance of all deep learning models and RKHS.

## 7. Supplementary
- [.Rmd file](./Supplementary/PhenoCorr.Rmd) Calculating phenotypical correaliton between metabolites in control and stress conditions.
- [.Rmd file](./SimultaneousRegression/MegaLMM_ggcorr.R) Drawing MegaLMM genomic correlation heatmaps.
- [.Rmd file](./FactorAnalysis/FA4Met.Rmd) Drawing factorial analysis heatmaps.
- [.Rmd file](./Supplementary/FA_drawing.Rmd) Drawing factorial analysis density plots.