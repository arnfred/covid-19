# Introduction & Contents

I've created this repository to answer two questions that I've wondered about
during the Covid-19 pandemic:

1. What are the costs of inaction?
2. When will policy measures take effect and do they work?

<!-- vim-markdown-toc GFM -->

* [The cost of Inaction](#the-cost-of-inaction)
	* [Costly inaction in other countries](#costly-inaction-in-other-countries)
		* [Spain](#spain)
		* [Italy](#italy)
		* [United States](#united-states)
		* [Denmark](#denmark)
* [Covid-19 Policy Effects](#covid-19-policy-effects)
	* [The United Kingdom](#the-united-kingdom)
	* [Germany](#germany)
	* [France](#france)
	* [Italy](#italy-1)
	* [Spain](#spain-1)
	* [Scandinavia](#scandinavia)
	* [Switzerland](#switzerland)
* [About the data](#about-the-data)
	* [Covid-19 Daily Data](#covid-19-daily-data)
	* [Policy Decisions](#policy-decisions)
	* [Covid-19 Case Statistics](#covid-19-case-statistics)
* [About me and this repository](#about-me-and-this-repository)

<!-- vim-markdown-toc -->

# The cost of Inaction

In the plot below I model the difference in total deaths, had the UK government
enacted the lock-down just one week earlier:

![UK Covid-19 Prediction Plot](/plots/predicted_uk.png)

The model is a simple back-of-the-envelope model which assumes that once the
peak in daily deaths have been reached, it will drop by roughly 50% every 15
days. I've based this number on data from the following countries: France (8
days), Norway (8 days), China (14 days), Spain (16 days), Denmark (16 days) and
South Korea (17 days). For each country in the list, I've noted the days it
took them to drop 50% after the moment they peaked in parenthesis. Based on
these numbers I've picked the 'median' of 15 days. I've later adjusted the UK
to 25 since that looks more closer to the actual data.

In the plot I've marked the time the lock-down was implemented (solid blue
vertical line), plus the time the effects of the lock-down would be expected to
start impacting the number of daily deaths (dotted blue vertical line). I've
also done the same for the hypothetical lock-down that the government could
have implemented one week earlier (green solid vertical line).

As should be apperant from the plot, the cost of a week's delay would be equal
to more than 10000 deaths by June 8th. That's more than 40% of the total amounts of
deaths at this point in time. What's not shown in the graph is that the
difference by April 22nd (today's day as I'm writing this), the difference is
already 6100 deaths.

## Costly inaction in other countries

I've run the same analysis for a few other countries to see how the UK stacks up:

### Spain

![ES Covid-19 Prediction Plot](/plots/predicted_es.png)

In Spain the benefit of acting a week earlier would have been 9500 saved lives by June 8th.

### Italy

![IT Covid-19 Prediction Plot](/plots/predicted_it.png)

Italy has seen a slower reduction in deaths than most other countries past the peak of covid-19, and at this point 23 days of data later the number of deaths still haven't halved when I apply a rolling average of 3 days to remove outliers. Because of this I've plotted the italian model using a half time of 25 days rather than 15 days as I've used for the other countries. It's a good example of how the model is making some fairly rough assumptions that might very well not hold true for individual countries.

For a half-life of 25 days, the model predicts that roughly 11300 deaths could have been prevented. However the model outcome is fairly stable to changes in half-life and when I use 15 days instead, the outcome is 9400 saved lives.

### United States

![US Covid-19 Prediction Plot](/plots/predicted_us.png)

The US doesn't have a clear point in time when a lock-down was enacted because the different states are responsible for its implementation. By April 22nd, 40 states are in lock-down. The variance in the reported data on daily deaths makes me reluctant to conclude much based on the plot. It's very possible that the line of predicted deaths should lie significantly lower, in which case the figure of 39000 deaths would be much smaller.

### Denmark

![DK Covid-19 Prediction Plot](/plots/predicted_dk.png)

While I think this plot is interesting from a policy perspective, I also think that the Danish goverment did a fairly good job in enacting timely measures. It was one of the first European countries to send public servants home and close schools.

# Covid-19 Policy Effects

Different countries have taken different approaches to stopping or mitigating the covid-19 pandemic. I've found myself reading news and pouring over numbers trying to understand the impact of different measures, but have so far found that most of my day-to-day sources make it non-trivial to reason much about policy and infection and answer questions like:

 - When should I expect to see an effect from the closure of pubs and restaurants in the UK?
 - Has the lock-down in Italy caused a decrease in the number of infections per day so far? -- Would it be expected to?
 - At what points in time does it make sense to compare the effects of the different approaches taken by the Danish and Swedish governments?

To make it easier to see when we would expect policy measures to have an impact on numbers, I've plotted the two together for separate countries. I'm hoping that as more time passes the plots will also help in a coarse and unsophisticated way to assess at a glance if the measures have had an impact.

## The United Kingdom

![UK Covid-19 Plot](/plots/uk.png)

The UK shifted from a track and test phase to a contain phase on March 12th where only serious cases where tested. I'm suspecting results of tests conducted on March 12th came in up until 48 hours later, possibly explaining the drop after March 14th. Recently testing has started for front-line workers with the first results expected in on March 23th which will likely inflate confirmed cases. Compared with most other European countries, the UK has chosen to introduce policies like the closing of schools later.

* 2020-03-24: We're getting close to seeing the initial effects of the governments guideline to self-isolate if showing symptoms. I'm curious to see if the change in behavior that following along this guidance including working from home and washing hands more often will start showing up in the number of confirmed cases over the next few days. So far it's a bit early to draw any conclusions.
* 2020-03-30: The UK has started increasing the number of people tested since March 23rd.
* 2020-03-30: There's little sign that the government calls for self-isolation if symptoms were effective enough to stop the exponential growth of daily confirmed cases. I'm starting to think that school closures are key in limiting the spread based on the fact that younger parts of the population are more often asymptomatic[1] and still shown to be infectious[2]. Before school closures, kids could infect each other without showing symptoms and then go on to effect parents and teachers. 
* 2020-04-04: Unlike Italy, Spain, France and Norway, Daily cases are still going significantly up 12 days after the lockdown has been instanted. I've added test data to the plot to see if this increase of cases was correlated with a big increase in daily test results, but that doesn't look like it's the case.
* 2020-04-12: The spike in daily cases is due to a change in reporting. Up until this point, the UK only reported positive cases admitted to the hospital and didn't include test results for health care workers that turned out to be positive
* 2020-04-14: We're past the point where the policy effects of the lockdown should start show an impact on the number of daily deaths reported. However it's hard to be sure if the recent dip in daily deaths is due to less reporting during the easter week or an actual decrease.

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
* 2020-04-14: Both confirmed cases and deaths have seen huge swings in the last few weeks. I haven't found any information as to why, but I suspect that reporting for some cases don't happen daily. The general trend for both confirmed cases and deaths have been downwards since the effects of the lockdown were to start showing their impact which is positive.

## Italy

![IT Covid-19 Plot](/plots/it.png)

* 2020-03-24: Looking at the plot, the 15th and 16th of March stands out and looks to me like numbers of confirmed cases for March 15th were rolled in to the numbers for March 16th. The italian figures indicate that a lot of the measures deployed by the italian government only managed to slow down the spread of the virus at best. I would have expected to see an effect on confirmed cases from the country wide lock-down happen on March 21st onwards, but so far the few datapoints we have don't show any significant drop in the number of new cases. I can't help but wonder if the health care system is under such strain that new cases only get registered a significant while after showing symptoms, increasing the delay between policy measures being implemented and their effect in the numbers of confirmed cases.

* 2020-03-25: I start notice a drop in confirmed cases that my brain is keen to associate with the lockdown, but with only two datapoints,  I think it's better to wait a bit and see if it continues for another couple of days before getting too optimistic.
* 2020-03-30: The confirmed case rate in Italy has stayed stable since the lock-down, a pattern that was also seen in Wuhan. In China it took around 2 weeks before the number of daily confirmed cases had halved after the lockdown had set in.
* 2020-04-04: It's looking like the Italian daily cases are have been going down unsteadily for the last week and the death rate is showing signs of doing the same. Based on China and Italy, I'm suspecting that the time between infection and death is more like 14 (the conclusion in one paper based on data from China) than 8 (the conclusion in another paper based on early data from Italy). 
* 2020-04-12: Reported deaths in Italy keep showing a steady decline from the point of impact of the country-wide lock-down. It looks like it has taken around two weeks to decrease by 1/3rd. I wonder if this pattern holds true for other countries.

## Spain

![ES Covid-19 Plot](/plots/es.png)

The Spanish measures were at first isolated to the worst affected regions (Madrid, Basque country, a few villages in Catalonia), and only relatively late did the central government take nationwide actions.

* 2020-03-24: It's still too early to expect to see much effect from any nationwide action. I'm hopeful though that we'll start to see a drop in new cases as the nation-wide closing of schools approaches.
* 2020-03-30: It's early days but it looks like Spain is starting to see an impact in daily infection rates after the lockdown set in. I'm crossing my fingers that numbers will remain stable or start dropping over the next week.
* 2020-04-14: It's curious to see how Spanish confirmed cases kept steady for a week after the effects of the lockdown would be expected to start show their effect. I don't have testing data at hand to see if this was caused by increased testing. Deaths in Spain have been following the general pattern of a gradual decline roughly three weeks after the country wide lock-down measures were taken. Over the last 10 days the count of daily deaths has almost halved which is a reduction that is significantly faster than in Italy. 

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

I'm not an epidemiologist and have no specialist knowledge that would make me
uniquely qualified to bring you this data. It's out of a desire to better
understand current events, that I've taken the time to write up this data
analysis. By publishing it, I hope it might be useful for someone else, but I
also want to be clear that these numbers aren't authoritative in any way.
