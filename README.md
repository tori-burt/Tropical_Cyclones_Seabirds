# Tropical_Cyclones_Seabirds
Data and code for the manuscript "Impacts of Tropical Cyclones on Northwest Atlantic Seabirds: Insights from a Category 1 hurricane"



### Tori V. Burt

### Robert J. Blackmore

### Sydney M. Collins 

### Kyle J. N. d'Entremont 

### Christopher R. E. Ward

### Joshua Cunningham

### Cerren Richards

### Fiona Le Taro

### Sabina I. Wilhelm

### Amanda E. Bates

### Stephanie Avery-Gomm

### William A. Montevecchi

## Abstract

Tropical cyclones are annual occurrences in the western North Atlantic Ocean, where many seabird species are vulnerable to the environmental factors associated with extreme weather events. We summarize the history of tropical cyclones in Newfoundland, Canada, which hosts globally significant populations of seabirds. We examine the interactions that historical tropical cyclones have had with breeding seabirds by plotting the temporal association of Category 1 hurricanes with the breeding phenology of colonial seabirds in Newfoundland and identifying which major colonies have fallen within the pathways of these hurricanes. As a case study, we explore how Hurricane Larry (2021) coincided with increased stranding and mortality of Northern Gannets and Leach’s Storm-Petrels. The breeding seasons of Northern Gannets and Leach’s Storm-Petrels overlapped with all Category 1 hurricanes that have made landfall with Newfoundland from 1851 to 2024, with the central pathways of at least one hurricane passing over each of the six large Leach’s Storm-Petrel colonies and one of the three Northern Gannet colonies. For Northern Gannets, a notable stranding and mortality event occurred with a minimum count of 146 stranded and 130 dead from September 13 to 24, 2021. For Leach’s Storm-Petrels, a minor stranding and mortality event occurred with a count of 19 stranded and 16 dead from September 10 to 14, 2021, which was significantly higher than strandings and deaths reported during this period in 2020, 2022, 2023, and 2024. As global climate change drives a shift in the timing, frequency, severity, and attributes of tropical cyclones, we raise the concern that the impacts of tropical cyclones on breeding seabirds may worsen.

## Data files

#### Feb_23_BreedingPhenology_hurricane.csv:
Population estimates and breeding stages of 8 seabirds breeding in Newfoundland, only NOGA, LESP, RAZO, COMU, and ATPU are included in manuscript analyses.

- Species: 4-letter alpha bird name code of seabird species
- BrPairs_NFLD: Number of breeding pairs in Newfoundland
- Lay_start: Estimated start of laying
- Lay_mean: Estimated mean of laying
- Lay_end: Estimated end of laying
- Hatch_date: Estimated hatch date
- Fledge_Early: Estimated start of fledging
- Fledge_mean: Estimated mean of fledging
- Fledge_Late: Estimated end of fledging
- Nest_Type: Type of nest
- Ref: Reference for population estimates and breeding stage dates

#### NL_hurricanes_cat1_best_tracks.csv
Information on Category 1 hurricanes that have made landfall on Newfoundland. Data subsetted from the National Oceanic and Atmospheric Administration's Atlantic hurricane database (HURDAT2) 1851-2023. Data and README files found at (https://www.nhc.noaa.gov/data/).


#### lesp_noga_colonies_large.csv: 
Information on six large Leach's Storm-Petrel colonies and three Northern Gannet colonies in Newfoundland from 2021.

- Species: 4-letter alpha bird name code of seabird species
- Colony_Name: Name of seabird colony
- Country: Country that colony is located in
- Location: Region that colony is located in
- Sub.Region: Sub-region that colony is located in
- Breeding_pairs: Number of breeding pairs at colony
- Colony.status: Classification of colony (increasing, decreasing, or stable)
- Lat: Latitude of colony
- Lon: Longitude of colony 
- citation: Reference for colony


#### Gannet_Summary_HL_2024_11_26.csv: 
Observations of stranded and dead Northern Gannets in Newfoundland near Cape St. Mary's collected by Environment and Climate Change Canada and Cape St. Mary’s Nature Interpreters from September 13 to 24, 2021, during Hurricane Larry.

- Date: Date survey was conducted
- Time: Time survey was conducted
- Location: Location of survey
- Lat: Latitude
- Lon: Longitude
- Num: Total number of stranded or dead Northern Gannets found during survey
- Species: 4-letter alpha bird name code of seabird species found during survey
- Age: Age classification of seabird (Adult/Subadult)
- Live_dead: Whether the bird was alive or dead
- Notes: Notes about survey


#### HL_Lesp_Bdv_Cpaws_Mar_11_2025: 
Observations of stranded and dead Leach's Storm-Petrels in eastern Newfoundland from public reports to CPAWS-NL and the Rock Wildlife Rescue and from daily surveys at the Quinlan Brothers Ltd. seafood processing plant in Bay de Verde from September 10 to 14 (2020-2024).

- Date: Date of observation
- Location: Location of observation
- Total_lesp: Total number of stranded and dead Leach's Storm-Petrels observed
- Alive_lesp: Number of stranded Leach's Storm-Petrels observed
- Dead_lesp: Number of dead Leach's Storm-Petrel observed
- Lat: Latitude
- Long: Longitude
- Source: Data source (CPAWS-NL or Bay de Verde)
- Notes: Notes about observation

## Code/Software

#### Breeding_phenology.Rmd 
- The code required to reproduce Figure 1 
- Input file is Feb_23_BreedingPhenology_hurricane.csv

#### Colony_risk_assessment.Rmd 
- The code required to reproduce Figure 2
- Iinput files are lesp_noga_large_colonies.csv and NL_hurricanes_cat1_best_tracks.csv

#### Hurricane_Larry_colonies.Rmd
- The code required to reproduce Figure 3
- Input files are lesp_noga_large_colonies.csv and Hurricane Larry "best track" and wind radii (https://www.nhc.noaa.gov/data/tcr/index.php?season=2021&basin=atl).

#### NOGA_stranding_map.Rmd 
- The code required to reproduce Figure 4
- Input files are lesp_noga_large_colonies.csv and Gannet_Summary_HL_2024_11_26.csv

#### LESP_stranding_map.Rmd
- The code required to reproduce Figure 5
- Input files are lesp_noga_large_colonies.csv and HL_Lesp_Bdv_Cpaws_Feb_24_2025.csv

#### HL_stranding_comparison.Rmd
- The code required to reproduce Figure 6
- Input file is HL_Lesp_Bdv_Cpaws_Mar_11_2025.csv


## Sharing/Access Information
#### Data were derived from the following sources:
- Best track data for Atlantic Tropical Cyclones: https://www.nhc.noaa.gov/data/
- Best track data for Hurricane Larry: https://www.nhc.noaa.gov/data/tcr/index.php?season=2021&basin=atl
#### Data availability statement:
- Data on Leach's Storm-Petrel strandings and deaths from CPAWS-NL and the Rock Wildlife Rescue were provided with written permission from CPAWS-NL. 
