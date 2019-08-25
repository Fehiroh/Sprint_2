    
# Boardgame_rule_submission_Sprint_2



![fig 11](https://github.com/Fehiroh/thrg/blob/master/figures/fig_11.png)
![fig 12a](https://github.com/Fehiroh/thrg/blob/master/figures/fig_12a.png)
![fig 12b](https://github.com/Fehiroh/thrg/blob/master/figures/fig_12b.png)
![fig_13.png](https://github.com/Fehiroh/thrg/blob/master/figures/fig_13.png)
![fig_14.png](https://github.com/Fehiroh/thrg/blob/master/figures/fig_14.png)
![fig_15.png](https://github.com/Fehiroh/thrg/blob/master/figures/fig_15.png)
![fig_16.png](https://github.com/Fehiroh/thrg/blob/master/figures/fig_16.png)
![fig_17.png](https://github.com/Fehiroh/thrg/blob/master/figures/fig_17.png)
![fig_18.png](https://github.com/Fehiroh/thrg/blob/master/figures/fig_18.png)

For the repository information (what the folders are, what they contain), scroll down to the **Repository Layout** section

## Overview: Purpose, and Progress
The purpose is to create a webapp that can sort board game rule submissions into those which are likely to be well received by the boardgame community versus those that aren't.

In Sprint 2, I have further investigated the data, cleaned the data based on the results, begun the modelling process, and evaluated my initial modeals. After cleaning the data based on the results 
of Sprint 1 (removing: expansions, games which have been rated by fewer than 25 users, games with unrealistic playtimes -- less than a minute, more than 6 hours--, games invented before 1960, 
games with player counts of zero),  I have trained three classification algorithms to predict whether a game is likely to be well received based on its mechanics, themes, and play conditions.
Alogirthms utilized at this point are SVM, Random Forest, and Logistic Regression. The success of each model has also been evaluated, with the Random Forest Model currently in performing the best in terms of specificity. 
However, I would like to utilize some bagging, stacking, and BLAH in order to facilitate dimensional reduction, and toy with feature engineering, binning, and dimensional reduction to boost the 
effectiveness of all models. Furthermore, I have developed  the basics of a UI that allows submiters to submit their rules, personal information, and provide the information required to run the 
models that predict a boardgame's success. The Server side has yet to be written. 


## Requirements
In order to run the R files contained in this repository, one needs to have R version 3.6.0 or greater installed. The necessary libraries will all 
automatically install (if necessary) and load due to the usage of the p_load() function from the pacman package. Here is an exhaustive list of the
libraries used throughout, presented alphabetically: 


* caret
* corrplot
* e1701
* httr
* RColorBrewer
* RCurl 
* rpart
* RSQite
* rvest
* scrapeR 
* splitstackshape
* stats
* tidyverse
* wesanderson

## Further Work
1. Increasing the effectiveness of all models via binning, bagging, and dimensional reduction. 
2. Writing the server portion of a shiny app, it should inputs into a form that can be fed into the models, while also storing contact information about the submitter for further follow-up.
3. Storing the initial SQLite database in such a way that it is remotely accessible. MySQL was the original choice for this, but server fees seem either too expensive in terms of monetary or 
time cost, at least with the current scope. Cloud-based services are a likely candidate, I will look into Azure and Google Cloud.
4. In a similar vein, I would like to be able to store pdfs of the rules remotely, in order to facilitate solving the business problem, which involves only reading the rules of games that 
are likely to be successful. In order to read them, you have to have them, which will involve either email or storage, dependant on time. 
5. Because the models (especially Random Forest) take non-negligable time to train, I would also like to store the trained models, and have the app access them remotely upon atart-up. 
This avoids having to train within the app.


## Repository Layout
These folders contained the files necessaary to create a recommender system for 
boardgames, based off of webscraping of Boardgamegeek.com, which was performed 
using R.

### **EDA**
Contains a pdf export of the early EDA of the data, which was initially performe in R (see **Files**).  

### **Files**
Contains the end results of my scrapping, as well as my initial work with the data set(lab2(version2).R)

###  **Scraping** 
Contains the R scripts used to scrape boardgamegeek and create the files present in the files folder.

For additional information on each folder, see the readme files located in each.
© 2019 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About
