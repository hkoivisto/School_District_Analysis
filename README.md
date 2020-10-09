# School_District_Analysis

## Overview

### Purpose

Reading and math test scores were reviewed and aggregated across the school district, comprised of 15 high schools and 39,170 total students. After noticing potentially altered grades for the ninth grade class at Thomas High School, these grades were removed from consideration. The ninth grade students are still represented in the school spending per captia and total student body counts.

  District Summary Before Removing THS 9th Grade:
  
  ![Original_District_Summary](https://github.com/hkoivisto/School_District_Analysis/blob/master/Resources/Original_District_Summary.png)
  
  Updated District Summary:
  
  ![Updated_District_Summary](https://github.com/hkoivisto/School_District_Analysis/blob/master/Resources/Updated_District_Summary.png)
  
### Method

The pandas .loc function was used wihtin python to search for and replace all math and reading scores fromt he Thomas High School ninth grade class.

    ...
      student_data_df.loc[((student_data_df["grade"] == "9th") & (student_data_df["school_name"] == "Thomas High School")), 'reading_score'] = np.nan
    ...
      


## Results
  - How is the district summary affected?
     - Removing the grades of the ninth grade students at Thomas High School caused the average math and reading scores, as well as the passing percentages to decline slightly for the district. These students account for only 1.2% of the total district student count, and do not make a significant impact in the overall passing percentages. We can also infer that the altered grades for the THS 9th grade class were higher, but not significantlly higher, than the district averages.
  - How is the school summary affected?
     - Similarliy, the school summary for Thomas High School saw a small drop in score averges and passing percentage. The impact of the ninth grade class had a larger impact on Thomas High School individually than the school district as a whole. The overall passing average dropped from 90.95% to 90.63%.
  - How does replacing the ninth graders' math and reading scores affect Thomas High School's performance relative to the other schools?
     - Thomas High School remained the 2nd ranked school in the district by overall passing percentage.
  - How does replacing the ninth-grade scores affect:
    - Math and Reading Scores by grade?
       - Because the ninth grade scores were removed, this of course became a null category for THS. The other schools and grades were not affected.
    - Scores by school spending?
       - THS per capita spending fell into the third category, "$630-644 per student." THis category saw no change in average math or reading scores, to the nearest tenth of a point. This category also saw no change in passing percentages, when rounded to the nearest whole percentage.
    - Scores by school size?
       - THS is considred a "Medium" school with 1635 students. Removing the ninth grade scores also did not create an impact for the size category in average scores or passing percentages.
    - Scores by school type?
       - THS is a charter school. Removing the ninth grade scores also did not create an impact for the type category in average scores or passing percentages.
 
## Summary

Removing the suspect grades from the Thomas High School ninth grade class was the ehtical choice to make when representing district averages and passing percentages. We can see in our analysis that the THS ninth grade calss represented a very small percentage of the total district, and also reported scores very similar to the district averges. These facts explain why we saw very little change between our original and updated summaries. However, we can be confident that the updated summary shows the most accurate information.

### Changes Noted:

   - School district math average score was reduced from 79.0 to 78.9.
   - School district reading average score was reduced from 81.9 to 81.9.
   - School district math passing percentage was reduced from 75.0% to 74.8%
   - School district reading passing percentage was reduced from 85.8% to 85.7%.
   - School distric overall passing percentage was reduced from 65.2% to 64.9%. This was the most siginificant reduction accross the district.
