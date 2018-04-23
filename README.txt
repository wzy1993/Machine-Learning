Zhuoyou Wang



This is the Hidden Markov Model mimicking Gaussian Mixture Model



************* Function ******************

the GMM function can take the following inputs:
# n: number of clusters
# train: training data
# dev: development data 
# x is the list for column x values
# y is the list for column y values

*************** Algorithm **************

I initialize pai to be 1/n for each cluster, matrix of mid be a 1*2*n matrix, covariance matrix to be a 2*2*n matrix, and randomly initial the transition matrix aij to be n*n and make sure each row add up to 1.

Get the value of alpha and gamma first, both of them are (# of data) * n matrix. The ending time gamma, which is the start of the backward is set to be 1, and the beginning time of alpha which is the start of the forward is set to be pai * aij with corresponding cluster(in aij[i][j], i represents the start cluster, j represents the ending cluster). After we have alpha and gamma, now we can get gamma and rnk. Gamma is a (# of data) * n matrix, and ink is a (# of data) * n * n matrix.

Now we can move to update miu, covariance matrix, and the aij(transition matrix). Moreover, since I need to use pai for calculating the first alpha, so I need to update pai as well.`

After each iteration, calculate the log likely hood for the whole dataset, and append it to the result, for plotting purpose. 
*************** Explanation **************

The function will return a list which contains the log likely hood value for each iteration for training data and development data.

I set the iteration to be 40, which is large enough to let the algorithm converge.

In my code, I have plotted 2 graphs regarding different log likely hood for different dataset. I have saved these graphs in to a Graph.pdf file.