-------------------------------SIMPLE LINEAR REGRESSION-----------------------------

test_data = [[1.0], [2.0], [3.0]]

Expected output:

    y = [ 8. 11. 14.]
    w = 3
    b = 5

Custum Simple Linear Regression model ( epoch = 1000, lr = 0.01):

    Weights : 3.036271684359493
    Bias    : 4.869048

    Predictions     : [ 7.9053, 10.9416, 13.9779]


Scikit-Learn Linear Regression Model:

    Weights   : [3.]
    Bias      : 5.000000

    Predictions     : [ 8. 11. 14.]



-------------------------------MULTIPLE LINEAR REGRESSION-----------------------------


test_data = [[4, 3]]

Expected output: 

    y = 22
    w1 = 2
    w2 = 3
    b = 5

Outputs:

Custum Multiple Linear Regression Model (epoch = 1000, lr = 0.05):

    Final Prediction for [4, 3] by our MultiLR model: 22.11
    custum builted models:	Weights (w1, w2): [2.0140130137387557, 3.0623190849207895] || Bias (Intercept): 4.87

Scikit-Learn Linear Regression Model:

    Final Prediction for [4, 3] by scikit-learn model: 22.00
    scikit-learn models:	Weights (w1, w2): [2. 3.] || Bias (Intercept): 5.00



-------------------------------LOGISTIC REGRESSION-----------------------------

PERFORMANCE COMPARISON:

    Custom Model Accuracy: 88.0%
    SKLearn Model Accuracy: 88.0%

WEIGHTS (Slopes):
    Custom Weights:  [-0.3246  2.04  ]
    SKLearn Weights: [-0.3354  2.0786]

BIAS (Intercept):
    Custom Bias:  0.2179
    SKLearn Bias: 0.2299



-------------------------------DECISION TREE-----------------------------

PERFORMANCE COMPARISON :

    Custom Tree Accuracy:  0.9386
    Sklearn Tree Accuracy: 0.9474

    Custom Tree Time:  1.7376 seconds
    Sklearn Tree Time: 0.0070 seconds


------------------------------- RANDOM FOREST V/S SKLearn GRADIENT BOOSTING V/S XGBoost ----------------------------- 


        Model  CV Best ROC-AUC  Test ROC-AUC  Minority Recall  Minority Precision  Minority F1  Macro F1  Search Time (s)

      XGBoost           0.9735        0.9781           0.8522              0.9402       0.8941    0.9343            64.38
   SklearnGBC           0.9712        0.9770           0.7931              0.9527       0.8656    0.9174           107.57
Random Forest           0.9675        0.9716           0.7635              0.9627       0.8516    0.9093            80.61


----------------------------------------------------------------------------------------------------------------------------------
                                                  DETAILED CLASSIFICATION REPORTS PER MODEL
----------------------------------------------------------------------------------------------------------------------------------

---------------------------------------- Random Forest ----------------------------------------

                    precision    recall  f1-score   support

Class 0 (Majority)     0.9428    0.9925    0.9670       797
Class 1 (Minority)     0.9627    0.7635    0.8516       203

          accuracy                         0.9460      1000
         macro avg     0.9528    0.8780    0.9093      1000
      weighted avg     0.9468    0.9460    0.9436      1000


---------------------------------------- SklearnGBC ----------------------------------------

                    precision    recall  f1-score   support

Class 0 (Majority)     0.9495    0.9900    0.9693       797
Class 1 (Minority)     0.9527    0.7931    0.8656       203

          accuracy                         0.9500      1000
         macro avg     0.9511    0.8915    0.9174      1000
      weighted avg     0.9501    0.9500    0.9482      1000


---------------------------------------- XGBoost ----------------------------------------

                    precision    recall  f1-score   support

Class 0 (Majority)     0.9632    0.9862    0.9746       797
Class 1 (Minority)     0.9402    0.8522    0.8941       203

          accuracy                         0.9590      1000
         macro avg     0.9517    0.9192    0.9343      1000
      weighted avg     0.9586    0.9590    0.9582      1000



------------------------------- KNN V/S NAIVE BAYES V/S SVM ----------------------------- 


--------------------------------------------------------------------------------
 MODEL: K-Nearest Neighbors (KNN)
 Best Params: {'clf__metric': 'manhattan', 'clf__n_neighbors': 3, 'clf__weights': 'uniform'}
--------------------------------------------------------------------------------
              precision    recall  f1-score   support

   malignant     0.9750    0.9286    0.9512        42
      benign     0.9595    0.9861    0.9726        72

    accuracy                         0.9649       114
   macro avg     0.9672    0.9573    0.9619       114
weighted avg     0.9652    0.9649    0.9647       114

Confusion Matrix [Rows: Actual, Cols: Predicted]:
  Malignant (0):   39 TN  |   3 FP
  Benign    (1):    1 FN  |  71 TP


--------------------------------------------------------------------------------
 MODEL: Gaussian Naive Bayes
 Best Params: {'clf__var_smoothing': np.float64(1e-11)}
--------------------------------------------------------------------------------
              precision    recall  f1-score   support

   malignant     0.9048    0.9048    0.9048        42
      benign     0.9444    0.9444    0.9444        72

    accuracy                         0.9298       114
   macro avg     0.9246    0.9246    0.9246       114
weighted avg     0.9298    0.9298    0.9298       114

Confusion Matrix [Rows: Actual, Cols: Predicted]:
  Malignant (0):   38 TN  |   4 FP
  Benign    (1):    4 FN  |  68 TP


--------------------------------------------------------------------------------
 MODEL: Support Vector Machine (SVM - RBF)
Best Params: {'clf__C': 10, 'clf__gamma': 0.01}
--------------------------------------------------------------------------------
              precision    recall  f1-score   support

   malignant     0.9762    0.9762    0.9762        42
      benign     0.9861    0.9861    0.9861        72

    accuracy                         0.9825       114
   macro avg     0.9812    0.9812    0.9812       114
weighted avg     0.9825    0.9825    0.9825       114

Confusion Matrix [Rows: Actual, Cols: Predicted]:
  Malignant (0):   41 TN  |   1 FP
  Benign    (1):    1 FN  |  71 TP
