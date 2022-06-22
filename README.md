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

What's perhaps less obvious in the above images, but important to note, is that Thomas High School was ranked fourth in "Average Math Score" when including the ninth grader's scores, and then dropped to sixth place once they were removed. Similarly, THS was ranked first in "% Passing reading" when including the ninth grader's scores, and then fell to third place once those students were removed. It is worth noting that the schools in this range were all quite close in terms of score, and that the slight changes for THS' scores resulted in losing multiple places on the leaderboards in the previously mentioned categories.

- Math and reading scores by grade:

_Origional dataset:_

![Pre_Reading_By_Grade](https://user-images.githubusercontent.com/106599446/174919524-3d3239fc-7f90-4215-92b3-02b22286c08b.png)

Unsurprisingly, the only differences here after removing the THS ninth graders in the value for Thomas High School ninth graders themselves, which have no values listed for either math or reading. Because we segmented the data by schools and grades, the data that we removed does not have any impact on the other rows or columns in these DataFrames.

- Scores by school spending:

The removal of THS ninth graders scores has a negligable impact on the results for scores broken down by school spending. In both 

_THS ninth graders removed:_

![Post_Scores_By_Spending](https://user-images.githubusercontent.com/106599446/174919587-88c5f78b-2020-499b-a3cc-3627a156140f.png)


- Scores by school size:

_THS ninth graders removed:_

![Post_Scores_By_Size](https://user-images.githubusercontent.com/106599446/174920002-80a92ef6-ccfc-4f60-bf83-bfd712ce9130.png)


- Scores by school type:

_THS ninth graders removed:_

![Post_Scores_By_Type](https://user-images.githubusercontent.com/106599446/174920061-f09fb9d0-93dd-4b3e-881c-86b969938406.png)

## School District Analysis Summary
