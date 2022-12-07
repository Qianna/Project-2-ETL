# Project-2-ETL

## Group 16 Animal shelter database
Members: Yuteng Zhang, Qianna Xu
## Project proposal can be found at: 
https://docs.google.com/document/d/15SQkvRzSfLdW-ADJFgEga5yCrzJgc03z/edit?usp=sharing&ouid=102507649283465667619&rtpof=true&sd=true

# Project report

## Extract
* Downloaded animal shelter intake and outcome record from the city of Long Beach from https://data.longbeach.gov/explore/dataset/animal-shelter-intakes-and-outcomes/ in JSON 
* Downloaded animal shelter data (CSV format) from the city of Dallas, TX from https://www.dallasopendata.com/Services/, including fiscal years 2018-2019, 2019-2020, and 2020-2021. 

## Transform
* The Long Beach data (JSON) was read into a pandas dataframe and filtered to remove unwanted information (excluded dataset ID, record ID, and record timestamp)
    * The field records were saved as a new dataframe

* Dallas datasets (CSV) were cleaned using pandas and saved as new dataframes accordingly.

## Load
* Using pymongo, four cleaned dataframes were imported into MongoDB. Each dataframe was loaded into MongoDB as a collection in the animal_shelter_db database.
* The database was created to host animal shelter intake and outcome record from different city to help people understand the operational processes at these animal shelters.
* We can also use the data to examine tempoal trends in how many animals were housed at animal shelters and how many of them were adopted, etc. across different years. The trends can also be compared across different cities.

