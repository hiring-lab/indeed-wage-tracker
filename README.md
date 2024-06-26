# Indeed Wage Tracker

**Note**: Beginning with publication of May 2024 data, Indeed Wage Tracker calculations for the UK, Ireland, Germany, France, Spain, Italy, Netherlands and the Euro Area were updated and changed, in part to harmonize methodologies across all nations and ensure a consistent universe of job postings included in national wage tracker series. The methodological treatment of job posting location was also modified in these nations in order to collect a higher number of relevant wage observations for final calculations. Data for the US and Canada were not impacted by these changes. More information on the data and methodology behind the Indeed Wage Tracker [can be found here](https://www.hiringlab.org/wp-content/uploads/2024/06/Wage_Tracker_Paper.pdf). In the interest of transparency, the number of observations collected in a given month for all nations is now published with the full dataset. Some historical data may show noticeable differences from prior data publications, and historic data may be somewhat volatile in case of any future restatements of underlying source data.

The Indeed Wage Tracker measures growth in wages advertised in job postings to help policymakers, labor market analysts, employers, and workers understand wage trends quickly and confidently.

We currently publish country-level trends for 9 countries: the UK, the US, Canada, and six euro-area countries — France, Germany, Ireland, Italy, the Netherlands, and Spain — that jointly account for over 80% of euro-area employment.

We will add more countries over time. We also plan to add data on wage growth in individual occupational categories, as we do in our [Job Posting Index](https://github.com/hiring-lab/job_postings_tracker).

The Indeed Wage Tracker will be updated monthly, with the exact timing depending upon Hiring Lab’s publication schedule.

## Methodology

The data in this repository are the average year-on-year percentage changes in wages and salaries advertised in job postings on Indeed, controlling for job titles.

To calculate the average rate of wage growth, we follow an approach similar to the Atlanta Fed [US Wage Growth Tracker](https://www.atlantafed.org/chcs/wage-growth-tracker), but we are tracking job titles, not individuals. We begin by calculating the median posted wage for each country, month, job title, region and salary type (hourly, monthly or annual). Within each country, we then calculate year-on-year wage growth for each job title-region-salary type combination, generating a monthly distribution. Our monthly measure of wage growth for the country is the median of that distribution. The data are not seasonally adjusted.

More information about the data and methodology is available in our accompanying research paper, [“Wage growth in Europe: evidence from job ads”](https://www.centralbank.ie/docs/default-source/publications/economic-letters/wage-growth-europe-evidence-job-ads.pdf) (Adrjan and Lydon, 2022), published in the Central Bank of Ireland’s Economic Letter series. We adopted this methodology in October 2022.

For Frequently Asked Questions regarding Indeed's data, click [here](https://www.hiringlab.org/indeed-data-faq/).

## Data Schema

The CSV file contains the following variables:

- jobcountry: two-letter code of the country of the Indeed site where the job was posted
- country: country name
- month: the month when the job was first posted
- n_obs: the number of observations (AKA sample size)
- posted_wage_growth_yoy: the year-on-year change in posted wages calculated using the methodology described above
- posted_wage_growth_yoy_3moavg: the 3-month lagged moving average of posted_wage_growth_yoy, which we use as our headline measure of growth

## License

The data generated by *Indeed Hiring Lab* are available under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

The data and files that we have generated are freely available for public use, as long as Hiring Lab is cited as a source.

## Indeed Hiring Lab

The [Indeed Hiring Lab](http://hiringlab.org/) is an international team of economists and data scientists dedicated to delivering insights that help drive the global labor market conversation.

This GitHub repo is intended to serve as a space to host various regularly-updated data series to help economists, journalists, and other interested parties better understand the labor market conditions in their countries.

We have economists covering Australia, Canada, France, Germany, Ireland, Japan, the UK, and the US. To read our research, visit the Indeed Hiring Lab blog: [https://www.hiringlab.org](https://www.hiringlab.org/).
