# ML_final_project
[111上] NYCU ML 的 final project
## Introduction
* Competition from <https://www.kaggle.com/competitions/tabular-playground-series-aug-2022/overview>  
* Mainly using RUSBoostClassifier from [imbalanced-ensemble](https://imbalanced-ensemble.readthedocs.io/en/latest/api/ensemble/_autosummary/imbalanced_ensemble.ensemble.RUSBoostClassifier.html#imbalanced_ensemble.ensemble.RUSBoostClassifier)  
* Prediction is produced by taking average from four models' preiction, two using all features, the others using selected features.  
## Rebuilding
This project was implemented by __Google Colab__
1. Downloads pretrained models from [__Models link__](https://drive.google.com/drive/folders/19EJSsf3mmSUNqthTP7i4VzodjZz3AsN4?usp=sharing)
2. Run “pip install imbalanced-ensemble”, and __RESTART RUNTIME__ after it finished.
3. Change __TRAIN_PATH__, __TEST_PATH__, and __MODEL_PATH__.
4. Run all.
## Environment
Using Google Colab, with installing imbalanced-ensemble, should restart runtime after pip install.  
| Package |
|---------|
|Python 3.8.16|
|imbalanced ensemble 0.1.7|
|numpy 1.16.0|
|pandas 1.1.3|
|scikit learn 1.0|
## Data Pre-proccessing
1. Drop unneeded column: “product_code”.
2. Transform “attribute_0”, “attribute_1” from strimbalanced ensemble 0.1.7|
|numpy 1.16.0|
|pandas 1.1.3|
|scikit learn 1.0|ing to int, using its material code.
3. Add column “measurement_5_wasmissing”, ” measurement_4_wasmissing”, by setting attributes which “measurement_5”, ” measurement_4” is Nan into 1, others as 0.
4. Set another dataset with selected features: "loading", "measurement_17", "measurement_6", "measurement_4", "measurement_2", "measurement_5_wasmissing", "attribute_3", "attribute_1", "measurement_9", "measurement_4_wasmissing", "measurement_7", "attribute_0", "failure".  
## Result
My model achieve the following performance on submission.
|Model|Private Score|Public Score|
|-----|-------------|------------|
|averag of best 4|0.59141|0.57584|
