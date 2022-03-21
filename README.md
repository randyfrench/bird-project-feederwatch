This is a project from TheCornellLab Project FeederWatch that I will be working on birds spotted at feeders.
The data is raw, taken from the site: https://feederwatch.org/explore/raw-dataset-requests/
I am using the checklist data 2021. 
From FeederWatch website:
"Data validation
As with all large-scale citizen science programs, it is impossible to validate each of the millions of records submitted to FeederWatch. Although we attempt to minimize errors, a small percentage of FeederWatch reports are incorrect and analysts must be aware that misidentifications, data entry errors, and other sources of error can evade our data validation system.

All FeederWatch data are passed through a series of geographically and temporally specific filters that “flag” reports of species (or high counts) that are unexpected at a given location at a certain time of the year. The geographic resolution is relatively coarse (one filter per state/province), and the temporal resolution is monthly. Only reports that are flagged by the filters undergo a systematic manual review. A flag may be removed by the expert reviewer without a request for supporting information, or additional evidence may be requested. If additional information is requested but is insufficient to validate the report, that record remains in the database and is identified as an unconfirmed report. Flagged records are identified using a combination of the Valid field and the Reviewed field as defined here:

Valid = 1; Reviewed = 0
Interpretation: Report did not trigger the automatic flagging system and was accepted into the database without review

Valid = 1; Reviewed = 1
Interpretation: Report triggered the flagging system and was approved by an expert reviewer

Valid = 0; Reviewed = 1
Interpretation: Report triggered a flag by the automated system and was reviewed; insufficient evidence was provided to confirm the report

Valid = 0; Reviewed = 0
Interpretation: Report triggered a flag by the automated system and awaits the review process"

The DATA DICTIONARY - Need to format it correctly to be readable.

*** Data Dictionary ***
List of variables provided in Project FeederWatch database. 				
*Asterisks indicate the information is stored as multiple fields in the database. 				
Variable in all capital letters are the actual field names. 				
				
Data fields stored in the Project FeederWatch "observation" data files:				
Variable name	Data level	Data Entry	Data Type	Definition
LOC_ID	site	assigned	categorical	Unique identifier for each survey site
LATITUDE	site	participant	continuous	Latitude in decimal degrees for each survey site
LONGITUDE	site	participant	continuous	Longitude in decimal degrees for each survey site
SUBNATIONAL1_CODE	site	assigned	categorical	Country abbreviation and State or Province abbreviation of each survey site. Note that the files may contain some "XX" locations. These are sites that were incorrectly placed by the user (e.g., site plotted in the ocean.)
ENTRY_TECHNIQUE	site	assigned	categorical	Variable indicating method of site localization
SUB_ID	checklist	assigned	categorical	Unique identifier for each checklist
OBS_ID	observation	assigned	categorical	Unique identifier for each observation of a species
MONTH	checklist	participant	date	Month of 1st day of two-day observation period
DAY	checklist	participant	date	Day of 1st day of two-day observation period
YEAR	checklist	participant	date	Year of 1st day of two-day observation period
PROJ_PERIOD_ID	season	assigned	categorical	Calendar year of end of FeederWatch season
SPECIES_CODE	observation	participant	categorical	Bird species observed, stored as 6-letter species codes
HOW_MANY	observation	participant	continuous	Maximum number of individuals seen at one time during observation period
VALID	observation	assigned	binary	Validity of each observation based on flagging system
REVIEWED	observation	assigned	binary	Review state of each observation based on flagging system
PLUS_CODE	observation	assigned	binary	Variable indicating if the total number of a species seen was larger than the value reported
DAY1_AM	checklist	participant	binary	Variable indicating if observer watched during morning of count Day 1
DAY1_PM	checklist	participant	binary	Variable indicating if observer watched during afternoon of count Day 1
DAY2_AM	checklist	participant	binary	Variable indicating if observer watched during morning of count Day 2
DAY2_PM	checklist	participant	binary	Variable indicating if observer watched during afternoon of count Day 2
EFFORT_HRS_ATLEAST	checklist	participant	categorical	Participant estimate of survey time  for each checklist
SNOW_DEP_ATLEAST	checklist	participant	categorical	Participant estimate of minimum snow depth during a checklist
DATA_ENTRY_METHOD	checklist	assigned	categorical	Data entry method for each checklist (e.g., web, mobile app or paper form)
Data fields stored in the Project FeederWatch "site description" data file:				
Variable name	Data level	Data Entry	Data Type	Definition
LOC_ID, PROJ_PERIOD_ID				As above, these fields function as primary keys for linking site with observation data
Yard type*	season	participant	binary	Variables indicating features of yard (*five fields)
Habitat type*	season	participant	binary	Variables indicating features of surrounding habitat (*fourteen fields)
Trees/shrubs*	season	participant	categorical	Variables indicating types of surrounding vegetation (*six fields)
Brush pile/water*	season	participant	categorical	Variables indicating presence of brush piles or water sources (*three fields)
NEARBY_FEEDERS	season	participant	binary	Variable indicating if other feeders are regularly operated within 90m of survey site
Other animals*	season	participant	binary	Variables indicating if squirrels, cats, dogs or humans are at the survey site (*four fields)
HOUSING_DENSITY	season	participant	categorical	Participant estimated housing density of neighborhood
Feeding schedule*	season	participant	binary	Variables indicating which months of the year participants provide food (*thirteen fields)
Feeder numbers by type*	season	participant	continuous	Variables indicating the number and types of feeders provided (*eight fields)
POPULATION_ATLEAST	season	participant	categorical	Participant estimated population of city or town
COUNT_AREA_SIZE_SQ_M_ATLEAST	season	participant	categorical	Participant estimated area of survey site
CREATION_DT	site	assigned	date	Date of site creation
LAST_EDITED_DT	site	assigned	date	Date of last site location edit