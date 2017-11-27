Introduction

The script run_analysis.R performs the 5 steps described in the course project's definition. Please notice you will also find explanations of the code step by step directly in the run_analysis.R file.

First of all, we need to download and unzip the data set stored in a zip file.
Then, we can load the library into our project.
Next, we create two distinct tables called train & test using cbind() and merge them into a unique table called human_activity with rbind()
The next step consists in extracting the columns containing mean and standard deviation measurements with the grepl() function.
We were then asked to Use descriptive activity names to name the activities in the data set. Which is done by using mutate() thanks to the information given in the activity_labels.txt.
Then we used the rm function to clean our space.
Dplyr functions are also used in the next step. It was asked to creates a second, independent tidy data set with the average of each variable for each activity and each subject. We first use group_by() to group the data by activity and subject and in a second time, we get the mean for each variable with summarise_all().
Finally, we generate a new dataset with all the average measures for each subject and activity type (30 subjects * 6 activities = 180 rows). The output file is called averages_data.txt, and uploaded to this repository.

Variables

x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
test and train merge the previous datasets to further analysis and merge in a unique dataset called human_activity.
features contains the correct names for the x_data dataset.
A similar approach is taken with activity names through the activities variable.
Finally, final_data contains the relevant averages which will be later stored in a .txt file.
