---
title: "Code Book"
output: html_document
---


## About

#### Background

Human Activity Recognition Using Smartphones Dataset
Version 1.0
  
==================================================================  
  
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.  
Smartlab - Non Linear Complex Systems Laboratory  
DITEN - Università degli Studi di Genova.  
Via Opera Pia 11A, I-16145, Genoa, Italy.  
activityrecognition@smartlab.ws  
www.smartlab.ws  
  
==================================================================  

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.  


#### Data sets

*tidydata.csv*

The base data set as described in the following sections, *Variables* and *Transformations*.

*tidydata_summary.csv*

The summarised data set. The variables from the base data set are summarised as averages by subject and activity. Each variable name apart from the first 3 variables is the original variable name prefixed by "Mean_".


## Variables

#### Overview

The first 3 variables identify the subjects, the activities performed and give activity descriptions.

* SubjectId
* ActivityId
* ActivityLabel

**Features are normalized and bounded within [-1,1].**

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (*tBodyAcc-XYZ* and *tGravityAcc-XYZ*) using another low pass Butterworth filter with a corner frequency of 0.3 Hz.

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (*tBodyAccJerk-XYZ* and *tBodyGyroJerk-XYZ*). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (*tBodyAccMag*, *tGravityAccMag*, *tBodyAccJerkMag*, *tBodyGyroMag*, *tBodyGyroJerkMag*). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing *fBodyAcc-XYZ*, *fBodyAccJerk-XYZ*, *fBodyGyro-XYZ*, *fBodyAccJerkMag*, *fBodyGyroMag*, *fBodyGyroJerkMag*. (Note the 'f' to indicate frequency domain signals).

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

* tBodyAcc-XYZ
* tGravityAcc-XYZ
* tBodyAccJerk-XYZ
* tBodyGyro-XYZ
* tBodyGyroJerk-XYZ
* tBodyAccMag
* tGravityAccMag
* tBodyAccJerkMag
* tBodyGyroMag
* tBodyGyroJerkMag
* fBodyAcc-XYZ
* fBodyAccJerk-XYZ
* fBodyGyro-XYZ
* fBodyAccMag
* fBodyAccJerkMag
* fBodyGyroMag
* fBodyGyroJerkMag

The set of variables that were estimated from these signals and kept in the dataset are: 

* mean(): Mean value
* std(): Standard deviation
* meanFreq(): Weighted average of the frequency components to obtain a mean frequency

Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:

* gravityMean
* tBodyAccMean
* tBodyAccJerkMean
* tBodyGyroMean
* tBodyGyroJerkMean  


#### Full list

1. SubjectId
2. ActivityId
3. ActivityLabel
4. tBodyAcc-mean()-X
5. tBodyAcc-mean()-Y
6. tBodyAcc-mean()-Z
7. tBodyAcc-std()-X
8. tBodyAcc-std()-Y
9. tBodyAcc-std()-Z
10. tGravityAcc-mean()-X
11. tGravityAcc-mean()-Y
12. tGravityAcc-mean()-Z
13. tGravityAcc-std()-X
14. tGravityAcc-std()-Y
15. tGravityAcc-std()-Z
16. tBodyAccJerk-mean()-X
17. tBodyAccJerk-mean()-Y
18. tBodyAccJerk-mean()-Z
19. tBodyAccJerk-std()-X
20. tBodyAccJerk-std()-Y
21. tBodyAccJerk-std()-Z
22. tBodyGyro-mean()-X
23. tBodyGyro-mean()-Y
24. tBodyGyro-mean()-Z
25. tBodyGyro-std()-X
26. tBodyGyro-std()-Y
27. tBodyGyro-std()-Z
28. tBodyGyroJerk-mean()-X
29. tBodyGyroJerk-mean()-Y
30. tBodyGyroJerk-mean()-Z
31. tBodyGyroJerk-std()-X
32. tBodyGyroJerk-std()-Y
33. tBodyGyroJerk-std()-Z
34. tBodyAccMag-mean()
35. tBodyAccMag-std()
36. tGravityAccMag-mean()
37. tGravityAccMag-std()
38. tBodyAccJerkMag-mean()
39. tBodyAccJerkMag-std()
40. tBodyGyroMag-mean()
41. tBodyGyroMag-std()
42. tBodyGyroJerkMag-mean()
43. tBodyGyroJerkMag-std()
44. fBodyAcc-mean()-X
45. fBodyAcc-mean()-Y
46. fBodyAcc-mean()-Z
47. fBodyAcc-std()-X
48. fBodyAcc-std()-Y
49. fBodyAcc-std()-Z
50. fBodyAcc-meanFreq()-X
51. fBodyAcc-meanFreq()-Y
52. fBodyAcc-meanFreq()-Z
53. fBodyAccJerk-mean()-X
54. fBodyAccJerk-mean()-Y
55. fBodyAccJerk-mean()-Z
56. fBodyAccJerk-std()-X
57. fBodyAccJerk-std()-Y
58. fBodyAccJerk-std()-Z
59. fBodyAccJerk-meanFreq()-X
60. fBodyAccJerk-meanFreq()-Y
61. fBodyAccJerk-meanFreq()-Z
62. fBodyGyro-mean()-X
63. fBodyGyro-mean()-Y
64. fBodyGyro-mean()-Z
65. fBodyGyro-std()-X
66. fBodyGyro-std()-Y
67. fBodyGyro-std()-Z
68. fBodyGyro-meanFreq()-X
69. fBodyGyro-meanFreq()-Y
70. fBodyGyro-meanFreq()-Z
71. fBodyAccMag-mean()
72. fBodyAccMag-std()
73. fBodyAccMag-meanFreq()
74. fBodyBodyAccJerkMag-mean()
75. fBodyBodyAccJerkMag-std()
76. fBodyBodyAccJerkMag-meanFreq()
77. fBodyBodyGyroMag-mean()
78. fBodyBodyGyroMag-std()
79. fBodyBodyGyroMag-meanFreq()
80. fBodyBodyGyroJerkMag-mean()
81. fBodyBodyGyroJerkMag-std()
82. fBodyBodyGyroJerkMag-meanFreq()


## Data

The raw data was split into training and test data files. Each set of files was provided as follows:

*Features:*  
Each observation was recorded as a space-separated feature vector containing a total of 561 feauture measurements in scientific notation. A separate file with feature labels was also provided.  

*Activities:*  
The activity IDs for each observation. A separate file with descriptive activity labels was also provided.  

*Subjects:*  
The volunteer subject IDs for each observation  


## Transformations

#### Step 1 - Read data

Read in all data files using the `fread` command. For the feauture files, `fread` automatically:

1. Separated the feauture vectors into 561 columns.
2. Transformed the meausurements into numeric data in standard decimal notation.

#### Step 2 - Combine files

1. For each of the 3 data categories (features, activities, subjects), combined test and training data sets into a single data set.
2. Attached activity labels to the combined activity IDs.

#### Step 3 - Merge and format data set

1. Attached subject IDs, activity IDs and activity labels to feauture data set.
2. Attached column names using the provided feauture labels (manually set names for ID and label columns).

#### Step 4 - Generate base data set

Reduced data set to contain only mean and standard deviation features. This reduced the data set from 564 columns (2 IDs, 1 label, 561 features) to 82 columns (79 features).

#### Step 5 - Generate summarised data set

1. Summarised base data set from previous step by averaging feautures by subject and activity.
2. Renamed feauture columns to indicate that they contain averages.

#### Step 6 - Write outputs to files

1. Base data set -> *tidydata.csv*
2. Summarised data set -> *tidydata_summary.csv*