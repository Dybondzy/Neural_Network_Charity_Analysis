# Neural_Network_Charity_Analysis

Module 19

Background
Bek’s come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively
What You're Creating
This new assignment consists of three technical analysis deliverables and a written report. You will submit the following:

Deliverable 1: Preprocessing Data for a Neural Network Model
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb

Deliverable 2: Compile, Train, and Evaluate the Model
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb

Deliverable 3: Optimize the Model
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimzation.ipynb

Deliverable 4: A Written Report on the Neural Network Model (README.md)

Files
Use the following links to download the dataset and starter code.

Alphabet Soup Charity dataset (charity_data.csv) (Links to an external site.)

Alphabet Soup Charity starter code (Links to an external site.)
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/edit/main/README.md

Before You Start
Create a new GitHub repository entitled "Neural_Network_Charity_Analysis" and initialize the repository with a README.

Deliverable 1: Preprocessing Data for a Neural Network Model (30 points)
Deliverable 1 Instructions
Using your knowledge of Pandas and the Scikit-Learn’s StandardScaler(), you’ll need to preprocess the dataset in order to compile, train, and evaluate the neural network model later in Deliverable 2.
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb

Deliverable 1.

Open the AlphabetSoupCharity_starter_code.ipynb file, rename it AlphabetSoupCharity.ipynb, and save it to your Neural_Network_Charity_Analysis GitHub folder.

Using the information we have provided in the starter code, follow the instructions to complete the preprocessing steps.

Read in the charity_data.csv to a Pandas DataFrame, and be sure to identify the following in your dataset:
What variable(s) are considered the target(s) for your model?
What variable(s) are considered the feature(s) for your model?
Drop the EIN and NAME columns.
Determine the number of unique values for each column.
For those columns that have more than 10 unique values, determine the number of data points for each unique value.
Create a density plot to determine the distribution of the column values.
Use the density plot to create a cutoff point to bin "rare" categorical variables together in a new column, Other, and then check if the binning was successful.
Generate a list of categorical variables.
Encode categorical variables using one-hot encoding, and place the variables in a new DataFrame.
Merge the one-hot encoding DataFrame with the original DataFrame, and drop the originals.
At this point, your merged DataFrame should look like this:

The merged DataFame shows four columns: STATUS, ASK_AMT, IS_SUCCESFUL, APPLICATION_TYPE_Other,  APPLICATION_TYPE_T_10, APPLICATION_TYPE_T19, APPLICATION_TYPE_T3 and contains 5 rows and 44 columns.

Split the preprocessed data into features and target arrays.
Split the preprocessed data into training and testing datasets.
Standardize numerical variables using Scikit-Learn’s StandardScaler class, then scale the data.
Save your AlphabetSoupCharity.ipynb file to your Neural_Network_Charity_Analysis folder.
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb

Deliverable 1 Requirements
You will earn a perfect score for Deliverable 1 by completing all requirements below:

The following preprocessing steps have been performed:
The EIN and NAME columns have been dropped (5 pt)
The columns with more than 10 unique values have been grouped together (5 pt)
The categorical variables have been encoded using one-hot encoding (5 pt)
The preprocessed data is split into features and target arrays (5 pt)
The preprocessed data is split into training and testing datasets (5 pt)
The numerical values have been standardized using the StandardScaler() module (5 pt)
Deliverable 2: Compile, Train, and Evaluate the Model (20 points)
Deliverable 2 Instructions
Using your knowledge of TensorFlow, you’ll design a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. You’ll need to think about how many inputs there are before determining the number of neurons and layers in your model. Once you’ve completed that step, you’ll compile, train, and evaluate your binary classification model to calculate the model’s loss and accuracy.
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimzation.ipynb

Continue using the AlphabetSoupCharity.ipynb file where you’ve already performed the preprocessing steps from Deliverable 1.
Create a neural network model by assigning the number of input features and nodes for each layer using Tensorflow Keras.
Create the first hidden layer and choose an appropriate activation function.
If necessary, add a second hidden layer with an appropriate activation function.
Create an output layer with an appropriate activation function.
Check the structure of the model.
Compile and train the model.
Create a callback that saves the model's weights every 5 epochs.
Evaluate the model using the test data to determine the loss and accuracy.
Save and export your results to an HDF5 file, and name it AlphabetSoupCharity.h5.
Save your AlphabetSoupCharity.ipynb file and AlphabetSoupCharity.h5 file to your Neural_Network_Charity_Analysis folder.
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.hs-20210630T011209Z-001.zip

Deliverable 2 Requirements
You will earn a perfect score for Deliverable 2 by completing all requirements below:

