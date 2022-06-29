# FEA-ML
This study investigates the use of finite element analysis (FEA) to generate feature data as an alternative to physical parts to train a machine learning (ML) algorithm for the purpose of predicting VCM manufacturing yield.  The reason why FEA was used was because of the time required and difficulty to get parts near the ends of the population distribution through random sampling on the factory floor.  During random sampling, most parts were clustered near the mean which meant only a small portion of the design space or matrix was used for training.  This resulted in poor model performance and posed problems in the linear regression model where high leverage points could misrepresent the model since very few samples were collected outside the mean.  The advantage of creating virtual parts using FEA, is that we can create samples at any location from the population distribution.  This allowed a broader design matrix to be created which the ML algorthim can train on versus a small subset during random sampling.           

The second portion of the study was to use the trained ML model to perform a Monte Carlo simulation to predict the output distrubution of product performance using sub-supplier incoming feature data distributions.  With this analytics method, poor yielding lots could be predicted and prevented from being built.

One obvious question is, why not just use the FEA model to perform the Monte Carlo simulation.  That is, why go through the trouble of creating a ML model which is simply a mapping function of the FEA results.  The reason is we need to run the FEA model 100,000 or more times.  This simply is not practical because the FEA model can take hours to run whereas the ML model can run in seconds.  

There are many extensions of this method which could be useful where measurement or procurring physical parts are difficult. The other reason is to use the ML model, which produces quick solutions, as a surrogate to the FEA model which is slower. For example, once a ML has been established and has good predictive power, one could use the ML model to perform an exhaustive exploration of the design matrix to locate optimum design points.  Later, the optimum design point, according to the ML model, could be verified running a FEA model.  



# Sample Code
A small portion of the data is presented in the sample code file: FEA_ML_pres01.ipynb (to view click link above)
