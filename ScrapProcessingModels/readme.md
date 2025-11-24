# Information about the contents
This folder contains a set of trained models for forecasting the total mass of sterile contents and contaminants in the scraps.
3 models are available, for plantA, plantB, plantC.

The models are stored in pkl files, which contain a scikit learn pipeline containing:
- scalers
- oneHotEncodings
- randomForestModel

The input data must be a dictionary or a pandas dataframe.
The input list is the following:
- Origin, a string defining the origin
- Scrap quality, a string defining the scrap quality
- Supplier code, a integer value defining the scrap supplier
- Weight of the scrap load
- Month of the scrap arrival
