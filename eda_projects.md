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

### Species Description 
The Purple Martin (Progne subis) is one of the largest swallows in North America. It feeds almost exclusively on aerial insects, making it an excellent indicator of ecosystem health. Notably, the species relies on communal nesting sites, often provided by humans in the form of gourds or nest boxes, which adds an interesting conservation dimension. Its migration is highly seasonal: during the summer, Purple Martins range across much of the central and eastern United States and Canada, and in the winter, they travel to central South America. This migratory pattern closely aligns with the seasonal availability of flying insects.

<figure style="flex-shrink: 0; width: 500px; margin: 0 auto;">
  <img src="/img/purplemartin.avif" 
       alt="Male & Female Purple Martins - Photo Credits: Henry T. McLin" 
       style="width: 100%; border-radius: 12px;">
  <figcaption style="text-align: center; font-style: italic; font-size: 0.9em; margin-top: 8px;">
    Male & Female Purple Martins - Photo Credits: Henry T. McLin
  </figcaption>
</figure>

### Data Description 
To study Purple Martin migration, I combined species occurrence data with ecoregion information to provide better ecological context.

#### GBIF Occurrences
I used observation records from the Global Biodiversity Information Facility (GBIF), which include precise coordinates and timestamps for each Purple Martin sighting (GBIF.org, 2025). These data allowed me to analyze seasonal distribution patterns across North America. By mapping these occurrences, I could quantify activity in each ecoregion and track changes throughout the 2024 calendar year.

#### Ecoregions Data
To contextualize sightings, I overlaid them on the WWF Terrestrial Ecoregions of the World (Olson et al., 2001). Ecoregions group land areas with similar climate, topography, and vegetation, providing a biologically meaningful framework for analyzing species distribution. This approach allowed for the calculation of occurrence densities relative to ecological context rather than just geographic space.

### Methods Description
Normalization -- why is it necessary, how did you do it? 
we normalized by ecoregion samples, by month samples, and by area. Normalized sampling effort over space and time.

### Plot Headline
Embed html file (plot) and give a description
plot description, discussion, conclusion
ideally link back to the early text for context

Since nest availability is influenced by humans, ecoregion-level patterns may reflect both natural habitat and human stewardship intensity.

Purple Martins (Progne subis) are unique among North American birds because the eastern subspecies nests almost exclusively in human-provided cavity nest boxes. Nest “landlords” manage these boxes using practices like cleaning nests, removing parasite larvae, checking boxes frequently, and adding nesting material. Research has shown that these stewardship practices significantly increase occupancy rates, highlighting the species’ reliance on human intervention for successful breeding (Kelly & Hvenegaard, 2022).

This reliance on human-maintained sites adds an interesting layer to their migration and distribution patterns: Purple Martins’ breeding success and population density in different ecoregions may partly reflect local human management practices, in addition to natural habitat quality.

LOOK FOR EVIDENCE OF THIS Normalized occurrences: Areas with more active nest box programs might show higher normalized densities — something to consider when interpreting your maps.

Migration interest: Because breeding success depends on human intervention, Purple Martins provide a unique case where conservation practices directly influence migration timing and population distribution


### References
GBIF.org (29 October 2025) GBIF Occurrence Download <https://doi.org/10.15468/dl.6w6vfb>

Olson, D. M., Dinerstein, E., Wikramanayake, E. D., Burgess, N. D., Powell, G. V. N., Underwood, E. C., D’Amico, J. A., Itoua, I., Strand, H. E., Morrison, J. C., Loucks, C. J., Allnutt, T. F., Ricketts, T. H., Kura, Y., Lamoreux, J. F., Wettengel, W. W., Hedao, P., & Kassem, K. R. (2001). Terrestrial ecoregions of the world: A new map of life on Earth. BioScience, 51(11), 933–938. <https://doi.org/10.1641/0006-3568(2001)051[0933:TEOTWA]2.0.CO;2>

Kelly, B. D., and Hvenegaard, G. T. (2022). Impacts of purple martin landlord stewardship activities on nest box occupancy. Wildlife Society Bulletin 46:e1247. <https://doi.org/10.1002/wsb.1247> 

