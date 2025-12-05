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

### Methods 

#### Data Processing
Occurrence records from GBIF were aggregated by ecoregion and month to quantify Purple Martin activity across North America. Each observation was linked to its corresponding ecoregion. Ecoregions with essentially no observations (n <= 1) in a given month were excluded to focus the analysis on areas with actual Purple Martin activity.

#### Normalization
Raw occurrence counts can be misleading because survey effort varies across space and time:

- By ecoregion: Some regions are surveyed more frequently than others, and larger ecoregions naturally contain more observations. Dividing by ecoregion-level sampling effort corrects for these differences.

- By month: Observation intensity fluctuates seasonally due to factors like weather and citizen science engagement. Normalizing by month controls for these temporal biases.

- By area: To account for the physical size of each ecoregion, counts were divided by area, producing a density measure (i.e., observations per square kilometer).

The final metric, normalized density, represents Purple Martin activity relative to both sampling effort and ecoregion size, enabling fair comparisons across months and regions.

### Plot 

Below is an interactive map in which you can explore the spatial patterns of Purple Martins across each month of 2024. 

<embed type="text/html" src="img/PurpleMartin_migration.html" width="850" height="830">


The map visualizes normalized Purple Martin occurrence densities by ecoregion and month. Polygon color represents the relative density of observations after accounting for sampling effort, month, and ecoregion area, allowing fair comparisons across space and time. Using this approach, we can observe the seasonal migration patterns of Purple Martins across North America, from breeding grounds in the central and eastern United States and Canada to wintering areas in Central and South America.

From April through July, sightings of Purple Martins are more focused in the central and especially eastern areas of North America. The eastern subspecies of Purple Martins nests almost exclusively in human-provided cavity nest boxes, and landlords manage these sites by cleaning nests, removing parasites, adding nesting material, and monitoring occupancy. Research indicates that these stewardship practices significantly increase occupancy rates (Kelly & Hvenegaard, 2022), meaning that ecoregion-level patterns may reflect not only natural habitat quality but also the intensity of human management. Areas with more active nest box programs may show higher normalized densities, even after controlling for sampling effort and area, suggesting that human intervention can directly influence observed Purple Martin activity, particularly during the breeding season.

### Supplemental Attachment
Below, you can find the code used to complete this analysis.

[Purple Martin Migration Code](./portfolio_posts/migration-portfolio-code.html)

### References
GBIF.org (29 October 2025) GBIF Occurrence Download <https://doi.org/10.15468/dl.6w6vfb>

Olson, D. M., Dinerstein, E., Wikramanayake, E. D., Burgess, N. D., Powell, G. V. N., Underwood, E. C., D’Amico, J. A., Itoua, I., Strand, H. E., Morrison, J. C., Loucks, C. J., Allnutt, T. F., Ricketts, T. H., Kura, Y., Lamoreux, J. F., Wettengel, W. W., Hedao, P., & Kassem, K. R. (2001). Terrestrial ecoregions of the world: A new map of life on Earth. BioScience, 51(11), 933–938. <https://doi.org/10.1641/0006-3568(2001)051[0933:TEOTWA]2.0.CO;2>

Kelly, B. D., and Hvenegaard, G. T. (2022). Impacts of purple martin landlord stewardship activities on nest box occupancy. Wildlife Society Bulletin 46:e1247. <https://doi.org/10.1002/wsb.1247> 


## Evaluating Vegetation Health in Boulder, CO from 2002 to 2022

### Background 
Vegetation is a key component of ecosystem health, and understanding how it changes over time can help us better interpret climate variability, land-use change, and natural disturbances in a region. Boulder County provides an excellent case study for examining long-term vegetation changes. Over the past two decades, the region has experienced several major events such as wildfires (2010 Fourmile Canyon fire, 2021 Marshall Fire), the multi-hundred year 2013 flood, as well as significant urban development and population growth. 

Analyzing NDVI across multiple years will allow us to observe these cumulative impacts and identify where vegetation has increased, decreased, or remained stable. These trends will help reveal how Boulder's landscape has been shaped over the last 20 years. 

<figure style="flex-shrink: 0; width: 500px; margin: 0 auto;">
  <img src="/img/boulder_view.avif" 
       alt="Aerial View of Boulder, Colorado - Photo Credits: University of Colorado Boulder" 
       style="width: 100%; border-radius: 12px;">
  <figcaption style="text-align: center; font-style: italic; font-size: 0.9em; margin-top: 8px;">
    Aerial View of Boulder, Colorado - Photo Credits: University of Colorado Boulder
  </figcaption>
</figure>

### Data 
This analysis uses two primary datasets. The first is MODIS NDVI from NASA EarthData (Didan, 2021), long-term global vegetation index product derived from the MODIS instruments on NASA's Terra satellite. MODIS NDVI provides cloud-filtered measurements of vegetation greenness at 250 meter spatial resolution and a 16-day temporal frequency. For this short analysis, I used NDVI data from May 1st-July 31st spanning 2002 through 2022, enabling comparison of vegetation conditions across two decades during peak vegetation times. 

