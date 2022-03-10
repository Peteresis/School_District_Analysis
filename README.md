# School District Analysis

# Overview

**Module 4 Challenge**: Thomas High School ninth-graders' reading and math grades appear to have been altered in the `students_complete.csv` file according to the school board. Even though the school board is unaware of the entire scope of the cheating, they are looking for assistance in upholding state testing requirements. Thomas High School's math and reading test scores should be replaced with NaN (Not a Number) values, but all other data should be left untouched. The school board wants to repeat the school district analysis conducted previously and receive a report about how these adjustments influenced the overall study once the reading and math scores have been replaced.

The analysis makes use of Python language Pandas library to review the data contained in the CSV file.

The Jupyter notebook contianing all the figures and datasets used for this report can be found at [PyCitySchools_Challenge_Final.ipynb](https://github.com/Peteresis/School_District_Analysis/blob/d692a11b75aac6d443415a7de0df3ded2d042fe7/PyCitySchools_Challenge_Final.ipynb)


# Results

## How is the district summary affected?

### **Fig. 1: School District Initial Summary**
![Fig. 1: School District Initial Summary](https://github.com/Peteresis/School_District_Analysis/blob/557a025e6e36ab12d7db77f577904ec7ee1d5184/Resources/Disctrict%20Summary%20Before.png)

### **Fig. 2: School District Final Summary**
![Fig. 2: School District Final Summary](https://github.com/Peteresis/School_District_Analysis/blob/557a025e6e36ab12d7db77f577904ec7ee1d5184/Resources/Disctrict%20Summary%20After.png)

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

The change in the Thomas High School ninth graders math and reading scores dropped the relative position of THS from the 2nd place in the district down to the 8th position.

## How does replacing the ninth-grade scores affect the following:

### Math and reading scores by grade

### **Fig. 7: Reading and Math Scores per School and Grade Summary - Before the change to 9th Grade at THS**
![Fig. 7: Reading and Math Scores per School and Grade Summary](https://github.com/Peteresis/School_District_Analysis/blob/dbd73fdbf25de8d7e581d4138e2f4720eb0d351d/Resources/Reading%20and%20Math%20Before.png)

### **Fig. 8: Reading and Math Scores per School and Grade Summary - After the change to 9th Grade at THS**
![Fig. 7: Reading and Math Scores per School and Grade Summary](https://github.com/Peteresis/School_District_Analysis/blob/dbd73fdbf25de8d7e581d4138e2f4720eb0d351d/Resources/Reading%20and%20Math%20After.png)

When reviewing the math and reading scores summary per school and grade, the change only affects the figures of Thomas High School, the numbers for the other schools remain unchanged.

### Scores by school spending

### **Fig. 9: Reading and Math Scores per School Size and Spending Summary - Before the change to 9th Grade at THS**
![Fig. 9: Reading and Math Scores per School Size and Spending Summary - Before the change to 9th Grade at THS](https://github.com/Peteresis/School_District_Analysis/blob/24ed7353f2666fc60e020768283d5abbd27c199c/Resources/Scores%20by%20School%20Spending%20Before.png)

### **Fig. 10: Reading and Math Scores per School Size and Spending Summary - After the change to 9th Grade at THS**
![Fig. 10: Reading and Math Scores per School Size and Spending Summary - After the change to 9th Grade at THS](https://github.com/Peteresis/School_District_Analysis/blob/24ed7353f2666fc60e020768283d5abbd27c199c/Resources/Scores%20by%20School%20Spending%20After.png)

The position of Thomas High School relative to other schools in the district did not change before and after making the change to the 9th graders; the school remained in 6th place in both cases.  This result was to be expected as the spending in each school is related to the number of students and not to the grades obtained.  Obviously, the reading and math average scores changed at THS, but that did not affect the total spending of the school.

### Scores by school size

### **Fig. 11: Grades Per School Size - Before the change to 9th Grade at THS**
![Fig. 11: Grades Per School Size - Before the change to 9th Grade at THS](https://github.com/Peteresis/School_District_Analysis/blob/f81e781ea6f9334e1f38da6df1eee945b36525ea/Resources/Spending%20Per%20School%20Size%20Before.png)

### **Fig. 12: Grades Per School Size - After the change to 9th Grade at THS**
![Fig. 12: Grades Per School Size - After the change to 9th Grade at THS](https://github.com/Peteresis/School_District_Analysis/blob/9473532f42a9d1dd9012cf10f116b3a5d5f0ab48/Resources/Spending%20Per%20School%20Size%20After.png)

The `Average Math Score`, `Average Reading Score` and the `% Overall Passing` values do not change from before to after the change to the grades of the 9th graders at Thomas High School.

There are no significant differences in math or reading scores between the groups `Small (< 1000)` and `Medium (1000-2000)`.  However, the scores drop considerably for the group `Large (2000-5000)`.  The `% Overal Passing` score stays between 90 to 91 for the Small and Medium groups, but drops to 58 to the Large group. 

### Scores by school type

### **Fig. 13: Grades Per School Type - Before the change to 9th Grade at THS**
![Fig. 13: Grades Per School Type - Before the change to 9th Grade at THS](https://github.com/Peteresis/School_District_Analysis/blob/e2a5eeb01f0f2c29ca24a4fcdff0b49755ed2c69/Resources/Spending%20Per%20School%20Type%20Before.png)

### **Fig. 14: Grades Per School Type - After the change to 9th Grade at THS**
![Fig. 14: Grades Per School Type - After the change to 9th Grade at THS](https://github.com/Peteresis/School_District_Analysis/blob/131fbbc63f0ce64b438d9147b1ed04a780694f6c/Resources/Spending%20Per%20School%20Type%20After.png)

When looking at the `% Overall Passing` score, it is evident that the `Charter` schools perform far better than the `District` schools. The first group received 90%, while the second received only 54%. The ratio is 1.67:1, which is quite substantial.

This large disparity appears to be driven primarily by Math, as `Charter` schools had an average score of 83.5 percent compared to 77 percent for `District` schools, a difference of 6.5 points. When looking at the reading scores, the gap between the two groups is less pronounced, just 2.9 points.

# Summary

Based on the data examined from the CSV file, we can arrive at the following conclusions:

1. The inclusion or exclusion of math and reading scores for 9th graders at Thomas High School has no meaningful impact on the School District's performance.
2. Based on the data studied, it is not possible to draw any conclusions about the possibility of dishonesty in the reading and math scores for ninth grade at Thomas High School. Perhaps if the analysis had focused on comparing THS's math and reading data with other schools using statistical analysis, it would have been possible to shed some light on this matter and confirm or deny the hypothesis, but the analysis was focused on reporting administrative metrics rather than on grading scores.
3. Small and medium-sized schools appear to perform better in terms of `Overall Passing Scores`. Large schools with over 2000 students underperform when compared to medium and small groups. There are exceptions to the norm, and data demonstrates that a large institution, such as `Wilson High School`, can achieve high Overall Grades despite its size.
4. From Figure 10 we can infer that the amount of money spent per student appears to have an inverse relationship with the grades earned. Schools in the highest budget category ($628 - $655) have abysmal Overall Scores hovering about 53%. The sole exception is Thomas High School, which spends $638 per pupil and has a 90.6 percent overall grade. This fact may support the notion of dishonesty, but it is not conclusive. The highest Overal Scores are seen near the bottom of the spending table, where the majority of schools have an Overal Score of 89 percent or above. 'Wilson High School,' once again, is the school in the category that spends less per student while achieving an enviable Overal Score of 90.6 percent.
5. In relation to the type of school, Figure 14 cleraly shows that `Charter` schools fare way better than `District` schools.


**From the data analyzed, it can be concluded that the schools that perfomd the best are Charter Schools, of Medium or Small size, and spending less than $625 per student**


