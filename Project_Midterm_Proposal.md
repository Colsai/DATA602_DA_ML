# Homework - Week 7 - Draft Outline for Project Proposal #
## Chicago Public Schools Revisted: Clustering + Analyzing the components of good, average, and bad Chicago public schools based on high school graduation rates.
--
Please craft an outline/draft of your proposed project. Please feel free to use the format that represents your thoughts and ideas.
A few PowerPoint slides would be helpful - so you can present to the class on Tuesday 10/19. 
However, the format is your choice - a MSWord document that represents a 'paper' outline is OK , as well. Overall it should include:

### 1. High-level overview - ideally should become the basis of your abstract for the final project paper at the end of the course
According to Desilver (2017), "The most recent PISA results, from 2015, placed the U.S. an unimpressive 38th out of 71 countries in math and 24th in science". 
This project postulates that advancements in an understanding of core factors that could be critical to identifying focus areas for funding and improvement of school systems. By identifying the correlative factors and creating a model that can predict high school graduation rate, educators and field experts can improve their fundamental understanding of focus areas within their own school.

### 2. Motivation - why or what is interesting or fascinating about the project; initial hypothesis.
While educational performance may be low within the US, expenditure on education per capita is not. According to NCES, in 2017 the United States ranked 4th in the world in terms of per-capita education spending. (https://nces.ed.gov/programs/coe/indicator/cmd). What are reasons for the disparity in expenditure to outcomes?

### 3. Datasets - what is the dataset you need or plan to use. Is it easily available OR are you still looking for data. Are there challenges to getting the data. Any limitations in terms of size that you anticipate - over-sized or under-sized dataset? 

- I want to use the most-recent Chicago Public School Report Cards. I've accessed this data before, but had a much more limited scope (looking at correlations). I want to flesh this data out a bit more. Additionally, Chicago Public Schools have data from 13-18, so shared/like columns can be compared here.
https://data.cityofchicago.org/Education/Chicago-Public-Schools-School-Progress-Reports-SY1/dw27-rash

### 4. Any pre-processing of data required? Cleansing, dropping, quality checks needed?
- Dataset is relatively clean, but there are likely null values that require imputation. I will focus on checking through the data when I do feature selection.

### 5. Overall flow/logic of the analyis. ( need not be technical ; the model etc. can be specified in a seperate section, if needed).
- Feature selection and proposed target (graduation rates) --> Clustering KNN or DBSCAN models and check for accuracy, yield results and refine model elements for feature selection, Create initial run of model, Train/Test split and test models, Summarize based on findings from model, draw conclusions based on model. 

### 6. Technical Description : Model, Methods to be used ( e.g. Regressiion, Classification, Clustering or combination). Training/test/validation data split; Any cross-validation required? 
- Classification (some kind of performance metric -- good school, average school, bad school based on high school graduation rates).

### 7. Proposed accuracy metrics, errors to be validated/verfied
- Accuracy/Precision/Recall/F1 score... other metrics as we go.

### 8. Anticipated conclusion - validation of hypothesis
- My expectation will be that some factors, such as high dropout rates, low test scores, and temporary home status may have a large effect in the model for yielding the success of school's attendance rates. However, I also think that there may be some other interesting factors that may be worth looking at for creating the model, as well as identifying standout schools/outliers which may break from the model's predictions (showing they may be doing something novel that other schools are not which leads to better outcomes). 

### 9. References to sample code available in the public domain like github links, books, articles . Please list potential code references, snippets that you are considering to adapt, retroft or think are good references foryou to work on.

--
*Any other thoughts - e.g. impediments, challenges, concerns , OR benefits etc. 
We will discuss and think aloud in the class and use this as a basis for the mid-term exam submission. Since this is a draft, it's OK if you include some of the points lists above and drop some or include some minimalist verbiage around above. The list above is intended to enable you to structure your ideas and thoughts.*
