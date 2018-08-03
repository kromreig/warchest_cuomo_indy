# warchest_cuomo_indy

## This is a repository for the summer 2018 Cuomo campaign finance investigation for the Indy
## To do:

* look at contribution data from 2010
* find top donors by total donation sum ($) even if repeated donations
* find companies and industries for individuals
* find industries for company names
* find the interesting or stand-out cases that are worth extra reporting

## Methodology

How I decided to go about linking entities to industry, to better understand Cuomo's campaign finances.

### Data sources

* Board of Elections Data of Campaign Contributions: [](http://www.elections.ny.gov/CFViewReports.html https://nyopengovernment.com/NYOG/index.jsp)
* NYC-DB: NYC Housing Data for connecting individuals/LLCs to real estate entities
* Follow The Money
* Open Corporates: Extensive US-centric/UK-centric (mostly) database of corporate information, has an API. Very strict API limits, and you have to email to request a key.
* ORBIS: Proprietary global database of companies, is the go-to for LLC entity matching, because it includes very detailed information for LLCs that you can leverage to match them to parent companies; user can decide which variables to export. Agent name, incorporation date, address, telephone are ones to pay particular attention to.

I've decided for this project to do my initial data analysis using data from 2010 onward; all the campaign donations that Cuomo has had as a governor. Later, this can be segmented into: 2014 campaign; 2018 campaign, etc. but the methodology will be the same.

### Methodology


2. NYC-DB: We already know Cuomo is very connected to the real estate industry, so check for matches here.
Tables to pay special attention to: Acris, DOB jobs.


