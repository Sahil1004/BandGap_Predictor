# BandGap_Predictor
This package offers a machine learning model that has been trained using experimental measurements to predict the bandgap energy (Eg) of inorganic materials through command-line use.  

**Citations**

To cite relative permittivity and centroid shift predictions, please reference the following work:

Zhuo. Y, Mansouri Tehrani., and Brgoch. J, Predicting the band gaps of inorganic solids by machine learning, J. Phys. Chem. Lett. 2018, 9, 1668-1673.

**Prerequisites**

This package requires:

pymatgen
scikit-learn
pandas
NumPy
xlrd

**Usage**

Define a customized prediction set

You should create a .xlsx file named to_predict.xlsx, in which the compositions that are of interest are listed in the first column with the header "Composition". There is an example of the to_predict.xlsx file in the repository.

Predict bandgap energy

After preparing to_predict.xlsx, you can get the Eg prediction by:

python Eg_model.py
Eg_model.py will automatically read elements.xlsx and Training_Set.xlsx to generate a prediction. A classifier will first categorize a composition into metals (Eg = 0) or nonmetals (Eg > 0), then the Eg of nonmetals will be predicted with a regressor. After running, you will get a .xlsx file named predicted.xlsx in the same directory, in which the predicted Eg is provided next to the corresponding composition.