The neural network model using Tensorflow Keras contains working code that performs the following steps:
The number of layers, the number of neurons per layer, and activation function are defined (2.5 pt)
An output layer with an activation function is created (2.5 pt)
There is an output for the structure of the model (5 pt)
There is an output of the model’s loss and accuracy (5 pt)
The model's weights are saved every 5 epochs (2.5 pt)
The results are saved to an HDF5 file (2.5 pt)
Deliverable 3: Optimize the Model (20 points)
Deliverable 3 Instructions
Using your knowledge of TensorFlow, optimize your model in order to achieve a target predictive accuracy higher than 75%. If you can't achieve an accuracy higher than 75%, you'll need to make at least three attempts to do so.


Adjusting the input data to ensure that there are no variables or outliers that are causing confusion in the model, such as:
Dropping more or fewer columns.
Creating more bins for rare occurrences in columns.
Increasing or decreasing the number of values for each bin.
Adding more neurons to a hidden layer.
Adding more hidden layers.
Using different activation functions for the hidden layers.
Adding or reducing the number of epochs to the training regimen.
NOTE
You will not lose points if your model does not achieve target performance, as long as you make three attempts at optimizing the model in your AlphabetSoupCharity_Optimzation.ipynb file.

Follow the instructions below and use the information file to complete Deliverable 3.

Create a new Jupyter Notebook file and name it AlphabetSoupCharity_Optimzation.ipynb.
Import your dependencies, and read in the charity_data.csv to a Pandas DataFrame.
Preprocess the dataset like you did in Deliverable 1, taking into account any modifications to optimize the model.
Design a neural network model, taking into account any modifications that will optimize the model to achieve higher than 75% accuracy.
Create a callback that saves the model's weights every 5 epochs.
Save and export your results to an HDF5 file, and name it AlphabetSoupCharity_Optimization.h5.
! ! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimization.h5

Save your AlphabetSoupCharity_Optimzation.ipynb file and AlphabetSoupCharity_Optimization.h5 file to your Neural_Network_Charity_Analysis folder.
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimzation.ipynb

Deliverable 3 Requirements
You will earn a perfect score for Deliverable 3 by completing all requirements below:

The model is optimized, and the predictive accuracy is increased to over 75%, or there is working code that makes three attempts to increase model performance using the following steps:
Noisy variables are removed from features (2.5 pt)
Additional neurons are added to hidden layers (2.5 pt)
Additional hidden layers are added (5 pt)
The activation function of hidden layers or output layers is changed for optimization (5 pt)
The model's weights are saved every 5 epochs (2.5 pt)
The results are saved to an HDF5 file (2.5 pt)
Deliverable 4: A Written Report on the Neural Network Model (30 points)
Deliverable 4 Instructions
For this part of the Challenge, you’ll write a report on the performance of the deep learning model you created for AlphabetSoup.

The report should contain the following:

Overview of the analysis: Explain the purpose of this analysis.

Results: Using bulleted lists and images to support your answers, address the following questions.

Data Preprocessing
What variable(s) are considered the target(s) for your model?
What variable(s) are considered to be the features for your model?
What variable(s) are neither targets nor features, and should be removed from the input data?
Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
Were you able to achieve the target model performance?
What steps did you take to try and increase model performance?
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

Deliverable 4 Requirements
You will earn a perfect score for Deliverable 4 by completing all requirements below:

Structure, Organization, and Formatting (6 points)
The written analysis has the following structure, organization, and formatting:

There is a title, and there are multiple sections (2 pt)
Each section has a heading and subheading (2 pt)
Links to images are working, and code is formatted and displayed correctly (2 pt).
Analysis (24 points)
The written analysis has the following:

Overview of the loan prediction risk analysis:

The purpose of this analysis is well defined (4 pt)
Results:

There is a bulleted list that answers all six questions (15 pt)
Summary:

There is a summary of the results (2 pt)
There is a recommendation on using a different model to solve the classification problem, and justification (3 pt)
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/edit/main/README.md

As a reminder, the deliverables for this Challenge are as follows:

Deliverable 1: Preprocessing Data for a Neural Network Model
Deliverable 2: Compile, Train, and Evaluate the Model
Deliverable 3: Optimize the Model
Deliverable 4: A Written Report on the Neural Network Model (README.md)
Upload the following to your Neural_Network_Charity_Analysis GitHub repository:

Your AlphabetSoupCharity.ipynb file for Deliverables 1 and 2.
Your AlphabetSoupCharity.h5 file for Deliverables 1 and 2.
Your AlphabetSoupCharity_Optimzation.ipynb file for Deliverable 3.
Your AlphabetSoupCharity_Optimzation.h5 file for Deliverable 3.
An updated README.md that has your written report.
! https://github.com/Dybondzy/Neural_Network_Charity_Analysis/edit/main/README.md
