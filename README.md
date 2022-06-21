# School_District_Analysis
Analyzing standardized testing trends (_using Python and Jupyter Notebook_)

### Overview of School District Analysis
I assisted the chief data scientist for a city school district in analysing the results of student standardized test scores, and how those results coorelated with various factors: school size, amount of funding, type of school, etc. After learning that a specific subcategory of the dataset may have been altered (_specifically, the reading and math scores for Thomas High School (THS)_), I reran the complete analysis process, replacing all the allegedly tampered data with NaN's (_Not A Number_). The following summarizes how the removal of both the math and reading scores of Thomas High School ninth graders impacted the overall findings.

## Resources
- Data Sources: schools_complete.csv, students_complete.csv 
- Python: 3.7.13, Jupyter Notebook

## School District Analysis Results

- District summary affected:

The overall district summary barely changed after removing the scores of THS ninth graders.

_Origional dataset:_
![Pre_District_Summary](https://user-images.githubusercontent.com/106599446/174904200-6ac3d005-f864-4d8d-9cf0-ca9950d5e8ec.png)

_THS ninth graders removed:_
![Post_District_Sum](https://user-images.githubusercontent.com/106599446/174904228-5ab89c6b-c66f-4ed1-a462-b3e53df8b9e2.png)

As depicted in the images above, the greatest difference was in the percentage of students that passed reading, which was merely .3% lower after adjusting the dataset. The percentage of students passing math was .2% lower. And the average math scores and overall percentage of students passing math and reading were .1% lower.

(_Note: a passing score meant that the student received a 70 or higher on the exam_).

- School summary affected:

Unsurprisingly, in the school breakdown summary, the only school impacted by the removal of THS ninth graders was Thomas High School.

_Origional dataset:_
![Pre_school_summary](https://user-images.githubusercontent.com/106599446/174906062-f2acf645-6df3-4bdc-bc2a-18ea3f69eebf.png)

_THS ninth graders removed:_
![Post_School_Summary](https://user-images.githubusercontent.com/106599446/174906090-ee2aeb99-fb38-47fa-8c0e-16499d33f5f4.png)

What's most surprising about the above images (_and what's perhaps most interesting about the repeated analysis_), is the lack of change that results in removing Thomas High School ninth graders' reading and math scores. The greatest changes here are seen in the "% Overall Passing" and the "% Passing Reading" metrics (_the furtherst right, and second furthest right columns, respectively_). Due to the lack of change here, the subsequent changes (_or lack of changes_) in the following tables are rather underwhelming.

- Thomas High School’s performance relative to the other schools:

Before and after removing the THS ninth graders, Thomas High School ranked second, in terms of "% Overall Passing", meaning they had the second highest percentage of students passing both reading and math. 

_Origional dataset:_
![Pre_Top_5](https://user-images.githubusercontent.com/106599446/174913097-032e7485-446e-46f7-a8ca-257afac45b76.png)

_THS ninth graders removed:_
![Post_Top_5](https://user-images.githubusercontent.com/106599446/174913087-28045751-3582-478f-86dc-6402cb1ca47f.png)




- Math and reading scores by grade:

The only differences seen in this 

- Scores by school spending:
- Scores by school size:
- Scores by school type:

## School District Analysis Summary
