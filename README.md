# School_District_Analysis
## Overview of School District Analysis
The purpose of the analysis was to study fifteen school districts and their students to compare reading and math scores. School spending, school size, and school type were also studied to compare reading and math scores among the fifteen schools. The school board also wanted to repeat the school district analysis after math and reading scores were removed from the database for Thomas High School ninth graders.

## Results

### District Summary
The school district has 15 schools with 39,170 students and a total budget of 24.65 million dollars. The average math and reading scores are not high enough for the school board and they are concerned with the scores especially the 64% overall passing percentage.

Total Schools	Total Students	Total Budget	  Average Math Score	Average Reading Score	% Passing Math	% Passing Reading	% Overall Passing
0	    15	    39,170	        $24,649,428.00	78.9	               81.9	                  75.9	          86.9	             64.1

### School Summary
Each of the fifteen schools was analyzed according to type of school, total students, budget, per student budget, average math score, average reading score, percent passing math, percent passing reading, and overall passing percentage which shows the percentage of students passing both math and reading.

School              Type	   Total Students	Budget	      Per Student Budget	Ave Math	Ave Reading	% Passing Math	% Passing Reading	% Overall Passing
Bailey High School	District	4976	        $3,124,928.00	$628.00	            77.048432	81.033963	   66.680064	    81.933280	        54.642283;
Cabrera High School	Charter	  1858	        $1,081,356.00	$582.00	            83.061895	83.975780	   94.133477	    97.039828	        91.334769
Figueroa High School	District	2949	      $1,884,411.00	$639.00	            76.711767	81.158020	   65.988471	    80.739234	        53.204476
Ford High School	District	 2739	          $1,763,916.00	$644.00	            77.102592	80.746258	   68.309602	    79.299014	        54.289887
Griffin High School	Charter	1468	          $917,500.00	  $625.00	            83.351499	83.816757	   93.392371	    97.138965	        90.599455
Hernandez High School	District	4635	      $3,022,020.00	$652.00	            77.289752	80.934412	   66.752967	    80.862999	        53.527508
Holden High School	Charter	427 	          $248,087.00	  $581.00	            83.803279	83.814988	   92.505855	    96.252927	        89.227166
Huang High School	District	2917	          $1,910,635.00	$655.00	            76.629414	81.182722	   65.683922	    81.316421	        53.513884
Johnson High School	District	4761	        $3,094,650.00	$650.00	            77.072464	80.966394	   66.057551	    81.222432	        53.539172
Pena High School	Charter	962	              $585,858.00	  $609.00	            83.839917	84.044699	   94.594595	    95.945946	        90.540541
Rodriguez High School	District	3999	      $2,547,363.00	$637.00	            76.842711	80.744686	   66.366592	    80.220055	        52.988247
Shelton High School	Charter	1761	          $1,056,600.00	$600.00	            83.359455	83.725724	   93.867121	    95.854628	        89.892107
Thomas High School	Charter	1635	          $1,043,130.00	$638.00	            83.350937	83.896082	   66.911315	    69.663609	        65.076453
 Wilson High School	Charter	2283	          $1,319,574.00	$578.00             83.274201	83.989488	   93.867718	    96.539641	        90.582567
Wright High School	Charter	1800	          $1,049,400.00	$583.00	            83.682222	83.955000	   93.333333	    96.611111	        90.333333

### Thomas High School performance
Thomas High School has a passing math percentage of 67% and a passing reading percentage of 70%. The percentage of students passing both math and reading (overall passing percentage) is 65%. The numbers are low compared to other schools and Thomas High School has a high spending amount per student ($635/student) compared to per student budgets of the other high schools. 

### Replacement of ninth grade scores
The loc method was used on the student_data_df to select all the reading and math scores from the 9th grade at Thomas High School and replace them with NaN. The code to replace both scores are:
student_data_df.loc[(student_data_df["grade"]=="9th") & (student_data_df["school_name"]=="Thomas High School"),"reading_score"] = np.nan
student_data_df.loc[(student_data_df["grade"]=="9th") & (student_data_df["school_name"]=="Thomas High School"),"math_score"] = np.nan

The new math and reading percentages for Thomas High School are shown below:
Thomas High School	Charter	1635	          $1,043,130.00	$638.00	            83.350937	83.896082	  93.185690	     97.018739	        90.630324

#### Math and Reading Scores
The math and reading scores of Thomas High School went up significantly when the ninth grade scores were removed. For math, the percentage of students passing math changed from 67% to 93%. For reading, the percentage of students passing reading changed from 70% to 97%. The overall passing percentage increased from 65% to 91%.

#### Scores by School Spending
The percentage passing math, percentage passing reading, and the overall passing percentage increased for the spending bin of $630-644. This is due to Thomas High School being categorized in that spending bin at $638/student. The significant increase in the math and reading scores after the 9th graders at Thomas High School were removed from the dataframe results in an increase in scores for the spending bin of $630-644.

#### Scores by School Size
Thomas High School had a student population of 1635 and the number decreased to 1174 when the 9th grade was removed from the dataframe. Both of the figures are in the medium size range for the high schools with a student population between 1000-2000 students. Because the 9th grade was removed, the math and reading scores increased in the medium size category along with the overall passing percentage.

#### Scores by School Type
Thomas High School is a charter school and the passing percentages for math and reading were much higher than the district schools when all 39,170 students were considered. When the 9th graders at Thomas High School were removed from the database, the passing percentages for math and reading did not change significantly because of the strong passing percentages of the other charter schools.

## Summary of Four Major Changes
There are four significant changes to the new dataframe when the ninth graders from Thomas High School are removed.
###
For Thomas High School, the percentage of students passing math increased from 67% to 93%.
###
For Thomas High School, the percentage of students passing reading increased from 70% to 97%.
###
For Thomas High School, the overall passing percentage increased from 65% to 91%.
###
Thomas High School became the second best performing high school after Cabrera High School which is another charter school.
