# School_District_Analysis

## Project Overview
### Purpose
I have been asked by th school board to identify evidence of academic dishonesty in the math and reading scores for ninth graders at Thomas High School. 
To do this analysis I've been asked to replace Thomas High School ninth-grade math and reading schores with NaNs while keeping the rest of the data intact, and then to repeat the school district analysis that I previously completed with the original data. I will compare the two school district analyses to determine how they are affected by the changes to the grades.

## Results

### Affect on District Summary
The average math score and average reading score both decreased slightly when teh THS ninth-grade scores were removed. As a result, the passing percentages decreased slightly as well.
![Original district summary](https://github.com/secicciari/School_District_Analysis/blob/main/Resources/Original district summary.PNG)
![District summary with THS ninth-grade scores removed](https://github.com/secicciari/School_District_Analysis/blob/main/Resources/Adjusted district summary.PNG)

### Affect on School Summary
As you can see in the images below, the THS passing percentages decreased slightly (by less than .1%).
![Original THS school summary](https://github.com/secicciari/School_District_Analysis/blob/main/Resources/Original THS school summary.PNG)
![THS school summary with ninth-grade scores removed](https://github.com/secicciari/School_District_Analysis/blob/main/Resources/Adjusted THS school summary.PNG)

### Affect on Thomas High School's Performance
Overall, THS's performance is only minimally impacted when I remove the ninth-grade scores. THS is still ranked as the second highest performing school based on overall passing percentage.

### Affect on Scores by Group
- Math and reading scores by grade
	- The only impact on math and reading scores by grade is that the average scores for THS ninth-graders are showing as NaN. None of the other scores in this analysis were impacted by the removal of the scores.
- Scores by school spending
	- There is no impact on the scores by school spending.
- Scores by school size
	- There is no impact on the scores by school size.
- Scores by school type
	- There is no impact on the scores by school type.
  
## Summary
Four major changes in the updated school district analysis after reading and math scores for the ninth grade at THS were replaced with NaNs.
The biggest change in the updated analysis is that there is no score data for the ninth-graders at THS, so we can't compare their performance to other ninth-graders.
The size of the student population that we analyzed from THS went from 1,635 to 1,174 when we removed ninth-graders through the below code. This is why the passing percentages changed. 
'''
remaining_thomas_student_count = school_data_complete_df.loc[(school_data_complete_df["school_name"] == "Thomas High School"), ["Student ID"]].count() - ninth_thomas_student_count
'''
THS passing percentages for both math and reading decreased slightly when the ninth-graders' scores were replaced with Nan. This means that the ninth-graders had a higher passing percentage than the other grades, which could be evidence of academic dishonesty, although we can't determine that for certain based on this analysis.