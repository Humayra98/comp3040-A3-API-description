# Slurpee Scout API

## API description

This API takes a location in coordinates and a radius around that location, and returns the 3 most popular stores in that radius as well as the number of slurpees they sold that year. This allows customers to find a store near to them and decide which one to visit based on other customer’s preferences. This can also be used by management teams to check on a location’s performance. The API returns information for Manitoba based locations only.

## Endpoint and Parameters
Do the following GET request to get 3 most popular store for slurpees. 

### Endpoint
https://slurpeesales.mb.ca/api/top_3

### Parameters
   * lat (float): Latitude of current location in decimal degrees. Required.
   * lng (float): Longitude of current location in decimal degrees. Required.
   * radius(int): Desired radius for the search in KM. Optional. Default value 10 KM.

## Description and Resources
The resources returned include the store, owner, latitude, longitude, and number of slurpee sales of a store.

## Sample

### Request
To get top 3 stores for slurpees within 5km radius of 49.8951° N latitude and 97.1384° W longitude do the following GET request:
https://slurpeesales.mb.ca/api/top_3?lat=49.8951&lng=-97.1384&radius=5

### Response
Response will contain a list of JSON objects where each contains the name of store, owner, latitude, longitude and sales during the year of the request. The result data will be formatted using JSON as follows:

```
{
	"top_3": [
			{ 
				"store": "McPhillips7Eleven",  
				"owner": "Elmo", 
				"lat": 49.8951, 
				"lng": -97.1384, 
				"sales": 546
			},
			{ 
				"store": "Keewatin7Eleven", 
				"owner": "Fred Rogers", 
				"lat": 49.8951, 
				"lng": 34.1384, 
				"sales": 123
			},
			{ 
				"store": "Pembina7Eleven", 
				"owner": "“Barney”", 
				"lat": 108.8951, 
				"lng": 57.1384, 
				"sales": 50 
			}
		 ]
}
```
