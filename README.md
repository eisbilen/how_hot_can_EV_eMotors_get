
# How Hot Can EV Motors Get? #

**A data-driven approach using test bench measurements collected by the LEA department at Paderborn University**

Electric vehicles are the future and e-motors are a big part of that future.
Engineers around the world aim to improve efficiency and reduce the cost of electric vehicles. In parallel, the primary goal of e-motor designers is to reduce the motor size and cost while improving power output at the same time.

The power will increase by pushing more current, however, the temperature inside the motor will also increase simultaneously which leads to component failures and decreased efficiency.


We can better optimize the e-motor parameters to utilize the motor up to its full capacity if we can estimate the temperatures of the critical components under a variety of loading conditions which ultimately means increased performance and reduced cost for the end user.

Hopefully, I will be able to provide answers to the questions below,
* What are the different types of driving profiles?
* Which part of the e-motor reaches the highest temperature?
* What factors correlate well to the temperature build-up?
* How well we can predict the temperature of critical components with a simple linear regression model?

**Part I: What are the different types of driving profiles (e-motor engine speed characteristics)?**
* 18 profiles have constant engine speed throughout the whole session
* 14 profiles have stepwise walks in engine speed
* Remaining 49 profiles have random ramp-ups and slow-downs in engine speed to better represent real-world driving cycles


**Part II: Which part of the e-motor reaches the highest temperature?**

The followings are the observations derived from the study:
* Stator winding reaches the highest temperature which is around 140 °C.
* The temperature has a high positive correlation with the engine speed.
* Permanent magnets cool down the slowest and engine windings cool down the fastest when the engine excitation stopped.
* Profiles with random speed variation show a normal distribution of temperature while the other profiles have many local peaks separately.


**Part III: What factors correlate well to the temperature build-up in an e-motor?**
With the help of correlation matrices, we can see that stator temperature is positively correlated with engine speed. We can also clearly see that engine speed is highly correlated with voltage and current which actually make sense as it is controlled by voltage and current.

**Part IV: How well we can predict temperature of critical components?**

The observations are:
* In general, our model can predict the stator temperatures with an average absolute error of 1.2 °C.
* %50 of the predictions is spot on with 0.7–0.2 °C error
* Profiles with random speed variations have prediction errors bigger than the constant and stepwise speed profiles.
* Predictions are worsened when the motor speed has drastic changes.
* In extreme cases, there are 30–35 °C prediction errors.


I used 180 hours of data collected from a permanent magnet synchronous motor (PMSM) by the LEA department at Paderborn University. 
Please follow the link for the [original data and corresponding ](https://www.kaggle.com/datasets/wkirgsn/electric-motor-temperature)license as well as the related [publication](https://ieeexplore.ieee.org/abstract/document/9296842).


**Python libraries used in the study:**

* pandas&numpy for data handling 
* seaborn&matplotlib for data visualization
* sklearn for modeling and predictions

** Files in this repository: **

* readme.md
* How_Hot_Can_EV_Motors_Get.ipynb
