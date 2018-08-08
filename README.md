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

### Reporting

## Project Compassion NY LLC
- gave a one-time contribution of $50,000 on 12/13/2017
- Is based in California?? No idea what the connection is and probably not something we should pursue. Small fish!

## Restorative Continuum LLC
- CEO is Anthony Bachi, also the founder of Telistat, which is received a 5 million grant in 2016, and in August 2017 a Long Island facility got a 1.5 million grant to implement a Telistat Restorative Care Unit.
- https://www.prnewswire.com/news-releases/telistat-introduces-innovative-healthcare-unit-to-long-island-300501207.html

## RXR, REXSCOTT, GABELI... Various LLCs
- Gabeli and REXSCOTT each gave 65000 on the same date (05/19/2017). Gabeli may be the same as "The Gabeli Private Equity Fund"
-
- REXSCOTT, Gabeli, RXR all have the same address: '625 RXR PLZ UNIONDALE, NY, 11556'.
- I'm not sure if they are the same, related, renting the same space, etc.
- RXR = REXSCOTT, still not sure about Gabelli.
- The Real Deal "Earlier this year, Rechler was appointed by Cuomo to the board of the Metropolitan Transportation Authority and previously served on the board of the Port Authority of New York and New Jersey."
- RXR is a big Cuomo donor and was also covered by the Intercept recently (Cea Weaver pitched this story):
- https://theintercept.com/2018/07/12/andrew-cuomo-donations-ice/
- But the story just covers their connection to ICE, and RXR DEFINITELY gives to Cuomo not because of ICE but because of real estate, which is our framing.
- Cea told me off the record... 
    - "RXR bought this group Urban America/Renaissance Downtowns in like 2016 or 2017...and i think they have a strategy to like take over the suburbs in small towns in like Westchester, Nassau County that are on the LIRR or the Metro North they are hyper focused on increasing density. Typically that is met with really racist resistance. But like .... it's also an explict strategy to focus on profiting from people of color being pushed out of the city and like small towns in the suburbs don't have the urban planning infrastructure that New York City has, so what they are doing is essentially siphoning off and privatizing an essential City function of town planning and privatizing it. Making the plan. Doing the development. All of it."
    - "And of course Rechler is on the Board of the RPA...which is making a big deal about regional development and is super "respected" and a huge validator...and he uses it to valdiate his own projects"

## Triangle Equities
- Real Deal reported they gave 50,000, but they actually gave 75,000 total in 2017 (and have been a big donor since 2011, when they gave 25,000) if you count all of the LLCs that used the same Whitestone, NY address: 30-56 WHITESTONE EXPRESSWAY WHITESTONE, NY, 11354
- 496 WEST JERICHO TURNPIKE LLC, TRIANGLE EQUITIES JUNCTION LLC, 755 CO-OP CITY LLC
- Their big "Lighthouse Point" project was delayed in the senate: https://therealdeal.com/2015/12/18/state-senate-delays-funding-for-lighthouse-point-project/

## Macquesten Development LLC
- Donated 40,000 in 4 separate donations on 5/18/2017 and 12/15/2017
- 3 different LLCs, all from the same address: STE 100 438 FIFTH AVE PELHAM, NY, 10803	
- Also their principals are big donors (and named as donors):

    - Rella Fogliano – President, 111000 total given to Cuomo as of January 2018
    - Joseph Breda – Principal/Special Projects Manager, 85,000 total given to Cuomo as of January 2018
    
## Maple Heights Sub, LLC
- Gave 20,000 and 30,000 to cuomo from the same address, within 2 weeks at the end of 2017/beginning of 2018.
- Open Corporates says 700 N Sam Houston Road Realty LLC used to be named: 
    - 700 N. SAM HOUSTON ROAD REALTY, LLC
    - FOUR M HOLDINGS II, LLC
- Bloomberg lists Four M. Holdings as "specialty finance" and they have deep pockets, one of their affiliates bought an 80,000,000 collection of production facilities, one of which is in New York. Paul Hastings brags about it here: https://www.paulhastings.com/news/details/?id=d97fd769-2334-6428-811c-ff00004cbded