The second dataset is the OpenStreetMap (OSM) boundary for Boulder County (OpenStreetMap contributors, 2025), which I used to spatially subset the NDVI raster data. I also retrieved the OSM boundary which defines the official city limits for Boulder, which allows the analysis to focus on vegetation within and outside the city. 

### Methods

#### Data Preprocessing
To examine multi-year changes, I divided the 21-year period into two groups (e.g., Group 1: 2002-2010, Group 2: 2011-2022). For each group, I calculated the mean NDVI across all years, producing an average NDVI per period. 

#### NDVI Change Calculation
To visualize how vegetation changed between the two periods, I computed and mapped the difference between group means:

<math display="block">
  <msub>
    <mtext>NDVI</mtext>
    <mtext>difference</mtext>
  </msub>
  <mo>=</mo>
  <msub>
    <mtext>NDVI</mtext>
    <mtext>group2</mtext>
  </msub>
  <mo>-</mo>
  <msub>
    <mtext>NDVI</mtext>
    <mtext>group1</mtext>
  </msub>
</math>

Looking at the temporal difference between the two time periods will reveal "hotspots" where vegetation health has significantly increased or decreased. Positive values indicate areas that became greener on average in the later period, while negative values indicate vegetation loss, disturbance, or reduced greenness.

#### NDVI Time Series
To examine long-term trends, I also calculated:
- Mean July NDVI inside the city of Boulder for each year
- Mean July NDVI outside the city boundary for each year

These annual values were plotted as a time series to identify overall trends, possible drought impacts, or disturbances (e.g., wildfires).

I then looked at the annual mean July difference inside and outside the city to better understand the magnitude of the gap in vegetation. 

<math display="block">
  <msub>
    <mtext>NDVI_July</mtext>
    <mtext>difference</mtext>
  </msub>
  <mo>=</mo>
  <msub>
    <mtext>NDVI</mtext>
    <mtext>inside</mtext>
  </msub>
  <mo>-</mo>
  <msub>
    <mtext>NDVI</mtext>
    <mtext>outside</mtext>
  </msub>
</math>

### Results 

#### Change in NDVI Between 2002–2010 and 2011–2022

<embed type="text/html" src="img/ndvi_difference_plot.html" width="620" height="430">

This map shows the difference in mean NDVI between the early period (2002–2010) and the later period (2011–2022). Overall, vegetation greenness across most of the Boulder area remained relatively stable between the two periods, with only small positive or negative changes. One of the only areas showing a clear decrease in NDVI between the two periods corresponds to the 2010 Fourmile Canyon Fire burn scar in the area west of Boulder. Previous work in the Northern Front Range has shown that recent fires are the dominant driver of forest loss in this region, with burned areas experiencing substantial and prolonged reductions in canopy cover (Rodman et al., 2019). This suggests that the localized NDVI decline observed in my analysis reflects long-lasting ecological impacts of the Fourmile Canyon and presumably other wildfires, rather than broader county-wide vegetation change. Outside of these disturbances, most of the region shows minimal long-term change.

#### Annual July NDVI Trends Inside vs. Outside the City Boundary

<embed type="text/html" src="img/time_series_difference.html" width="750" height="325">

The second figure compares annual mean July NDVI inside the City of Boulder with NDVI in the surrounding area from 2002–2022. Across all years, NDVI values inside the city are consistently lower than those outside the city, reflecting the greater proportion of impervious surfaces, developed land, and managed vegetation within urban boundaries. Outside the city, NDVI values are generally higher and more variable, consistent with the mix of grasslands, forests, and agricultural areas surrounding Boulder.

Both regions show substantial year-to-year variability, likely driven by differences in precipitation, drought conditions, and local disturbances. However, neither region exhibits a clear long-term upward or downward trend during the study period.

#### Difference in July NDVI Between Urban and Non-Urban Areas

<embed type="text/html" src="img/total_difference.html" width="750" height="325">

The third plot shows the annual difference between mean July NDVI outside the city and inside the city. The difference is negative in every year, confirming that vegetation greenness is consistently lower in the city than the surrounding natural and agricultural landscapes. The size of this gap fluctuates through time, following similar patterns to the annual preciption plot below. 

<figure style="flex-shrink: 0; width: 500px; margin: 0 auto;">
  <img src="/img/wet&dryyearsBoulder.webp" 
       alt="Annual Precipitation Changes, Boulder, CO - Photo Credits: University of Colorado Boulder Center for Sustainable Landscapes and Communities" 
       style="width: 100%; border-radius: 12px;">
  <figcaption style="text-align: center; font-style: italic; font-size: 0.9em; margin-top: 8px;">
    Annual Precipitation Changes, Boulder, CO - Photo Credits: University of Colorado Boulder Center for Sustainable Landscapes and Communities
  </figcaption>
</figure>

