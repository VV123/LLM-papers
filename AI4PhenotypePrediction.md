
- (Example) [A machine learning pipeline for quantitative phenotype prediction from genotype data](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-11-S8-S3)
  * Venue: BMC Bioinformatics
  * Summary: 2-3 sentences for summerization

- A machine learning pipeline for quantitative phenotype prediction from genotype data.
  * Venue: BMC Bioinformatics
  * Summary: This study introduces a machine learning pipeline that integrates L1L2 regularization for effective feature selection and prediction of quantitative phenotypes from genomic data, demonstrating comparable performance to traditional methods like SVR and MCMC while addressing issues of correlated features.
    
- A novel machine learning framework for phenotype prediction based on genome-wide dna methylation data.
  * Venue: IEEE IJCNN 2017
  * Summary: This paper proposes a novel machine learning framework for predicting cervical cancer stages based on genome-wide DNA methylation data. The method leverages CpG site information and outperforms existing approaches like MS-SPCA and EVORA in terms of AUC accuracy. It demonstrates strong predictive power for identifying disease stages using epigenetic markers. The framework shows promise for both current analysis and future biological applications.

- Machine learning models for phenotype prediction from genotype.
  * Venue: IEEE BIBE 2023
  * Summary: This paper addresses the problem of predicting phenotypes from genotypes using both traditional machine learning and deep learning models. The authors implement elastic net, MLP, CNN, and multi-task learning to perform phenotype regression. Experimental results on yeast data show that their proposed elastic net and CNN models achieve superior performance over existing methods. The study highlights the potential of combining linear and deep learning approaches in phenotype prediction.

- Biom2: biologically informed multi-stage machine learning for phenotype prediction using omics data.
  * Venue: Briefings in Bioinformatics
  * Summary: This paper introduces BioM2, an R package that incorporates biological domain knowledge into multistage machine learning for phenotype prediction. It enhances model accuracy and interpretability by stratifying high-dimensional omics data based on functional biological categories, such as Gene Ontology pathways. 

- Phenolinker: Phenotype-gene link prediction and explanation using heterogeneous graph neural networks
  * Venue: arXiv (q-bio.GN)
  * Summary: This work presents PhenoLinker, a novel heterogeneous graph neural network system for phenotype–gene link prediction. By integrating data from sources like HPO and applying graph-based CNN architectures, the model delivers both prediction scores and interpretability. It outperforms prior models and provides visual and explainable outputs through a Hugging Face demo platform.

- Plant genotype to phenotype prediction using machine learning.
  * Venue: Frontiers in Genetics
  * Summary: This review highlights the limitations of GBLUP in capturing nonlinear patterns from high-dimensional data. Machine learning models outperform traditional methods in genotype-to-phenotype prediction, especially with image and environmental data.

- Genotype-to-phenotype predictions: Boosting accuracy with machine learning.
  * Venue: PLOS ONE
  * Summary: The authors propose a nonlinear prediction framework combining XGBoost-based SNP selection and ensemble modeling. Their method selects 2–5× fewer SNPs than GWAS while maintaining accuracy. Nonlinear models outperform linear ones only when rich covariates are included. Ensembling Snpnet and XGBoost yields the highest overall performance, with XGBoost alone outperforming Snpnet on asthma.

- DeepGAMI: deep biologically guided auxiliary learning for multimodal integration and imputation to improve genotype–phenotype prediction
  * Venue: Genome Medicine
  * Summary: The authors propose DeepGAMI, an interpretable neural network that integrates multimodal data for genotype–phenotype prediction. It incorporates biological priors (e.g., eQTLs) and uses auxiliary learning to impute missing modalities. DeepGAMI outperforms existing models on brain disorder datasets using both full and partial modalities. It also identifies disease-relevant variants and gene networks.

- Gptransformer: a transformer-based deep learning method for predicting fusarium related traits in barley.
  * Venue: Frontiers in Plant Science
  * Summary: The authors proposed GPTransformer, a Transformer-based model for predicting Fusarium-related traits in barley. SNPs were encoded using Hardy-Weinberg frequencies, and key markers were selected for prediction. GPTransformer outperformed or matched RFCNN and BLUP in predicting FHB and DON. Hardy-Weinberg encoding improved performance by 6.9% for FHB and 9.6% for DON.

- Effective gene expression prediction from sequence by integrating long-range interactions.
  * Venue: Nature Methods
  * Summary: The authors proposed Enformer, a Transformer-based model that predicts gene expression by capturing long-range DNA interactions up to 100 kb. Unlike previous CNN-based models limited to 20 kb, Enformer uses self-attention to aggregate signals from distant regulatory elements. It improves accuracy in predicting expression levels, enhancer–promoter interactions, and mutation effects. The model outperforms prior methods in CRISPRi and eQTL benchmarks.

