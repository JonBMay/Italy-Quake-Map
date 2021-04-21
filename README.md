# Italy-Quake-Maps

Earthquake data from ....
GeoJson data from ....


I include already cleaned and combined geojson files for Italian Regions, Provinces and Municipalities.
The file CleanNames.ipynb contains the code which makes the required changes to the names, it is only needed if a newer version of the geojson file is produced using the same naming.

Notebook to combine data

Notebook to remove repeated events

Notebook to plot graphs


Within each Python cell I use '##' to denote labels used to separate code and '#' to comment optional commands which may be used as needed.

The user should check that the files and directories expected inside the cells match those that exist on their system

The current setup expects the following directories: 'Epicentee' containing the CSV epicenter file(s); 'geojson-italy-master' which contains 'geojson' which contains the geojson files; 'Maps' which is where the saved html map files are stored






Part A reads the information from a single or multiple CSV files stored in the directory Epicenter and saves .....





I have provided the necessary input files for Part B which allows the testing of the plotting without the need of Part A.
Files needed for Part A are also provided, however some files which may be produced by Part A but are not required in Part B are not provided and must be generated using Part A.



In some cases the maps generated in Part B may not display properly due to plotting complexity, however the saved html file is correct.



Clicking on a municipality of the map in Part B will automatically zoom around that area. Each point represents an Earthquake and will produce a popup when clicked containing its coordinates and magnitude.


All required input files are provided, as well as all files which are created during the running of the scripts, this allows the user to immediately check the plotting as an example without needing to setup the required data before. 






Earthquakes occuring at sea are ignored as the municipalities within the GeoJson files finish at the coast.



Each of the Regional, Provincial and Municipal epicenter assignements in Part A contains a command to sort the data before storing it to a CSV file, this sorting may be removed to save time without effecting the plotting within Part B.