Larger differences occur in years when outside-the-city vegetation peaks (e.g., wetter years) or when urban vegetation may be more stressed (e.g., during drought). Despite these fluctuations however, the relative pattern remains stable over the two decades: outside-Boulder NDVI is always higher than inside-Boulder NDVI.

### Supplemental Attachment
Below, you can find the code used to complete this analysis.

[Boulder NDVI Code](./portfolio_posts/Boulder-NDVI-portfolio-code.html)

### References
Didan, K. (2021). <i>MODIS/Terra Vegetation Indices 16-Day L3 Global 250m SIN Grid V061</i> [Data set]. NASA Land Processes Distributed Active Archive Center. <https://doi.org/10.5067/MODIS/MOD13Q1.061> Date Accessed: 2025-11-26

OpenStreetMap contributors. (2025). Planet dump [Data set]. Retrieved from <https://planet.openstreetmap.org>

Rodman, K. C., Veblen, T. T., Saraceni, S., & Chapman, T. B. (2019). Wildfire activity and land use drove 20th-century changes in forest cover in the Colorado Front Range. Ecosphere, 10(2), e02594. <https://doi.org/10.1002/ecs2.2594> 

## Assessing the Greening of Vegetation Across Space & Time in Boulder, CO

### Introduction 

Vegetation phenology, the seasonal timing of green-up and plant peak growth, is a sensitive indicator of ecological change. Across landscapes like Boulder County, Colorado, phenological timing varies with strong environmental gradients, especially temperature. 

Satellite-derived vegetation metrics such as the Normalized Difference Vegetation Index (NDVI) allows researchers to quantify these patterns consistently across both natural and developed environments. Phenology in urban regions, in particular, has received growing attention because cities modify local climate through the Urban Heat Island (UHI) effect, characterized by elevated temperatures due to greater impervious surface area and lower vegetation cover (Jia et al., 2021). Warmer microclimates, such as those seen in urban areas, can shift the timing of vegetation activity, often advancing green-up or extending the growing season (Gazal et al., 2008; Dallimer et al., 2016; Qiu et al., 2017). These phenological shifts have implications for ecosystem services, including cooling, carbon uptake, biodiversity support, and human well-being. Understanding how phenology responds across urban–rural gradients is therefore important for both ecological insight and land-management planning

Recent research demonstrates that urbanization can alter vegetation phenology, with the start of the growing season found to be significantly associated with elevated land-surface temperatures, such as those found in urban areas (Jia et al., 2021). In other work, differences between urban and rural tree phenology have been linked not only to temperature but also to species composition. Some species exhibit increased temperature sensitivity in urban environments, leading to stronger phenological shifts than climate alone would predict (Wu et al., 2025).

Taken together, these findings point towards a consistent pattern: the Urban Heat Island effect tends to advance vegetation greenness and alter peak timing, though local climate and species composition shape the exact nature of the shift.

Boulder County provides a particularly compelling setting for examining these dynamics. It contains a rapidly growing urban corridor along the Front Range, immediately adjacent to steep elevation gradients and snow-dominated mountain systems. This juxtaposition creates an ideal natural laboratory for investigating how urban warming shapes local vegetation phenology.

This project therefore asks:

How do NDVI-based greenness patterns and peak greening timing differ across Boulder County, and do urban areas exhibit earlier or altered phenological timing consistent with UHI-related effects?

### Methods 

### Results 

### Discussion

### References 
Dallimer, M., Tang, Z., Gaston, K. J., & Davies, Z. G. (2016). The extent of shifts in vegetation phenology between rural and urban areas within a human-dominated region. Ecology and evolution, 6(7), 1942–1953. <https://doi.org/10.1002/ece3.1990>

Qiu, T., Song, C., & Li, J. (2017). Impacts of Urbanization on Vegetation Phenology over the Past Three Decades in Shanghai, China. Remote Sensing, 9(9), 970. <https://doi.org/10.3390/rs9090970>

Gazal, R., White, M. A., Gillies, R., Rodemaker, E., Sparrow, E., & Gordon, L. (2008). GLOBE students, teachers, and scientists demonstrate variable differences between urban and rural leaf phenology. Global Change Biology, 14, 1568–1580. <https://doi.org/10.1111/j.1365-2486.2008.01602.x>

Jia, W., Zhao, S., Zhang, X., Liu, S., Henebry, G. M., & Liu, L. (2021). Urbanization imprint on land surface phenology: The urban–rural gradient analysis for Chinese cities. Global Change Biology, 27, 2895–2904. <https://doi.org/10.1111/gcb.15602>

Wu, Z., Zohner, C. M., Zhou, Y., et al. (2025). Tree species composition governs urban phenological responses to warming. Nature Communications, 16, 3696. <https://doi.org/10.1038/s41467-025-58927-8>

Fully reproducible, well-documented code
Write-up includes an introduction (background + motivation), methods, results, and discussion/interpretation section
Well-researched, including references to at least 4 peer-reviewed publications and/or reports from government agencies or NGOs
