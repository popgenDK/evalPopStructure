# evalPopStructure
PCA evaluation for population structure

Principal component analysis (PCA) is commonly used in genetics to infer and visualize population structure and admixture between populations. PCA is often interpreted in a way similar to inferred admixture proportions, where it is assumed that individuals belong to one of several possible populations or are admixed between these populations. We propose a new method to assess the statistical fit of PCA (interpreted as a model spanned by the top principal components) and to show that violations of the PCA assumptions affect the fit. Our method uses the chosen top principal components to predict the genotypes. By assessing the covariance (and the correlation) of the residuals (the differences between observed and predicted genotypes), we are able to detect violation of the model assumptions. Based on simulations and genome wide human data we show that our assessment of fit can be used to guide the interpretation of the data and to pinpoint individuals that are not well represented by the chosen principal components. Our method works equally on other similar models, such as the admixture model, where the mean of the data is represented by linear matrix decomposition. 





# R code with multiple PCA normalazation examples and ADMIXTURE results
[colab notebook](evalPCA.ipynb)
The notebook can also be run in jypeter or using the colab link (link in top of document)


# step my step example using the Cehn & Storey nomalization
[colab notebook](evalPCA_step_by_step_example_with_Chen%26Story_PCA.ipynb)
The notebook can also be run in jypeter or using the colab link (link in top of document)

# citation
Evaluation of population structure inferred by principal component analysis or the admixture model
Jan van Waaij, Song Li, Genís Garcia-Erill, Anders Albrechtsen, Carsten Wiuf
https://arxiv.org/abs/2302.04596

## scripts used in paper
https://github.com/Ginwaitthreebody/evalPCA
