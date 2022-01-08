# community-sentinel-app

*About this app*

Community Sentinel (`community-sentinel-app.rmd`) is an rmarkdown/shiny demo app based on the flexdashboard package, associating mobility patterns and point-of-interest visits with covid-19 community infection within Philadelphia, estimating a risk profile for specific behaviors within neighborhoods.

*About our approach*

We model the dynamics of the COVID-19 epidemic as a network of neighborhoods connected by people moving about Philadelphia visiting places and points of interest, transmitting or acquiring the disease at a rate functionally related to the prevalence of the disease within their dwelling geographies and visited places. Following the approaches presented in [3, 4, 5, 6], we look at mobility patterns from anonymized and aggregated location data to analyze the progression of the epidemic within a dynamic network of locally connected sub-populations.

Using Philadelphia’s COVID-19 cases data, as published in OpenDataPhilly by the Philadelphia Department of Public Health, we track the daily course of the epidemic across neighborhoods, summarized by zip code.

Using SafeGraph's mobility data, as made available by the COVID-19 Data Consortium, we estimate the number of people who have visited any point of interest (POI), and which geography people visit from, on a weekly basis. Infection resulting from mobility is modeled to happen within one period and with two transmission paths, assuming random mixing: 1) from the encounter of visitors at specific places; and 2) from visitors' general mobility within and outside their local geographies, accounting for other non-POI mobility-related factors.

We aggregate mobility patterns by census tract, and distribute confirmed infections proportionally from zip code to census tract using zip-code-tract crosswalks, in order to use a common geographic unit between mobility and epidemic data.

*Credits*

COVID-19 data is provided by the Philadelphia Department of Public Health, published daily through the OpenDataPhilly platform, and cumulatively archived by Ambient Point. To access this data, visit the OpenDataPhilly COVID-19 catalog: https://www.opendataphilly.org/dataset?q=covid

Mobility data is provided by SafeGraph (https://www.safegraph.com/), a data company that aggregates anonymized location data from numerous applications in order to provide insights about physical places, via the Placekey Community (https://www.placekey.io/). To enhance privacy, SafeGraph excludes census block group information if fewer than five devices visited an establishment in a month from a given census block group. For more information, visit SafeGraph's documentation: https://docs.safegraph.com/docs

*References*

1. Master Question List for COVID-19 (caused by SARS-CoV-2); Science and Technology Weekly Report, Department of Homeland Security: https://www.dhs.gov/publication/st-master-question-list-covid-19
2. Determining Point-of-Interest Visits From Location Data: A Technical Guide To Visit Attribution; SafeGraph, Inc.: https://www.safegraph.com/visit-attribution
3. Bjørnstad, O.N, Shea, K., Krzywinski, M., Altman, N.; Modeling infectious epidemics; Nature Methods 17, 455-456 (2020)
4. Bjørnstad, O.N, Shea, K., Krzywinski, M., Altman, N.; The SEIRS model for infectious disease dynamics; Nature Methods 17, 555-558 (2020)
5. Long, E.F., Nohdurft, E., Spinler, S.; Spatial Resource Allocation for Emerging Epidemics: A Comparison of Greedy, Myopic, and Dynamic Policies; Manufacturing & Service Operations Management 20(2):181-198 (2018)
6. Chang, S., Pierson, E., Koh, P.W., Gerardin, J., Redbird, B., Grusky, D., Leskovec, L.; Mobility network models of COVID-19 explain inequities and inform reopening; Nature (2020)

*Disclaimer*

Warranty: References in this wep app to any specific commercial products, process, or service by trade name, trademark, manufacturer, or otherwise do not necessarily constitute or imply the endorsement, recommendation, favoring, opposition, discouragement or dissuasion by Ambient Point Corp. This web app and the information, software, and other material available on or accessible from this site are provided on an “AS IS” and “AS AVAILABLE” basis without warranties of any kind, either express or implied, including but not limited to warranties of title, non-infringement or implied warranties of merchantability or fitness for a particular purpose. Ambient Point Corp. does not warrant that the web app will be uninterrupted or error free or that any information, software or other material available on or accessible through the site is free of material errors or inaccuracies.

Liability: By accessing the information provided on this web app, each user waives and releases Ambient Point Corp. to the full extent permitted by law from any and all claims related to the use of the subject information. Under no circumstances shall Ambient Point Corp. be liable for any direct, indirect, incidental, special, punitive or consequential damages that result in any way from your use of or inability to use the web app or your reliance on or use of information, services, or merchandise provided on or through the site, or that result from mistakes, omissions, interruptions, deletion of files, errors, inaccuracies, defects, delays in operation or transmission, or any failure of performance.
