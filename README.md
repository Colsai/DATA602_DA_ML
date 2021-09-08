# DATA602_DA_ML
Saved Notes Each Week

## Week 1:
Reviewed Syllabus

## Week 2:
### I. What is statistical learning? 
- If there is a relationship between two variables
- Yi = f(xi) + Ei
- Simple example- plotting x against y, curve pattern.
- The difficulty of estimating f will depend on the standard deviation of the error.
(ie most points fall around the line, but perhaps not on the line; this is error/standard deviation-- variance)
- Different kinds of fitting, etc.
- These graphs can be 2d or 3d. 

### II. How do we estimate the function f?
There are 2 reasons for estimating f:
- Prediction (predicting other values) 
For example, value for house prices in the year.
& 
- Inference (running live data points into the model)

We assume observed training data == {(x1, y1), (x2, y2), (xn, yn)}
Use this training data to estimate f.

Parametric Methods:
Reduces the problem of estimating a set of parameters, two step.

Linear Regression Estimate:
*Can still get a bad answer with the wrong model.*
Polynomials are taken in bits and pieces and segments, and combined (smoothing of lines).

Non-Parametric Methods:
Do not make explicit assumtpions (do not assume linear/quadratic/polynomial fit)
Accurately fit a wider range of possible shapes
However, need a very large number of observations to do accurately.
(see: Thin-Plate Spline Estimate)
Non-linear regression methods are more flexible.

### III. Tradeoff between prediction accuracy and model interpretability
Possible to get more accurate predictions with a simple than complex model. Harder to fit a more-flexible model (easier to fit simple equation). However, accuracy can be a question. 

*Learning about f*

### IV. Supervised/Unsupervised Learning?
Supervised: Supervised learning is where both the predictors and response are observed.
Unsupervised: Only the predictors (Xi) are observed. For example, this will cluster data, which will show patterns around certain areas. 

More of an application for market segmentation, finding seasonal peaks, drops in sales. 
Very common approach is clustering, which looks for similar patterns within data. 
How close is the point to a specific cluster? 

### V. Regression vs. Classification:
Regression = predicts numerical value
Predicting the value of the DOW in 6 months; predicting housing values. 

Classification = predicts categorical value
Will DOW go up or down; is this email spam?

Also 'logical regression', which falls towards classification. 

### VI. Measuring Quality of Fit
We have a regression problem. One measure of accuracy is mean squared error (MSE)

MSE = 1/n sum 1->n (yi - predicted value)^2
ie. AVERAGE OF SUM OF SQUARED ERRORS.

ie mean squared error equals (1/n) times the sum of squared errors from 1 -> value
Square all the errors, sum it, and divide by the number of values (literally the MEAN squared error).

*After* creating the model, 

### VII. Training vs. Testing MSE's
The more flexible the method is, the lower the training MSE will be.
However, the test MSE may in fact be higher for a more flexible method than for a simple approach. 
