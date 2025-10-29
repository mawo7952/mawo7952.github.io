# Projects from Earth Data Science Class 

## Map of CU Boulder
Below is an interactive map of CU Boulder's main campus. I completed my undergrad here and am now pursuing my Master's.

<embed type="text/html" src="img/UCB.html" width="750" height="700">


## Exploration of Climate Change in Round Rock, Texas
### Introduction
Areas across the globe are facing the dangers of a changing climate. In this short exercise, I will explore the changing climate in my hometown of Round Rock, Texas. Specifically, I will be investigating changes in temperature patterns from 1982 up through 2024. 

### Climate History of Round Rock, TX
Round Rock is a medium-sized suburban development just north of Austin, Texas. It is named after a literal rock that is round...ish. Being the place that I grew up and spent 18 years of my life, and where my mother still lives, I'm curious to investigate its climate trends with empirical data. 

<figure style="flex-shrink: 0; width: 500px; margin: 0 auto;">
  <img src="/img/round_rock.jpg" 
       alt="The Round Rock - Photo Credits: Texas State University" 
       style="width: 100%; border-radius: 12px;">
  <figcaption style="text-align: center; font-style: italic; font-size: 0.9em; margin-top: 8px;">
    The Round Rock - Photo Credits: Texas State University
  </figcaption>
</figure>

Located in central Texas, Round Rock experiences hot summers, often exceeding 100°F, with high humidity and generally dry conditions. The region’s climate is influenced by the Gulf of Mexico, which provides a primary source of moisture, particularly in summer when warm sea surface temperatures and winds bring humid air inland. In contrast, winter conditions are shaped by continental air masses from the interior of North America, which bring dry and cool air. This creates strong seasonal temperature contrasts with the hot, dry air masses originating from central Mexico that contribute to Texas’ characteristically hot summers. These conditions drive frequent droughts and can trigger “weather whiplash”, with dry periods quickly replaced by intense rainfall and flooding (Gerlich et al., 2025).

Since the early 1900s, average temperatures in Texas have risen nearly 1.5°F, with nighttime temperatures increasing particularly rapidly (Runkle et al., 2022). These rising temperatures pose serious risks to human health (U.S. Environmental Protection Agency, 2016), as elevated nighttime temperatures prevent the body from cooling down and recovering, further exacerbating the dangers of heat during the day. 

Building on this context, the goal of this project is to examine historical temperature trends in Round Rock and provide continued evidence of a warming climate in my hometown/state.

### Data
Data used for this project will be from the Global Historical Climatology Network–Daily (GHCN-Daily) dataset (Menne et al., 2012), curated by the National Centers for Environmental Information (NCEI). The NCEI’s GHCN-Daily dataset compiles daily climate observations from land-based stations worldwide, including airports, weather stations, and other observer-run sites. These stations measure variables such as temperature (standardized in degrees Fahrenheit; although it can be changed based on user preference), precipitation, snowfall, and snow depth. Data are updated frequently from ~30 different sources and then integrated and quality-checked by NCEI to ensure accuracy and consistency.

Because there is no monitoring station in Round Rock with sufficient historical data, I am using a station in Georgetown, TX, a nearby suburb approximately 10 miles away. This station has recorded temperatures daily at 8 a.m. continuously from July 1, 1981, and has only 4% missing data. Observations from 1981 and 2025 were excluded in this analysis due to the incompleteness of those years.

### Temperature trends in Round Rock since 1982
To examine long-term trends in Round Rock’s temperatures, daily observations were first averaged annually to reduce short-term variability and highlight underlying patterns. This upscaling approach is consistent with previous climate trend analyses, such as Sonet and Reygadas (2025), who aggregated daily data to annual values to reveal regional warming patterns in Texas from 1981 to 2023. 

Despite some year-to-year variability, the overall trend is clear: there's a steady increase in the annual average temperature in Round Rock, TX, since the 1980s. An interactive plot is displayed below in which you can further examine the temperature data over time. 

<embed type="text/html" src="img/RR_annual_temp_interactive.html" width="750" height="325">

#### Ordinary Least Squares (OLS) Regression
Following this, an ordinary least squares (OLS) regression was applied to quantify the magnitude and direction of the trend over time. 