## STGG Realty LLC
- Donation total: 50,000 on 9/26/2017
- Owned by Steven E Plotnick according to a DOB application for a development that was declined: http://a810-bisweb.nyc.gov/bisweb/JobsQueryByNumberServlet?requestid=3&passjobnumber=321501987&passdocnumber=01
- Business address: 227 EAST 58TH STREET NEW YORK NY 10022
- Aro Holdings, LLC is also registered to Steven Plotnick, at the same address
- DOS ID: 4111399
- Can't find anything about Aro Holdings, LLC except that they are a landlord here: 18 EAST 68 STREET, MANHATTAN
- Don't seem to own any other buildings

## NYSAFAH PAC (New York State Association for Affordable Housing PAC)
- This is a very misleading name
- They have people in common with RSA (!)
- 400 members: real estate entities
- Have given tons of money to Cuomo, from this address: FRNT 3 242 W 36TH ST NEW YORK, NY, 10018
- They also have received money from BFC, Norstar, NYS senate committee housekeeping

## PITTA & GIBLIN LLP, VINCENT PITTA, ANTOINETTE PITTA, PITTA BISHOP DEL GIORNO & GIBLIN LLC, PITTA LLP
- Donation total: 245798.0
- From not very many addresses:
    '120 BROADWAY NEW YORK, NY, 10022'
    '120 BROADWAY NEW YORK, NY, 10271'
    '124 OVERLOOK TERRACE STATEN ISLAND, NY, 10305'
    'ATTN VINCENTPITTA, 120 BROADWAY NEW YORK, NY, 10271'
    'FL 28, 120 BROADWAY NEW YORK, NY, 10271'
    '124 OVERLOOK TER STATEN ISLAND, NY, 10305'
    'FL 28 120 BROADWAY NEW YORK, NY, 10271'
   
## Orbach Group, Harry Tawil
- Donation total: 35,000
- Harry Tawil works at the Orbach Group, which was in the news recently for their aggressive and unlawful eviction cases against rent-controlled tenants: https://therealdeal.com/2018/05/21/these-are-the-industry-players-cited-in-the-massive-nyt-housing-investigation/
- They gave under a few names which I found in Department of Buildings filings data

## Steiner Equities Group
- 

## Atlantic Development Group, Peter Fine, Marc Altheim
- Donation total: 120,000
- Donations under various LLC's, Peter Fine, and Marc Altheim.
- Some LLC's found through DOB data: 'KNICKERBOCKER MANAGEMENT LLC','KNICKERBOCKER MANAGEMENT, LLC'
    - Registered to Marc Altheim
- Peter Fine was in a fight with Marc Altheim, who owns 80 percent of Atlantic: https://therealdeal.com/2017/06/19/developer-peter-fine-sued-for-allegedly-withholding-3-5m-from-partner/
- Atlantic Development Group "made millions by selling 421a certificates to developers"...
- "Affordable Housing Developer"


*Edward Kaminsky*
- a luxury real estate agent. Is he related to senator Todd Kaminsky?

*Jonathan Resnick*
- member of REBNY, who used 7 different LLC's to contribute to Cuomo
- for a total of $20,000$ all on the same day: November 16, 2017.
- The LLC's were all totally different, but registered to the same address. The donations were for $2,500 each.

*Louis Esposito* used 5 different LLC's to donate 212,500 to Cuomo.
- He is a lobbyist with Durst, according to Little Sis: https://littlesis.org/org/68088-Durst_Organization_Inc
- Durst is a member of REBNY.

*Leonard Litwin* (deceased) and *Charles Dorego* are both executives at *Glenwood Management*, Cuomo's biggest single donor. All together they've donated more than 1/2 million to Cuomo.

*Jorge Madruga*
-ceo of MADDD Equities and has also given to Marco Rubio

*Exact Capital*
-50,000 to Cuomo on January 9. Politico reported, Real Deal summarized: https://therealdeal.com/2017/01/23/cuomo-raises-4-4m-with-help-of-real-estate-donors/

*Sabah Rajput*
- Walison Corporation
- Affordable Housing Developer, https://commercialobserver.com/2017/03/sterling-lends-16m-on-bronx-affordable-housing-development-15-more-projects-on-the-way/


