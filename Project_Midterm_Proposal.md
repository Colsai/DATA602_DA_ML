# Homework - Week 7 - Draft Outline for Project Proposal #
## Chicago Public Schools Revisted: Clustering + Analyzing the components of good, average, and bad Chicago public schools based on high school graduation rates.
---

*Please craft an outline/draft of your proposed project. Please feel free to use the format that represents your thoughts and ideas.
A few PowerPoint slides would be helpful - so you can present to the class on Tuesday 10/19. 
However, the format is your choice - a MSWord document that represents a 'paper' outline is OK , as well. Overall it should include:*

### 1. High-level overview - ideally should become the basis of your abstract for the final project paper at the end of the course
According to Desilver (2017), "The most recent PISA results, from 2015, placed the U.S. an unimpressive 38th out of 71 countries in math and 24th in science". 

Chicago Public Schools, one of the largest public school systems in the country, is one such school system that struggles with performance. In 2018, nearly 20% of schools were labeled as 'underperforming' (the lowest ranking of 5) in school performance. (https://chicago.chalkbeat.org/2018/10/30/21106019/illinois-report-card-94-chicago-schools-earn-low-performance-rating). 

This project postulates that advancements in an understanding of core factors that could be critical to identifying focus areas for funding and improvement of school systems. By identifying the correlative factors and creating a model that can predict high school graduation rate, educators and field experts can improve their fundamental understanding of focus areas within their own school.

The scope of the project is to focus primarily on High School performance, as graduation rates and dropout rates are 

### 2. Motivation - why or what is interesting or fascinating about the project; initial hypothesis.
While educational performance may be low within the US, expenditure on education per capita is not. According to NCES, in 2017 the United States ranked 4th in the world in terms of per-capita education spending. (https://nces.ed.gov/programs/coe/indicator/cmd). What are reasons for the disparity in expenditure to outcomes?

One important note is that these datasets are not new to me, and were used as the basis for an EDA project in DATA601. However, as the Chicago Datasets. Since some initial data cleaning was already done on these datasets, my hope is that careful feature selection based on the high schools in Chicago will yield a dataset that has enough entries for meaningful results and model building. I felt that there was a lot to build on from this previous project, which is why I would like to attempt to return to it and incorporate basic Machine Learning models, etc. 

#### These were my early conclusions from a summary analysis of the Chicago Datasets, done in DATA601.
> Conclusions
The focus of this project was to merge datasets, look through historical records of the schools in terms of performance data, and compare. I used two kinds of T-testing, as well as visualizations.

> *From an exploratory look, I found...*
Students at neighborhood schools have better attendance rates than students at Charter Schools.  
Charter Schools appear to perform better for students in terms of graduation rates, although many fewer schools did not report data.  
Charter Schools do not appear to do any better on College Entrance rates, however, with only a statistically-insignificant difference between Neighborhood and Charter Schools.
Overall, charter schools appear to have some advantages and disadvantages to neighborhood schools.  

> *Caveats*
This analysis only looked at Educational outcomes for students (high school graduation and college attendance rates). It does not control for possible factors in terms of differences between schools within neighborhood schools and charter school groups, nor control for differences in the populations of students who are attending each school.

### 3. Datasets - what is the dataset you need or plan to use. Is it easily available OR are you still looking for data. Are there challenges to getting the data. Any limitations in terms of size that you anticipate - over-sized or under-sized dataset? 

```
#Import each dataset (Chicago Public Schools)
start_time = time.time()

cps_1516_df = pd.read_csv("https://data.cityofchicago.org/api/views/fvrx-esxp/rows.csv?accessType=DOWNLOAD&bom=true&format=true")
cps_1617_df = pd.read_csv("https://data.cityofchicago.org/api/views/cp7s-7gxg/rows.csv?accessType=DOWNLOAD&bom=true&format=true")
cps_1718_df = pd.read_csv("https://data.cityofchicago.org/api/views/wkiz-8iya/rows.csv?accessType=DOWNLOAD&bom=true&format=true")
cps_1819_df = pd.read_csv("https://data.cityofchicago.org/api/views/dw27-rash/rows.csv?accessType=DOWNLOAD&bom=true&format=true")

dur = time.time()- start_time

print(f"{round(dur,3)}s")
```

- I want to use the most-recent Chicago Public School Report Cards. I've accessed this data before, but had a much more limited scope (looking at correlations). I want to flesh this data out a bit more. Additionally, Chicago Public Schools have data from 13-18, so shared/like columns can be compared here.
https://data.cityofchicago.org/Education/Chicago-Public-Schools-School-Progress-Reports-SY1/dw27-rash

### 4. Any pre-processing of data required? Cleansing, dropping, quality checks needed?
- Dataset is relatively clean, but there are likely null values that require imputation. Additionally, because there were different values and columns, if I analyze based on the full joined datasets, I will have to merge like columns (which can be challenging as each year has different naming conventions, etc.). 
- I will focus on checking through the data when I do more feature selection after careful reflection of model building.

### 5. Overall flow/logic of the analyis. ( need not be technical ; the model etc. can be specified in a seperate section, if needed).
- Step 1: Clustering and general analysis. 
- Feature selection and proposed target (graduation rates) --> Clustering KNN or DBSCAN models and check for accuracy, yield results and refine model elements for feature selection, Create initial run of model, Train/Test split and test models, Summarize based on findings from model, draw conclusions based on model. 

### 6. Technical Description : Model, Methods to be used ( e.g. Regressiion, Classification, Clustering or combination). Training/test/validation data split; Any cross-validation required? 
- Classification (some kind of performance metric -- good school, average school, bad school based on high school graduation rates).
- Unsure yet on cross-validation- depends on how many schools I am able to look at. 

### 7. Proposed accuracy metrics, errors to be validated/verfied
- Accuracy/Precision/Recall/F1 score... other metrics as we go.

### 8. Anticipated conclusion - validation of hypothesis
- My expectation will be that some factors, such as high dropout rates, low test scores, and temporary home status may have a large effect in the model for yielding the success of school's attendance rates. However, I also think that there may be some other interesting factors that may be worth looking at for creating the model, as well as identifying standout schools/outliers which may break from the model's predictions (showing they may be doing something novel that other schools are not which leads to better outcomes). 

### 9. References to sample code available in the public domain like github links, books, articles. Please list potential code references, snippets that you are considering to adapt, retroft or think are good references foryou to work on.

## Notebooks  
- **EDA for Kaggle Unification Project: https://www.kaggle.com/yanpapadakis/us-edu-eda/notebook**
This eda notebook was done in R, but was helpful to see in terms of choosing EDA visualizations to introduce the product itself. 

- **Clustering Analysis and Comparison Graphs https://www.kaggle.com/peterme21/clustering-analysis-and-comparison-graphs**
Another eda notebook in Python, this notebook cleans up and organizes data and prepares it for possible clustering - helpful for how to visualize educational data.. 

- **Improving SAT scores in public high schools https://www.kaggle.com/lgl12b/improving-sat-scores-in-public-highschools**:
This notebook (in R), provides a good overview of preparing data for modeling. 

- **Identifying factors for education success https://www.kaggle.com/mhaupt/identifying-factors-for-education-success**
Focusing on clustering and identifying factors for educational success, the author provides a detailed data cleaning, and runs multiple linear regression models, as well as identifies colineaerity through eigenvectors. I'd like to borrow some of the way that the author is defining educational success here. 

## Research/Videos
### Predicting Key Educational Outcomes in Academic Trajectories: A Machine-Learning Approach
https://link.springer.com/article/10.1007/s10734-020-00520-7#Sec1  
This article stated how Artificial Neural Networks could be run to predictively analyze dropout rates for College students. By using ML models, Musso (et. al)
looked to analyze predictors for GPA, academic retention, and degree completion. Ultimately, the models were successful at classifications of students in these outputs, finding that motivation, isolation, processing of information, and attention were significant features for predicting high or low GPA scores.
   
Additionally, it found that selecting main ideas, information processing and anxiety management were the strongest predictors for degree completion. The study shows that "it is possible to identify the predictors of positive educational outcomes, as well as those that are related to failure to achieve these outcomes, with the high level of precision provided by the machine-learning approach in this research." This suggests attempting to use an ANN model may be successful in predictive analysis of educational data as well.

### "The Value of Machine-Driven Initiatives for K-12 Schools"  
http://edtechmagazine.com/k12/k12/higher/k12/k12/article/2019/12/value-machine-driven-initiatives-k-12-schools-perfcon
- Purpose-based, Bonderud states the possibilities of AI and leveraging datasets to understand student performance. By doing so, learner patterns can be better understood; additionally, intelligent algorithms can assist IT teams serve their schools better by use of detection and warning systems.

### "K???12 Educators Emphasize Personalized Learning for Class of 2030"
https://edtechmagazine.com/k12/media/video/k-12-educators-emphasize-personalized-learning-class-2030  
- This video describes the possibility of learning analytics leading to better-individualized student instruction through differentiation, course adjustments, and opportunity creation through AI. These educators suggest that AI can help create valuefor younger learners.

---
*Any other thoughts - e.g. impediments, challenges, concerns , OR benefits etc. 
We will discuss and think aloud in the class and use this as a basis for the mid-term exam submission. Since this is a draft, it's OK if you include some of the points lists above and drop some or include some minimalist verbiage around above. The list above is intended to enable you to structure your ideas and thoughts.*
