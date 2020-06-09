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
<p> The difference between a .250 hitter and a .300(all-star) is 1 hit per week, given on average a batter would have 500 at bats in a season that is approximately six months long.  In our analysis, the difference between the top 50 greatesthitters vs the bottom 50 greatest hitters of all-time is about 1.2 hits / week ranging from the very best Ty Cobb(.3663) to Mike Marshall(.2702).  The complexity of this project is understanding the sublte differences between angles given the fact that many batting stances display a wide range of variance as you can see below from a small sample.
  
![batters](/images/Image_Stack_12.png)
  