- Dnabert: pre-trained bidirectional encoder representations from transformers model for dna-language in genome.
  * Venue: Bioinformatics
  * Summary: The authors proposed DNABERT, a pre-trained bidirectional Transformer model for non-coding DNA. It captures upstream and downstream context to improve prediction of regulatory elements. DNABERT achieves state-of-the-art performance on promoter, splice site, and TF binding site prediction after minimal fine-tuning. It also supports cross-species transfer and motif-level interpretability.

- A transformer-based genomic prediction method fused with knowledge-guided module.
  * Venue: Briefings in Bioinformatics
  * Summary: The authors proposed GPformer, a Transformer-based model for genomic prediction using SNP data. It captures global dependencies across SNPs through an auto-correlation mechanism and outperforms RR-BLUP, SVR, LightGBM, and DNNGP across five crop datasets. A knowledge-guided module (KGM) based on GWAS results is integrated to weight SNPs by biological relevance. GPformer + KGM further improves accuracy and shows robustness across datasets and phenotypes.

- Deep kernel and deep learning for genome-based prediction of single traits in multienvironment breeding trials.
  * Venue: Frontiers in Genetics
  * Summary: The authors compared deep learning (DL), deep kernel methods (arc-cosine kernel, AK), Gaussian kernel (GK), and GBLUP for genomic prediction in wheat. AK and GK slightly outperformed DL and GBLUP across datasets. AK required fewer hyperparameters and was easier to tune than DL and GK. In the 2015–2016 dataset, AK showed a clear advantage over DL due to DL’s tuning difficulty.

- Learning from methylomes: epigenomic correlates of Populus balsamifera traits based on deep learning models of natural DNA methylation.
  * Venue:  Plant Biotechnology Journal
  * Summary: The authors used deep learning to model plant traits based on natural DNA methylation variation in Populus balsamifera. Methylation features predicted tissue type, provenance, and explained major variance in wood traits like biomass (57.5%) and wood density (40.9%). The models required only small sets of methylated markers, highlighting their efficiency and biological relevance.

- Efficient genomic selection using ensemble learning and ensemble feature reduction.
  * Venue: Journal of Crop Science and Biotechnology
  * Summary: This study applies ensemble regression techniques to improve phenotype prediction in genomic selection (GS) using high-dimensional SNP data. By combining multiple feature selection and extraction methods, the model enhances prediction accuracy and reduces computational time. Compared to existing methods, prediction accuracy improved for all tested traits (e.g., grain yield: 0.304 → 0.330). A faster variant of the model further cuts runtime by 90% while maintaining competitive accuracy.

- Phenotype Prediction and Genome-Wide Association Study Using Deep Convolutional Neural Network of Soybean
  * Venue: Frontiers in Genetics
  * Summary: This paper introduces a CNN-based deep learning framework for phenotype prediction and marker discovery in soybeans. Unlike traditional methods that require genotype imputation, this model handles missing SNPs directly as a separate category. Experiments on both synthetic and real datasets show improved prediction accuracy and effective SNP marker identification via saliency maps.
  * https://www.frontiersin.org/journals/genetics/articles/10.3389/fgene.2019.01091/full

- Eye-color and Type-2 diabetes phenotype prediction from genotype data using deep learning methods
  * Venue: BMC Bioinformatics
  * Summary: This study proposes a hybrid statistical–machine learning approach for predicting eye color and Type-2 diabetes from SNP data. Multiple mutation-based SNP sets were derived and evaluated using 9 classifiers. Ensemble LSTM achieved the highest accuracy (96%) and AUC (0.98 for brown eyes). For Type-2 diabetes, the final model reached 97% accuracy. Results demonstrate the effectiveness of deep learning models in SNP-based binary classification tasks.
  *https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-021-04077-9

- A deep convolutional neural network approach for predicting phenotypes from genotypes
  * Venue: Planta (Springer Nature)
  * Summary: This paper presents DeepGS, a CNN-based model for phenotype prediction from genotype data in genomic selection. The model applies convolution, sampling, and dropout to manage high-dimensional SNP input. Compared with RR-BLUP, DeepGS performs competitively and shows complementary strengths. An ensemble of DeepGS and RR-BLUP further improves selection accuracy.
  * https://link.springer.com/article/10.1007/s00425-018-2976-9

- Human genotype-to-phenotype predictions: Boosting accuracy with machine learning.
  * Venue: PLOS ONE
  * Summary: The authors compared nonlinear models (e.g., boosted decision trees) with linear models for genotype-to-phenotype prediction and found nonlinear models outperform when rich covariates are included. They proposed a decision-tree-based SNP selection method that produces more compact and informative SNP sets than GWAS. Finally, they showed that ensemble models combining linear and nonlinear predictors achieve the best accuracy, setting new state-of-the-art results on traits like asthma and hypothyroidism.

- Transfer learning for genotype–phenotype prediction using deep learning.
  * Venue: BMC Bioinformatics
  * Summary: This study investigates the use of transfer learning for genotype–phenotype prediction in small populations with limited data. The authors used large-population data to train deep learning models and fine-tuned them on small-population data. They demonstrated improved classification accuracy (2–14.2%) across eight simulated phenotypes. Statistical tests confirmed the improvement was significant. 

