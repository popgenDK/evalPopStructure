# evalPopStructure
PCA evaluation for population structure

Principal component analysis (PCA) is commonly used in genetics to infer and visualize population structure and admixture between populations. PCA is often interpreted in a way similar to inferred admixture proportions, where it is assumed that individuals belong to one of several possible populations or are admixed between these populations. We propose a new method to assess the statistical fit of PCA (interpreted as a model spanned by the top principal components) and to show that violations of the PCA assumptions affect the fit. Our method uses the chosen top principal components to predict the genotypes. By assessing the covariance (and the correlation) of the residuals (the differences between observed and predicted genotypes), we are able to detect violation of the model assumptions. Based on simulations and genome wide human data we show that our assessment of fit can be used to guide the interpretation of the data and to pinpoint individuals that are not well represented by the chosen principal components. Our method works equally on other similar models, such as the admixture model, where the mean of the data is represented by linear matrix decomposition. 


## quick start ( PCA in R)
````
#load functions
source("https://raw.githubusercontent.com/popgenDK/evalPopStructure/main/R/evalPCA.R")

#load matrix with genotypes (geno)
load(url("http://pontus.popgen.dk/albrecht/open/admixTjeck/data.Rdata"))

#perform PCA with genotypes zero mean normalized
 pca <-  makePCA(t(geno),method="standard",center=TRUE,scale=FALSE)
 plot(pca2vectors[,1:2],col=pop,xlab="PC1",ylab="PC2",cex.lab=1.5,main="centered genotypes")
 legend("center",fill=1:4,levels(pop),cex=2,bty="n")

# estimate correlations
res <- evalPCA(pca,k=2)
plotCorRes(res$corres, pop,max=0.1)
````
which produces the plots
![Alt text](data/evalAdmixTestDataPCA2.png?raw=true "Title")
![Alt text](data/evalAdmixTestDataPCA2eval.png?raw=true "Title")

## R code with multiple PCA normalazation examples and ADMIXTURE results
[colab notebook](evalPCA.ipynb)
The notebook can also be run in jypeter or using the colab link (press the "open in colab" link in top of document to run interactively)

## step by step example using the Chen & Storey nomalization
[colab notebook](evalPCA_step_by_step_example_with_Chen%26Storey_PCA.ipynb)
The notebook can also be run in jypeter or using the colab link (press the "open in colab" link in top of document to run interactively)

# citation
Evaluation of population structure inferred by principal component analysis or the admixture model
Jan van Waaij, Song Li, Genís Garcia-Erill, Anders Albrechtsen, Carsten Wiuf
https://arxiv.org/abs/2302.04596

## scripts used in paper
https://github.com/Ginwaitthreebody/evalPCA
