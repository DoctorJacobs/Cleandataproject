1. One downloads required data from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
2. Then unzips the file if it has not been uncompressed, into a folder "UCI HAR Dataset" in their working directory
3. Run Run_analysis.R
4. The code reads in the the following text files:
x_train.txt, data for the "train" group, are read into the variable traindata
y_train.txt, labels for the train group, are read into the variable trainlabel
subject_train.txt, subjects for the train group, are read into the variable trainsubject
x_test.txt, test group data, variable testdata
y_test.txt, test labels, variable testlabel
subject_test.txt, test subjects, variable testsubject
5. Test and train data are combined into three new sets
masterdata - rows of traindata and testdata combined
masterlabel - rows of trainlabel and testlabel combined
mastersubject - rows of trainsubject and testsubject combined
6. Read "features.txt" into features variable
7. use grep to make meansandstds, which picks out the mean and std columns we need for the project.
8. read activity_labels.txt from initial dataset into activity
9. clean up formatting on activity
10. Combine our nice new three "master" pieces into one file called masterclean.
11. Make tidydata, an independent tidy data set with the average of each variable for each activity
and each subject from our masterclean file.
12. Write out tidydata.txt
13. Be so, so happy that this project is finished.

Important file dimensions:
traindata: 7352x561
testdata: 2947x 561
masterdata: 10299x561
masterlabel: 10299x1
mastersubject: 10299x1
meansandstds: 66
masterdata(permuted by meansandstds): 10299x61
masterclean: 10299x68
tidydata: 180x68
