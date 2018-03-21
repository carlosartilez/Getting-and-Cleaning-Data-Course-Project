## Human Activity Recognition Using Smartphones Dataset CodeBook
Version 2.0

----

### Original Version Authors:

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

---

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. In this version, the obtained tidy dataset merged the two original randomly partitioned sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

See `'tidyData.txt'` for more details.

---

The dataset includes the following **Variables**:

- **_SubjectNum_**: Factor with 30 levels "1","2","3","4",..."30". Identifies the subject who performed the activity for each window sample.

- **_Activity_**: Factor w/ 6 levels "WALKING", "WALKING_UPSTAIRS", "WALKING_DOWNSTAIRS", "SITTING", "STANDING", "LAYING". Identifies each tested activity performed by each subject. 

- **_Features_**: Factor w/ 66 levels (details below). Identifies the measured signal for each corresponding Activity. The features selected on the original database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz.

   Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag).

   Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals).
   
   These signals were used to estimate variables of the feature vector for each pattern: '-X/Y/Z' is used to denote 3-axial signals in the X, Y and Z directions.

  For each Activity:

   - tBodyAcc-mean-X/Y/Z and tBodyAcc-std-X/Y/Z
   - tGravityAcc-mean-X/Y/Z and tGravityAcc-std-X/Y/Z
   - tBodyAccJerk-mean-X/Y/Z and tBodyAccJerk-std-X/Y/Z
   - tBodyGyro-mean-X/Y/Z and tBodyGyro-std-X/Y/Z
   - tBodyGyroJerk-mean-X/Y/Z and tBodyGyroJerk-std-X/Y/Z
   - tBodyAccMag-mean and tBodyAccMag-std
   - tGravityAccMag-mean and tGravityAccMag-std
   - tBodyAccJerkMag-mean and tBodyAccJerkMag-std
   - tBodyGyroMag-mean and tBodyGyroMag-std
   - tBodyGyroJerkMag-mean and tBodyGyroJerkMag-std
   - fBodyAcc-mean-X/Y/Z and fBodyAcc-std-X/Y/Z
   - fBodyAccJerk-mean-X/Y/Z and fBodyAccJerk-std-X/Y/Z
   - fBodyGyro-mean-X/Y/Z and fBodyGyro-std-X/Y/Z
   - fBodyAccMag-mean and fBodyAccMag-std
   - fBodyBodyAccJerkMag-mean and fBodyBodyAccJerkMag-std
   - fBodyBodyGyroMag-mean and fBodyBodyGyroMag-std
   - fBodyBodyGyroJerkMag-mean and fBodyBodyGyroJerkMag-std

- **_Measurement_**: Contains each mean or standard deviation of each measured signal on each corresponding Feature.

_Notes:_ 

- _Features are normalized and bounded within [-1,1]._
- _Each feature vector is a row on the text file._

For more information about the orginal datasets contact: activityrecognition@smartlab.ws

For more information in this simplified tidy dataset contact: carlos.artilez@gmail.com
