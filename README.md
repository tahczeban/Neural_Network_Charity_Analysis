# Neural_Network_Charity_Analysis
MODULE 19

![image](https://user-images.githubusercontent.com/90135381/158728342-b5af1520-0e50-4350-b6a7-67d94aaba4cf.png)


_____________
***RESOURCES:***

IMAGE obtained from: https://www.google.com/search?q=neural+network+png&client=safari&rls=en&sxsrf=APq-WBvSO03A2x_EOGPG5farh_VZJq_Asw:1647486007940&tbm=isch&source=iu&ictx=1&vet=1&fir=XZ_juTWZWKbSGM%252Cu9zd-tqA_aFABM%252C_%253BuXBGLLUgyByDYM%252CrqkqCs8r6_WhfM%252C_%253BY2H80jdVb0PGpM%252CkWSLhpAFhxAM9M%252C_%253Bx4GV4wojKQpwSM%252CnyFviiNER8SVKM%252C_%253B2C-j0zMonIHVVM%252C1WZUytvpCoxRyM%252C_%253BMhycC_T2f88kLM%252C8z9c-H0HzmMdoM%252C_%253BtZ_eHORXPRizzM%252CVABu_aoLH5aOYM%252C_%253B3H6iTkkkskaEUM%252C--CNOEusv_-DiM%252C_%253BFv0CmRNk1sbQxM%252CrqkqCs8r6_WhfM%252C_%253B1E-Ei4rBcVOqVM%252CP2Cge2RcKWHTJM%252C_%253BYNudwgHh9uoLEM%252CcrfOpdFQOd1VnM%252C_%253B8ybo2srHe8-r9M%252CTuGZk4cFtXfkAM%252C_&usg=AI4_-kRbAFvkDsAWCp9UYf-oO-cDQIEu0A&sa=X&ved=2ahUKEwiB05nSk8z2AhVTds0KHYWyBwYQ9QF6BAg4EAE&biw=1028&bih=1069&dpr=2#imgrc=I3j8tmTn4ytZAM

*DATA:*  AlphabetSoupCharity_starter_code.ipynb, charity_data.csv

*SOFTWARE:* Jupyter Notebook/Pandas, Python/VSC, Google Colab: 

Limitations of this challenge: M1 processor incompatible with Tensorflow installation on Jupyter Notebook; therefore, challenge completed on Google Colab, per instructional team.
______________
***OVERVIEW:***

In this challenge, a contribution to help Beks with investment placement predictions for Alphabet Soup was implemented,  considering the utilization of artificial neural networks (ANN) and Machine Learning (ML). Algorithms were created to recognize what the patterns and features of input were and then give a quantitative output/binary classifier, in order to predict the success of the applicant, if funded by Alphabet Soup. The steps necessary to complete this task are as follows:

1. Preprocess the data 
2. Compile, train and evaluate model
3. Then attempt to optimize it for improved accuracy
4. Lastly compose a written analysis of the model


______________
***RESULTS:***

***DELIVERABLE 1: PREPROCESSING DATA FOR A NEURAL NETWORK MODEL***

For this Deliverable, Pandas and Scikit-Learn's StandardScaler() were implemented and a Pandas DF was created from the charity_data.csv file.First, the "EIN" and "NAME" columns were then dropped and data points for unique values were obtained. Density plots were created (FIGURES: 1-2) to determine column distribution and the bin cutoff points for "rare" categorical variables, which were placed in 'other' column. Categorical variables were encoded with one-hot encoding and were placed in a new DF (FIGURE:3). Lastly, the preprocessed data was split into features and target arrays, as well as training and testing datasets, at which point the numerical variables were standardized with StandardScaler and the data was scaled.


 <img width="1423" alt="DEL1-counts of APPLICATION_TYPE" src="https://user-images.githubusercontent.com/90135381/159174868-b1404df2-76f7-4deb-b979-cc2a54099553.png">

                      FIGURE 1: Counts of "APPLICATION_TYPE"


 <img width="1407" alt="DEL1-counts of CLASSIFICATION" src="https://user-images.githubusercontent.com/90135381/159174870-00f748b7-d1ed-4674-b126-3abea486c575.png">
 
                      FIGURE 2: Counts of "CLASSIFICATION"


<img width="1378" alt="DEL1-DF" src="https://user-images.githubusercontent.com/90135381/159174876-27c861d8-117a-485c-90d4-6a38eb667005.png">




                       FIGURE 3: DataFrame

***DELIVERABLE 2: COMPILE, TRAIN, EVALUATE THE MODEL***

Pandas was supposed to be utilized for this Deliverable for ML design with TensorFlow; however, there were complications with installation due to M1 processor incompatibility despite attempted resolutions from Stackoverflow; therefore, the same model design was completed on Google Colab (per instructional team suggestion). A predictive binary classification model was designed to determine success of Alphabet Soup funding based on features from the data. The number of features and nodes for each layer, as well as the activation functions. An output layer with it's associated activation function  was then created, model structure was checked, compiled and training was introduced. A callback was created, saving the model's weights every 5 epochs and the model was evaluated (FIGURES:4-5). Finally, the results were exported to an HDF5 file and renamed.



<img width="1411" alt="DEL2-model evaluation" src="https://user-images.githubusercontent.com/90135381/159174883-cfd5c259-57b6-4ea8-a888-ec7ffabcb750.png">

                       FIGURE 4: Model evaluation

<img width="1440" alt="DEL2-weights:5epochs" src="https://user-images.githubusercontent.com/90135381/159183600-30005e26-bbd2-4f97-aa1e-fe160ea02e46.png">


                       FIGURE 5: Saved Weights/5 epochs       

***DELIVERABLE 3: OPTIMIZE THE MODEL***

TensorFlow was utilized in order to attempt to optimize the model to attain a target predictive accuracy greater than 75%. Three attempts were made via:

1. Changing the hidden layers (FIGURES: 6-7)
2. Changing the # of nodes (FIGURES: 8-9)
3. Changing activation functions (FIGURES: 10-11)

A callback was again created to save the weights every 5 epochs and the results were exported to an HDF5 file as AlphabetSoupCharity_Optimization.h5.


<img width="1431" alt="DEL3-1change hidden layers" src="https://user-images.githubusercontent.com/90135381/159175470-9ea6a35b-7564-4e81-9662-c4420ed9d51a.png">

                        FIGURE 6: Change Hidden Layers

<img width="1440" alt="DEL3-1 accuracy" src="https://user-images.githubusercontent.com/90135381/159175479-c4b9cf33-a9f0-43c6-8b1d-b70f5f15cffa.png">


                        FIGURE 7: Accuracy/Loss

<img width="1431" alt="DEL3-2change nodes" src="https://user-images.githubusercontent.com/90135381/159175490-737b9a55-71f3-44d7-81e9-1dff2c4af053.png">


                        FIGURE 8: Change # Nodes

<img width="1440" alt="DEL3-2" src="https://user-images.githubusercontent.com/90135381/159175496-4c5273e9-98d0-498f-8b0d-4291ec390a39.png">

                        FIGURE 9: Accuracy/Loss


<img width="1431" alt="DEL3-3change activation fxn" src="https://user-images.githubusercontent.com/90135381/159175520-76bcb424-bdf1-486c-80ff-704dcb6ca54f.png">

                         FIGURE 10: Change Activation Function


<img width="1421" alt="DEL3-3" src="https://user-images.githubusercontent.com/90135381/159175523-951fcc25-611d-4520-8911-3453aa85a4bb.png">

                         FIGURE 11: Accuracy/Loss

_______________
***DELIVERABLE 4: WRITTEN REPORT/SUMMARY***

For this last Deliverable an analysis of the ML model was complied with the following 6 considerations:

**DATA PREPROCESSING:**

1) The target variable is in: "IS_SUCCESSFUL" (which depicts if successful with Alphabet Soup funding)
2) The features variables are:
 
