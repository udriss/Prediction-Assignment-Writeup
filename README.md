# See HTML file :
[On Github](https://udriss.github.io/Prediction-Assignment-Writeup/main_scripts.html)
[On RPubs](http://rpubs.com/IdrissS/C8_W4)
# Coursera : Prediction Assignment Writeup
One thing that people regularly do is quantify how  much of a particular activity they do, but they rarely quantify how well they do it. In this project, the goal is to use data from accelerometers on the belt, forearm, arm, and dumbell of 6 participants.
# Summary :

### Initialization code
### Loading data
### Cleaning and preparing data
#### First : discard variables with variances close to zero.
#### Second : eliminate variables containing too high a proportion of `NA`.
#### Third : columns going from the first to the sixth are to be deleted.
#### Fourth : get rid of the variables related to _dumbbell_.
#### Fifth : spliting the last subset data `data_sub_4` into training and testing sets.
### Classification problem (output : discrete values) with supervised learning
#### Generating the object `model` that contains the classification tree by using `rpart()` from the `caret` package.
#### Predictions using `model` and _testing set_.
#### Reducing tree size by modifing the *complexity parameter*.
#### Two way of coding the learning procedure
##### The classic way, with `train()` from `caret` package.
##### Using multiple cores and `train()`.
#### Predictions using `model2` and _testing set_.
#### Discussions
### Random forest classifier with supervised learning
#### Circumscription of parameters to be determined
#### Use multiple cores
##### `ntree` from 10 to 130 by 20.
##### `ntree` from 150 to 230 by 20.
##### Time cost.
##### Merging the two resulting objects `results` and `results_2` into one for visualization.
##### Visualization of the evolution of `accuracy` according to `mtry`. Curves are grouped by the value of `ntree`.
##### Selection of best tunes.
##### Build a Random Forest learning named `model5` with the best tunes
#### Predictions using `model` and _testing set_.
#### Discussion
##### We can notice  the classifications with Random Forest and `rpart` return the same results.
