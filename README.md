# US_Bandwidth_Enhancement
This directory contains all the code to run all the models as well as code to calculate the metric values for the model outputs.
Each model variation for each architecture has a seperate notebook in total 12. 
So 4 for each architecture: RED-net(residual encoder decoder), U-net and SRCNN. 

The 4 variations are: 
                     M1/Perceptual: The model that uses a combination of perceptual and mse loss
                     M2/ResidualMSE: The model that is trained on the difference between the low and full bandwidth images with a scaled MSE loss.
                     M3/Cascade: The model that is trained on the difference between the output of M2 and the full bandwidth images as output.
                     M4/Double-input: The model that uses the outputs of M1 and M2 as input.

The calculate_metrics notebook contains all the code neccesary to save the RMSE,PSNR,SSIM and gCNR metric values in an excel file for all the models. It also contains code to save either a small part or a full image for all models and test data and saves them in a folder.
