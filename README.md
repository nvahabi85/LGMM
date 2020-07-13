### LGMM

## DATA
We collected county-level cumulative COVID-19 confirmed cases and death from March 25 to June 3, 2020, across the contiguous United States from USAFacts (usafacts.org). MIR, as a proxy for survival rate, is calculated by dividing the number of confirmed deaths in each county by the confirmed cases in the same county at the same time-period multiplied by 100. MIR ranges from 0%-100%, 100% indicating the worst situation where all the confirmed cases have died.
Thirty-four potential risk factors (covariates), including county-level MR of comorbidities & disorders, demographics & social factors, and environmental factors were retrieved from the University of Washington Global Health Data Exchange (http://ghdx.healthdata.org/us-data). "Comorbidities & disorders" include CVD, cardiomyopathy and myocarditis and myocarditis, hypertensive heart disease, peripheral vascular disease, atrial fibrillation, cerebrovascular disease, hepatitis, HIV/AIDS, tuberculosis (TB), lower respiratory infection, interstitial lung disease and pulmonary sarcoidosis, asthma, COPD, ischemia, mesothelioma, tracheal cancer, leukemia, pancreatic cancer, rheumatic disease, drug use disorder, and alcohol use disorder. "Demographics & social" factors include age, female African American%, female white American%, male African American%, male white American%, Asian%, smokers%, unemployed%, income rate, and uninsured%. "Environmental" factors include air quality index (AQI), temperature, and PM. 

## CODE
Part1: R-code for the univariate/multiple GEE models, and the multinomial model 
Part2: M-plus script to run an 8-class LGMM model.
