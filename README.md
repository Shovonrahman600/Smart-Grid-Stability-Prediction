# Improved-Ensemble-Machine-Learning-Framework-for-Superior-Smart-Grid-Stability-Prediction
Paper link:https://ieeexplore.ieee.org/abstract/document/11490240 
DOI: 10.1109/ICCIT68739.2025.11490240
Adding renewable energy sources to the power grid has become essential as population growth continues to increase electricity demand. The rising use of fossil fuels, the impact of global warming, and the falling costs of renewable technologies have made it essential to incorporate them into the grid grid a major requirement. The developed countries have already taken steps toward this integration. The rise of smart grids marks a major change in power systems to address these challenges. In this model, consumers, producers, and those who play both roles are smartly connected, with the main aim of ensuring electricity that is reliable, cost-effective, secure, and sustainable.
## Setting Up 
The model is developed on the following system environments,

    python 3.8
    tensorflow 2.7.

Use the following steps to run the model. In the future update the readme file will be modified accordingly.

    clone the repository into the local machine.
    download the data files from drive link above and into the dataset directory.
    run ipynb file
## Dataset
The data employed in this machine learning exercise consists of grid stability simulation results of a base 4-node star network with one generation center node and three consumer nodes equal the ”four” total nodes. Two widely utilized datasets for predicting the SG stability have been taken into account in this study. Both datasets share the same feature and target columns. The entire data set of each dataset varies. The augmented dataset has 60K samples, while the original dataset has 10K samples. There are two dependent labels and twelve features for both the raw as well as the augmented database. One dependent variable can be handled best by regression, whereas the other can be handled best by classification. The proposed models treat the two dependent labels of the datasets independently for only the classification phases. The dataset includes important electrical characteristics like voltage levels (V1, V2), active and reactive power outputs (P1, P2, Q1, Q2), and frequency deviations (f). These are all things that modern smart grids keep an eye on with sensors and AMI systems. It also has dynamic parameters like rotor angle deviations (delta1, delta2) and load time constants (tau1, tau2), which record important transient behaviors. These variables all fit with industry-standard stability metrics, so the dataset is a good stand-in for early-stage algorithm development.
## Feature Importance

<img width="836" height="470" alt="image" src="https://github.com/user-attachments/assets/76b9ffbf-e7ac-4701-8bf2-5281b57e3840" />

The relative value of each model feature is displayed in fig, which indicates that the generator-related features (g1-g4) and the tau parameters have the greatest contributions to the prediction. In contrast, the power characteristics p1–p4 display considerably lesser relevance. Overall, the graphic shows that generator characteristics and system time constants have a significant impact on the model’s output.

## Model Build Up


<img width="1532" height="801" alt="image" src="https://github.com/user-attachments/assets/2743926a-d855-4c80-b10e-3b30371bc43e" />

Stacking is an ensemble strategy that creates a more refined final output by learning from the predictions of multiple algorithms to develop a new model. Using stacking and Logistic Regression as the meta-learner, this work combined the advantages of several machine learning models to produce the final prediction. By combining the outputs of the underlying models, the meta-learner which might be any appropriate algorithm improves predictive performance beyond that of any one model alone. The suggested stacking ensemble structure used to forecast the smart grid’s stability
## Results

<img width="1653" height="993" alt="Picture1" src="https://github.com/user-attachments/assets/8df5e51a-0c75-4590-acfd-51406dcaa97a" />

Metric Score
Accuracy 99.18%
F1-score 98.90%
ROC AUC 99.14%
Precision 98.83%
Recall 98.96%

## Confusion Matrix


<img width="544" height="558" alt="image" src="https://github.com/user-attachments/assets/e48cf575-75b2-455a-b534-4197028e293c" />

According to these findings, the model consistently maintains a very low misclassification rate for both classes, with a notably higher number of accurate predictions than errors. The equilibrium between true positives and true negatives demonstrates how accurately the stacking technique handles both groups.


<img width="590" height="381" alt="image" src="https://github.com/user-attachments/assets/58ddb2f0-5d39-410d-bf3d-faaeadbfd012" />

The Area Under the Curve (AUC) is the primary evaluation metric used in the ROC AUC curve comparison, This demonstrates the classification performance of different machine learning models. The proposed Stacking Classifier produced a flawless AUC of 1.00, clearly surpassing all other models. This implies that the stacking strategy has the best ability to distinguish between positive and negative classes with almost no trade-off between actual positive and false positive rates.

