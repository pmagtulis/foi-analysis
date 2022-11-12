# foi-analysis
Output repository of scraped information from foi-ph-scraper. A data analysis of FOI requests in the Philippines.

# Recent updates

|date|update|
|---|---|
|*Nov 11*|Updated data as of November 7, 2022| 
|*Sept 12*|Updated data as of September 6, 2022| 
|*June 27*|Updated data as of June 26, 2022| 
|*Apr 13*|Updated the notebook to merge recently scraped information from the FOI website. Data on **foi_final.csv** file now up to April 10, 2022.| 

# What is this?

An analysis of FOI requests data scraped by [foi-ph-scraper](https://github.com/pmagtulis/foi-ph-scraper) from the [FOI website](https://foi.gov.ph) of the 
Philippines.

# How it works

CSVs in the **output** directory are automatically updated each Sunday when the autoscraper pushes newly scraped information from the website. Files are overwritten
by new ones, but CSVs are generated with a unique file name each time the scraper runs to avoid losing older data.

For instance, if the scraper runs on February 8, it will have that latest data plus other entries before that so long as the scraped info do not exceed **3,000 
entries** as the scraper intends to do. The scraper is designed that way since one, older data from 2016 are already saved in a separate CSV. Two, this is to avoid 
scraping the entire site again which results in failure to scrape due to size.

Hence every week, new CSVs are added to the directory. Use the Jupyter Notebook to merge all those with older data from 2016 (contained in CSV with file name
**foi_final** for analysis.

# The process

1. Download everything into one path in your computer. Open Jupyter Notebook and run **foi-analysis.ipynb**.

2. The current notebook only read **foi_final.csv** through pandas in default. To add newly-scraped requests files, you need to **read the other CSVs in output
directory**, generate data frames out of them and **concat** them with the first data frame. 

3. Run analysis through pandas.

# Definition of terms

The following information were scraped from the website:

|column name|definition|
|---|---|
|**agency**|the name of the government agency where the request was submitted| 
|**date**|date when request was made through the FOI portal|
|**status**|shows at which stage of the FOI process is the file request in. Examples are "SUCCESSFUL", "PARTIALLY SUCCESSFUL", "DENIED", etc.|
|**date**|date when request was made through the FOI portal|  
|**period_covered**|a required information when filing a request meant to serve as filter for the extent of period covered by each request|
|**purpose**|the purpose why the request is being made, typically indicating how the data will be used. This is required when filing an FOI request|     
|**link**|hyperlink to each FOI request, containing details and direct messages between the filer and agency concerned. Only available for data from December 7, 2021|
|**reasons_denial**|a brief reason cited for a denial of request. Only available for data from 2016-December 31, 2021|

# Requirements

* Python: pandas, regex

# Contact

Prinz Magtulis, [ppm2130@columbia.edu](mailto:ppm2130@columbia.edu)

**Comments and suggestions are always welcome! All rights reserved.**
