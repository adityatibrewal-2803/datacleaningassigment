# Code Book

The script `run_analysis.R`performs the below activities:

* Step 1: Setting up the working directory

* Step 2: Downloading and unzipping the input dataset

* Step 3: Merging the training and test data - Training and test data ses are joined with respective activity codes and subject IDs, and then merged together. Files used:<br/>
`UCI HAR Dataset/train/X_train.txt`: Training dataset<br/>
`UCI HAR Dataset/train/y_train.txt`: Activity codes for respective rows of training data<br/>
`UCI HAR Dataset/train/subject_train.txt`: Subjects for respective rows of training data<br/>
<br/>
`UCI HAR Dataset/test/X_test.txt`: Test dataset<br/>
`UCI HAR Dataset/test/y_test.txt`: Activity codes for respective rows of test data<br/>
`UCI HAR Dataset/test/subject_test.txt`: Subjects for respective rows of test data<br/>

* Step 4: Selecting mean and standard deviation columns. Files used:<br/>
`UCI HAR Dataset/features.txt`: Helps obtain columns which need to be extracted

* Step 5: Replacing activity code with activity description<br/>
`UCI HAR Dataset/activity_labels.txt`: Activity code and name mapping

* Step 6: Calculating mean based on activity description and subject

* Step 7: Creating the `output` files<br/>
`wearablesdata.txt`: The cleaned up dataset<br/>
Key Fields:<br/>
&nbsp;&nbsp;* activitydescription: Name of the activity being carried out.<br/>
    &nbsp;&nbsp;&nbsp;&nbsp;Character<br/>
    &nbsp;&nbsp;&nbsp;&nbsp;Possible values:<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;WALKING<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;WALKING_UPSTAIRS<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;WALKING_DOWNSTAIRS<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;SITTING<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;STANDING<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;LAYING<br/>
&nbsp;&nbsp;* subjectid: Random ID between 1-30 given to each subject
&nbsp;&nbsp;* datatype: Specifies if this is training data or test data<br/>
    &nbsp;&nbsp;&nbsp;&nbsp;Character<br/>
    &nbsp;&nbsp;&nbsp;&nbsp;Possible values:<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;train<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;test<br/>
&nbsp;&nbsp;* The remaining fields contain mean and std values which have been explained in file `features.txt`<br/><br/>
`wearablesdatameans.txt`: Averages at activity description and subject level<br/>
Key Fields:<br/>
&nbsp;&nbsp;* activitydescription: Name of the activity being carried out.<br/>
    &nbsp;&nbsp;&nbsp;&nbsp;Character<br/>
    &nbsp;&nbsp;&nbsp;&nbsp;Possible values:<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;WALKING<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;WALKING_UPSTAIRS<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;WALKING_DOWNSTAIRS<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;SITTING<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;STANDING<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;LAYING<br/>
&nbsp;&nbsp;* subjectid: Random ID between 1-30 given to each subject
&nbsp;&nbsp;* The remaining fields contain mean of each variable from wearables dataset