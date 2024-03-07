# Fed Funds Classifier: Your Key to Early Retirement
Flatiron School Data Science Project - Phase V

## Overview
* Purpose: To be able to correctly predict fed funds rate decisions in order to preemptively enter the market at either a short or long position before it moves on the decision. Essentially using the model as a predictor of market trends.
  
![Screenshot 2024-03-06 104358](https://github.com/bpolke13/Fed_Funds_Predictor/assets/151547876/8c33f470-3b7a-4c44-a798-1d36703ab1bf)

* Source of data: Sourced data from FRED
* Focus areas and consideration:
  * Focused on finding the features that the FED is known to use in their decision and then using those features to predict the decision coming in the next meeting
* Data Limitation: I used data from 1990 to 2022 essentially to observe modern day economic practice and thinking as well as encapsulate multiple Federal Reserve chairs.

 
# Presentation and Sources
Presentation: [Link](https://docs.google.com/presentation/d/1zaHZP5Oxs1ik3aK5e4Af8dCEzHtYJPRO2AZg73R5rXc/edit#slide=id.g2c00271e0b8_0_32)



# Repository Navigation
My Github Repository contains a Jupyter Notebook which contains all of my data colleciton and various modeling analysis. The Data folder contains all the various CSVs that I compiled from FRED

## Data Analysis & Recommendations

The first step I took was to figure out features that the FED uses to determine interest rates based on its dual mandate of limiting inflation and maximizing employment. These features included things like Consumer Pricing Index, GDP, M2 Velocity, Manufacturing Orders, and FX rates.



After that I did a train test split and fit the data to a simple model, which expectedly performed poorly, and moved on to more robust classification models. The three I chose to use were decision tree, bagging classifier, and random forest. Ultimately, the decision tree model performed the best. The random forest model fit the data slightly better but had a much higher margin of error on the classes I cared about (predicting increases and decreases)

![Screenshot 2024-03-06 110232](https://github.com/bpolke13/Fed_Funds_Predictor/assets/151547876/98495820-ddae-4356-8b7e-db9d2aa85f91)

 
Based on an analysis of the Fed Rate decisions which occur mid month, if you used the model to predict the outcome of the meeting, you would be able to take advantage of that by buying a future that is priced at the current interest rate. Going back 2 years, my model would outperform the market in this way by ~2.2% of interest

![Screenshot 2024-03-06 143713](https://github.com/bpolke13/Fed_Funds_Predictor/assets/151547876/68a91911-9280-421e-ab0e-4dd5091d87dd)
