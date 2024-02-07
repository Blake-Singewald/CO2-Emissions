Authors: Jerrica Raemer, Blake Singewald, Jesse Rivera & James Montgomery<br>
Instructor: Thomas Tellner<br>
Bootcamp: UofO-VIRT-DATA-PT-12-2023-U-LOLC-MWTH<br>
2/7/2024

# Correlation of CO<sub>2</sub> Emissions and Water Toxins

## INTRODUCTION:

  Most of the world’s population is acutely aware of the yearly net increase of carbon dioxide, a greenhouse gas released from the combustion of hydrocarbons which currently is the main energy source for almost all countries.<sup>1</sup> Our group hypothesizes that within countries with high CO2 emissions there will also be moderate to high levels of water toxins within those countries’ water catchments. To test our hypothesis, we incorporated datasets of countries’ population growth <sup>2</sup>, CO2 emissions by country <sup>3</sup> and water toxins present in three countries with the highest amount of CO2 emissions per capita and three countries with the lowest amount per capita.<sup>4</sup> 

## CO2 EMISSIONS AND WORLD POPULATION

  The first step in the discovery of countries with the most and least amount of carbon dioxide emissions per capita was to calculate every country’s yearly CO2 emission amount in tons and then divide it by that country’s population for every year from 1960 to 2019. For comparison’s sake we then limited our search to 2019 emissions per capita. Kenya with 0.4373 tons of CO2 emissions per capita, Burundi (0.0606) and Rwanda (0.1036) were the three lowest emitting countries in 2019 with datasets of water toxins available. Czechia (9.0228), Japan (8.5410) and Netherlands (8.4317) comprised our top three CO2 emitting countries due to Libya (8.6466) not having any water toxins data available.
  
Further research into these six countries resulted in the following information:

* Kenya with a large population of more than 52 million is East Africa’s financial, trade and communications hub.
  * Has made plans to reduce their emissions by increasing renewable energy and climate smart agriculture.
  * Approximately 19,000 people die each year in Kenya due to air pollution.
  * Main sources of air pollution include: traffic, roadside fires, road dust, industry and the use of solid fuels such as charcoal and wood to cook in open fires.

* Burundi’s land use exploitation for consumption and commercialization contribute to 49% of the gas emissions.
  * Average person in Burundi generates approximately 88 tons of CO2 per year.
  * Coal and oil are the main source of fuel with coal accounting for 49,000 metric tons per year and oil accounting for 613,000 metric tons per year.

* Rwanda has 39% of its greenhouse gas emissions coming from agriculture, followed by waste, energy, land use and industrial processes.
  * In 2022, Rwanda’s per capita CO2 emissions were at .1 tonnes (1 tonnes = 1,000 kilograms).

* Japan’s fossil fuels of oil, coal and natural gas make up 87% of their energy production.
  * Fossil fuel combustion and industrial processes in Japan released 1.08 billion metric tons of carbon dioxide in 2022. 
  * In 2022, Japan had a per capita CO2 emissions of 8.5 tonnes (1 tonnes = 1,000 kilograms).
  * 92% of total greenhouse gas emissions in Japan come from CO2 emissions.
  * In 1998, Japan passed the Act of Promotion of Global Warming Countermeasures to commit the state, local governments and companies to develop emission reduction plans. These outlines plans to greatly improve energy efficiency by 2030. Since then Japan’s emissions have decreased by 10% to 25% over the past 10 years.

* Czechia’s burning of fossil fuels are the largest contributors of nearly 90% of all carbon dioxide emissions.
  * Total CO2 emissions have decreased from the 1970s to 2022.
  * High coal use and older diesel fuel automobiles contributed to the high CO2 emissions.
  * Have seen almost 40% reduction of CO2 emissions since 1990.
  * The country has reduced its greenhouse gas emissions by 43% over the past three decades by decreasing the amount of coal used in its energy mix while improving energy efficiency in buildings and polluting technologies.

