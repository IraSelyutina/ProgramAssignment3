The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

Source files(needed for work):

- 'features.txt' [561x2]: List of all features 

- 'activity_labels.txt'[6x2]: Links the class labels with their activity name. 

- 'X_train.txt'[7352x561]: Training set. 
- 'X_test.txt'[2947x561]: Test set. 

- 'y_train.txt': Training labels. [7352x1]
- 'y_test.txt': Test labels. [2947x1]

- 'subject_train.txt' [7352x1]
- 'subject_test.txt' [2947x1]
Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

In code we did following action
1. Preparation part - Load, unzip and read source files
2. intermediate part
  Created intermediate data sets
  - total_set [10299x79]: Training set+Test set .Includes data which represent mean of std values from source data
  - activity  [10299x1]: Training labels+Test labels. Represents code of  activity in each row of total_set
  - total_set_activity [10299x80]: total_set with correct descriptive column names+activity (description)
  - subject  [10299x1] :subject_train+subject_test. Represents code of  subject in exact row
  - total_set_activity_subject [10299x80]:total_set_activity with code of subject
3. Target data [35x81]: the average of each variable(mean+std) for each activity and each subject.
