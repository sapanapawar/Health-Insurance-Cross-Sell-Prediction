# Health-Insurance-Cross-Sell-Prediction
Building a model to predict whether a customer would be interested in Vehicle Insurance is extremely helpful for the company because it can then accordingly plan its communication strategy to reach out to those customers and optimise its business model and revenue.

# Problem Statement
Our client is an Insurance company that has provided Health Insurance to its customers now they need your help in building a model to predict whether the policyholders (customers) from past year will also be interested in Vehicle Insurance provided by the company.

An insurance policy is an arrangement by which a company undertakes to provide a guarantee of compensation for specified loss, damage, illness, or death in return for the payment of a specified premium. A premium is a sum of money that the customer needs to pay regularly to an insurance company for this guarantee.
Just like medical insurance, there is vehicle insurance where every year customer needs to pay a premium of certain amount to insurance provider company so that in case of unfortunate accident by the vehicle, the insurance provider company will provide a compensation (called ‘sum assured’) to the customer.

Building a model to predict whether a customer would be interested in Vehicle Insurance is extremely helpful for the company because it can then accordingly plan its communication strategy to reach out to those customers and optimise its business model and revenue.

Now, in order to predict, whether the customer would be interested in Vehicle insurance, you have information about demographics (gender, age, region code type), Vehicles (Vehicle Age, Damage), Policy (Premium, sourcing channel) etc.

## Attribute Information
id : Unique ID for the customer

Gender : Gender of the customer

Age : Age of the customer

Driving_License 0 : Customer does not have DL, 1 : Customer already has DL

Region_Code : Unique code for the region of the customer

Previously_Insured : 1 : Customer already has Vehicle Insurance, 0 : Customer doesn't have Vehicle Insurance

Vehicle_Age : Age of the Vehicle

Vehicle_Damage :1 : Customer got his/her vehicle damaged in the past. 0 : Customer didn't get his/her vehicle damaged in the past.

Annual_Premium : The amount customer needs to pay as premium in the year

PolicySalesChannel : Anonymized Code for the channel of outreaching to the customer ie. Different Agents, Over Mail, Over Phone, In Person, etc.

Vintage : Number of Days, Customer has been associated with the company

Response : 1 : Customer is interested, 0 : Customer is not interested

## Handling Imbalance Data:
The provided data is highly imbalanced data so I have used Random Oversampling Technique to overcome this problem.
Random Oversampling: Random Oversampling includes selecting random examples from the minority class with replacement and supplementing the training data with multiple copies of this instance, hence it is possible that a single instance may be selected multiple times.

As from the distribution of target variables, we know that our data is highly imbalanced.

![target](https://user-images.githubusercontent.com/89305804/156879197-70ff674f-842d-4796-9f16-0778642ed9b4.png)

So to handle such a problem, we have balance  the data. For this problem I have used Random Oversampling technique.

After using Random oversampling technique now our data is balanced.

![imbalnce](https://user-images.githubusercontent.com/89305804/156879171-4c8309a8-0375-4132-80cd-9aa3408b8d5f.png)


## Model Implementation and Evaluation:

Model Name                           | Accuracy | Precision | Recall | f1 score | AUC score |
----------                           |----------|-----------|--------|----------|-----------|
Logistic Regression                  | 0.78     | 0.59      | 0.96   | 0.73     | 0.82      |
Random Forest Classifier             | 0.94     | 0.90      | 0.99   | 0.94     | 0.99      |
XG Boost Classifier                  | 0.80     | 0.66      | 0.91   | 0.77     | 0.85      |
Naive Baye's Classifier              | 0.78     | 0.59      | 0.96   | 0.73     | 0.82      |

## Conclusion:
After Hyperparameter tuning on Random Forest model using Random Search CV we can see the slight change in the accuracy i. e.

Accuracy is increased from 0.9450 to 0.9464

Precision is increased from 0.9031 to 0.9055

Recall is increased from 0.9967 to 0.9970

F1-Score is increased from 0.9477 to 0.9489

This results can said to be good for this dataset.









