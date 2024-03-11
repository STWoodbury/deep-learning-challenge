# deep-learning-challenge

## Overview:

The purpose of this analysis is to create a binary classification model using deep learning techniques to predict whether organizations funded by the non-profit organization, Alphabet Soup will be successful in their ventures. 

The analysis uses past data from funding campaigns ad involves data preprocessing using python and pandas to isolate, bin and create dummies of categorical data for use as model features for predictive modeling. After preprocessing, a neural network is designed with keras, and the model is tuned in an effort to achieve a target predictive accuracy higher than 75%. 

## Results:
<ul>
<li><b>Data Preprocessing</b></li>
    <ul>
    <li>Target Variable: Is_Successful (a binary measure of whether or not funded applicants met their goals)</li>
    </ul>
    <ul>
    <li>Feature Variables:</li>
        <ul>
        <li>Application Type: An internal classification of applications</li>
        <li>Affiliation: The sector or industry of the applicant</li>
        <li>Classification: the government organization classification</li>
        <li>Use Case: the use case for the funding</li>
        <li>Organization: The organization type of the applicant</li>
        <li>income amt: the income classification of the applicant</li>
        <li>Special Considerations: special considerations for the application (binary Y or N)</li>
        <li>Ask Amount: funding amount requested (this was found to be uncorrelated and etraneous to the analysis)</li>
        <li>Status: and active status (this was found to be uncorrelated and etraneous to the analysis)</li>
        </ul>
    </ul>
    <ul>
    <li>Removed Variables: The following were removed from the dataset as they were neither features or targets and did not contribute to the predictive power of the model.</li>
        <ul>
        <li>EIN: the employer identification number</li>
        <li>Name: the name of the applicant</li>
        </ul>
    </ul>
    <li><b>Compiling, Training, and Evaluating the Model:</b></li>
        <ul>
        <li>Structure: The initial structure was based on the following, as gleaned from research:</li>
            <ul>
            <li>Input layer: This layer had 38 neurons: 1 for each feature and 1 for bias<li>
            <li>Hidden layer: There was one hidden layer with 25 neurons (2/3 the size of the input layer, plus the entire output layer)
            <li>Output layer: 1 neuron, chosen due to the binary categorization of the target.<li>
            <li>The activation functions for the input and hidden layers were both relu to allow for non-linear tranformation, and to increase the computational efficiency of the model. The output layer used sigmoid due to the binary categorization of the target</li>
            </ul>
        </ul>
        <li>Model Performance:</li>
            <ul>
            <li>The analysis attempted to optimize the model with the following methods:</li>
                <ul>
                <li>Increasing the hidden layers and neurons</li>
                <li>Feature Selection using CHI2 and p-value</li>
                <li>Adjusting the train-to-test ratio to 90/10%</li>
                <li>Doubling the number of Epochs the model used to train</li>
                </ul>
            <li>Despite these adjustments, the origninal model perfomed best with a predictive accuracy of .73, missing our target of 75%
            </ul>
        </ul>
    </ul>
</Ul>

##Summary:

The deep learning model created by this analysis was able to achieve a predictive accuracy of 73%. This is not up to the target range of 75%, and so some revision may be necessary to achieve target accuracy. Recommendations for improvement include trying alternative neural network architectures, increasing the available training data, or exloring ensemble methods to compare performance and achieve more accurate results. Using the data provided, a single model is ineffective for achieving the target accuracy and so each of these methods would be a potential step forward in that direction.  