- APPLICATION_TYPE (Alphabet Soup application)
- AFFILIATION (sector of industry)
- CLASSIFICATION (Gov't org classification)
- USE_CASE (for funding)
- ORGANIZATION (type)
- STATUS (active)
- INCOME_AMT (income class)
- SPECIAL_CONSIDERATIONS (for application)
- ASK_AMT (funding requested)

3) The variables that should be removed are as they are neither targets nor features are: "EIN" and "NAME"

**COMPILING, TRAINING and EVALUATING THE MODEL:**

4) Alterations to hidden layers, neurons and activation functions were completed as follows:

   -changed the number of hidden layers from 2: to 4 (to increase mathematical functions to attempt to improve output accuracy)
   
   -changed number of nodes from 50, 20 to: 100, 50 (to attempt to increase perceptrons with weighted input connections combinations to improve accuracy)

   -changed activation functions from relu, relu to: sigmoid, linear (for attempted improved learning of patternsto improve output accuracy)

5) No, I was not able to acheive the target model performance of 75%. The models created yielded the following parameters, model_loss and Accuracy:

     original: params=3,291/model loss=0.5564/Accuracy=0.7254
 
     change hidden layers: params= 3,911/model loss=0.5553/Accuracy=0.7251
 
     change # nodes:params=9,601/model loss=0.5570/Accuracy=0.7249
 
     change activation function:params=3291/model loss=0.5533/Accuracy=0.7243

6) In conclusion, after three attempts, the ML model was still unable to attain 75% or higher accuracy, despite the steps of increasing hidden layers, #  of nodes and activation functions to improve model performance.

   Possible Recommendations:

    -could further increase the number of hidden layers

    -possibly increase dataset size, if feasible

    -try Random Forest Classifier with increaedto reduce potential for outlier influence

_______________
***REFERENCES:***. BCS, Google, Stackoverflow, GitHub
