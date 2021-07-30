# Hypothesis-Testing---Student-s-t-test-ANOVA-test
Hypothesis Testing is done on a payroll database using various testing methods.

1.	Importing Relevant Libraries:
Pandas,	Numpy,	Seaborn,
Matplotlib,	Sklearn, Scipy,
Warning,	Researchpy	

2.	Exploratory Data Analysis:
-	Checking variables
   `df.info()`
-	Checking Null Values
`df.isnull().sum()`
-	Correlation Matrix
-	Visualization

3.	Preparing  the dataset:
-	Dropping Correlated Rows
-	Removing Dollar Sign & Converting to float
-	Renaming the fields
-	Scaling the fields
-	Grouping the dataset

4.	Normality Test:
-	Visually: Q-Q Plot
-	Shapiro-Wilk Test
   
5.	Sampling:
Divided into 4 samples according to year 2013,2014,2015,2016
 
6.	Levene’s test:
Checking variance

`Stats, Pvalue = stats.levene(sample_1['Annual_sal'], sample_2['Annual_sal'])`

7.	Student’s test:

`std_err = np.std(sample_3['Base_Pay'])/np.sqrt(48063)
z_stat = (np.mean(sample_4['Base_Pay'])-np.mean(sample_3['Base_Pay']))/std_err` 

8.	Student’s Independent test:

`t_stat, df, cv, p = independent_ttest(data1, data2, alpha)`

9.	ANOVA test:

`_,p=st.f_oneway(groups[comb[0]],groups[comb[1]])`
