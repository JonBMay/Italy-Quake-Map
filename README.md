# Italy-Quake-Maps

## Citations
The file contained inside the directory 'Epicenter' was produced and released by INGV with the following notes:
	
	CPTI15 is openly available via its dedicated website at http://emidius.mi.ingv.it/CPTI15-DBMI15, and the “web service” via the Italian Archive of Historical Earthquake Data (ASMI; https://emidius.mi.ingv.it/ASMI/services/).
	CPTI15 is a scientific product released by Istituto Nazionale di Geofisica (INGV) that required several years of work, and makes available data released by various authors from different institutions.
	CPTI15 can be used for scientific purposes, and the source must always be cited.
and citation: 
	
	Rovida A., Locati M., Camassi R., Lolli B., Gasperini P. (eds), 2019. Italian Parametric Earthquake Catalogue (CPTI15), version 2.0. Istituto Nazionale di Geofisica e Vulcanologia (INGV). https://doi.org/10.13127/CPTI/CPTI15.2

All data contained within 'geojson-italy-master' is from https://github.com/openpolis/geojson-italy, the original README is contained within the directory.
I have removed the topojson directory as it was not needed for this work.


## Three notebooks provided
The file CleanNames.ipynb contains the code which makes some required changes to the region, province and municipality names, it is only needed if a newer version of the geojson files are produced using the same naming.
I include already cleaned and combined geojson files for Italian Regions, Provinces and Municipalities: 'IT_regions.json', 'IT_provinces.json', 'IT_municipalities.json'.

A.ipynb: 
  - reads data from CSV input file(s)  
  - removes any duplicates and entries with NaN values within required fields  
  - matches each epicenter to a region/province/municipality using geojson files & optionaly filters by magnitude  
  - writes generated dataframe into a csv file  

B.ipynb: 
  - reads municipalty.csv file  
  - filters plotting area using regions/provinces
  - creates an interactive map with coloured municipalities based on the number of earthquakes & includes points showing epicentral locations  


## Notes for users
Within each Python cell I use '##' to denote labels used to separate code and '#' to comment optional commands which may be used as needed.  
The user should check that the files and directories expected inside the cells match those that exist on their system.  
The current setup expects the following directories: 'Epicentee' containing the CSV epicenter file(s); 'geojson-italy-master' which contains 'geojson' which contains the geojson files; 'Maps' which is where the saved html map files are stored.  
I have provided the necessary input files for Part B which allows the testing of the plotting without the need of Part A.  
Files needed for Part A are also provided, however some files which may be produced by Part A but are not required in Part B are not provided and must be generated using Part A.  
In some cases the maps generated in Part B may not display properly due to plotting complexity, however the saved html file is correct.  
Earthquakes occuring at sea are ignored as the municipalities within the GeoJson files finish at the coast.  
Each of the Regional, Provincial and Municipal epicenter assignements in Part A contains a command to sort the data before storing it to a CSV file, this sorting may be removed to save time without effecting the plotting within Part B.  
