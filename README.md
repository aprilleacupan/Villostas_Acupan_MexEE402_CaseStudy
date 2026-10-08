# MexEE 402: Data Preprocessing Case Study

MexEE Elective 2: Data Science and Machine Learning
Batangas State University, Alangilan Campus
1st Semester, AY 2026-2027

## Members

| Name | Student Number | MEXE - 4101|
|---|---|---|
| Villostas, Justine Aaron R. | 23-00117 |  MEXE - 4101| 
| Acupan, Kyla Aprille M. | 23-06845 |  MEXE - 4101

## Notebook links

| Chapter | Member 1 | Member 2 |
|---|---|---|
| Ch1_2_3 | https://colab.research.google.com/drive/1TX9TqJ4LbEwVYg0amNBOGSbtGRR5lPZf?usp=drive_link | https://colab.research.google.com/drive/1GeOf8f5pAFONnWHuB1GWw2zwk2JhAylS?usp=drive_link |
| Ch4 | https://colab.research.google.com/drive/1oRWsr8mT0pBurDHpXj5TAkh1jtQsZwql?usp=drive_link |                                  https://colab.research.google.com/drive/1utiiZYI0OnsEjr-sD6ymQhIJvj9A8NXM?usp=drive_link |
| Ch5 | https://colab.research.google.com/drive/1xxCgZButjHa2PUtFeVQDQ0FZYZiNVkTt?usp=drive_link | https://colab.research.google.com/drive/1PtVZgkL00O272TRlhaODc3H2XEAKH35f?usp=drive_link |
| Ch6 | https://colab.research.google.com/drive/1v1DG0OwkZ2Wa0k7eortpcdRwFMGlQeC7?usp=drive_link | https://colab.research.google.com/drive/1PtVZgkL00O272TRlhaODc3H2XEAKH35f?usp=drive_link |
| Ch7 | https://colab.research.google.com/drive/1xA9M1ZL_xxnBaAz7LzbG3kUGu3-affLI?usp=drive_link |https://colab.research.google.com/drive/1DrEjLZ53yokGrK1dJ0Ad_ZjogAjdyHS7?usp=drive_link|
| Ch8 | https://colab.research.google.com/drive/1RwWAv2OIsi0Y5IiLCozzqbP9oaQoW9IW?usp=sharing |https://colab.research.google.com/drive/1E66qBToJ2sxIvXQZB-e4P0jZ_1-LYcIo?usp=drive_link |
| Ch9 | [link]() | https://colab.research.google.com/drive/10Tec9nZkh0_gAJXcf5WYW5cYH7NQ4jYX?usp=drive_link |

<h2>What we learned</h2>

<h3>Ch1_2_3</h3>
<p align="justify">The chapter 1_2_3 taught us that data analysis is not just using Python or creating models because every codes has it own function. We learned that data processing is important so that the data is clean and organized. We learned that the raw data can have missing values, duplicates, irrelevant information, and errors that can affect the results. What surprised us the most was how much data quality can affect the results it makes the results clean, easy to understand, and only the needed information for the analysis will be included.  One of the example of this is the Rank Column was dropped because it does not provide information that is needed for the analysis. The chapters made us realized that good analysis starts with good and organized prepared data.</p>

<h3>Ch4</h3>
<p align="justify">The chapter 4 thought us that raw data can be transformed to a more useful features that help reveal patterns and improve machine learning models. We learned about the techniques such as binning, and interaction features. For example, in the notebook, temperature and lemonade sales were used to create a new feature called "lemonade per degree", which gives a clearer idea of the relationship between temperature and sales.  What surprised us the most was that simple changes to existing data, such as combining two variables or creating new features, can provide insights that are not obvious in the original data. </p>

<h3>Ch5: Data Scaling and Normalization</h3>
<p align="justify">We understood how data scaling puts columns on a similar range so the model treats them fairly. In our student example, Grades (76 to 92) has bigger numbers than Study Hours (8 to 15), so the model might favor Grades even if both matter equally. We learned how to use StandardScaler, which makes each column's mean 0 and standard deviation 1, so some values became negative like -0.64, meaning below the average. We also learned how to use MinMaxScaler, which squeezes the values into 0 to 1. What surprised us is that scaling isn't always needed. It depends on our data and on the algorithm, so we can't just apply it to everything.</p>

<h3>Ch6: Dealing with Outliers</h3>
<p align="justify">We understood how outliers are values that are very different from the rest, like one student who studies way more hours than everyone else. We learned how to spot them using the Z-score method, which checks how far a value is from the mean, and the IQR method, which sets a lower and upper fence around the middle part of the data. What surprised us is that the two methods can give different results, so one can miss an outlier that the other catches. We also understood how to handle outliers by capping and flooring them, using a log transformation, or removing them only if they are errors. We enjoyed this chapter because we could see how each method treats the same data differently.</p>

<h3>Ch7: Feature Selection</h3>
<p align="justify">We understood how feature selection picks only the features that really help in predicting the target, because features that don't matter can make the model less accurate. We learned how to use the filter method, where we score each feature by its correlation with final grade and keep only those above 0.5. We also learned how to use RFECV, which removes the weakest feature one at a time and keeps the set with the best cross-validated score, and LassoCV, which shrinks the coefficients of unimportant features to 0. What surprised us is that the three methods gave different answers. The filter kept study hours, assignments completed and class participation, RFECV kept only assignments completed, and LassoCV kept extracurricular activities, which the filter dropped. This showed us there is no single correct list of features, because it depends on the method we use.</p>

<h3>Ch8: Constructing a Preprocessing Pipeline</h3>
<p align="justify">We understood how a preprocessing pipeline works like a conveyor belt, where each station is one step like cleaning or scaling, and the raw data comes out ready for the model. We learned how to build one using Pipeline and ColumnTransformer, where we first fill the missing values with SimpleImputer and then scale the data with StandardScaler, and apply it only to the columns we choose. What surprised us is that the order of the steps matters, because the missing values have to be filled first before the data can be scaled. We also understood why pipelines are useful: they automate the routine steps, make the work faster, and give the same result every time with fewer human errors.</p>

<h3>Ch9: Real-World Application: Data Preprocessing</h3>
<p align="justify">We understood how all the preprocessing steps we learned before come together on one real dataset, the Titanic. We learned how to handle the numerical and categorical columns separately, where missing values are filled with the median for the numbers and with "missing" for the categories, then the numbers are scaled and the categories are one-hot encoded. We also learned how to use discretization to turn Age into life stages like Child, Adult, and Elderly instead of exact ages. What surprised us is that Pclass is treated as a category even though it is a number, because it stands for a class and not an amount. We also understood why we make plots after preprocessing: they help us check if the cleaning worked and make the patterns in the data easier to see.</p>

## Errors we found

When it comes to the code, all of our chapter notebooks run smoothly. We tested this by using Restart and Run All in each notebook, and every cell ran without errors.

## Note on AI tools

Yes, we used an AI tool specifically Claude AI for this project. We used it to fix the format of our chapter questions and answers so they were consistent across all the notebooks. We also used it to understand the topics better and to explain the code, which made it easier for us to write the code in the notebooks. For the README, it helped us organize the layout, including the chapter table with the Colab links, so everything is easy to read and follow.

## References

McKinney, W. (2021). Python for Data Analysis, 3rd ed. O'Reilly.
VanderPlas, J. Python Data Science Handbook.
Any other page or article you used.
