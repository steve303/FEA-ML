# FEA-ML
This study investigates the use of finite element analysis (FEA) to generate feature data as an alternative to physical parts to train a machine learning (ML) algorithm for the purpose of creating a analytics tool to predict product yield.  The reason why FEA was used was because of the time required (difficulty) to get parts near the ends of the population distribution through random sampling on the factory floor.  As expected, most parts were clustered near the mean which meant only a small portion of the design space was used for training.  This resulted in poor model performance and posed problems in the linear regression model where high leverage points could misrepresent the model since very few points were collected outside the mean.  

The second portion of the study was to use the trained ML model to perform a Monte Carlo simulation to predict the output distrubution of product performance using sub-supplier incoming feature data distributions.  With this analytics method, poor yielding lots could be predicted and prevented from being built.  There are many extensions of this method which could be useful where measurement or procurring physical parts are difficult. 

# Sample Code
A small portion of the data is presented in the sample code file: https://steve303.github.io/FEA-ML/FEA_ML_pres01.ipynb 
