# Indeed Wage Tracker

This repository contains the data behind the *Indeed Hiring Lab's* Wage Tracker data product. The data frequency is monthly and published after the 15th of each month.

We currently publish country-level trends for 9 countries: the UK, the US, Canada, and six euro-area countries — France, Germany, Ireland, Italy, the Netherlands, and Spain — that jointly account for over 80% of euro-area employment.

## Methodology

The data in this repository are the average year-on-year percentage changes in wages and salaries advertised in job postings on Indeed, controlling for job titles.

To calculate the average rate of wage growth, we follow an approach similar to the Atlanta Fed [US Wage Growth Tracker](https://www.atlantafed.org/chcs/wage-growth-tracker), but we are tracking job titles, not individuals. We begin by calculating the median posted wage for each country, month, job title, region and salary type (hourly, monthly or annual). Within each country, we then calculate year-on-year wage growth for each job title-region-salary type combination, generating a monthly distribution. Our monthly measure of wage growth for the country is the median of that distribution. The data are not seasonally adjusted.

More information about the data and methodology is available in our accompanying research paper, [“Wage growth in Europe: evidence from job ads”](https://www.centralbank.ie/docs/default-source/publications/economic-letters/wage-growth-europe-evidence-job-ads.pdf) (Adrjan and Lydon, 2022), published in the Central Bank of Ireland’s Economic Letter series. We adopted this methodology in October 2022.

Changes to the data can be followed under the "What's New" section of the Hiring Lab Data Portal: [data.indeed.com/whats-new](https://data.indeed.com/#/whats-new). For Frequently Asked Questions regarding Indeed's data, click [here](https://www.hiringlab.org/indeed-data-faq/).

## Data Schema

### Country-level

Filename: `posted-wage-growth-by-country.csv`

Data dictionary:

| variable                      | definition                                                                             |
|-------------------------------|----------------------------------------------------------------------------------------|
| jobcountry                    | Two-character [ISO 3166-1 alpha-2 country code](https://www.iban.com/country-codes)    |
| country                       | Country name                                                                           |
| month                         | Month when the job was first posted                                                    |
| n_obs                         | Number of observations (AKA sample size)                                               |
| posted_wage_growth_yoy        | Year-on-year change in posted wages                                                    |
| posted_wage_growth_yoy_3moavg | 3-month lagged moving average of `posted_wage_growth_yoy` (headline measure of growth) |

## License

The data generated by *Indeed Hiring Lab* are available under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

The data and files that we have generated are freely available for public use, as long as Hiring Lab is cited as a source.

## About Hiring Lab

[Indeed Hiring Lab](https://hiringlab.org) creates innovative data insights on the global labor market that inspire new conversations about the state of work. As the economic research arm of [Indeed](https://www.indeed.com/), the world's number one job site, Hiring Lab is driven by a team of leading economists and data scientists who provide real-time thought leadership on global labor market conditions, including hiring trends, salary information, popular skills, and employer benefits. Hiring Lab analyzes millions of data points across time collected from Indeed's proprietary job postings, resumes, and job seeker behaviors to reveal emerging trends in the United States and across the world.

The unique insights generated by Hiring Lab inform talent management, employment, and labor policy decisions for businesses, researchers, academics, and job seekers alike. Hiring Lab partners with a range of policy-making organizations and NGOs including the International Monetary Fund, the European Central Bank, and the Bank of Canada to produce timely, incisive research. Hiring Lab data is also regularly cited in prominent business publications such as The Wall Street Journal, CNN, Reuters, The Globe and Mail, Der Spiegel, and The Financial Times. Hiring Lab economists regularly speak about labor market trends at leading industry, policy, and academic conferences.

Indeed has websites in over 60 markets and 28 languages. Our economists have a deep knowledge of the factors that affect global markets and are based across the world in the United States, Canada, the United Kingdom, Ireland, Germany, France, Japan, and Australia.

If you are interested in data about other markets, please contact us at <hiringlabinfo@indeed.com>.
