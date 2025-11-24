# Information about the contents

This folder contains a set of trained models for forecasting the quality check of the production of brake discs.
The models focus on a specific cast-iron and a specific product type.
Scalers and Models are separated in different folders.

Classifiers are trained through scikit learn (decision tree) while Neural Networks are trained through keras 2.5

## Scalers:
The scalers are available in the pkl files, with the format:
scalerType_castIronType_productType_targetVariable.pkl
where, scalerType:
- inScaler: input scaler
- outScaler: output scaler
For classifiers, only the input scalers are available, while for NN both input and output scalers are available.


## Models:
The format of the file is the following:
modelType_castIronType_productType_targetVariable.[keras, pkl]

Where, 
- Model type:
	- nn: neural networks
	- dtc: decision tree classifier
- Cast-iron type:
	- castIron 1: High carbon
	- castIron 2: grey cast-iron
- Target variable:
	- micro-shrinks: the occurrence of micro-shrinks defects (1: defect, 0: nominal)
	- cementite: the occurrence of cementite defects (1: defect, 0: nominal)
	- frequency: the natural frequency of the brake disc (UoM: [Hz])
	
## Inputs:
All the models have the same set of inputs. In the right order:
- chemical analysis at the pouring:
	- IN_Element_CLF, where Element is in the following list [C, Si, Mn, P, S, Cr, Cu, Mo, Sn, Ti, Al, Pb, W, Ni, V, Nb]
- thermal analysis at the pouring:
	- IN_Type_TLF, where Type is in the following list: [Tliquidus, TeStart, TeMin, TeI, TeMax, TSolidus, Rec, Apr, PAE, VPS, tA, tB, tC, tD, tE]
- Pouring parameters:
	- IN_Temperature[°C]: the pouring temperature
	- inoculant quantity[g]: the mass of inoculant injected 

