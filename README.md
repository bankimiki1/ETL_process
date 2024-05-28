This code retrieves historical taxi and weather data for a specified date, uploads it to S3 for processing, and prints status messages upon successful upload, utilizing functions for data retrieval and S3 upload while adhering to a specific datetime format.

Main functions:

**get_taxi_data()** - This function retrieves taxi data for a specific date by making an API call to the City of Chicago's database, utilizing the formatted datetime parameter to specify the time range of the data, and returns the obtained taxi data as a JSON dictionary.

**get_weather_data()** - This function retrieves weather data for a specific date and time by sending a request to the Open Meteo API, with parameters including latitude, longitude, start date, end date, and hourly data fields, returning the obtained weather data as a dictionary containing temperature, wind speed, rain, and precipitation information.

**upload_to_s3()** - The function uploads data as a JSON object to a specified folder within an S3 bucket using the boto3 library.

**lambda_handler()** - This function retrieves taxi and weather data for a specified date, formats the data, uploads it to an S3 bucket, and prints confirmation messages.
