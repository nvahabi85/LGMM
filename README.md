### LGMM

## DATA
We collected county-level cumulative COVID-19 confirmed cases and death from March 25 to June 3, 2020, across the contiguous United States from USAFacts (usafacts.org). MIR, as a proxy for survival rate, is calculated by dividing the number of confirmed deaths in each county by the confirmed cases in the same county at the same time-period multiplied by 100. MIR ranges from 0%-100%, 100% indicating the worst situation where all the confirmed cases have died.

Thirty-four potential risk factors (covariates), including county-level MR of comorbidities & disorders, demographics & social factors, and environmental factors were retrieved from the University of Washington Global Health Data Exchange (http://ghdx.healthdata.org/us-data). "Comorbidities & disorders" include CVD, cardiomyopathy and myocarditis and myocarditis, hypertensive heart disease, peripheral vascular disease, atrial fibrillation, cerebrovascular disease, hepatitis, HIV/AIDS, tuberculosis (TB), lower respiratory infection, interstitial lung disease and pulmonary sarcoidosis, asthma, COPD, ischemia, mesothelioma, tracheal cancer, leukemia, pancreatic cancer, rheumatic disease, drug use disorder, and alcohol use disorder. "Demographics & social" factors include age, female African American%, female white American%, male African American%, male white American%, Asian%, smokers%, unemployed%, income rate, and uninsured%. "Environmental" factors include air quality index (AQI), temperature, and PM. 

## CODE
Part1: R-code for the univariate/multiple GEE models, and the multinomial model 
Part2: M-plus script to run an 8-class LGMM model.

## METHODS
Details of the methods we have used in this study is provided in the Supplementary Materials of the manuscript DOI# 10.21203/rs.3.rs-40632/v1 (https://www.researchsquare.com/article/rs-40632/v1). 
We first provide summary statistics for COVID-19 data for the period under consideration. Full descriptive statistics for n=34 potential risk factors are provided in Table S1. 

Second, we applied GEE marginal approaches to model the COVID-19 MIR over time, and to find the significant risk factors within the U.S. We first used the forward-selection method to select the most relevant risk factors (covariates) using univariate GEE models2 (univariate P-value<0.2 considered a significant). Variables with (multivariate) P-value<0.05 selected as the potential risk factors. We then applied a multivariate GEE model with selected potential risk factors. Variables with (multivariate) P-value<0.05 selected as the risk factors.

Third, we evaluated COVID-19 MIR growth trajectory over the study time using a latent growth model (LGM). An LGM approach considers both the mean MIR differences between counties at each time point (inter-subject) and MIR growth trajectories over time (intra-subject). We also calculated Moran’s I3 to evaluate the spatial autocorrelation of COVID-19 MIR across the U.S. counties.

Forth, we identified clusters of the U.S. counties based on the COVID-19 MIR growth trajectory over time using longitudinal LGMMs4. Information criteria such as AIC, BIC, and a bootstrap likelihood ratio test (BLRT), and a relative entropy (REN5) statistic greater than 0.8 were used to find the optimum number of the clusters. Geographical distribution of the clusters was illustrated in a color-coded geographical map using ArcGIS 10.7 (ESRI, Redland, CA).
