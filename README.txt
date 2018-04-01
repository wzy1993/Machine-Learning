Zhuoyou Wang



This is the Gaussian Mixture Model



************* Function ******************

the GMM function can take the following inputs:
# n: number of clusters
# train: training data
# dev: development data 
# x is the list for column x values
# y is the list for column y values
# cov_type the default value is None, set it as ‘Tied’ can ask the model use tied covariance



*************** Explaination **************

The function will return a list which contains the log likely hood value for each iteration for training data and development data.

I set the iteration to be 40, which is large enough to let the algorithm converge.

In my code, I have plotted 4 graphs regarding different log likely hood for different dataset with different covariance type. I have saved these graphs in to a PDF file.