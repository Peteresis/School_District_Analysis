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
![Fig. 4: Per School Final Summary](https://github.com/Peteresis/School_District_Analysis/blob/a76ae9bb01ec3fc786d39876b56ee28787bf2379/Resources/Per%20School%20Summary%20After.png)

## How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?


## How does replacing the ninth-grade scores affect the following:


## Math and reading scores by grade


## Scores by school spending


## Scores by school size


## Scores by school type


# Summary

Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
