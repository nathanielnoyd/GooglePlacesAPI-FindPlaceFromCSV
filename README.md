# Google Places API - Find Place from CSV/Excel/Spreadsheet

This script takes a CSV file, looks up each row in the Google Places API, then spits out an Excel file. As configured, it takes the text from the first column and searches for the corresponding Google place ID, but it can be configured to return any field from the API.

If you have a spreadsheet with a list of places, this is a quick and easy way to find and store the corresponding Google place IDs.

## What it does

It reads the CSV into a pandas DataFrame and creates a new column for the place ID. Then it goes through each row, looking up the place ID, which it places into the new column. If the API returns no result, the cell is left blank.

The final product is saved as "output.xlsx" in the same folder.

## How to use it

### Starting in Excel/Google Sheets/etc:

1. Format your data. 

By default, this script reads data from the first column and adds the place ID to the second column. If you have multiple columns (place name, city, country, etc.), you can concatenate the columns into a single string.

The first row is for the header and will be ignored.

2. Export your data as a CSV file. The script looks for "input.csv", but you can change that.


### In a Juypter notebook:

3. Set your Google Places API key. Place it within the quotation marks on the line that says "api_key =".

If desired, change the input and output file names and locations (defaults are "input.csv" and "output.xlsx" in the current folder).

4. Run.

