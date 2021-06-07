# Pewlett-Hackard-Analysis
Relational databases for analyzing retirement and mentorship data

## Overview of the analysis:
We were tasked with determining the number of people retiring, by title and department. Once that data was collected, we then needed to find out who of the remaining employees would be eligible for a mentorship program which would allow them to train with retiring senior staff.

##Purpose of the project

We set out to determine the number of retiring employees by title and identify which employees would be eligible to to participate in a mentorship program. Our Retiring Employees by Title query will show the titles of all employees born between January, 1 1952 and December, 31 1955. The first query retrieved the emp_no, first_name and last_name columns from the "employees" table and the title,from_date and to_date columns from the "titles" table. By using the primary key (employee number) and filtering the data by birth_date, we were able to put the information into a new table. A new table called "unique_titles" was created to hold the first occurance of the emp_no by using the DISTINCT ON function. To achieve the count, the function ORDER BY COUNT was used to show the total number of each title from the unique_titles table.
For mentorship eligibility, a query was created using columns from the "employees" and "dept_emp" table, it was then filtered on current employees born in 1965 then ordered by emp_no.

##Results
By running the queries, we were able to create for lists of data for the managers.

* All of the people who are eligible for retirement: [Retirement Titles CSV](https://github.com/ssheggrud/Pewlett-Hackard-Analysis/blob/081726c8fc4fb06dc2b5e8930594051c4a2d0b5d/Data/retirement_titles.csv)
* A tally of all the titles for those eligible for retirement: [Retiring Titles](https://github.com/ssheggrud/Pewlett-Hackard-Analysis/blob/081726c8fc4fb06dc2b5e8930594051c4a2d0b5d/Data/retiring_titles.csv)
* A list used to narrow the results down to the most recent title for each retiree: [Unique Titles](https://github.com/ssheggrud/Pewlett-Hackard-Analysis/blob/081726c8fc4fb06dc2b5e8930594051c4a2d0b5d/Data/unique_titles.csv)
* And finally, the list of current employees eligible for the mentorship program: [Mentorship Eligibility](https://github.com/ssheggrud/Pewlett-Hackard-Analysis/blob/081726c8fc4fb06dc2b5e8930594051c4a2d0b5d/Data/mentorship_eligibility.csv)

By using these lists, management should be able to make the appropriate decisions to limit the impact of the pending "silver tsunami" of retirees. Something the company may want to consider looking into is a comparison of the retiree salaries vs the current employee salaries. This would help underscore the potential positive impact of the retiring workforce on the bottom line. It would also help underscore potential wages for those who successfully complete the mentorship program. Additionally, it might be worthwhile to examine the employee to manager ratio to make sure that no department is understaffed or has an abundance of management. It could lead to a restructuring that has the potential to improve both working conditions and output.