<figure style="flex-shrink: 0; width: 600px; margin: 0 auto;">
  <img src="/img/RR_OLS_graph.png" 
       alt="OLS regression of annual temperatures in Round Rock" 
       style="width: 100%; border-radius: 12px;">
  <figcaption style="text-align: center; font-style: italic; font-size: 0.9em; margin-top: 8px;">
    The OLS regression slope (β₁) is 0.147°F per year, indicating a long-term warming trend.
  </figcaption>
</figure>

According to the OLS regression, the average annual temperature in Round Rock has increased by approximately 0.15°F per year between 1982 and 2024, corresponding to an estimated total increase of about 6.3°F over the study period. This estimate reflects the linear trend predicted by the model. 

### Conclusion
This analysis of annual average temperatures in Round Rock, Texas, provides clear evidence of a long-term warming trend. By aggregating daily measurements to annual averages and applying an OLS regression, I found that temperatures have increased at an average rate of approximately 0.15°F per year. Even with data from only one monitor, this pattern of warming is evident. This trend is consistent with broader regional observations across Texas (Runkle et al., 2022; Sonet & Reygadas, 2025; Nielsen-Gammon, 2011) and underscores the ongoing effects of climate change at the local scale.

### Supplemental Attachment
Below, you can find the code used to complete this analysis.

[Round Rock, Texas Climate Investigation Code](./portfolio_posts/RR-climate-change-portfolio-code.html)

### References
U.S. Environmental Protection Agency. (2016). *What climate change means for Texas* (EPA 430-F-16-045, 2 pp.). <https://www.epa.gov/sites/production/files/2016-09/documents/climate-change-tx.pdf> 

Nielsen-Gammon, J. W. (2011). The changing climate of Texas. In J. Schmandt, G. R. North, & J. Clarkson (Eds.), *The impact of global warming on Texas*. University of Texas Press.

Gerlich, J., Lisonbee, J., Hoell, A., Mahoney, K., & Lang, A. (2025, July 23). *From dust to deluge: Weather whiplash devastates Texas*. National Integrated Drought Information System. <https://www.drought.gov/news/dust-deluge-weather-whiplash-devastates-texas-2025-07-23>

Runkle, J., Kunkel, K. E., Nielson-Gammon, J., Frankson, R., Champion, S. M., Stewart, B. C., Romolo, L., & Sweet, W. (2022). Texas state climate summary 2022 (NOAA Technical Report NESDIS 150-TX, 5 pp.). NOAA/NESDIS.

Menne, M. J., Durre, I., Korzeniewski, B., McNeill, S., Thomas, K., Yin, X., Anthony, S., Ray, R., Vose, R. S., Gleason, B. E., & Houston, T. G. (2012). *Global Historical Climatology Network – Daily (GHCN-Daily), Version 3* [Dataset]. NOAA National Climatic Data Center. <https://doi.org/10.7289/V5D21VHZ>. Retrieved September 29, 2025.

Sonet, M. S., & Reygadas, Y. (2025). Unveiling four decades of spatiotemporal climate trends in Texas (1981–2023). Journal of Hydrology: Regional Studies, 60, 102539. <https://doi.org/10.1016/j.ejrh.2025.102539>


## Tracking Purple Martin Migration with GBIF and Ecoregions 

## Species Description 
Why did you choose this species? Is there any relevant information about it that makes its migration interesting?

<figure style="flex-shrink: 0; width: 500px; margin: 0 auto;">
  <img src="/img/purpleMartin.avif" 
       alt="Male & Female Purple Martins - Photo Credits: Henry T. McLin" 
       style="width: 100%; border-radius: 12px;">
  <figcaption style="text-align: center; font-style: italic; font-size: 0.9em; margin-top: 8px;">
    The Round Rock - Photo Credits: Texas State University
  </figcaption>
</figure>

## Data Description 
include citations
Ecoregion
GBIF occurrences 
## Methods Description
Normalization -- why is it necessary, how did you do it? 
we normalized by ecoregion samples, by month samples, and by area. Normalized sampling effort over space and time.

## Plot Headline
Embed html file (plot) and give a description
plot description, discussion, conclusion
ideally link back to the early text for context


