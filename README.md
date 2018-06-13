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
* Open Secrets: data on donors' past contributions, also has a column "Occupation" that may link to industry.
Has an API but it is extremely limited.
* Open Corporates: Extensive US-centric/UK-centric (mostly) database of corporate information, has an API. Very strict API limits, and you have to email to request a key.
* ORBIS: Proprietary global database of companies, is the go-to for LLC entity matching, because it includes very detailed information for LLCs that you can leverage to match them to parent companies; user can decide which variables to export. Agent name, incorporation date, address, telephone are ones to pay particular attention to.

I've decided for this project to do my initial data analysis using data from 2010 onward; all the campaign donations that Cuomo has had as a governor. Later, this can be segmented into: 2014 campaign; 2018 campaign, etc. but the methodology will be the same.

### Methodology

First, a series of passes to get ALL THE DATA on each of the entities.

1. ORBIS will give us the most-complete data for each entity, so if we can find an entity on ORBIS first, we should stop there.

* First do a batch search, uploading a file not to exceed 1000 rows with one column: company name (no quotes), with no index and no header:

`$ split -l 999 unique_donors.csv chunk_donors` 

* Press the "View List of Results" button, and change your presets to determine what variables are exported.

* These steps will take forever. It's easier to do them one-by-one instead of simultaneously, since I got kicked out after opening too many windows (it slows way down, anyway).

* Export as tab-delimited text file, and specify ',' as the delimiter for ease of use going forward. Use "current list" from the drop down menu. No extra lines.

This step gets associated data for about 2/3 of the entities.

* Join this set of 13,000 business entities onto the original list of donors in Pandas, and check that the addresses match. This is important: what if there is a "Joan Johnson" in New York but a "Joan Johnson Ltd" company in New Haven: they should not match up, or if they do, there should be caveats. Avoid misattribution.

2. NYC-DB: We already know Cuomo is very connected to the real estate industry, so check for matches here.
Tables to pay special attention to: Acris, DOB jobs.

3. Open Secrets: Use regex to find donor names that have 'PAC' in them. Scrape Open Secrets' PAC search page for all of the PACs that are in the 13,000 unique donors list: [](http://opensecrets.org/pac/search)

4. Open Corporates: match registered addresses only. the API is good, but you must email and ask for an API key, and the API documentation is ridiculously, inexplicably, stupidly complicated.

5. What is left?

Second, after I've sucked up all the data possible, I'll use fuzzy matching to connect entities. Probably should not use fuzzy matching for full addresses: just for the streetname, city.

* [](http://jonathansoma.com/lede/algorithms-2017/classes/fuzziness-matplotlib/fuzzing-matching-in-pandas-with-fuzzywuzzy/)

* [](https://github.com/maxharlow/csvmatch)
