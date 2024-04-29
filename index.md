## Portfolio

---

### Kaggle Competitions 

#### Home Credit Default Risk

Home Credit wants to serve customers who are unbanked or lack credit history, so they need to identify if an applicant is capable of repayment or likely to have payment difficulties. The target variable was highly imbalanced, with only 8% of the training data representing customers who had problems with loan payments. I created a few supervised classification models to predict whether or not the client is likely to have difficulties repaying the loan based on the application and supplementary data.
<br><br>
After cleaning the data and handling many NA values, and engineering domain-related features such as debt-to-credit ratio, the best model was logistic regression with an estimated out-of-sample accuracy of 92% (equal to the majority class benchmark) and ROC AUC metric of 0.72.
<br><br>
I went on to work with two colleagues on a lasso model which utilized downsampling and resampling to get a higher estimated out-of-sample ROC AUC, but a lower Kaggle score, so we determined the model was overfitting.

- [EDA Notebook (Rmd)](projects/EDA_Notebook_Jessica_Kersey.Rmd)
<br><br>
- [Modeling Notebook (Rmd)](projects/Modeling_Notebook_Jessica_Kersey.Rmd)



#### House Prices: Advanced Regression Techniques

Predict housing prices in Ames, Iowa with a supervised model. I developed a linear regression model of housing prices with the limitation of using only 5 predictors entered additively, with a goal of estimated 0.75 estimate out-of-sample R-squared value.
<br><br>
My final model reached an estimated 0.76 out-of-sample R-squared value, with a Kaggle score of 0.16281.
<br><br>
After this individual work, I went on to collaborate with a teammate on a model which was more effective, with estimated out-of-sample R-squared of 0.88 and a higher Kaggle score of 0.14828.

- [House Prices Notebook (Rmd)](projects/Kaggle Notebook - House Prices.Rmd)









---
<p style="font-size:11px">Page template forked from <a href="https://github.com/evanca/quick-portfolio">evanca</a></p>
<!-- Remove above link if you don't want to attibute -->
