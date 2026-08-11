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