# Alma Citation Item Report

[Video Guide](https://youtu.be/9e6h1qcpxas)

*Video is outdated. This no longer requires you to download an analytics report. Simply pull the file into Colab or your preferred IDE, place a keys.env file in the runtime folder with the three required read-only API keys (bibs, courses, analytics), and run all code cells.*

## Requirements
- Create a keys.env file within your runtime environment or source folder. Enter your bibs key (read only) as bibKey=bibkeyhere, and on a new lines enter your courses key (read only) as courseKey=coursekeyhere, and your analytics key as analyticsKey=analyticskeyhere.

- If you're not using Google Colab, delete the pip commands after you install the required libraries the first time.

### General Information

- Columns in final report: course code, title, author, instructor, edition, call number, isbn, barcode, permanent location, temp location, in temp location, temp call number, temp policy, due back date, course end date.

- Report includes the physical item information for all unique barcodes under a title heading, including ones not in a temp location at a reserve desk.

- Once the report is downloaded, select a cell in the area containing data and select "Format as Table". This will allow you to drill down to specific subsets of reserves or items.

### Acknowledgements

A big thank you to Dolsy Smith (GWU Library) for his excellent presentation in the ELUNA learns 2020 - Alma Developer Deep Dives, *Optimized Python for Working with Data and API's*. The asyncronous code examples were very helpful in understanding how to construct async api calls in Python and I used some of the same structures in this code.
