Code Book for Course Project

Overview

Source of the original data:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Full Description at the site where the data was obtained:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Process

The script run_analysis.R performs the following process to clean up the data and create tiny data sets:

Merge the training and test sets to create one data set.

Read in the data from files in txt (features, activity_labels, subject_train, x_train and y_train)

Assign column names to the data sets mentioned above.

Extract only the measurements on the mean and standard deviation for each measurement.

Use descriptive activity names to name the activities in the data set. 

Merge the tidyData with activityType to include descriptive acitvity names.

Export the tidyData set as tidyData.txt.

Variables

trainingData - data set created by merging YTrain, subjectTrain, and XTrain

testData - final test set by merging the XTest, yTest and SubjectTest data

finalData - combine training and test data keeping only desired columns and after that, merge with the activityType table to include descriptive activity names.

logicalVector - vector that contains TRUE values for the ID, mean & stddev and FALSE for others.

finalDataNoActivityType - finalData without the activityType column

tidyData - subsetted, human-readable data ready for output according to project description, that is, independent tidy data set with the average of each variable for each activity and each subject.

Output

tidyData.txt is a data frame 180 x 21

"activityId"
"subjectId"
"timeBodyAccMagnitudeMean"       
"timeBodyAccMagnitudeStdDev"      
"timeGravityAccMagnitudeMean"     "timeGravityAccMagnitudeStdDev"  
"timeBodyAccJerkMagnitudeMean"    "timeBodyAccJerkMagnitudeStdDev"  
"timeBodyGyroMagnitudeMean"      
"timeBodyGyroMagnitudeStdDev"     "timeBodyGyroJerkMagnitudeMean"   "timeBodyGyroJerkMagnitudeStdDev"
"freqBodyAccMagnitudeMean"        
"freqBodyAccMagnitudeStdDev"      
"freqBodyAccJerkMagnitudeMean"   
"freqBodyAccJerkMagnitudeStdDev"  
"freqBodyGyroMagnitudeMean"       
"freqBodyGyroMagnitudeStdDev"    
"freqBodyGyroJerkMagnitudeMean"   "freqBodyGyroJerkMagnitudeStdDev" 
"activityType"     