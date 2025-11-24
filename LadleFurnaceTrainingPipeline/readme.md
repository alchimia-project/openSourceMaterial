# LF Model training pipeline.
In this folder you can find a jupiter notebook with the main functions and pipelines for training the components of the Ladle Furnace (LF) Model.
The ladle furnace model is composed of two neural networks for predicting:
- the final steel chemical composition
- the final steel temperature

These two models exploit simple feed forward neural networks, composed of two dense layers connected in series and a final linear layer.

The inputs of the models are the following:
- ScrapWeight,
- StartTemperature
- Argon
- Energy
- Starting chemical composition: LF_CA_ELEMENT_S
- Chemical additions (in terms of the main elements added):
    - Ca, F, Si, C, S, O, N, B, Al, Fe, P, Mg, Zn, Cu, V, Mn, Cr, Ti
	
The possible targets are:
- Final chemical composition: LF_CA_ELEMENT_F
- Final temperature

