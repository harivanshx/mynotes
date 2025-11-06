1.  Start with random values of weight - m1., m2.....c\
2. Calculate Error with mse 
3. Minimize Error with change the weight compo in such a way that your next error will should be minimum one .
	 m1New = m1Old - learning Rate * gradient m1
4. Recalculate Error
5. If it is minimum one then stop and go with final model else go to step 3.b 