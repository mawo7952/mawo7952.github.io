# Projects from Earth Data Science Class 

## Map of CU Boulder
Below is an interactive map of CU Boulder's main campus. I completed my undergrad here and am now pursuing my Master's.

<embed type="text/html" src="img/UCB.html" width="750" height="700">


## Exploration of Climate Change in Round Rock, Texas
### Introduction
Areas across the globe are facing the dangers of a changing climate (CITATION). From heightened extremes (CITATION), to worsened natural disasters (CITATION), climate change is exposing the vulnerability of communities everywhere. 

In this short exercise, I will explore the changing climate in my hometown, Round Rock, Texas. I will investigate changes in temperature patterns from the 1980s up through 2024. 

### Climate History of Round Rock, TX
Round Rock is a medium-sized suburban development just north of Austin, Texas. It is named after a literal rock that is round...ish. *INSERT PICTURE HERE* 

Given its location in central Texas, summers are hot (often exceeding 100°F), humid, and usually dry. Droughts and heatwaves are common during this time.

### Data
Data used for this project will be from the Global Historical Climatology Network–Daily (GHCN-Daily) dataset, curated by the National Centers for Environmental Information (NCEI). The NCEI’s GHCN-Daily dataset compiles daily climate observations from land-based stations worldwide, including airports, weather stations, and other observer-run sites. These stations measure variables such as temperature (standardized in degrees Fahrenheit; although it can be changed based on user preference), precipitation, snowfall, and snow depth. Data are updated frequently from ~30 different sources and then integrated and quality-checked by NCEI to ensure accuracy and consistency.

I am using a station in Georgetown, TX, another suburb just about 10 miles from Round Rock. The station measured at 8am everyday and only has 4% missingness. All observations for 1981 and 2025 were removed, however, due to the incompleteness of the year. *CHANGE THIS*

#### Data Reference
Menne, Matthew J., Imke Durre, Bryant Korzeniewski, Shelley McNeill, Kristy Thomas, Xungang Yin, Steven Anthony, Ron Ray, Russell S. Vose, Byron E.Gleason, and Tamara G. Houston (2012): Global Historical Climatology Network - Daily (GHCN-Daily), Version 3. NOAA National Climatic Data Center. doi:10.7289/V5D21VHZ. Retrieved September 29, 2025. 

### Temperature trends in Round Rock since 1981
<embed type="text/html" src="img/RR_annual_temp_interactive.html" width="750" height="600">



