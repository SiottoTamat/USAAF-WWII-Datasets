# United States Army Air Forces (USAAF) Historical Databases

This repository contains structured datasets derived from historical sources related to the United States Army Air Forces (USAAF) during the Second World War.
THIS IS A WORK IN PROGRESS. NOT ALL THE DATA HAS BEEN VALIDATED AND THERE ARE ERRORS.

## Project Overview

The data was extracted, cleaned, and organized from complex and unstructured original sources to provide a clear, accessible, and machine-readable format.  
It is intended to support research, data analysis, historical mapping, and visualization projects related to the USAAF during WWII.

Currently, the project includes:

- **USAAF Chronology of World War II**: A structured timeline of key events involving USAAF units, operations, and missions.
- **USAAF Squadrons History**: A detailed database of squadrons, including activations, deployments, redesignations, and notable activities.


## Data Sources

- *USAAF Chronology of World War II* (official USAF historical publication)
- *Combat Squadrons of the Air Force, World War II* (Office of Air Force History)


## Fields

Each file contains structured fields including (examples):

**Chronology:**
-Index: index number
-Event#: the event number in chronological order as from the source
-date: the date of the event
-theatre: the theatre to which the event pertained as from the sourde
-old_text: the text coming from OCR and automatic cleaning techniques
-text: the text coming from automatic cleaning up from AI analyis
-locations: the unique location pertaining to the event (the event is duplicated for each location) it is a json/compatible string with specific data added
-name_location: just the name of the location chosen
-latitude: the latitude if found
-longitude: the longitude if found
-source: the method used to acquire the coordinates. auto-GNS (from Geonames); auto-Wiki (searching automatically wikipedia); manual

**Squadrons History:**
It is a structured XML: each unit has 
-name
-lineage
-assingments
-stations (a list of all the places they were assigned to)
-aircraft (a list of all airframes used)
-aircraft_types (a list of the airframe as single objects)
-operations
-service streamers
-campaings
-decorations
-emblem  


## Methodology

The Combat Chronology dataset was created through:

- OCR processing of historical documents
- procedural cleaning of the data
- AI cleaning of the data
- AI extraction of the list of geographic features in the text
- procedural geocoding of the location
- AI geocoding when not found via procedural techniques
- manual revision (ongoing)

Tools used include:
- Python (Pandas, OpenPyXL, JSON libraries)
- Excel
- ArcGIS, QGIS for geospatial validation

## License

This dataset is provided for research, educational, and non-commercial use.  
Please cite original sources where applicable when using this material.

## Contact

For questions, corrections, or collaboration inquiries, please contact:

**Andrea Siotto**  
[LinkedIn Profile](https://www.linkedin.com/in/andrea-siotto/)
