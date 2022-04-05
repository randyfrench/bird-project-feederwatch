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
Variable name	    Data level	Data Entry	Data Type	Definition
LOC_ID	            site	    assigned	categorical	Unique identifier for each survey site
LATITUDE	        site	    participant	continuous	Latitude in decimal degrees for each survey site
LONGITUDE	        site	    participant	continuous	Longitude in decimal degrees for each survey site
SUBNATIONAL1_CODE	site	    assigned	categorical	Country abbreviation and State or Province abbreviation                                                         of each survey site. Note that the files may contain                                                           some "XX" locations. These are sites that were                                                                 incorrectly placed by the user (e.g., site plotted in                                                           the ocean.)
SUB_ID	            checklist	assigned	categorical	Unique identifier for each checklist
OBS_ID	            observation	assigned	categorical	Unique identifier for each observation of a species
MONTH	            checklist	participant	date	    Month of 1st day of two-day observation period
DAY	                checklist	participant	date	    Day of 1st day of two-day observation period
YEAR	            checklist	participant	date	    Year of 1st day of two-day observation period
PROJ_PERIOD_ID	    season	    assigned	categorical	Calendar year of end of FeederWatch season
SPECIES_CODE	    observation	participant	categorical	Bird species observed, stored as 6-letter species codes
HOW_MANY	        observation	participant	continuous	Maximum number of individuals seen at one time during                                                           observation period
VALID	            observation	assigned	binary	    Validity of each observation based on flagging system
REVIEWED	        observation	assigned	binary	    Review state of each observation based on flagging                                                             system
PLUS_CODE	        observation	assigned	binary	    Variable indicating if the total number of a species                                                           seen was larger than the value reported
DAY1_AM	checklist	participant	binary	    Variable    indicating if observer watched during morning of count                                                         Day 1
DAY1_PM	checklist	participant	binary	    Variable    indicating if observer watched during afternoon of                                                             count Day 1
DAY2_AM	checklist	participant	binary	    Variable    indicating if observer watched during morning of count                                                         Day 2
DAY2_PM	checklist	participant	binary	    Variable    indicating if observer watched during afternoon of                                                             count Day 2
DATA_ENTRY_METHOD	checklist	assigned	categorical	Data entry method for each checklist (e.g., web, mobile                                                         app or paper form)

