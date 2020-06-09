### Predicting MLB Batting Averages using Machine Learning and Angle Triangulation
![firstimage](/images/object_angle_head.png)

## _Overview_
<p> The overall objective for this project was to gain a greater insight into the body mechanics a major league
  baseball player uses to optimize power and efficiency in their swing based on the initial batting stance and calculating
  two different angles illustrated below.  Our data set used the top 1000 MLB batting averages of all time using the following
  reference: [https://www.baseball-reference.com/leaders/batting_avg_career.shtml].

<p> Utilizing cvlib, PyCharm, Math, and LabelIMG[https://github.com/tzutalin/labelImg], we have been able to make great strides in defining what constitues the optimal batting efficiency by calculating various angles of a batting stance.  We also provided a classfication range within the top 1000 hitters of all-time (Top, Middle, and Bottom) in concert with the actual batting average statistic.  Once the optimal classification and contingent on results, we hope to be able to detect through machine learning a potential draft or recruiting analysis as to the validity of impact that an indivdiual player would contribute to MLB and predict or forecast their batting averages.  
  
![angle1](/images/object_detect.png).    ![angle2](/images/object_angle.png)

## _Model Summary_
<p> The difference between a .250 hitter and a .300(all-star) is 1 hit per week, given on average a batter would have 500 at bats in a season that is approximately six months long.  In our analysis, the difference between the top 50 greatesthitters vs the bottom 50 greatest hitters of all-time is about 1.2 hits / week ranging from the very best Ty Cobb(.3663) to Mike Marshall(.2702).  The complexity of this project is understanding the sublte differences between angles given the fact that many batting stances display a wide range of variance as you can see below from a small sample of 14 MLB batters from the universe of 1000.  
  
![batters](/images/Image_Stack_14.png)
  
<p> We opted for utilizing a multi-output machine learning classification model with two hidden layers.  This allows our network to predict a set of class labels for each head, making it possible to learn asymetric label combinations.  Again, the dual outputs in the machine learning would output 1 = tier class(Top, Middle, Bottom) and output 2 = batting average.  
  
![model](/images/multi_ouptut_ml.png)

## _Model Evaluation_
<p> Utilizing the multi-output machine learning we compiled the model using loss category = "sparse_categorical_crossentropy", and "mean_squared_error" with an adam optimize and loss_weights = 0.5 to 0.5 measuring accuracy as our metric.  To fit the model we used a train/test splits with X_train and the two output y/Y trains where
  vector y = Batting Average and vector Y = "Tier".  

* 1. The Dual Output Classifier accuracy equated to 67% vs. naive prediction of 33%. 
* 2. No obvious signs of overfitting. 
* 3. Multi-output model helps accuracy

## _Import and Code_

![imports](/images/imports.png)
![code](/images/code_1.png)


## _Applications/Libraries Used For Project_
<p> The following Libraries were used for this project
* Math - Calculate Angles Based on YOLO coordinates
* Numpy - Used in concert with Pandas for array conversion
* Scikit learn - Train Test Splitting
* Py Charm - Image Processing with Python
* Keras/Tensorflow - Mult-output Modeling
* LabelIMG - YOLO coordinates for angle dissemination (CNN Neural Network)
* cvlib - open source / object detection and manipulation

![applications](/images/applications_used.png)

## _Final Thoughts For Future Development_
<p> While we are delighted with the results that provided a 67% accuracy for the machine learning model, we feel that integrating video analysis and additional player profiles will help increase the overall accuracy of the project.   The idea would be to train the object detection model to monitor muti-angles from when the batter first steps up to the plate until the swing culminates.  We would ideally use a weighted angle of time function to determine the data sets to be used.  
