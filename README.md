# Does Covid-19 affect youths disproportionately in the labour market?

Youth unemployment has been a pressing problem in the European Union and the Covid-19 pandemic only brought the issue to the fore. The International Labour Organization claims that the pandemic has a "devastating and disproportionate" impact on youth unemployment.

Many worry about a "lockdown generation" or "lost generation", as the current crisis might blight their long-term employment and earnings prospect. The Centre for Economic Policy Research found that one month of unemployment at age 18-20 is associated with a lifetime income loss of 2% as unemployed youths miss out on gaining skills and experience necessary to climb the career ladder.

In this project, I investigate if youths are disproportionately affected by the Covid-19 pandemic in the job market. This project uses unemployment data by sex and age for the European Union (obtained from the EU Open Data Portal). I also used an ISO dataset to map the ISO country codes to the country names. I will compare the average youth unemployment rate before and after March 2020. I then use difference-in-differences to isolate the differential impact of the pandemic on youth unemployment in Europe. This approach is sound insofar as there are no other factors that might cause unemployment rate to change at differing rates for youths and adults.

This personal project is meaningful for two reasons. As an economics major, crunching unemployment figures and investigating the inequalities in labour markets is something that feeds my curiosity. In addition, I have picked up R programming recently and I was happy to put it to practice on a real-world dataset.

# Methods
1) Importing data
2) Data cleaning (separating columns, joining tables, filtering, pivoting columns etc.)
3) Exploratory data analysis (data visualisation using ggplot)
4) Hypothesis testing (I ran a multivariate linear regression to investigate if the coefficient on the DiD variable is statistically significant)
The difference-in-differences was performed with 2 groups (youths, adults) across 2 time periods (pre-Mar 2020, post-Mar 2020)

# Exploratory Data Analysis
For most countries, there is a sharp rise in unemployment in early 2020. It seems that youth unemployment is already high before the pandemic and increased substantially in early 2020.
<img src="images/unemployment_by_country.png?raw=true"><br>
On an aggregate level, youth unemployment is significantly higher than adult and total unemployment. All unemployment rates increased in early 2020.
<img src="images/unemployment_by_age.png?raw=true"><br>
There does not seem to be any visually apparent difference in total unemployment rate between males and females. Male youths are slightly more likely to be unemployed vis-a-vis female youths but the gap seems to have narrowed after the onset of the pandemic.
<img src="images/unemployment_by_gender.png?raw=true"><br>

# Results of Difference-in-Differences Analysis
<img src="images/diff_in_diff_results.png?raw=true"><br>
I conducted a 2-tailed hypothesis test. From the results of the above regression, we observe that the coefficient on youths is statistically significant and positive at 0.1% level of confidence. This is congruent with our existing understanding that youths in the European Union face significantly higher unemployment rates.

While the DiD-coefficient is positive, it is not statistically significant. This implies that there is no evidence to suggest that youths in Europe are disproportionately affected by the ongoing global pandemic, at least based on data from the select group of countries and time-period. It might be useful to continue monitoring the numbers for the months to come to arrive at a more conclusive result.

Regardless, this project reinforces the severity of youth unemployment in Europe. The EU announced the Youth Employment Support package in July 2020, which will comprise of improved vocational education, training, apprenticeships and guidance. This package is a step in the right direction, and will hopefully mitigate pressures on youth unemployment.
