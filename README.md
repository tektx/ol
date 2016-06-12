# OwnLocal REST API
This application creates a REST API from a CSV file, and provides endpoints to view information for businesses as a paginated group or by individual business. It was created using Flask and Python 2.7.

## Prerequisites
1. Python 2.7 - Download [here](https://www.python.org/downloads/).
2. virtualenv for Python - Open a command-line window and run ```pip install virtualenv```.
3. Flask for Python - Open a command-line window and run ```pip install flask```.

## Run
Run the command ```python api.py``` to start the server at http://localhost:5000.

## Usage
Two endpoints are provided:

### GET /businesses
Retrieves the first 50 results in JSON format in descending order by ID.

Two parameters are supported: ```page``` will display a specific page of results, and ```entries``` will change the number of results displayed per page.

Example: ```http://localhost.com:5000/businesses?page=2&entries=10``` will show the second page of businesses at 10 entries per page.

### GET /businesses/{id}
Retrieves the information for the business with the specified ID.

Example: ```http://localhost.com:5000/businesses/5``` will show the information for the fifth business.