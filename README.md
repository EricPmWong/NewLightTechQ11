# New Light Technologies (FEMA) - Question 11
Contributors: Linnea Miller, Aidan Keyes, Mohammed Faysal, Eric Wong
---
## Project Goal
#### Using Indeed or Glassdoor platforms together with number and type of affected businesses to estimate the expected economic loss due to a disaster.
--- 

### Deliverables:

1. Slideshow (https://docs.google.com/presentation/d/1vFJROQiT1h9lYUYn6DY9kdo7iQ4gsyy8PW1OYvT78lY/edit?usp=sharing)
2. Adzuna Scraper (https://github.com/EricPmWong/NewLightTechQ11/blob/master/AdzunaScrape.ipynb)
3. Adzuna Graphs (https://github.com/EricPmWong/NewLightTechQ11/tree/master/Adzuna-Graphs)
3. BLS Scraper (https://github.com/EricPmWong/NewLightTechQ11/blob/master/BLSscrapeGRAPH.ipynb)
4. BLS Graphs (https://ericpmwong.github.io/)
5. BLS Data (https://github.com/EricPmWong/NewLightTechQ11/tree/master/BLS-Data)
4. Glassdoor Scraper (https://github.com/EricPmWong/NewLightTechQ11/blob/master/glassdoor_scrape/scrape.ipynb)
5. SARIMA models Harvey+Irma (https://github.com/EricPmWong/NewLightTechQ11/blob/master/SARIMA-Harvey%2BIRMA.ipynb)
6. SARIMA model - Katrina (https://github.com/EricPmWong/NewLightTechQ11/blob/master/SARIMA-Katrina.ipynb)
7. SARIMA model - Sandy (https://github.com/EricPmWong/NewLightTechQ11/blob/master/SARIMA-Sandy.ipynb)
8. Industry Concat code (https://github.com/EricPmWong/NewLightTechQ11/blob/master/IndustryConcatScript.ipynb)
9. Industry by Disaster Data (https://github.com/EricPmWong/NewLightTechQ11/tree/master/Disaster-Industry-Data)
10. Team peer reviews (Sent via Slack)
---

### 3rd Party sites/tools:

- [Adzuna API](https://rapidapi.com/baskarm28/api/adzuna?gclid=Cj0KCQiAj4biBRC-ARIsAA4WaFiFc5JhXuZUpQS8Xcr7w-gS4qTdYHd7mbD0WhCFBk_4TmVUap0BqwAaAhlhEALw_wcB)
- [Bureau of Labor Statistics API](https://www.bls.gov/developers/home.htm)
- [Glassdoor - WARNING Glassdoor Authorization required to use](https://www.glassdoor.com/index.htm)
- [Github](https://www.github.com)
- [GoogleSlides](https://www.google.com/slides/about/)
- [glassdoor.com Scrape on scrapehero](https://www.scrapehero.com/how-to-scrape-job-listings-from-glassdoor-using-python-and-lxml/)


### Libraries and Imports:
-Matplotlib
-Numpy
-Pandas
-Plotly
-Requests
-Time/Datetime
-Json
-Sklearn
-Statsmodels
-Urllib
-Argparse
-Unicodecsv
-OS
-RE
-Lxml
-Sys
-Beautiful Soup

## Data Dictionary - glassdoor.com
- **City** - name of city
- **Company** - name of company
- **Days Old 1** - how old the job posting is
- **Days Old 2** - another field recording how old the job posting is
- **Location** - city name, state abbreviation
- **Name** - title of the position
- **Salary** - estimated salary range for position (string)
- **State** - state abbreviation
- **Url** - URL for spevicifc job posting on its own, NOT the link to listing in the overall list of search results
- **Job ID** - unique ID for a position; relevant to help remove duplicate scrapes later on 
- **URL_CHECK** - When using the **Url** column to extract URLs, we then take those URL's as input for  another, smaller scraper to get **Industry** and **Date Posted** - in the end, this column exists to verify that we're matching the correct Industry and Date Posted information to the preexisting columns
- **Industry** - industry of the company that posted the position
- **Date Posted** - actual date that the job was posted (vs. Days Old 1/2 that gives a relative measure of how old the posting is)

## Data Dictionary - Disaster Industry Data
- **col1** - Date
- **col2** - Aggregate employment for affected counties of Foldered Data

## Data Dictionary - BLS Data
- **Index** - Index (Fyi Reversed to reflect start by oldest date)
- **Date** - Dates
- **natural_resources_mining_all_employees** - Employment Figures
- **natural_resources_mining_avg_monthly_pay** - Avg industry wage per month
- **natural_resources_mining_aggr_value** - Employment and Wage combined (multiplied)
- **manufacturing_avg_monthly_pay** - Employment Figures
- **manufacturing_avg_monthly_payonstruction_avg_monthly_pay** - Avg industry wage per month
- **manufacturing_aggr_value** - Employment and Wage combined (multiplied)
- **trade_resources_all_employees** - Employment Figures
- **trade_resources_avg_monthly_pay** - Avg industry wage per month
- **trade_resources_aggr_value** - Employment and Wage combined (multiplied)
- **information_all_employees** - Employment Figures
- **information_resources_avg_monthly_pay** - Avg industry wage per month
- **information_mining_aggr_value** - Employment and Wage combined (multiplied)
- **financial_activities_all_employees** - Employment Figures
- **financial_activities_avg_monthly_pay** - Avg industry wage per month
- **nfinancial_activities_aggr_value** - Employment and Wage combined (multiplied)
- **professional_business_services_all_employees** - Employment Figures
- **professional_business_services_avg_monthly_pay** - Avg industry wage per month
- **professional_business_services_aggr_value** - Employment and Wage combined (multiplied)
- **education_health_services_all_employees** - Employment Figures
- **education_health_services_avg_monthly_pay** - Avg industry wage per month
- **education_health_services_aggr_value** - Employment and Wage combined (multiplied)
- **leisure_hospitality_all_employees** - Employment Figures
- **leisure_hospitality_avg_monthly_pay** - Avg industry wage per month
- **nleisure_hospitality_aggr_value** - Employment and Wage combined (multiplied)
- **other_services_all_employees** - Employment Figures
- **other_services_avg_monthly_pay** - Avg industry wage per month
- **other_services_aggr_value** - Employment and Wage combined (multiplied)
- **unclassified_all_employees** - Employment Figures
- **unclassifiedg_avg_monthly_pay** - Avg industry wage per month
- **nunclassified_aggr_value** - Employment and Wage combined (multiplied)
- **total_industries_aggr_value** - Employment and Wage combined (multiplied)




