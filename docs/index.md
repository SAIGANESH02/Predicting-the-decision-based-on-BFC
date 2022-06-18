## Maintaining the Brain Functional Connectivity (BFC) in the gambling task using the HCP fMRI data-set.

Are there any regions and networks in the brain which are more affected by the Win and Loss Event conditions corresponding to someone’s decision?

### Introduction

To analyze data-set being preprocessed by HCP© for NMA-2021 that they recorded using fMRI is to analyze in this project to maintain connectivity and correlation of the areas which are involved in the task. What we did was make it inquiry what rate of connectivity and correlation are involved during the gambling task designed to evaluate reaction of participants to stimulus.

The test info:  
- 339 subjects, aged 22-35
- 360 Parcellated cortical regions, 180/hemisphere

### Project Plan

- We use fMRI data of 339 subjects from Human Connectome Project’s gambling task. 

- A contrast of the brain's Parcells average activity in  reward and loss conditions will be computed for each subject 

- We will do a parcel based GLM to identify the most sensitive areas of the brain to lose/win distinction. 

- Then we will make a correlation matrix of task-dependent functional connectivity of the whole brain to those ROIs we found and compare it for loss and win conditions.

### Methodology
![image](https://user-images.githubusercontent.com/53213766/174432999-09d87b2f-58ea-42f0-b63c-4c5782d9f9ee.png)

### Step by step into the gambling
![image](https://user-images.githubusercontent.com/53213766/174433022-16ea030f-73ae-47b4-8ab4-f29dd19540c7.png)

### Data Wrangling
Our data: explanatory variables / condition time / regions.

**Our approach:**

- Creating a data frame for the brain activity.  for each subject and run

- Averaging the activity over the condition time.  for each parcel

- Choosing the highest informative parcels. rate of activity in fMRI

- Using GLM models.  to ensure that our findings are accurate  

- Building the correlation matrix for win/loss conditions among all interested parcels.
 
- Visualizing the brain connectivity based on the correlations.

### Correlation Matrix
![image](https://user-images.githubusercontent.com/53213766/174433118-533b6369-1ced-40ce-8ce0-c0edcccf675f.png)

### True / Predication
- The 20 parcels give the accuracy of result in amount of 0.76, which is analyzed with Ridge Classifier with 20 cross-validation
- While using the whole 360 parcels with a Logistic Regression model and 20 cross-validation, gave us 0.82 accuracy.
- Which is higher than our chosen 20 parcels by 6% only.

![image](https://user-images.githubusercontent.com/53213766/174433171-e4309fad-bd9d-4686-850e-785fe9d573af.png)

## Model weights for the 20 parcels
![image](https://user-images.githubusercontent.com/53213766/174433229-6b605b16-f3c0-4006-a249-7ddce620ab71.png)
## In the brain
![image](https://user-images.githubusercontent.com/53213766/174433248-352116f0-f29a-4a39-a394-77a5759b67f4.png)

