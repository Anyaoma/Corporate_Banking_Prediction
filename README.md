# Corporate_Banking_Prediction

**DATA PREPROCESSING**

![image](https://github.com/user-attachments/assets/4a0f6257-3299-44ed-9392-2ed0f0688bce)


The data is organised such that each company is labelled either failed or alive. The data is effectively organised in batches of failed companies or alive companies. Some companies have just a single row of data for a particular year, some have two rows, and others have as many as 16 rows for 16 years. To maintain the temporal order within each data and let the machine learning model learn effectively from the data, while also preserving information from one-row companies, I chose to employ the use of summary statistics for each company, resulting in just a single row for each. This includes the calculation of mean, standard deviation, min, max, first, last, range(max – min), delta(last – first). By implementing these, one is effectively feeding the ML model informative data. 

![image](https://github.com/user-attachments/assets/c88f0de9-44c7-49d7-85f7-dc22a72c8969)


Random forest models are considered black box models. It doesn’t explicitly possess interpretability compared to logistic regression models and other low-variance models. Nevertheless, the result from the random forest model shows that change in Unemployment (Unemployment Rate delta), Mean of Inflation, mean of unemployment, mean of GDP Growth rate, and change in inflation rate (inflation rate delta) are among the top 20 features that contribute the most in the random forest model. This implies that they influence the bankruptcy of a company. The model does not inform on the direction or magnitude of impact (you can try out logistic regression for this), but it does imply that they hold an impact. The delta of any variable measures the change in that variable from inception to closing. Hence, a growth (positive delta) or a decline (negative delta) in unemployment and inflation impacts the bankruptcy of a company. Similarly, the mean value of GDP growth rate, inflation, and unemployment around the time the company functioned does have an impact on whether the company survived or failed.
