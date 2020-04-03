# Contents

* [Covid-19 Policy Effects](#covid-19-policy-effects)
* [How to read the plot](#how-to-read-the-plot)
* [Analysis](#analysis)
	* [The United Kingdom](#the-united-kingdom)
	* [Germany](#germany)
	* [France](#france)
	* [Italy](#italy)
	* [Spain](#spain)
	* [Scandinavia](#scandinavia)
* [About the data](#about-the-data)
	* [Covid-19 Daily Data](#covid-19-daily-data)
	* [Policy Decisions](#policy-decisions)
	* [Covid-19 Case Statistics](#covid-19-case-statistics)
* [About me and this repository](#about-me-and-this-repository)

# Covid-19 Policy Effects

Different countries have taken different approaches to stopping or mitigating the covid-19 pandemic. I've found myself reading news and pouring over numbers trying to understand the impact of different measures, but have so far found that most of my day-to-day sources make it non-trivial to reason much about policy and infection and answer questions like:

 - When should I expect to see an effect from the closure of pubs and restaurants in the UK?
 - Has the lock-down in Italy caused a decrease in the number of infections per day so far? -- Would it be expected to?
 - At what points in time does it make sense to compare the effects of the different approaches taken by the Danish and Swedish governments?

To make it easier to see when we would expect policy measures to have an impact on numbers, I've plotted the two together for separate countries. I'm hoping that as more time passes the plots will also help in a coarse and unsophisticated way to assess at a glance if the measures have had an impact.

# How to read the plot

![UK Covid-19 Plot](/plots/uk.png)

The Figure contains three plots, the leftmost showing the development in total cases of Covid-19, while the two figures to the right plot the daily cases (top) and deaths (bottom). On all plots I've marked a few policy events with a vertical line. The dashed line of the same colour shows after which point we'd hope to see changes in the numbers based on the policy beginning to appear. The gap in days between the policy and start of effect is 12 days for confirmed cases and 19 days for deaths on average. That means that we might see effects of a policy change before the dotted line, but that most of the effect of it should happen after. For more information about these numbers, see the [about the data section](#about-the-data).

At the top of the plots I've marked the different phases the countries have taken to curtail the spread of the virus. I've found it useful because the confirmed cases only makes sense when considering how the government were testing people. It's been difficult to dig up the testing practices of different countries, and in many countries different parts of the country have taken different approaches at different times, so take these phases with a grain of salt.

# Analysis
I'll include plots from a few different countries here and jot down some thoughts if there's things standing out to me.

## The United Kingdom

![UK Covid-19 Plot](/plots/uk.png)

The UK shifted from a track and test phase to a contain phase on March 12th where only serious cases where tested. I'm suspecting results of tests conducted on March 12th came in up until 48 hours later, possibly explaining the drop after March 14th. Recently testing has started for front-line workers with the first results expected in on March 23th which will likely inflate confirmed cases. Compared with most other European countries, the UK has chosen to introduce policies like the closing of schools later.

* 2020-03-24: We're getting close to seeing the initial effects of the governments guideline to self-isolate if showing symptoms. I'm curious to see if the change in behavior that following along this guidance including working from home and washing hands more often will start showing up in the number of confirmed cases over the next few days. So far it's a bit early to draw any conclusions.
* 2020-03-30: The UK has started increasing the number of people tested since March 23rd.
* 2020-03-30: There's little sign that the government calls for self-isolation if symptoms were effective enough to stop the exponential growth of daily confirmed cases. I'm starting to think that school closures are key in limiting the spread based on the fact that younger parts of the population are more often asymptomatic[1] and still shown to be infectious[2]. Before school closures, kids could infect each other without showing symptoms and then go on to effect parents and teachers. 
* 2020-04-04: Unlike Italy, Spain, France and Norway, Daily cases are still going significantly up 12 days after the lockdown has been instanted. I've added test data to the plot to see if this increase of cases was correlated with a big increase in daily test results, but that doesn't look like it's the case.

[1]: https://medium.com/@andreasbackhausab/coronavirus-why-its-so-deadly-in-italy-c4200a15a7bf
[2]: https://www.patientcareonline.com/infectious-disease/covid-19-viral-load-asymptomatic-patient-found-similar-those-overtly-ill

## Germany

![DE Covid-19 Plot](/plots/de.png)

The German states are individually responsible for health component of the German response to covid-19 and have taken different approaches to testing. This makes it a bit harder to reason about the daily cases because different states might employ different testing practices at different times. It's also the reason I haven't included phases in the plot, since there isn't at least as far as I can gather a clear point in time when Germany has shifted from containment to delaying the virus.

* 2020-03-24: I find the German numbers hard to make sense of because of the big delta between confirmed cases on March 20th and March 21st. I haven't been able to figure out if this change is due to a change in testing practices or if it might indicate that measures taken before the school closures have started to show effect.
* 2020-03-30: German cases show a very irregular pattern that has fluctuated a lot but not shown any significant growth over the last 9 days. If we ignore the peak on March 20th and assume it's cases accumulated from earlier days (which is guesswork on my part), then it looks like the number of confirmed cases has been growing linearly and fairly slowly since the effect of school closures would be expected to set in.
* 2020-04-04: I think April 3rd data is a blip in the data. I'm hoping it'll be corrected as I pull in more updated data tomorrow.

## France

![FR Covid-19 Plot](/plots/fr.png)

The French government has categorised the epidemic in their [own four phases](https://sante.journaldesfemmes.fr/maladies/2622449-plan-orsan-reb-definition-signification-qui-declenche-coronavirus-definition/) of which we're currently in the third one, where the country is focused on dealing with on-going spread of the virus. I've tried to translate and summarise them in to one word at the top of the plot. Something I'm fairly sure I've done a mediocre job of.

* 2020-03-24: We're at the point in time where we would hope to see the initial effect of the early measures introduced by the French government, like limiting events with crowds of more than a 1000+ people. It's still too early to judge if they had any impact.
* 2020-03-30: It doesn't look like liming crowds made a significant impact in the exponential curve of the infection rate. This upcoming week will show if school closures and the lock down will stop the contiued exponential growth in confirmed cases.
* 2020-04-04: I'm guessing that March 30th and April 1st are related blips in the data, in which case daily cases seem to have stabilised somewhat after the effects of the country-wide lockdown started to set in on March 29th.

## Italy

![IT Covid-19 Plot](/plots/it.png)

* 2020-03-24: Looking at the plot, the 15th and 16th of March stands out and looks to me like numbers of confirmed cases for March 15th were rolled in to the numbers for March 16th. The italian figures indicate that a lot of the measures deployed by the italian government only managed to slow down the spread of the virus at best. I would have expected to see an effect on confirmed cases from the country wide lock-down happen on March 21st onwards, but so far the few datapoints we have don't show any significant drop in the number of new cases. I can't help but wonder if the health care system is under such strain that new cases only get registered a significant while after showing symptoms, increasing the delay between policy measures being implemented and their effect in the numbers of confirmed cases.

* 2020-03-25: I start notice a drop in confirmed cases that my brain is keen to associate with the lockdown, but with only two datapoints,  I think it's better to wait a bit and see if it continues for another couple of days before getting too optimistic.
* 2020-03-30: The confirmed case rate in Italy has stayed stable since the lock-down, a pattern that was also seen in Wuhan. In China it took around 2 weeks before the number of daily confirmed cases had halved after the lockdown had set in.
* 2020-04-04: It's looking like the Italian daily cases are have been going down unsteadily for the last week and the death rate is showing signs of doing the same. Based on China and Italy, I'm suspecting that the time between infection and death is more like 14 (the conclusion in one paper based on data from China) than 8 (the conclusion in another paper based on early data from Italy). 

## Spain

![ES Covid-19 Plot](/plots/es.png)

The Spanish measures were at first isolated to the worst affected regions (Madrid, Basque country, a few villages in Catalonia), and only relatively late did the central government take nationwide actions.

* 2020-03-24: It's still too early to expect to see much effect from any nationwide action. I'm hopeful though that we'll start to see a drop in new cases as the nation-wide closing of schools approaches.
* 2020-03-30: It's early days but it looks like Spain is starting to see an impact in daily infection rates after the lockdown set in. I'm crossing my fingers that numbers will remain stable or start dropping over the next week.

## Scandinavia

![DK Covid-19 Plot](/plots/dk.png)
![SE Covid-19 Plot](/plots/se.png)
![NO Covid-19 Plot](/plots/no.png)

The approaches taken in Scandinavia are interesting to compare and contrast. All have similar health care systems and welfare systems, but their responses to covid-19 has been different. The measures taken by Denmark and Norway has been much more heavy handed or proactive (depending on how you look at it) than the Swedish response, where for example schools still aren't closed. Denmark stopped the contain phase using tracking and testing on March 11th with a big impact in the number of confirmed cases, as evident from the figure.

* 2020-03-24: It makes me hopeful to see the Danish numbers of daily confirmed cases. There aren't enough data-points to establish a clear trend as far as I can tell, but numbers are starting to go down around the time that the first measures of the Danish state would be expected to take effect, so I'm crossing my fingers that this trend will continue and be strengthen once the stronger measures start having an impact on the number of cases too.
* 2020-03-25: Denmark has a spike in reported deaths because of a change in reporting practice[1].
* 2020-03-30: Denmark has rolled out more testing which I've marked on the graph at the top as '+Tests'. It has likely had an impact on the rise in daily cases around March 25th. The figures still look stable though, which is encouraging.

[1]: https://www.dr.dk/nyheder/indland/32-coronasmittede-danskere-er-doede

## Switzerland

![CH Covid-19 Plot](/plots/ch.png)

Despite being close to Italy, where a lot of foreign workers come everyday, Switzerland has been slow to issue nation-wide laws to react. The federal system was guilty - When Ticino faced a rapid growth of sick people, it reacted and closed its borders, while the rest of the cantons stayed open. Still to date, Switzerland has not officially locked the country entirely.

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
   
Based on these sources I've chosen to use 12 days as the time between a policy is implemented to we expect to see results and 19 (14+5) days between a policy is implemented to we expect it to impact the number of deaths. The latter number comes from the study based on Chinese data cited above and is chosen because both data from China and Italy are displaying this general pattern.

* 2020-04-04: I used to use the figure of 16 days between the time a policy is implemented and the starting point where we would expect to see an impact on the death rate. I had chosen this number as a average of the two studies cited above, but since then data has come out more clearly from Italy that supports the larger number.

# About me and this repository

I'm not an epidemiologist and have no specialist knowledge that would make me uniquely qualified to bring you this data. I've written up these numbers to satisfy my own curiosity and share my findings with friends. 
