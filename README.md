# Renzi_et_al_202X
Data and analysis for Renzi et al. 202X: An abundant mutualist can protect corals from multiple stressors

- `data` folder contains all original data from the project
- `figures` folder stores figure outputs from code
- `scripts` folder holds all annotated code (in R-markdown format) used for analyses and figure creation
- `generated_data` folder holds summarized data summaries generated from scripts


# Permanent data availability

Dryad data repository: [https://doi.org/10.5061/dryad.hdr7sqvtd](https://doi.org/10.5061/dryad.hdr7sqvtd)

## Description of the data and file structure

These data were collected as part of a study on the Great Barrier Reef examining the effect of a coral-associated crab on coral health from 2020-2023.

### Files and variables

###### Lead & Corresponding Author Contact Information

```
Name: Julianna Renzi
Institution: University of California, Santa Barbara
Email: jrenzi@ucsb.edu
```

###### Principle Investigator Contact Information

```
Name: Brian Silliman
Institution: Duke University
Email: brian.silliman@duke.edu
```

## Dataset Overview

This dataset contains the data required to replicate analyses in Renzi et al. (in review), examining the effects of a common coral-dwelling crab on coral health.

### Permitting

All research was conducted on Heron Island, a small (0.29 km2) coral cay in the Capricorn Bunker sector of the southern Great Barrier Reef (23°25.800'S 151°59.940'E) under Great Barrier Reef Marine Park Authority permit G19/43415.1. We collected all organisms and conducted all surveys in the scientific research zone of the reef flat on the southern portion of the island adjacent to the Heron Island Research Station.

### Recommended Citation

Julianna J. Renzi, Joseph P. Morton, Jessica L. Bergman, Devin Rowell, Edwin S. Iversen Jr., Leo C. Gaskins, Juliana Hoehne-Diana, and Brian R. Silliman. In Review. An abundant mutualist can protect corals from multiple stressors.

### Acknowledgements

This work would not be possible without the help of many, but particularly: the StatLab at the University of California, Santa Barbara; Tracy Ainsworth; Selina Ward, Stephanie Valdez; Walter Torres; and the entire staff at the Heron Island Research Station. Thank you. JJR was funded by a National Science Foundation Graduate Research Fellowship (DGE-1644868), Duke University, and a Rhodes Data Expedition grant. LCG was supported by a National Science Foundation Graduate Research Fellowship (DGE-1644868). BRS was supported by Duke RESTORE and Foundation for the Carolinas.

### Citations

Davies, S. (1989). Short-term growth measurements of corals using an accurate buoyant weighing technique. Marine Biology, 101(3), 389–395. [https://doi.org/10.1007/BF00428135](https://doi.org/10.1007/BF00428135)

Schneider, C.A., Rasband, W.S., Eliceiri, K.W. (2012). NIH Image to ImageJ: 25 years of image analysis. Nature methods, 9(7):671-5.

## Files

### Field surveys

#### File: benthic\_survey.csv

*Field surveys*

**Description:** Results from benthic surveys of the scientific zone of the Heron Island reef flat where organisms were collected and the field experiment was conducted. To document the abundance of macroalgae on the flat, we surveyed the benthos of the scientific zone along six transects with 15, 1 m^2 photo quadrats per transect, each spaced 3 m apart. Percent cover of macroalgae, live coral, and dead coral was visually estimated from photos.

##### Variables

* Date: Date of the survey in M/DD/YY format
* Transect: Transect number; transects ran perpendicular to shore and there are 6 transects total
* Quadrat: Quadrat number along a given transect; there are 15 quadrats/transect
* Perc_macroalgae: Estimated percent cover of macroalgae; 10 = 10%
* Perc_coral: Estimated percent cover of live stony corals; 10 = 10%
* Perc_dead_coral: Estimated percent cover of dead corals/reef structure; 10 = 10%

#### File: field\_crab\_surveys.csv

*Field surveys*

**Description:** To assess how common crabs were on *Acropora aspera* colonies, we surveyed crab communities on *A. aspera* at low tide, counting the abundance of crabs and noting what part of the colony they were on (living, dead, or the boundary between living and dead).

##### Variables

* Coral_ID: colony identifier for survey purposes; these ID's do not match any other ID's in the datasets provided here
* Substrate_type: classification of which part of the *A. aspera* colony the *Cyclodius* crab was on (i.e., living tissue, dead, or the boundary between living and dead). No_cyclodius means that there were no crabs observed for a colony.
* Cyclodius: the abundance of *Cyclodius* crabs in each category on a given colony

### Mesocosm experiment

#### File: initial\_buoyant\_weights.csv

*Mesocosm experiment*

**Description:** Starting weights of *A. aspera* fragments, which we used to make sure that there were not significant differences in size among treatments. Corals were weighed using buoyant weighing techniques (Davies 1989) on January 31, 2020 prior to treatment application.

##### Variables

* Coral_ID: Coral identifier for experimental corals; matches coral identifiers for other CSVs related to the tank-based experiment
* Initial_dry_weight: initial coral weight in grams

#### File: coral\_tissue\_loss.csv

*Mesocosm experiment*

**Description:** Daily estimates of tissue loss on experimental corals. The front and back of fragments were photographed daily and estimates made from photographs.

##### Variables

* Coral_ID: Coral identifier for experimental corals; matches coral identifiers for other CSVs related to the tank-based experiment
* Date: Date corals were observed
* Side: Which side (front or back) estimate relates to--sides were averaged to get percent tissue loss for a given fragment on a given day
* Percent_dead: Estimate of tissue loss; 10 = 10%

#### File: metadata.csv

*Mesocosm experiment*

**Description:** Metadata for the mesocom experiment

##### Variables

* Coral_ID: Coral identifier that matches other mesocosm datasets
* Treatment: Experimental treatment identifier; NNW = no crab, no algae, wounding; NAW = no crab, algae, wounding; CNN = crab, no algae, no wounding; CAN = crab, algae, no wounding; NAN = no crab, no algae, no wounding; NNN = no crab, no algae, no wounding (full control); CAW = crab, algae, wounding; CNW = crab, no algae, wounding
* Crab_treatment: Binary (Y = yes, N = no) as to whether a crab was added
* Algae_treatment: Binary (Y = yes, N = no) as to whether a macroalgal clump was added
* Wounding_treatment: Binary (Y = yes, N = no) as to whether a coral was wounded
* Tank_ID: Tank identifier; there were 20 total tanks with 4 units per tank
* Crab_size_mm_initial: Carapace length, in mm, of the crab added; NA written if the coral was not in a crab treatment
* HOBO_ID: HOBO temperature logger identifier, if one was attached to the unit; NA was written if there was not a temperature logger attached
* Initial_algal_biomass_g: Initial algal biomass, in grams, added to corals in macroalgal treatments; NA was written if the coral was not in a macroalgal treatment 

#### File: 10550964.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10550964

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10550964: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10551958.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10551958

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10551958: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10550963.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10550963

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10550963: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10550969.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10550969

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10550969: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10568876.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10568876

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10568876: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10550956.csv

**Description:** Temperature logger file for HOBO logger 10550956

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10550956: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10551961.csv

**Description:** Temperature logger file for HOBO logger 10551961

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10551961: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10550962.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10550962

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10550962: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: HOBO\_metadata.csv

*Temperature: mesocosm experiment*

**Description:** Metadata for temperature logger CSVs

##### Variables

* Hobo_ID: HOBO identifier
* Tank: Tank identifier that the logger was recording from
* Date_pulled: Day the logger was pulled from the mesocosm experiment

#### File: 10551954.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10551954

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10551954: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10550960.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10550960

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10550960: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10551953.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10551953

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10551953: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10550958.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10550958

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10550958: Information below is the un-modified logger information, including temperature, date, and light intensity

#### File: 10551956.csv

*Temperature: mesocosm experiment*

**Description:** Temperature logger file for HOBO logger 10551956

##### Variables

* Plot Title: HOBO logger ID--see logger metadata for information on tank placement
* 10551956: Information below is the un-modified logger information, including temperature, date, and light intensity

### Field experiment

#### File: colony\_specs.csv

*Field experiment*

**Description:** Colony location and size for *A. aspera* colonies used for the field wounding-algal experiment

##### Variables

* Colony_ID: Experimental colony identifier; matches with other experimental datasets, but not survey or mesocosm datasets
* length_cm: Maximum length, in centimeters, of the coral colony
* width_cm: Width, in centimeters, of the coral colony
* height_cm: Height, in centimeters, of the coral colony
* lat: Latitude of the coral colony's location
* long: Longitude of the coral colony's location

#### File: algae\_weight.csv&#x20;

*Field experiment*

**Description:** Weight of macroalgae used in the field experiment

##### Variables

* Colony_ID: Experimental colony identifier; matches with other experimental datasets, but not survey or mesocosm datasets
* NW_algae_initial_weight: Initial weight in grams of the macroalgae added to the control/not wounded part of the colony
* W_algae_intial_weight: Initial weight in grams of the macroalgae added to the wounded part of the colony
* NW_final_weight: Final weight in grams of the macroalgae added to the control/not wounded part of the colony
* W_final_weight: Final weight in grams of the macroalgae added to the wounded part of the colony

#### File: algal\_monitoring.csv

*Field experiment*

**Description:** 

##### Variables

* Colony_ID: Experimental colony identifier; matches with other experimental datasets, but not survey or mesocosm datasets
* algae_remaining_yn: Binary value (1 = yes, 0 = no) detailing whether there was any macroalgae left on the patch at a given time point
* time_point: Day of the field experiment on which the observation was made; on the seventh day, algal clumps were carefully removed from the patch and reweighed
* treatment: Experimental treatment; NW = no wound/control, W = wounded
* notes: Notes


### Behavioral trials

#### File: crab\_feeding\_behavior.csv

*Behavioral trials*

**Description:** Results from video analysis of crab trials detailing the number of bites crabs took on different parts of an *A. aspera* coral. Videos were reviewed to determine the number of bites each crab took on live tissue, dead skeleton, and along the tissue loss margin in each trial. We defined a bite as any time a crab used a claw to scrape along the coral and then brought the claw to its mouth. Given that the margin between living and dead coral is a thin line, we defined *C. ungulatus* as feeding along the margin if its claw scraped across both live tissue and dead skeleton before bringing its claw to its mouth.

##### Variables

* Trial: Trial identifier
* Carapace_mm: Carapace length, in mm, of crab used in the trial
* Bites_alive: Number of bites taken on live coral tissue
* Bites_margin: Number of bites taken on the margin of live and dead
* Bites_dead: Number of bites taken on the recently dead zone of tissue loss

#### File: crab\_feeding\_imageJ.csv'

*Behavioral trials*

**Description:** Point contact data used for approximating the percent cover of live tissue, the zone of recent tissue loss, and the margin on each coral fragment used in feeding video trials. The grid was created using a uniform grid in ImageJ (Schneider et al. 2012)

##### Variables

* Trial: Feeding video trial identifier
* Date: Date the trial was conducted
* Pixels^2: Pixel grid size set within ImageJ
* Alive_Pixels: Number of grid cross sections that fell on top of alive coral tissue
* Margin_Pixels: Number of grid cross sections that fell on top of the margin between alive and dead
* Dead_Pixels: Number of grid cross sections that fell on top of the zone of tissue loss

#### File: algal\_feeding\_trial.csv

*Behavioral trials*

**Description:** To test whether *C. ungulatus *reduces macroalgal biomass in tanks, we placed crabs in containers with macroalgae and monitored biomass removal over three days. Each algal clump was spun for 60 seconds and weighed before and after the trial to calculate biomass loss and percent biomass loss. Given that there were holes in each container to allow for water flow, we also ran 8 control trials to approximate background algal loss rate.

##### Variables

* Species: Whether there was a *Cyclodius* crab ("Cyclodius") in the container or not ("Control")
* Carapace_mm: Carapace width of the crab used in a trial if *Cyclodius* was added; NA indicates control
* Jar_number: Container identifier
* Initial_weight_g: Initial weight of the macroalgae in grams per trial
* Final_weight_g: Final weight of the macroalgae in grams per trial
