
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

I used 180 hours of data collected from a permanent magnet synchronous motor (PMSM) by the LEA department at Paderborn University. 
Please follow the link for the [original data and corresponding ](https://www.kaggle.com/datasets/wkirgsn/electric-motor-temperature)license as well as the related [publication](https://ieeexplore.ieee.org/abstract/document/9296842).
