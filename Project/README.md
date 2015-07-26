The first few lines of the run_analysis script open the train, test, and features files. Because the dataset has so many files, the working directory had to be changed to the dataset. All of the data had been split up amongst raw data, data titles, subject identifiers, and activity identifiers. In order to make the information easier to read, the column names of the train and test data were changed to match their corresponding feature variable names. Because the activity labels and the y_train/y_test files are refer to the same information, they were joined together to merge together the common names. 

In order to match up all the relevant information, the train and test variable were created. The cbind function appends all the columns together into one data frame. In order to find the standard deviations and means, the grep function is used to find those values in the features file. Mean and mean were both used because the questioning is ambiguous and does not mention whether or not the weighted means should be used. Next, the values of x_test and x_train corresponding to the means and standard deviations are used in the new data frames, omitting any other values. 

Rbind, as opposed to merge, was used to put the test and train data together. Using merge coerces too many NAs to make a legible data frame, whereas rbind puts the two values together based on column names. 

In order to take the mean of the data based on subject and activity values, the aggregate function is used. This function allows data to be broken up based on certain levels of a given factor and perform computations on those separate levels. Columns 87-89 were ommitted because they correspond to categorical data and their means wouldn't hold any significance. 