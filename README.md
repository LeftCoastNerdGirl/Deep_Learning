# deep_learning_challenge

# Background
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

# Preprocess data

-Use Pandas to import the csv file and create a dataframe.
-Remove non-beneficial colums - EIN and NAME because they are attributes that do not affect success.
-Used the dtypes.index and APPLICATION_TYPE. value_counts to get a better idea of the compositon of the data.
-Used a cutoff value to create an "Other" category to group the smaller values.
-Coverted categorical data to boolean columns using get_dummies.
-Separted the 'IS_SUCCESSFUL' column as y to solve for and set the remaining data as X.
-Used train_test_split function to divide the data into a set for training the model and a different set for testing the model's accuracy after training.
-Used StandardScaler to scale the test and train data. 

# Training the model

# Test 1
-Created a model with the following: layer 1 with 80 nodes, layer 2 with 30 nodes.
-Complied the model.
-Trained using 100 epochs.
-Outcome: Loss - 0.5646m, Accuracy - 0.7261.
-Does not meet the desired target of 75% accuracy.

# Test 2
-Increased nodes to 200 in layer 1 and 100 in layer 2.
-Outcome: Loss - 0.6277, Accuracy - 0.7257.
-Does not meet the desired targe of 75% accuracy.

# Test 3
-Increased epochs to 200.
-Outcome: Loss 0.9926, Accuracy - 0.7263.
-Does not meet the desired targe of 75% accuracy.

# Test 4
-Added a 3rd hidden layer with 100 nodes.
-Outcome: Loss 0.7831, Accuracy 0.7279.
-Does not meet the desired targe of 75% accuracy.

# Test 5
-At the suggestions of ChatGPT, added batch normalization to both hidden layers and batch size of 50 to train model.
-Outcome: Loss - 0.5567, Accuracy - 0.7278.
-Does not meet the desired targe of 75% accuracy.

# Summary
The model did not return the desired accuracy of 75%. Increasing nodes, number of hidden layers, epochs, and adding batching did not improve the accuracy outcome. 
Possible steps to increase model's accuracy could include

-Use a different model other than the ones covered in our class.
-Augment the data set to increase the size of the training and testing data.
-Check for outliers that may be skewing the overal output.
-Explore the weight of the various attributes and test removing the lowest weighted to see if that increases accuracy.
