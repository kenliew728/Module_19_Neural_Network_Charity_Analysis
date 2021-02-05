# **Neural Network Charity Analysis**

## ***Objectives***
The objective of this analysis is to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. 

## ***Data Source***
The data source is in a form of CSV file containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. 

## **Results**

### *Data Preprocessing*

1. Variables(s) considered as target(s) for the model
   -   The IS_SUCCESSFUL variable is set as a target for the model
  
2. Variable(s) considered as feature for the model
   - The following variables were considered as feature for the model
     - Application type
     - Affiliation
     - Classification
     - Use case
     - Organization
     - Income Amt
     - Ask Amt

3. Variable(s) that are neither target nor features
    - The following variables were removed from the model
      - EIN
      - Name
      - Status
      - Special considerations

### *Compiling, Training, and Evaluating the Model*

The following models were used to optimize the model:

1. Model 1: Removing additional columns considered as noise variables (Status & Special Considerations) and binning new column (Affiliation)
   
2. Model 2: Add 2 additional hidden layers to create deep learning model for a total of 3 layers
   - Layer 1: Total input features x 3
   - Layer 2: Total input features x 2
   - Layer 3: Total input features 
  
3. Model 3: Used different activation function
    - Sigmoid in input and output features instead of RELU on input feature. 
     

None of the 3 different attempts seems to improve the model accuracy compare to the base neural network model. 

## **Summary**

Here are the accuracy results from the base model run vs. different model attempts.

1. Base model: 0.7305

![Base_Model](https://user-images.githubusercontent.com/70525492/107080072-5dc78e00-67b6-11eb-8b08-ccb170dd888c.png)
![Base_Model_Accuracy](https://user-images.githubusercontent.com/70525492/107080073-5e602480-67b6-11eb-8f26-4ea0637687ee.png)



2. Model 1: 0.7269

![Model_1](https://user-images.githubusercontent.com/70525492/107080075-5e602480-67b6-11eb-930d-747baa58efb7.png)
![Model_1_Accuracy](https://user-images.githubusercontent.com/70525492/107080076-5e602480-67b6-11eb-8b8d-79398fed9dc0.png)

3. Model 2: 0.7285

![Model_2](https://user-images.githubusercontent.com/70525492/107080077-5e602480-67b6-11eb-97b2-0c9efaa0a27d.png)
![Model_2_Accuracy](https://user-images.githubusercontent.com/70525492/107080078-5ef8bb00-67b6-11eb-9fde-4e28641911fd.png)

4. Model 3: 0.7303
   
![Model_3](https://user-images.githubusercontent.com/70525492/107080079-5ef8bb00-67b6-11eb-9525-d7df26da9f66.png)
![Model_3_Accuracy](https://user-images.githubusercontent.com/70525492/107080081-5ef8bb00-67b6-11eb-9ace-937b74063fb2.png)

## **Recommendations**

1. Review source data to identify noisy variables or review current input features if any of the data can be binned.
2. Add more hidden layers and neurons.
3. Utilize different activation function to determine accuracy.
4. Use Random Forest Classifier modeling instead of deep learning model to save time. 




