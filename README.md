# Logistic_Regression_Lead_Score_Analysis

### Introduction:
    An education company named X Education sells online courses to industry professionals. On any given day, many 
    professionals who are interested in the courses land on their website and browse for courses.
    The company markets its courses on several websites and search engines like Google. Once these 
    people land on the website, they might browse the courses or fill up a form for the course or watch some videos. 
    When these people fill up a form providing their email address or phone number, they are classified to be a lead.
    Although X Education gets a lot of leads, its lead conversion rate is very poor. 
    Company is facing a low lead conversion rate. Company has approached us to create a solution in such a way that the 
    customers with high lead score have higher conversion rate and low lead score have lower conversion chance. The 
    vague of the target lead conversion rate is above 80%.

### Data Cleaning: 
    a. The first step we loaded the dataset and performed initial data 
    analysis like its size, shape, statistical description, and Null value 
    counts.
    b. We found that some columns are having label as ‘Select’ which 
    means the customer has chosen not to answer the question. The ideal 
    value to replace this label would be null value as the customer has not 
    opted any option. Hence, we changed those labels from ‘Select’ to 
    null values.
    c. Removed columns having more than 40% null values
    d. For remaining missing values, we have imputed values with 
    maximum number of occurrences for a column.
    e. We found for one column is having two identical label names in 
    different format (capital letter and small letter). We fixed this issue by 
    changes the labels names into one format.
### Data Transformation: 
    a. Changed the multicategory labels into dummy variables and binary 
    variables into ‘0’ and ‘1’.
    b. Checked the outliers and created bins for them.
    c. Removed all the redundant and repeated columns.

### Data Preparation: 
    a. Split the dataset into train and test dataset and scaled the dataset.
    b. After this, we plot a heatmap to check the correlations among the 
    variables.

### Model Building: 
    a. We created our model with rfe count 20 evaluated score like AUC 
    and choose our final model variables as more stability and accuracy 
    were present.
    b. For our final model we checked the optimal probability cutoff by 
    finding points and checking the accuracy, sensitivity and specificity.
    c. We found one convergent points and we chose that point for cutoff 
    and predicted our final outcomes.
    d. We checked the precision and recall with accuracy, sensitivity and 
    specificity for our final model and the tradeoffs. 
    e. Prediction made now in test set and predicted value was recoded.
    f. We did model evaluation on the test set like checking the accuracy, 
    recall/sensitivity to find how the model is
    g. We found the score of accuracy and sensitivity from our final test 
    model is in acceptable range.
    h. We have given lead score to the test dataset for indication that high 
    lead score are hot leads and low lead score are not hot leads.

### Conclusion: 
    Learning gathered are below:
    i. Train & Test set is having accuracy, recall/sensitivity in an 
    acceptable range.
    ii. In business terms, our model is having stability an accuracy 
    with adaptive environment skills. Means it will adjust with the 
    company’s requirement changes made in coming future.
    iii. Top features for good conversion rate:
    1. Tags and Total Time Spent on Website are among the 
    top indicators for convertible leads. 
    2. Tags and Last Notable Activity are among the top 
    indicators for un-convertible leads.
