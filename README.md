# Alma Reserve Inventory

[Video Guide](https://youtu.be/nmApjxm8vFE)

## Overview
This generates an excel spreadsheet (xlsx format) that contains the physical item information for your course reserve citations in Alma. Think of it like being able to combine the Courses and Physical Items subject areas in an Analytics report. The code makes a series of API calls, first to a shared report in Analytics that contains some basic course information, some of which is included in the final report and some of which is used to build the physical item API calls. For each MMS ID a Bibs call is made. If items exist under that bib, the item information is linked to the course. If it doesn't, a Courses call is made to retrieve Citation information.

## Requirements
- Create a keys.env file within your runtime environment or source folder. Enter your bibs key (read only) as bibKey=bibkeyhere, and on a new lines enter your courses key (read only) as courseKey=coursekeyhere, and your analytics key as analyticsKey=analyticskeyhere. It should look like this:
    
`bibKey=bibkeyhere`
\
`courseKey=coursekeyhere`
\
`analyticsKey=analyticskeyhere`


### General Information

- If you're not using Google Colab, delete the pip commands after you install the required libraries the first time.

- Columns in final report: course code, title, author, instructor, edition, call number, isbn, barcode, permanent location, temp location, in temp location, temp call number, temp policy, due back date, course end date.

- Report includes the physical item information for all unique barcodes under a title heading, including ones not in a temp location at a reserve desk.

- Once the report is downloaded, select a cell in the area containing data and select "Format as Table". This will allow you to drill down to specific subsets of reserves or items.


### Acknowledgements

A big thank you to Dolsy Smith (GWU Library) for his excellent presentation in the ELUNA learns 2020 - Alma Developer Deep Dives, *Optimized Python for Working with Data and API's*. The asyncronous code examples were very helpful in understanding how to construct async api calls in Python and I used some of the same structures in this code.
