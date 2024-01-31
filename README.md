# VGO Oropharyngeal Resistome Data Analysis

[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

**Authors**: Beatrice Cornu Hewitt <a href="https://orcid.org/0000-0002-4594-4393" target="orcid.widget" rel="noopener noreferrer" style="vertical-align:top;"><img src="https://orcid.org/sites/default/files/images/orcid_16x16.png" style="width:1em;margin-right:.5em;" alt="ORCID iD icon"></a><br>
**Contact**: b.cornuhewitt@uu.nl<br>
**Date**: 31-01-2024<br>

## Description
The scripts in this repository are related to a COPD case-control study conducted with data from the VGO project which involves study participants living in a livestock dense region in the South Eastern Netherlands (https://www.rivm.nl/veehouderij-en-gezondheid/onderzoek-veehouderij-en-gezondheid-omwonenden-vgo). We aimed to investigate associations between the OP resistome composition and (1) COPD status, (2) the OP microbiome composition and (3) residential exposure to livestock-related microbial emissions.

## Scripts
All scripts are saved as Rmarkdown files in the folder 'Rscripts' within this repository. Scripts are separated into the following sections:

*  [`Rscripts/1%20-%20Load%20libraries.Rmd`](Rscripts/1 - Load libraries.Rmd): Load required libraries for entire project
*  [`2 - Load data and create phyloseq.Rmd`](Rscripts/2 - Load data and create phyloseq.Rmd): Load data for whole project and create phyloseq objects ready for analysis
*  [`3 - Identify contaminants.Rmd`](Rscripts/3 - Identify contaminants.Rmd): Script to identify contaminants using decontam combined method
*  [`4 - Resistome basics.Rmd`](Rscripts/4 - Resistome basics.Rmd): Basic analysis of the resistome including abundance analysis, bacterial load analysis
*  [`5 - Visualisations.Rmd`](Rscripts/5 - Visualisations.Rmd): Visualisations of the resistome including stacked bar charts and heatmaps on different taxonomic levels
*  [`6 - Alpha diversity.Rmd`](Rscripts/6 - Alpha diversity.Rmd): Alpha diversity analyses in relation to COPD status and livestock exposure status
*  [`7 - Beta diversity.Rmd`](Rscripts/7 - Beta diversity.Rmd): Community composition analyses in relation to COPD status and livestock exposure status
*  [`8 - Differential abundance analysis.Rmd`](Rscripts/8 - Differential abundance analysis.Rmd): Differential abundance analysis of resistance genes in relation to COPD status and livestock exposure status using DESeq and ALDEx algorithms
*  [`9 - Bacteriome and resistome.Rmd`](Rscripts/9 - Bacteriome and resistome.Rmd): Comparison of the composition of the bacteriome and the resistome using Procrustes analysis and co-occurrence networks


## Session Info 
```
R version 4.3.2 (2023-10-31 ucrt)
Platform: x86_64-w64-mingw32/x64 (64-bit)
Running under: Windows 10 x64 (build 19045)

Matrix products: default

locale:
[1] LC_COLLATE=English_United Kingdom.utf8  LC_CTYPE=English_United Kingdom.utf8   
[3] LC_MONETARY=English_United Kingdom.utf8 LC_NUMERIC=C                           
[5] LC_TIME=English_United Kingdom.utf8    

time zone: Europe/Berlin
tzcode source: internal

attached base packages:
[1] grid      stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
 [1] ALDEx2_1.34.0         latticeExtra_0.6-30   zCompositions_1.5.0-1 truncnorm_1.0-9      
 [5] NADA_1.6-1.1          survival_3.5-7        MASS_7.3-60           renv_1.0.3           
 [9] annotater_0.2.3       here_1.0.1            decontam_1.22.0       phyloseq_1.46.0      
[13] writexl_1.4.2         vegan_2.6-4           permute_0.9-7         lubridate_1.9.3      
[17] purrr_1.0.2           tidyr_1.3.0           tidyverse_2.0.0       tibble_3.2.1         
[21] stringr_1.5.1         scales_1.3.0          readr_2.1.4           RColorBrewer_1.1-3   
[25] plyr_1.8.9            patchwork_1.1.3       openxlsx_4.2.5.2      olsrr_0.5.3          
[29] matrixStats_1.1.0     magrittr_2.0.3        lattice_0.21-9        knitr_1.45           
[33] igraph_1.5.1          Hmisc_5.1-1           styler_1.10.2         TempPackage_1.0      
[37] docstring_1.0.0       ggpubr_0.6.0          ggplot2_3.4.4         foreach_1.5.2        
[41] forcats_1.0.0         e1071_1.7-13          DT_0.30               dplyr_1.1.4          
[45] cowplot_1.1.1         corrplot_0.92         car_3.1-2             carData_3.0-5        
[49] BiocManager_1.30.22   lintr_3.1.1          

loaded via a namespace (and not attached):
  [1] splines_4.3.2               bitops_1.0-7                R.oo_1.26.0                
  [4] rpart_4.1.21                rex_1.2.1                   lifecycle_1.0.4            
  [7] rstatix_0.7.2               rprojroot_2.0.4             processx_3.8.2             
 [10] backports_1.4.1             sass_0.4.7                  rmarkdown_2.25             
 [13] jquerylib_0.1.4             yaml_2.3.7                  remotes_2.4.2.1            
 [16] zip_2.3.0                   pkgbuild_1.4.2              ade4_1.7-22                
 [19] abind_1.4-5                 pkgload_1.3.3               zlibbioc_1.48.0            
 [22] quadprog_1.5-8              GenomicRanges_1.54.1        R.cache_0.16.0             
 [25] R.utils_2.12.3              BiocGenerics_0.48.1         RCurl_1.98-1.13            
 [28] nnet_7.3-19                 GenomeInfoDbData_1.2.11     IRanges_2.36.0             
 [31] S4Vectors_0.40.2            nortest_1.0-4               goftest_1.2-3              
 [34] DelayedArray_0.28.0         codetools_0.2-19            xml2_1.3.5                 
 [37] tidyselect_1.2.0            stats4_4.3.2                base64enc_0.1-3            
 [40] roxygen2_7.2.3              jsonlite_1.8.7              multtest_2.58.0            
 [43] Formula_1.2-5               iterators_1.0.14            tools_4.3.2                
 [46] Rcpp_1.0.11                 glue_1.6.2                  SparseArray_1.2.2          
 [49] gridExtra_2.3               xfun_0.41                   mgcv_1.9-0                 
 [52] MatrixGenerics_1.14.0       GenomeInfoDb_1.38.1         withr_2.5.2                
 [55] fastmap_1.1.1               rhdf5filters_1.14.1         fansi_1.0.5                
 [58] callr_3.7.3                 digest_0.6.33               timechange_0.2.0           
 [61] R6_2.5.1                    colorspace_2.1-0            jpeg_0.1-10                
 [64] R.methodsS3_1.8.2           utf8_1.2.4                  generics_0.1.3             
 [67] data.table_1.14.8           class_7.3-22                S4Arrays_1.2.0             
 [70] prettyunits_1.2.0           htmlwidgets_1.6.3           pkgconfig_2.0.3            
 [73] gtable_0.3.4                XVector_0.42.0              htmltools_0.5.7            
 [76] biomformat_1.30.0           Biobase_2.62.0              png_0.1-8                  
 [79] cyclocomp_1.1.1             rstudioapi_0.15.0           tzdb_0.4.0                 
 [82] reshape2_1.4.4              checkmate_2.3.1             nlme_3.1-163               
 [85] proxy_0.4-27                cachem_1.0.8                rhdf5_2.46.1               
 [88] parallel_4.3.2              RcppZiggurat_0.1.6          foreign_0.8-85             
 [91] desc_1.4.2                  pillar_1.9.0                vctrs_0.6.4                
 [94] cluster_2.1.4               htmlTable_2.4.2             evaluate_0.23              
 [97] cli_3.6.1                   compiler_4.3.2              rlang_1.1.2                
[100] crayon_1.5.2                ggsignif_0.6.4              interp_1.1-6               
[103] ps_1.7.5                    fs_1.6.3                    stringi_1.8.2              
[106] BiocParallel_1.36.0         deldir_2.0-2                munsell_0.5.0              
[109] Biostrings_2.70.1           lazyeval_0.2.2              Matrix_1.6-1.1             
[112] hms_1.1.3                   Rhdf5lib_1.24.0             SummarizedExperiment_1.32.0
[115] Rfast_2.1.0                 broom_1.0.5                 RcppParallel_5.1.7         
[118] bslib_0.6.1                 directlabels_2024.1.21      xmlparsedata_1.0.5         
[121] ape_5.7-1  
```
