# Prediction of Adult Income
An exploratoration of data analysis using supervised Machine Learning

![income](https://github.com/NemesisCrociata/Prediction-of-Adult-Income/assets/132013562/0b33380a-cfae-4c53-9fc3-313de599988a)

**Author:** Nemesis Crociata

We've been tasked predict adult income based on standard features taken by the U.S. Census from 1994. An analysis of products and outlets will be conducted following the CRISP-DM workflow.

- In order to make a clearer goal for the direction of the model, it can be imagined this data is being used in order to identify lower-income individuals who qualify for supportive services.

## Data:
[Original Dataset](https://www.kaggle.com/datasets/wenruliu/adult-income-dataset)

### The data was cleaned and certain data was dropped due to irrelevance to the data
This includes all samples below the age of 18.

Countries of origin were merged into regions of origin to reduce cardinality.
This process was repeated for levels of education completed, as well as occupations held.

## Exploratory Data Analysis
To explore the correlations between features and income, barcharts were created for comparison. The most significant correlations are noted below.

![education vs income](https://github.com/NemesisCrociata/Prediction-of-Adult-Income/assets/132013562/9bfe7761-8eae-4d5d-8ce0-aef0635f206c)

- When comparing levels of education with income, there is a clear correlation. As higher education is achieved, the more likely a sample is to make over $50k annually.
- The majority of samples make over $50k at the Professional Schooling, Masters, and Doctorate levels.

![marital status vs income](https://github.com/NemesisCrociata/Prediction-of-Adult-Income/assets/132013562/d1cc6f17-ede1-4972-9481-a71421dcd3df)

- There is almost an equal distribution of higher and lower reported incomes for people who are married where the spouse is not absent.
- All other marital statuses are highly correlated with lower income.

![capital loss vs income](https://github.com/NemesisCrociata/Prediction-of-Adult-Income/assets/132013562/cd90ad60-a427-410f-97e8-6038cc41fff1)

- There is a strong correlation between higher income (over $50k annually) and higher capital loss.
- It can be assumed that this is due to samples making greater income having more income to dispose of.

## Models
The following Machine Learning models were tested:
- Logistic Regression Model
- KNeighbors Classifier Model
- Random Forest Classifier Model

**The Random Forest Classifier Model was chosen as the final model.**
- This model showed the lowest rate of false positives, or people who should qualify for supportive services but were instead flagged as making higher income
- This model showed the lowest rate of false negatives, or people who made higher income but were flagged as making lower income and are therefore eligible for supportive services
- This model had the highest accuracy score overall

## Limitations and Next Steps
- Although the Random Forest Classifier model is the best model so far, the disparity between the testing and the training results show it is overfit to the data. This could be due to computational limitations while setting parameters.

- Further development of the model to reduce both false positives and false negatives is suggested. The reduction of false positives takes priority, but since the accuracy rate of predicting false negatives is only 62%, this would be a major focus.

- Due to the relatively low accuracy rate of predicting false negatives/predicting people who are high-income as low-income, it is recommended that stakeholders implement further income screening to make sure that funding is allocated only for people who are low-income and truly need supportive services.

- Due to the trends seen regarding education level vs. income, as well as marital status vs. income, it is recommended that stakeholders focus supportive services on pre-graduate individuals, as well as people who are not currently married (including widows and people who are separated).

**For any additional questions, please contact nemcrociata@gmail.com**
