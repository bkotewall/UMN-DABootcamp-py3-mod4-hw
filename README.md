Please refer to PyCitySchools_Challenge.ipynb for homework submission.
The module playbook of which this is all derived from is in
PyCitySchools_testing.ipynb

# py3-mod4-hw:  Test scores and circumstances.  How are they correlated? 

## Overarching method and goals.

We were given data about students, schools and the test scores yielded
by the students.  From the source data we are to illustrate relationships
between differing circumstances, e.g. different grades, different schools,
different funding per student, with respect to the student test scores.  

In our original study materials, once the school and student
information were loaded into seperate dataframes, the data was merged so that
school and student information were relatable to one another in subsequent
dataframe queries.

### Methods employed in data cleanup in subsequent attempt

In this assignment, we are to make the following adjustments:

There was new information that the data from Thomas High School's test
grades may in fact be contaminated with academic misconduct.  We are to
remove the testing data for all 9th grade tests, reading and math and redo
the reporting we performed in Step 1.  We adjusted also for total
student attendance because we removed the 9th grade testing population from
our consideration.  Last but not least, we re tabulated much of the test
passing summary data and re-inserted them into the same data frames that
were calculated in the previous step.

## Calculations performed:

On both the original and corrected data sets, the following steps were
performed: 

1) A series of calculations were performed to garner the number and percentage
   of students whom attained passing grades in their reading and math tests 
   respectively, using 70% as a pass mark.  
   
   This lead to computing the number and percentage of students that were 
   passing both tests.  
   
   A summary report of this data was presented in a dataframe.  

2) Further manipulation of the data was performed to group students passing 
   respect tests by student budget.  
   
   A new summary report was construed as a dataframe, using the the 
   same techniques as part (1).

3) Furthermore, students were grouped into budgetary bins based on the amount of 
   funding they were alloted.  
   
   This information was garnered via the highschool the student was attending 
   and henceforth one could acertain the budget per student.  
   Test scores were then tabulated per budget bin and collated into a dataframe.  

   Curiously we saw that student budget seemed to be inversely related to student test scores.

4) We then used school size as a groupby and performed the same analysis.
   Using the methods in step 3, a new data frame was created to showcase the
   results. 

5) We also used school typeas a groupby and performed the same analysis. 
   A new dataframe was used to showcase the results.


## Interpretation of results:

Originally with the erroneous test scores included, Thomas High School
performed poorly.  Once the 9th grade test scores were expunged, Thomas High
School Students were perceptably more performant in both reading and math
scores.  

Budget seemed to be inversely correlated with testing scores on both math and
reading.

Medium school sizes performed better than small or very large schools.

Last but not least, Charter schools out performed state schools by a large
margin.

N.B. This lab contains some elementary CI stuff deployed using github actions.  This was for my own edification.

