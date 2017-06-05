## Writeup for PID Controller

A PID controller takes three aspects of error between measurement and expected value.

1. The first is an error that is proportional to the actual error. This is the *P*.
2. Next, we keep a running sum of the errors in the previous time, this helps to increase the correction if the error accumulates over time. This is the *I*.
3. Finally, we also keep a differential of the error over time. This helps to alleviate osciallations caused by overcorrection. This is the *D*.

To make a nice PID controller, getting these parameters if the most important. For tuning I used trial and error.

Steps:

1. I started with P, which is the main aspect of the controller. I settled on a value of 0.1 for this. Now in certain cases I wanted the car to correct faster.
2. For this, I began tuning the I and D, for which I used 0.1 and 1. Using just I without D, would cause the car to oscillate continuously.
3. Before submitting I attempted to reduce D, to 0.9 - in which case I was able to reduce I to 0 and get a more stable drive.
