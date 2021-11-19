# Slurpee Scout API

## API description

This API takes a location in coordinates and a radius around that location, and returns the top 3 most popular 7Elevens in that radius as well as the number of slurpees they sold that year. This allows customers to find a 7Eleven branch near to them and decide which one to visit based on other customer’s preferences. It can also be used by management teams to check on a location’s performance.

## Endpoint with Parameters


## Description of Resources

The resources returned include the owner, coordinates, and number of Slurpee sales of the top 3 most popular 7Eleven locations.

### Sample Response

```
{
“McPhillips7Eleven” : {
		“Owner”: “Elmo”,
		“Lng”: 49.8951,
		“Lat”: -97.1384,
		“Sales”: 546,
},
“Keewatin7Eleven” : {
		“Owner”: “Fred Rogers”,
		“Lng”: 49.8951, 
		“Lat”: 34.1384,
		“Sales”: 123,
}
“Pembina7Eleven” : {
		“Owner”: “Barney”,
		“Lng”: 108.8951, 
		“Lat”: 57.1384,
		“Sales”: 50,
}
}
```
