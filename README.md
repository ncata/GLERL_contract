
# GLERL_contract
Code, activity logs, and other documents relevant to operationalizing Dan Buscombe's OWG for use in the Great Lakes.  
This project resides in d/GLERL/'GLERL drive'/njc/src/glerl_contract

### Usage
This code and data can be used to take publically available information and run the OWG.      
In later testing stages, Google Colab was used to reduce computational load on local machines and meet extended GPU RAM requuirements. Extensive testing with various hyperparameters proved that further adjustment was not neccesary. Batch size should not be manipulated beyond under 8 or over 32.   
Since the model being used in the Jupyter Notebook (MobileNetV2) is not supported through tensorflow, further effort should be focused on running the model using the .py files in [Dan's orginal repo](https://github.com/OpticalWaveGauging/OpticalWaveGauging_DNN)   
   
   
These files are optimized to use the example snap data provided and so need to be updated to use the files that will be generated using the code in the prepdata notebook. Training of the model can be incredibly time consuming. Ensuring that the data has been prepared properly and that the hyperparametrs are correctly set will ensure that training and validation occur accordingly. 
