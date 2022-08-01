# Predict whether an employee remains in the company
## Description
  This project predicts whether an employee will leave a company in the near future. The dataset in this problem contains the ratings, remarks and the votes for these remarks from other employees. This project tries to extract useful information from these datasets and use them to train a model that can predict the decision of employee.
  
 ## File description
 The **mainNotebook.ipynb** is the ipython notebook used for building the model. The **Data** folder contains the data available for this project, the description of which is provided below.
 
 ## Dataset
 The files available in the dataset are :
 1. **ratings.csv** - This dataset contains the ratings given by an employee to a company on a specific date. The columns are :
  - *emp* - unique Id for an employee
  - *comp* - the name of the company
  - *Date* - The date on which the employee gave the rating
  - *rating* - the rating given by an employee
2. **remarks.csv** - This dataset contains the remarks made by an employee about a particular company on a given date. The columns are : 
  - *emp* - unique Id of an employee
  - *comp* - name of the company
  - *remarkId* - contains an id associated with each remark
  - *txt* - the text of the remark written by the employe. The text is in '*****' form.
  - *remarkDate* - The date at which the remark as given
3. **remarks_supp_opp.csv** - This dataset contains the information about other employees supporting or opposing the remark made by an employee. The columns are :
  - *emp* - the unique Id for an employee
  - *comp* - name of the company
  - *remarkId* - the Id of the remark
  - *support* - whether the employee supports the remark with the given remark id
  - *oppose* - whether the employee opposes the remark with the given remark id
4. **test.csv** - This dataset contains the test data. The columns are :
  - *id* - index
  - *emp* - unique Id of the employee
  - *comp* - company name
  - *lastratingDate* - the date when the employee gave the last rating
5. **train.csv** - the training dataset

## Libraries
The libraries used are *pandas*, *sklearn*, *matplotlib* and *plotly*. 

## Evaluation
There I have used a weighted accuracy to evaluate the performance of the model. Class 1 (employee left the company) has a weight of 5 and Class 0 (employee remains in the company) has weight of 1. The Formula for accuracy is <br>
 
<img src="https://github.com/tesla-24/EmployeeLeavingCompanyPrediction/blob/main/support/CodeCogsEqn.png" width="128"/>
