[[Machine Learnign]]


A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, improves with experience E.

Your spam filter is a [[Machine Learning]] program that, given examples of spam emails (flagged by users) and examples of regular emails (nonspam, also called “ham”), can learn to flag spam. The examples that the system uses to learn are called the training set. Each training example is called a training instance (or sample). The part of a machine learning system that learns and makes predictions is called a model. Neural networks and random forests are examples of models.

Consider how you would write a spam filter using traditional programming techniques (Figure 1-1): 1. First you would examine what spam typically looks like. You might notice that some words or phrases (such as “4U”, “credit card”, “free”, and “amazing”) tend to come up a lot in the subject line. Perhaps you would also notice a few other patterns in the sender’s name, the email’s body, and other parts of the email. 2. You would write a detection algorithm for each of the patterns that you noticed, and your program would flag emails as spam if a number of these patterns were detected. 3. You would test your program and repeat steps 1 and 2 until it was good enough to launch.


![[Pasted image 20251119121242.png]]



![[Pasted image 20251119121417.png]]




![[Pasted image 20251119121356.png]]




![[Pasted image 20251119121432.png]]




