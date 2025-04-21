## Portfolio

---

### MSBA Capstone

#### Swire Coca-Cola Delivery Standardization

**Problem and Approach**
<br>
Swire Coca-Cola (SCC) wants to reduce delivery costs by offloading some customers to use third-party distributors. They considered a volume threshold for some customers, however, they do not want to exclude customers with current low volume but high growth potential from their mutually-beneficial direct delivery relationship.
<br><br>
My group initally approached the problem with the intent to use supervised and unsupervised models to identify characteristics of customers which had high growth across the 2023-2024 data provided. My contribution was clustering, with poor results.
<br><br>
After other groupmates found that certain "frequent order type" factors were associated with high growth, we pivoted to investigating potential treatment effects. I used matching with multiple linear regression to estimate average treatment effect (ATE) between using the old "MyCoke Legacy" online ordering platform vs the new "MyCoke 360". I also tried causal forest as heterogenous treatment effect (HTE) models to estimate individual treatment effects (ITEs) of Sales Reps vs the remaining frequent order types as control. The causal forest models again had poor results, but a groupmate used T-learner HTE models with better performance.
<br><br>
**Impact and Solution**
<br>
I analyzed the ITEs from the T-learner and calculated CATEs for some customer groups to show examples of how TE could be used. For one example, for the set of all customers below 400 average gallons per year and not already frequently ordering via Sales Rep, they might increase an average of 10 gallons per year by switching to Sales Rep. In contrast, customers below 400 average gallons per year, not already frequently ordering via Sales Rep, and in the sub-trade channel of Middle School could increase an average of 92 gallons per year by making the swap!
<br><br>
In the end, our solution was a "proof-of-concept" that SCC could use heterogenous treatment effect (HTE) modeling as a complement to their decision criteria for delivery method. Following our modeling approach, they could utilize ITEs to determine targeted interventions to individual customers or aggregate the ITEs into conditional average treatment effects (CATEs) of sub-groups of customers, for example, they can target members of a trade channel with a high CATE. The ITEs could help determine if customers not currently meeting SCC's decision criteria to remain on direct delivery could improve their outcomes enough to be valuable to retain.
<br><br>
**Challenges and Lessons Learned**
<br>
Everyone in our group found the large and diverse dataset challenging to extract value from. One challenge was categorical variables with a high number of factors, such as the "sub trade channel" with 48 categories and the "primary group number" indicating customers as part of a chain which had 1021 unique values! My causal forest models had extremely low and even negative r-squared values (which should be impossible)! I suspect this was due to the categorical variables being turned into dummies and the data being scaled, resulting in a ton of categorical dummies and fewer numerical columns which contain more variation.
<br><br>
In this project, I gained real-world experience with models that I had mostly only used with nicely curated data for learning purposes, such as clustering, matching, and causal forest models. This was the largest group project I had worked on with 4 other people, and it was challenging trying to combine different approaches and coding styles, including sometimes different coding languages. Though I had presented to various business leaders before, this was the first time I presented such a technical subject, and the process of developing the presentation, iterating, and refocusing to be both succinct and also detailed with respect to the technical aspects was a great learning exercise.

- [EDA Notebook (html)](projects/Capstone_EDA_Notebook.html)
- [EDA Notebook (Rmd)](projects/Capstone_EDA_Notebook.Rmd)
<br><br>
- [Modeling Notebook (html)](projects/Capstone_Modeling_Notebook.html)
- [Modeling Notebook (Rmd)](projects/Capstone_Modeling_Notebook.Rmd)
<br><br>
- [Modeling Notebook 2 (html)](projects/Capstone_Modeling_Notebook_2.html)
- [Modeling Notebook 2 (Rmd)](projects/Capstone_Modeling_Notebook_2.Rmd)

<br><br><br>

### Kaggle Competitions 

#### Home Credit Default Risk

Home Credit wants to serve customers who are unbanked or lack credit history, so they need to identify if an applicant is capable of repayment or likely to have payment difficulties. The target variable was highly imbalanced, with only 8% of the training data representing customers who had problems with loan payments. I created a few supervised classification models to predict whether or not the client is likely to have difficulties repaying the loan based on the application and supplementary data.
<br><br>
After cleaning the data and handling many NA values, and engineering domain-related features such as debt-to-credit ratio, the best model was logistic regression with an estimated out-of-sample accuracy of 92% (equal to the majority class benchmark) and ROC AUC metric of 0.72. I also worked with two colleagues on a lasso model which utilized downsampling and resampling to get a higher estimated out-of-sample ROC AUC and much higher specificity with the target of risky customers. Ultimately this model received a lower Kaggle score, as it was overfitting the training data.
<br><br>
This project was challenging due to the large data set and imbalanced target variable. I learned new modeling techniques such as lasso regression, downsampling, resampling, and the challenges of version control when individuals are using separate Rmd notebooks.

- [EDA Notebook (Rmd)](projects/HC_EDA_Notebook.Rmd)
<br><br>
- [Modeling Notebook (Rmd)](projects/HC_Modeling_Notebook.Rmd)

<br><br><br>

#### House Prices: Advanced Regression Techniques

Predict housing prices in Ames, Iowa with a supervised model. I developed a linear regression model of housing prices with the limitation of using only 5 predictors entered additively, with a goal of estimated 0.75 estimate out-of-sample R-squared value.
<br><br>
My final model reached an estimated 0.76 out-of-sample R-squared value, with a Kaggle score of 0.16281. After this individual work, I went on to collaborate with a teammate on a model which was more effective, with estimated out-of-sample R-squared of 0.88 and a higher Kaggle score of 0.14828.
<br><br>
This project was my first experience writing code collaboratively and was the largest data set I had worked with. Additionally, I learned how to effectively customize table and graph formatting in R.

- [House Prices Notebook (Rmd)](projects/Kaggle_Notebook_House_Prices.Rmd)









---
<p style="font-size:11px">Page template forked from <a href="https://github.com/evanca/quick-portfolio">evanca</a></p>
<!-- Remove above link if you don't want to attibute -->
