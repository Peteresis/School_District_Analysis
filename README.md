# School District Analysis

# Overview

**Module 4 Challenge**: Thomas High School ninth-graders' reading and math grades appear to have been altered in the `students_complete.csv` file according to the school board. Even though the school board is unaware of the entire scope of the cheating, they are looking for assistance in upholding state testing requirements. Thomas High School's math and reading test scores should be replaced with NaN (Not a Number) values, but all other data should be left untouched. The school board wants to repeat the school district analysis conducted previously and receive a report about how these adjustments influenced the overall study once the reading and math scores have been replaced.

The analysis makes use of Python language Pandas library to review the data contained in the CSV file.

The Jupyter notebook contianing all the figures and datasets used for this report can be found at [PyCitySchools_Challenge_Final.ipynb](https://github.com/Peteresis/School_District_Analysis/blob/d692a11b75aac6d443415a7de0df3ded2d042fe7/PyCitySchools_Challenge_Final.ipynb)


# Results

## How is the district summary affected?

### **Fig. 1: School District Initial Summary**
![Fig. 1: School District Initial Summary](https://github.com/Peteresis/School_District_Analysis/blob/6dc7b7f1124e6651c4c6b6173f8f62654a8dfc3b/Resources/Disctrict%20Summary%20Before.png)

### **Fig. 2: School District Final Summary**
![Fig. 2: School District Final Summary](https://github.com/Peteresis/School_District_Analysis/blob/dada53eb63700219f07716a286c14fe529890425/Resources/Disctrict%20Summary%20After.png)

As the images above show, after changing to `NaN` the math and reading scores of all the **9th grade students at Thomas High School** there is almost no difference between the two summaries at district level.  The `Average Math Score` changed by 0.1 points, while the `Average Reading Score` is the same in both cases. It is worth noting that, based on the data extracted from the CSV, the number of 9th Grade students at Thomas High School is 461, which represents 461/39170 = 1.18% of the total.  This percentage is too low to make a big difference on the results for the total school district.

## How is the school summary affected?

### **Fig. 3: Per School Initial Summary**
![Fig. 3: Per School Initial Summary](https://github.com/Peteresis/School_District_Analysis/blob/a76ae9bb01ec3fc786d39876b56ee28787bf2379/Resources/Per%20School%20Summary%20Before.png)

### **Fig. 4: Per School Final Summary**
![Fig. 4: Per School Final Summary](https://github.com/Peteresis/School_District_Analysis/blob/a86c3c8665f038fee063711fb09df349dd6db4dc/Resources/Per%20School%20Summary%20After.png)

Before and after changing to `NaN`, the grades of 9th graders at Thomas High School (THS), the results stayed the same for all the schools, with the obvious exception of the THS school itself.  The values for `Average Reading Score` and `Average Math Score` remained pretty much unchanged, however, the value for `% Passing Reading`, `% Passing Math` and `% Overall Passing` dropped significantly for THS.  The reason is that the `.mean()` function in Pandas ignores the NaN values, but the `% Passing` is a formula that uses the `count()` function and whose result depends on the number of students.  Since the total number of students at THS is not affected because it is based in the number of `unique()` names but the number of students passing math or reading is reduced by ignoring the `NaN` values, then the `% Passing` is affected.

The formula for calculating the `% Passing` is `% Passing = Total Students Passing / Total Students in School * 100`


## How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?



### **Fig. 5: Initial School Ranking**
![Fig. 5: Initial School Ranking](https://github.com/Peteresis/School_District_Analysis/blob/b4a6fd16c4b25c62126efaa293da046975ccd1df/Resources/School%20Ranking%20Before.png)

### **Fig. 6: Final School Summary**
![Fig. 6: Final School Summary](https://github.com/Peteresis/School_District_Analysis/blob/b4a6fd16c4b25c62126efaa293da046975ccd1df/Resources/School%20Ranking%20After.png)


## How does replacing the ninth-grade scores affect the following:


## Math and reading scores by grade


## Scores by school spending


## Scores by school size


## Scores by school type


# Summary

Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