* The Netherlands’ number of oil refineries is proportional to its population.
  * Ijmuiden steel plant and Eemshaven Power plant contribute to the majority of the country’s CO2 emissions.
  * In accordance with the Climate Act in 2019, the Netherlands wants to reduce their emissions by 49% by 2030 and obtain a 95% reduction by 2050.

 ## RESEARCHING WATER TOXINS WITHIN CATCHMENTS
  After retrieving the data for the six countries from gemstat.org and converting the Excel spreadsheets to .csv files, we first researched the pH levels within each country’s water catchments and created averages to compare. Unfortunately, Czechia’s data did not include pH values and was not in the bar chart that compared each country’s average pH level. We found an online resource that stated Czechia’s groundwater to have a pH of 7.61.<sup>5</sup> This confirmed that every country except the Netherlands (9.63 pH) had their pH in comparable acceptable ranges and thus we could not infer more from the data.
  
  Next we compared all the water toxins (pollutants) summed up for each country against their CO<sub>2</sub> emissions from 2019. The Netherlands pollutants data was extremely skewed due to an extreme outlier which we had to remove to continue a reasonable comparison between the total number of pollutants and CO<sub>2</sub> emissions. Once the Netherlands’ outlier was removed and all six countries could be analyzed against one another, a box and whiskers chart revealed another pollutant outlier this time emanating from Japan at 180.61 while all the other countries fall within the quartiles. 
## PROVING STATISTICAL SIGNIFICANCE OF WATER TOXINS CORRELATION TO CO<sub>2</sub> EMISSIONS
  After a visual side by side comparison of the average pollutants of the six countries and average CO<sub>2</sub> emissions of the same six countries in 2019, we were confident to continue forward with the calculations of a two-sample t-test. The resulting p-value approximated  t ≈ 0.085 which is greater than 0.05. Therefore, we could not reject the null hypothesis.
## RESULTS AND CONCLUSION
  Due to the p-value being greater than 0.05, the mathematical survey we completed of the water toxins within the water catchments of the top three CO<sub>2</sub> emitting countries compared to the lowest 3 countries was not statistically significant. Therefore, our hypothesis of a correlation between CO<sub>2</sub> emissions and moderate to high levels of water toxins could not be proven or disproven due to the inconclusive data. There are possibly many factors that may have created the inconclusive data such as the data collection of pollutants across all countries may not be strict enough or even uniformly gathered. It could also be a possibility that high energy producing, industrialized nations have stricter laws against water pollution, thus having high CO<sub>2</sub> emissions while maintaining lower levels of water toxins. In the end, these are just speculative observations and to properly retest our hypothesis we would need to take a more concentrated focus on specific water toxins that occur within all six countries or zoom in on water catchments only near the major cities of the six countries could possibly convey statistically significant data. 


<sup>1</sup> Iceland and Costa Rica produce 100% and 98% of their electric energy from renewable sources, respectively. https://www.climatecouncil.org.au/11-countries-leading-the-charge-on-renewable-energy/<br>
<sup>2</sup> https://www.kaggle.com/code/hasibalmuzdadid/world-population-analysis/input<br>
<sup>3</sup> https://www.kaggle.com/datasets/ulrikthygepedersen/co2-emissions-by-country<br>
<sup>4</sup> Entered in Czechia, Netherlands, Japan, Burundi, Kenya and Rwanda: https://portal.gemstat.org/applications/public.html?publicuser=PublicUser#gemstat/Stations<br>
<sup>5</sup> Tailin Li, Jakub Jeřábek, Jan Winkler, Magdalena Daria Vaverková, David Zumr."Effects of prescribed fire on topsoil properties: a small-scale straw burning experiment ." Journal of Hydrology and Hydromechanics 70 ,(2022), 4,: Pages 450–461 Print. https://intapi.sciendo.com/pdf/10.2478/johh-2022-0032<br>

