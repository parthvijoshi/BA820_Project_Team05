# Project Title (Primary) - A Data‑Driven Study of the Alone TV Series:  Survival, Strategy, and Screens
### Domain
Alone is a survival reality TV series on the History Channel in which 10 survivalists are dropped into remote wilderness locations, living in complete isolation and self-filming until they tap out or win. Survival shows are key assets for networks and streaming platforms, driving ratings, brand partnerships, and subscriptions.This dataset uniquely connects human performance under extreme isolation with audience engagement (viewership and ratings), offering a structured view of both survival outcomes and viewer behavior.
### Stakeholders
TV networks and producers: decisions on locations, difficulty, casting, and episode structure
Advertisers, sponsors, and outdoor-gear brands: identifying seasons and episodes that attract high-value audiences
Streaming platforms: promotion and catalog positioning of seasons
Viewers and fans: expectations around fairness, difficulty, authenticity, and entertainment value
### Dataset
Survivalists: demographics, home location, profession, days lasted, placement, medical evacuations, and detailed tap-out reasons
Episodes: air dates, U.S. viewership (millions), titles, opening quotes/authors, IMDb ratings, and rating counts
Seasons: filming locations, country, number of survivalists, latitude/longitude, and drop-off dates
Loadouts: up to 10 items per survivalist with detailed and simplified descriptions
Data Description
Size & structure: 70.52 KB; 94 entries; 22 columns; relational
Data types: integers, floats, booleans, date strings, and multiple categorical/text fields (names, locations, professions, quotes, reasons, items)
### Preliminary EDA
#### Contestants and Outcomes
- Winners are predominantly US men around age 30-40 in different professions, suggesting a recurring “champion profile” rather than random outcomes.
- Days lasted are highly skewed, with many early exits and a few extreme long-duration outliers.
- Medical tap-outs tend to occur after longer stays than family or personal exits, indicating different physical versus psychological limits.
#### Environment and Survival Conditions
- Filming locations (e.g., Quatsino, Patagonia, Great Slave Lake) vary in average days lasted, number of survivalists, and medical evacuation rates, implying location-specific survival profiles.
- Season number is strongly correlated (~0.8) with latitude/longitude, as later seasons move into different geographic and difficulty bands.
#### Audience Response
- Viewership declines after Season 1 while IMDb ratings remain relatively stable, indicating strong initial interest but weaker long-term retention.
- Episodes featuring intense survival moments (multiple tap-outs, late-stage survival) often align with local peaks in viewership and ratings, suggesting high-intensity content is more engaging.
  
### Winners profile  EDA based on M2

**Motivation:**  Help casting directors cast a diverse set of demographic and talent (“winner-type”, "looser-type","neither the winner nor looser" ) such that fairness and viewership is improved

| Category   | Winner (Result == 1) | Looser  (Result == 10) |  Distinction (Yes/No) |   |
|---------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|---|---|
| Country             | There were 10 winners even though there <br>were only 9 seasons because S4 had two winners.<br>Thus 70% US and 30% canadian won | All US<br>No looser for S4                    |  No |   |
| Age Range           | 24-50 <br>Mostly winners in the range 30-35                                                                                  | Range 23-55<br>Mostly 35                      | After 50 no winners. There might be a combination<br> of factors with age can play a role  |   |
| Gender              | Male                                                                                                                            |7/8 Male and 1/8 female                         | No  |   |
| Medically Evacuated | None                                                                                                                            | 2 evacuated one Male (in S6) and one female (S5) | Yes, winners not medically evacuated  |   |
|Locations            | Though most of locations are in Canada S1,S2,S3,S5,S6,S7,S8 US won;<br> where S4,S9 CAD WON                                                                                            | All loosers were from US           | No, As Quastino in S1 and S2 was won by US<br> and S4 were won by Canadian. Also the loosers<br> were from US  |   |
| Days Lasted         | Min 56 max 100 days                                                                                                             | Dont last more than 15 days                   |  Yes Winners last longer |   |
| Profession          |  Both Indoor(writer) and outdoor professionals won<br> however some outdoor professionals who work in tough environments<br> like correction officers and wilderness skills instructors did have the <br>lowest days lasted compared to others like hunting guide and even<br> freelance writers performed better than them                                              |        Both Indoor(writer) and outdoor professionals lost <br> howevers outdoor professionals like wildlife guide <br> lasted longer whereas indoor professional lasted for <br> less period                                       | No not clear  |   |
| Item (gear list)    |   all winners used Saw                                                                                                                |     Fishing gear was used by all loosers                                          | No, though there are some common tools,<br> SAW was possesed by all winners but <br> there were 70% loosers using it too   |   |


#### Motivation for Analysis
- Help casting directors cast a diverse set of demographic and talent (“winner-type”, "looser-type","neither the winner nor looser" ) such that fairness and viewership is improved
- Group locations into difficulty bands and link them to audience engagement.
- Cluster episodes by survival and narrative patterns and compare viewership outcomes.
#### Feasibility
Merging Constraint: It must be done carefully to avoid row duplication as it leads to wrong analysis



# Project Title (Backup) : Uncovering County-level Childcare Affordability in the United States
### Project Motivation and Key Stakeholders 
This project examines the economics of childcare affordability across U.S. counties using data from 2008–2018 published by the National Database of Childcare Prices. Rising childcare costs have become a critical economic and social issue in the United States, influencing parents’ employment decisions (particularly for mothers), household financial stability, and fertility choices. Understanding geographic patterns and the structural drivers of childcare costs is therefore essential for designing effective interventions that help families, and societies as a whole, achieve improved overall well-being. Through this project, we aim to help the governments, employers, and community organizations in identifying high-burden regions, targeting subsidies, and evaluating whether childcare access aligns with local income levels and workforce needs.
### Major stakeholders include:
Policymakers and government agencies at the federal, state, and county levels who design childcare subsidies, taxation, and workforce programs.
Employers and HR departments, particularly large firms, or regional labour coalitions, that consider childcare benefits as part of recruitment and retention strategies.
Families and caregivers, who actually bear the financial and logistical burden of childcare.
Children, the ultimate beneficiaries or victims of childcare affordability and availability.
Researchers and economists studying labour markets, inequality, and demographic change.
### Data Description
1. childcare_costs.csv - This is the primary dataset and contains county-level information on childcare costs, family structures, labour force participation, and other key demographic indicators from 2008-2018.
Data types: Float and integer
File size: 10.5 MB
Data structure: 34,567 rows × 61 columns
2. counties.csv - This auxiliary dataset provides county-level geographic identifiers, including county names, state names, and county FIPS codes.
Data types: Integer and object
File size: 0.10 MB
Data structure: 3,144 rows × 4 columns

## AI Disclosure
We used ChatGPT to assist with EDA coding and text refinement. All outputs were reviewed, modified, and validated by the authors, and links to the chat sessions are provided in the Google Collab notebook.
