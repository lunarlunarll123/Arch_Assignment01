# SA_Assignment01

Pick a GitHub repo that has some good history and large size (more than 500 files, and several hundreds if not thousands of commits).  I want each group 
to pick a different Repo as well, please post on Teams which repo you are using.  This will be first come first serve basis.  (Reasoning, one person 
could do all the work, and the entire class could copy all the data from that persons repo).

Setup for this assignment is here - http://www.adamtornhill.com/code/crimescenetools.htm

NOTE :
To get the evo log for before and after (as case study just uses one of these), but you will most likely want to use both.

git log --pretty=format:'[%h] %an %ad %s' --date=short --numstat --before=2013-09-05 --after=2012-01-01 > X_evo.log

Report should consist of:

1.	Repo description and rough number of files (hint the summary shown in the lecture).
1.	Timeframe chosen for analysis.  Try to limit the epoch of analysis to be no longer than a year.  Your repo may vary, so this is suggestion.  If you use the entire history, please give an justification of why.  Submit to (https://github.com/olekaspt/SA_Assignment01/blob/main/RepoAnalayzed.txt) your choice ASAP, as each group must evaluate a unique repo and time period
1.	Perform the analysis that was done in Case Study 1 – Effort as frequency, and complexity as Lines of Code (LOC).  And then use merge_comp_freqs.py 
Show the top 20 hits.  And then show top ten potential TD hotspots of that 20 using Names a guideline (i.e. skip the readme and build files). [This data to be analyzed will be file commit frequency, LOC]
A spreadsheet snippet, and using highlighting would make this easier to report 😊
1.	Pick the top two TD hotspot candidates to be used in Part 5 where we will look at the complexity trend. 
1.	Doing a deeper dive on it using git_complexity_trend.py (as was done in lecture).    Does the “code shape” complexity measurement confirm or deny the hypothesis that file is a TD hotspot?  
On the two files from the above step, using git_complexity_trend.py to plot the complexity trend for the files for the time period we are querying under.  To get the hash commit values for the file you can look at the specific file in github and see the history (ex. https://github.com/hibernate/hibernate-orm/commits/main/hibernate-core/src/main/java/org/hibernate/cfg/Configuration.java )
Would you classify this file as Deteriorating, Refactored, or stable.  It is possible to be all three 😊  as it could have been stable, then refactored, and then deteriorated.  But idea for this question is are we recommending the Architect of the produce to spend time looking at this file to see if we should refactor the file to reduce our TD.
1.	Perform a Sum of Coupling (SOC) analysis on the repo, and what are the top five files on most pull requests.   Filter this list by names (i.e. skip the build files and readme files).
1.	Perform an temporal analysis (using the -a coupling option).   And analyze the top 20 hits.  Do they look reasonable (module to unit test relationships)?  

NOTE: It is outside of the scope of this HW assignment to analyze the code in question 😊  You do not need to do a deeper dive like that.  If you are curious go for it, but this is outside the scope of the HW assignment.  So don’t “project creep” and end spending more time on this.

Most of these reports generate csv files, which can be brought up on MS Office\Google Docs.  So I’d use these to help format your HW assignment.  We will grade a certain percentage based on how tidy things look (i.e use tables and copy them over to doc, Don’t give a giant dump of data that line wraps and is a headache to grade).  Imagine you are giving a report to your boss on what files to investigate for TD and refactor.  You would want this to look readable.


1.	Perform  Evaluation of team members
Participation rubric of teammates.  List out for your all team members how much they participated.  This will go into your Lab report.
```
	             Member1	Member2	
Member1 (opinion)	55	     45
Member2 (opinion)	50	     50
```			

## Rubric
* 20% readability and format
* 60% Content
* 20% Conclusions (if required for each step).  For example, if you tell us there is no temporal coupling in any of the files, and we see two files are changed 80% of the time together from the data in the report, expect your grade to suffer. 


