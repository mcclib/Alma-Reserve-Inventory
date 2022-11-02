# Alma Citation Item Report

[Video Guide](https://youtu.be/q-sS8sSg2Ks)

## Requirements
- Create a keys.env file within your runtime environment or source folder. Enter your bibs key (read only) as bibKey=bibkeyhere, and on a new line enter your courses key (read only) as courseKey=coursekeyhere.

- Generate an analytics report that contains the following columns: Citation Id, Course ID, Course Code, Course Instructor, Reading List Id, Current Course End Date, MMS Id. Leave column names default. Download as data > excel format. Name it citation ids.xlsx and upload it to the runtime environment.

- If you're using Google Colab to generate the report, you'll need to install both the asyncio-throttle and python-dotenv libraries. To do so, use the following pip commands: !pip install python-dotenv, !pip install asyncio-throttle.

### General Information

- Columns in final report: ['course code', 'title', 'author', 'instructor', 'edition','call number', 'isbn', 'barcode', 'permanent location', 'temp location', 'in temp location', 'temp call number', 'temp policy', 'due back date', 'course end date']

- Report includes the physical item information for all unique barcodes under a title heading, including ones not in a temp location at a reserve desk.

- Once the report is downloaded, select a cell in the area containing data and select "Format as Table". This will allow you to drill down to specific subsets of reserves or items.

### Acknowledgements

A big thank you to Dolsy Smith (GWU Library) for his excellent segment in the ELUNA learns 2020 - Alma Developer Deep Dives, titled *Optimized Python for Working with Data and API's*. The asyncronous code examples were very helpful in understanding how to construct async api calls in Python.
