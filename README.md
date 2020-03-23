# Covid-19 Policy Effects

Different countries have taken different approaches to stopping or mitigating the covid-19 pandemic. I've found myself reading news and pouring over numbers trying to understand the impact of different measures, but have so far found that most of my day-to-day sources make it non-trivial to reason much about policy and infection and answer questions like:

 - When should I expect to see an effect from the closure of pubs and restaurants in the UK?
 - Has the lock-down in Italy caused a decrease in the number of infections per day so far? -- Would it be expected to?
 - At what points in time does it make sense to compare the effects of the different approaches taken by the Danish and Swedish governments?

To make it easier to see when we would expect policy measures to have an impact on numbers, I've plotted the two together for separate countries. I'm hoping that as more time passes the plots will also help in a coarse and unsophisticated way to assess at a glance if the measures have had an impact.

# How to read the plot

![UK Covid-19 Plot](/plots/uk.png)

The Figure contains three plots, the leftmost showing the development in total cases of Covid-19, while the two figures to the right plot the daily cases (top) and deaths (bottom). On all plots I've marked a few policy events with a vertical line. The dashed line of the same colour shows after which point we'd hope to see changes in the numbers based on the policy beginning to appear. The gap in days between the policy and start of effect is 12 days for confirmed cases and 16 days for deaths. For more information about these numbers, see the [about the data section](#about-the-data).

At the top of the plots I've marked the different phases the countries have taken to curtail the spread of the virus. I've found it useful because the confirmed cases only makes sense when considering how the government were testing people. 

# Analysis
I'll include plots from a few different countries here and jot down some thoughts if there's things standing out to me.

## The United Kingdom

![UK Covid-19 Plot](/plots/uk.png)

The UK shifted from a track and test phase to a contain phase on March 12th where only serious cases where tested. Recently testing has started for front-line workers with the first results expected in on March 23rd which will likely inflate confirmed cases. Compared with most other European countries, the UK has chosen to introduce policies like the closing of schools later.

## Germany

![DE Covid-19 Plot](/plots/de.png)

The German states are individually responsible for health component of the German response to covid-19 and have taken different approaches to testing. This makes it a bit harder to reason about the daily cases because different states might employ different testing practices at different times. It's also the reason I haven't included phases in the plot, since there isn't at least as far as I can gather a clear point in time when Germany has shifted from containment to delaying the virus.

## Scandinavia

![DK Covid-19 Plot](/plots/dk.png)
![SE Covid-19 Plot](/plots/se.png)
![NO Covid-19 Plot](/plots/no.png)

The approaches taken in Scandinavia are interesting to compare and contrast. All have similar health care systems and welfare systems, but their responses to covid-19 has been different. The measures taken by Denmark and Norway has been much more heavy handed or proactive (depending on how you look at it) than the Swedish response, where for example schools still aren't closed. Denmark stopped the contain phase using tracking and testing on March 11th with a big impact in the number of confirmed cases, as evident from the figure.

# About the data

To plot policy alongside covid-19 statistics and mark when it would be expected to take place, I've had to collect 3 different type of data:

## Covid-19 Daily Data
I've sourced [ourworldindata.com](https://ourworldindata.org/coronavirus-source-data)'s daily updated data on Covid-19 cases and deaths which in turn is sourced from the [European Centre for Disease Prevention and Control](https://www.ecdc.europa.eu) which publishes [Covid-19 data](https://www.ecdc.europa.eu/en/publications-data/download-todays-data-geographic-distribution-covid-19-cases-worldwide) daily in an excel spreadsheet. The number of confirmed cases is hugely dependent on the ability and approach of different countries to conduct tests and the numbers vary from place to place and day to day for different countries for this reason. The testing approaches of a lot of countries can roughly be divided in to a containment phase where cases a tracked and people at risk are tested and a delay phase where it's predominantly severe cases that are tested as patients are admitted to hospitals. I've marked these phases in the plots when applicable. The number of people dying from Covid-19 is a more consistent measure across time and place, but changes in policy takes longer to affect the figures. I've plotted both confirmed cases and deaths.

## Policy Decisions
The source of policy decisions of each country is annotated in the metadata used in the notebook. I've predominantly sourced it from timelines on [Wikipedia](https://en.wikipedia.org/wiki/2020_coronavirus_pandemic_in_Europe) and occasionally from newspaper articles and manually added them to the dataset used for the figures. Of course a policy decision does not neccesarily take effect the moment it's been announced. The UK policy of closing pubs and restaurants did not mean that many pubs and restaurants across the country had not already shut when the government urged people to stay home. In other countries, a policy might only cover part of the country while the plotted data covers all of it.

## Covid-19 Case Statistics
To understand the delay between policy is implemented and it shows up in the daily covid-19 datapoints, I've collected the following figures:
 * Incubation Period:
   * Infected to symptoms: [5.1 days](https://annals.org/aim/fullarticle/2762808/incubation-period-coronavirus-disease-2019-covid-19-from-publicly-reported)
 * Hospitalisation: 
   * symptoms to hospitalisation: [7 days in China](https://els-jbs-prod-cdn.literatumonline.com/pb/assets/raw/Lancet/infographics/coronavirus/Coronavirus_MedianTimeline_Infographic-1584612208650.jpg)
   * infected to hospitalisation: [12 days in China](https://jamanetwork.com/journals/jama/fullarticle/2762130)
 * Death
   * Symptoms to death: [14 days median in China](https://pubmed.ncbi.nlm.nih.gov/31994742/)
   * Symptoms to death: [8 days median in Italy](https://www.epicentro.iss.it/coronavirus/bollettino/Report-COVID-2019_17_marzo-v2.pdf)
   
Based on these sources I've chosen to use 12 days as the time between a policy is implemented to we expect to see results and 16 days between a policy is implemented to we expect it to impact the number of deaths. The latter number comes from adding 5 (incubation) to the average between the two last studies.

# About me and this repository

I'm not an epidemiologist and have no specialist knowledge that would make me uniquely qualified to bring you this data. I've written up these numbers to satisfy my own curiosity and share my findings with friends. 
