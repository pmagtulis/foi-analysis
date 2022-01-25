# foi-analysis

This follows the **foi-ph-scraper** notebook and collates over 96,000 FOI requests into one file for analysis.

# What is this?

This is a code meant to run analysis on requests filed under the Philippines' **Freedom of Information** under Executive Order No. 2, Series of 2016 issued by
President Rodrigo Duterte. It analyzes the requests on various fronts such as trends, break from trends, agency treatment, types of requests, etc.

# Where does the information come from?

The bulk of data here came from a publicly accessible CSV file from the Presidential Communications Office, which manages the FOI portal. The CSV file is uploaded 
on this repository.

In addition, to cover for newer data specifically for 2022, we scraped information directly from the FOI website itself and **merged** them with the contents of
the CSV file. Over 96,000 records had been generated and cleaned. 

# Definition of terms

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

# Contact

Prinz Magtulis, [ppm2130@columbia.edu](mailto:ppm2130@columbia.edu)

**Comments and suggestions are always welcome! All rights reserved.**