- Deepat: A deep learning wheat phenotype prediction model based on genotype data.
  * Venue: Agronomy (MDPI), 2024, Volume 14, Issue 12
  * Summary: This paper proposes DeepAT, a deep learning model designed to predict wheat yield from genotype data. The model features a multi-layer architecture including feature extraction and self-attention modules, effectively capturing complex SNP–phenotype relationships. Compared to other methods, DeepAT achieved the highest prediction accuracy (99.98%), lowest MSE (28.93), and a near-perfect Pearson correlation, outperforming traditional machine learning and deep learning baselines. 

- machine learning for predicting phenotype from genotype and environment.
  * Venue: Current Opinion in Biotechnology, Volume 79, February 2023
  * Summary: This review categorizes phenotype prediction into three scenarios: using genotype, environment, or both. It summarizes machine learning models applied in each, discusses model feasibility, and highlights challenges in capturing complex interactions.

- Explainable artificial intelligence for genotype-to-phenotype predictions in plant breeding.
  * Venue: Frontiers in Plant Science, 2024 Sep 8, Volume 15
  * Summary: This study applies explainable AI (XAI) methods to predict shelling fraction in almonds using genotype data. Among tested models, Random Forest achieved the best performance. SHAP analysis revealed key SNPs, including one linked to seed development, offering both accurate prediction and biological interpretability.

- G2PDiffusion: Cross-Species Genotype-to-Phenotype Prediction via Evolutionary Diffusion
  * Venue: arXiv (Preprint), Computer Science > Machine Learning, 2025-02-07
  * Summary: G2PDiffusion is a diffusion model that generates morphological phenotypes from DNA across species. It incorporates multiple sequence alignments and environmental context through three modules: a co-evolutionary pattern retriever, an environment-aware encoder, and an adaptive phenomic alignment module. The model enhances genotype-to-phenotype consistency and generalization across species, enabling cross-domain phenotype prediction with limited labeled data.

- Can deep learning improve genomic prediction of complex human traits?
  * Venue: Genetics, Volume 210, Issue 3, November 2018
  * Summary: This study evaluated MLP and CNN performance on predicting five human traits using UK Biobank data (~100k individuals, ~500k SNPs). While CNNs and MLPs performed comparably to linear models on highly heritable traits like height, deep learning did not outperform linear models overall. CNNs showed potential but lacked a consistent advantage. Further adaptation of CNN architectures to genomic tasks is needed.

- An evaluation of machine-learning for predicting phenotype: studies in yeast, rice, and wheat
  * Venue: Machine Learning, Volume 109, 2020 
  * Summary: This paper benchmarks classical statistical genetics methods against standard ML models across three phenotype prediction tasks: yeast (simple), rice and wheat (complex). ML methods generally outperform traditional approaches. GBM performs best in yeast with complex mechanisms; lasso leads in simpler ones. SVM and BLUP excel in rice and wheat. Random forests show robustness to noise and missing data. BLUP performs well with population structure, indicating that ML models may benefit from incorporating such information.

- Graphgonet: a self-explaining neural network encapsulating the gene ontology graph for phenotype prediction on gene expression.
  * Venue: Bioinformatics
  * Summary: GraphGONet embeds Gene Ontology into neural layers for phenotype prediction from gene expression. It matches state-of-the-art accuracy and outputs interpretable biological concepts as explanations.

- Hpod-nets: deep graph convolutional networks for predicting human protein–phenotype associations.
  * Venue: Bioinformatics, Volume 38, Issue 3, February 2022, Oxford University Press
  * Summary: HPODNets employs a deep 8-layer GCN to integrate multiple biomolecular interaction networks and capture high-order topological features for predicting HPO-based protein–phenotype associations. It outperforms seven existing methods including HPI-SAGA, DeepGO, NetGO, GOLabeler, TMC, Mashup, and deepNF. 

- Phenotype prediction in plants is improved by integrating large-scale transcriptomic datasets
  * Venue:  NAR Genomics and Bioinformatics, Oxford University Press, 2024 (Advance Access published: 27 Dec 2024)
  * Summary: This study used 21,612 maize RNA-seq samples to train ML models that predict plant phenotypes using only highly variable genes (HVGs), achieving high accuracy across tissue types, developmental stages, cultivars, and stress conditions. A similar framework was applied to rice, showing partial cross-species generalization, though performance dropped due to HVG divergence. Results suggest ML models built on transcriptome data can guide precise crop phenotype prediction.

- TrG2P: A transfer-learning-based tool integrating multi-trait data for accurate prediction of crop yield
  * Venue: Plant Communications, Volume 5, Issue 7, July 08, 2024
  * Summary: TrG2P applies transfer learning using CNNs to improve crop yield prediction by pretraining on non-yield traits and fine-tuning on yield data. Tested on maize, rice, and wheat, it outperformed rrBLUP, RF, SVR, LightGBM, CNN, DeepGS, and DNNGP, boosting accuracy by up to 39.9%. The improvement is attributed to multi-trait information transfer and dataset augmentation.

