### Hi there 👋

Dataset -  https://www.kaggle.com/datasets/arnabchaki/data-science-salaries-2023
This dataset is about data science job salaries. The dataset contains 11 columns:
work year: The year the compensation was paid.
experience_level: The experience level in the job during the year
employment_type: The type of employment for the role
job title: The role worked during the year.
salary: The total gross salary amount paid.
salary currency: The currency of the salary paid as an ISO 4217 currency code.
salary in USD: The salary in USD
employee_residence: Employee's primary country of residence during the work year as an ISO 3166 country code.
remote ratio: The overall amount of work done remotely
company location: The country of the employer's main office or contracting branch
company size: The median number of people that worked for the company during the year
Lab2 

View(dssalaries)
first <- dssalaries$salary
mean(dssalaries$salary)
mean(first)
median(dssalaries$salary)
max(dssalaries$salary)
min(dssalaries$salary)
var(dssalaries$salary)
sd(dssalaries$salary)
IQR(dssalaries$salary, 0.25)
IQR(dssalaries$salary, 0.75)
medsalary <- 138000
meansalary <- 190695.6
minsalary <- 6000
maxsalary <- 30394000
sdsal <- 671676.5
lower <- meansalary - 3 * sdsal
upper <- meansalary + 3 * sdsal
dssalaries$salary[dssalaries$salary > lower & dssalaries$salary < upper]
sqrt(var(first))
IQR(first)
quantile(first, 0.25)
quantile(dssalaries$salary, 0.25)
quantile(first, 0.75)
quantile(first, 0.75) - quantile(first, 0.25)
quantile(first, 0.75) - quantile(first, 0.25)
Q1 <- 1e+05
Q3 <- 180000
IQR <- 80000
Q3 - Q1
meansalary - 3* sd
meansalary + 3* sd
mean(first)
med(first)
max(first)
maxsalary <- 30400000
maxsalary - minsalary
mean(first) - 3* sdsal(first)
mean(dssalaries$salary) - 3* sdsal (dssalaries$salary)
mean(first) + 3* sdsal(first)
values <- c(first, -1824334,2205725 )
lower <- -1824334
upper <- 2205725
values[values > lower & values < upper]
mean(values[values > lower & values < upper])
median(values[values > lower & values < upper])


lab3

Plot1 
ggplot(data = dssalaries, aes( x = salary_in_usd)) +
  geom_boxplot() +
  labs( x = "salary in usd", title = "Data Science Salaries")

plot2
ggplot(data = ds_salaries, aes( x = company_size , y = salary_in_usd))  +
  geom_violin( color = "violet", fill = "lightpink") + 
  labs( x = "company size", y = "salary in usd", title = "Data Science Job")


