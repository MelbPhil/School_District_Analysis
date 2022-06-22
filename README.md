# School_District_Analysis
Analyzing standardized testing trends (_using Python and Jupyter Notebook_)

### Overview of School District Analysis
I assisted the chief data scientist for a city school district in analysing the results of student standardized test scores, and how those results coorelated with various factors: school size, amount of funding, type of school, etc. 

After learning that a specific subcategory of the dataset may have been altered (_specifically, the reading and math scores for Thomas High School (THS)_), I reran the analysis, replacing all the allegedly tampered data with NaN's (_Not A Number_). The following summarizes how the removal of both the math and reading scores of Thomas High School ninth graders impacted the overall findings.

## Resources
- Data Sources: schools_complete.csv, students_complete.csv 
- Python: 3.7.13, Jupyter Notebook

## School District Analysis Results

- District summary:

The overall district summary barely changed after removing the scores of THS ninth graders.

_Origional dataset:_
![Pre_District_Summary](https://user-images.githubusercontent.com/106599446/174904200-6ac3d005-f864-4d8d-9cf0-ca9950d5e8ec.png)

_THS ninth graders removed:_
![Post_District_Sum](https://user-images.githubusercontent.com/106599446/174904228-5ab89c6b-c66f-4ed1-a462-b3e53df8b9e2.png)

As depicted in the images above, the greatest difference was in the percentage of students that passed reading, which was merely .3% lower after adjusting the dataset. The percentage of students passing math was .2% lower. And the average math scores and overall percentage of students passing math and reading were both .1% lower.

(_Note: a passing score means that a student received a 70 or higher on the standardized test_).

- Per School summary:

Unsurprisingly, in the school breakdown summary, the only school impacted by the removal of Thomas High School ninth graders was Thomas High School.

_Origional dataset:_
![Pre_school_summary](https://user-images.githubusercontent.com/106599446/174906062-f2acf645-6df3-4bdc-bc2a-18ea3f69eebf.png)

_THS ninth graders removed:_
![Post_School_Summary](https://user-images.githubusercontent.com/106599446/174906090-ee2aeb99-fb38-47fa-8c0e-16499d33f5f4.png)

What's most surprising about the above images (_and what's perhaps most interesting about the second round of analysis_), is the lack of change that results in removing Thomas High School ninth graders' reading and math scores. The greatest changes seen above are seen in the "% Overall Passing" and the "% Passing Reading" metrics (_the furtherst right, and second furthest right columns, respectively_).

- Thomas High School’s performance relative to the other schools:

Before and after removing the THS ninth graders, Thomas High School ranked second, in terms of "% Overall Passing", meaning they had the second highest percentage of students passing both reading and math. 

_Origional dataset:_
![Pre_Top_5](https://user-images.githubusercontent.com/106599446/174913097-032e7485-446e-46f7-a8ca-257afac45b76.png)

_THS ninth graders removed:_
![Post_Top_5](https://user-images.githubusercontent.com/106599446/174913087-28045751-3582-478f-86dc-6402cb1ca47f.png)

What's perhaps less obvious in the above images, is that Thomas High School was ranked fourth in "Average Math Score" when including the ninth grader's scores, and then dropped to sixth place once they were removed. Similarly, THS was ranked first in "% Passing reading" when including the ninth grader's scores, and then fell to third place once those students were removed. It is worth noting that these schools at the upper range of the index clustered closely together, and that the slight changes for THS' scores did result in the school losing multiple places on the leaderboards in the aformentioned categories.

- Math and reading scores by grade:

Because we segmented the data by schools and grades, the data that we removed does not have any impact on the other rows or columns in these DataFrames.

_Origional datasets:_

![Pre_Reading_By_Grade](https://user-images.githubusercontent.com/106599446/174919524-3d3239fc-7f90-4215-92b3-02b22286c08b.png)
![Pre_Reading_By_Grade](https://user-images.githubusercontent.com/106599446/175039113-6f2fe74a-8c2a-4074-b8ec-921b586f7ce6.png)

The only difference seen after removing the THS ninth graders (_examples not shown_) is that the THS ninth grader's scores are replaced with "NaN", indicating that their math and reading scores, respectively, have been removed from the overall dataset.

- Scores by school spending:

The removal of THS ninth graders scores had a negligable impact on the results for scores broken down by school spending.

_THS ninth graders removed:_

![Post_Scores_By_Spending](https://user-images.githubusercontent.com/106599446/174919587-88c5f78b-2020-499b-a3cc-3627a156140f.png)

I only show the data from the second round of analysis above, as both rounds produced the exact same table. What is interesting here, is that the data seems to indicate that there is a correlation between lower spending (per student) and higher testing performance.

- Scores by school size:

The removal of THS ninth graders scores had a negligable impact on the results for scores broken down by school size.

_THS ninth graders removed:_

![Post_Scores_By_Size](https://user-images.githubusercontent.com/106599446/174920002-80a92ef6-ccfc-4f60-bf83-bfd712ce9130.png)

I only show the data from the second round of analysis above, as both rounds produced the exact same table. What is most notable in the data presented here, Small and Medium sized schools performed rather similarly, however, the performance of students at larger schools was lower across the board.

- Scores by school type:

The removal of THS ninth graders scores had a negligable impact on the results for scores broken down by school type.

_THS ninth graders removed:_

![Post_Scores_By_Type](https://user-images.githubusercontent.com/106599446/174920061-f09fb9d0-93dd-4b3e-881c-86b969938406.png)

I only show the data from the second round of analysis above, as both rounds produced the exact same table. The data presented here finds that students at Charter schools scored higher than students from District schools. 

## School District Analysis Summary

As mentioned previously, what I found most surprising regarding the removal of THS ninth graders was in fact the lack of any substantial differences made to the overall performance of the school. It is perhaps possible that the THS ninth graders' scores were adjusted such that they would produce results in line with the other grades. Maybe they were previously dragging down the schools overall metrics, and someone decided to elevate them, but only to the point that they were alligned with the rest of the school. Had the scores raised the school's standings drastically, it would have been more obvious that they had been tampered with. 

Further analysis is needed to better understand the nature of the correlation between school spending (per student) and testing performance. Perhaps larger schools are spending more on average per student, but considering these larger schools are providing a less intimate teaching experience, their efforts in spending are less effective. More analysis needed before any difinitive conclution can be reached. 

