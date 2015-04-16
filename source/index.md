---
title: Miami Transit API Docs

language_tabs:
  - shell

toc_footers:
  - <a href='http://codeformiami.org/'>Code for Miami</a>

search: true
---

# Miami Transit API

Welcome to the Miami Transit API documentation. This API provides transit data for Miami-Dade County and City of Miami. The data is available in `JSON` and `XML` formats.

The first thing you will need is the API endpoint for this service.

* [http://miami-transit-api.herokuapp.com/api/](http://miami-transit-api.herokuapp.com/api/)

# Making Requests

All endpoints use `HTTP GET`. The response format (`json` or `xml`) must be included in all request URLs.  The general URL structure is:

* **JSON**: `/api/{resource}.json?param=value` 
* **XML**: `/api/{resource}.xml?param=value`

# Miami-Dade County

## Buses

```shell
$ curl http://miami-transit-api.herokuapp.com/api/Buses.json
```

> Response: HTTP/1.1 200 OK

```json
{
    "RecordSet": {
        "Record": [
            {
                "BusID": "1085",
                "BusName": "06303",
                "Direction": "S",
                "Latitude": "25.77049",
                "LocationUpdated": "11:02:25 AM",
                "Longitude": "-80.13512",
                "RouteID": "123",
                "Service": "CW",
                "ServiceDirection": "Clockwise",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "SBL - SOUTH BEACH LOCAL S POINTE via WEST",
                "TripID": "3407120"
            },
            {
                "BusID": "1669",
                "BusName": "06346",
                "Direction": "N",
                "Latitude": "25.78806",
                "LocationUpdated": "11:02:29 AM",
                "Longitude": "-80.14233",
                "RouteID": "123",
                "Service": "CW",
                "ServiceDirection": "Clockwise",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "SBL - SOUTH BEACH LOCAL S POINTE via WEST",
                "TripID": "3407122"
            },
            {
                "BusID": "1687",
                "BusName": "06367",
                "Direction": null,
                "Latitude": "25.7932",
                "LocationUpdated": "11:01:46 AM",
                "Longitude": "-80.1416",
                "RouteID": "123",
                "Service": "CW",
                "ServiceDirection": "Clockwise",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "SBL - SOUTH BEACH LOCAL S POINTE via WEST",
                "TripID": "3407118"
            },
            {
                "BusID": "1135",
                "BusName": "06334",
                "Direction": "N",
                "Latitude": "25.78521",
                "LocationUpdated": "11:02:29 AM",
                "Longitude": "-80.13191",
                "RouteID": "123",
                "Service": "CCW",
                "ServiceDirection": "CntrClockwise",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "SBL - SOUTH BEACH LOCAL S POINTE via WASHINGTON",
                "TripID": "3407058"
            },
            {
                "BusID": "1696",
                "BusName": "09102",
                "Direction": "W",
                "Latitude": "25.79862",
                "LocationUpdated": "11:02:29 AM",
                "Longitude": "-80.26196",
                "RouteID": "150",
                "Service": "EB",
                "ServiceDirection": "Eastbound",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "150 - MIAMI BEACH",
                "TripID": "3406867"
            },
            {
                "BusID": "1839",
                "BusName": "09113",
                "Direction": "S",
                "Latitude": "25.79031",
                "LocationUpdated": "11:02:30 AM",
                "Longitude": "-80.13193",
                "RouteID": "150",
                "Service": "EB",
                "ServiceDirection": "Eastbound",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "150 - MIAMI BEACH",
                "TripID": "3406868"
            },
            {
                "BusID": "1695",
                "BusName": "09101",
                "Direction": "E",
                "Latitude": "25.79069",
                "LocationUpdated": "11:02:29 AM",
                "Longitude": "-80.13018",
                "RouteID": "150",
                "Service": "WB",
                "ServiceDirection": "Westbound",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "150 - AIRPORT",
                "TripID": "3406834"
            },
            {
                "BusID": "1697",
                "BusName": "09103",
                "Direction": null,
                "Latitude": "25.8047",
                "LocationUpdated": "11:01:46 AM",
                "Longitude": "-80.2646",
                "RouteID": "150",
                "Service": "WB",
                "ServiceDirection": "Westbound",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "150 - AIRPORT",
                "TripID": "3406835"
            },
            {
                "BusID": "1142",
                "BusName": "12303",
                "Direction": "W",
                "Latitude": "25.57666",
                "LocationUpdated": "11:02:24 AM",
                "Longitude": "-80.35486",
                "RouteID": "200",
                "Service": "CW",
                "ServiceDirection": "Clockwise",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "200 - CUTLER BAY LOCAL",
                "TripID": "3345001"
            },
            {
                "BusID": "1023",
                "BusName": "06143",
                "Direction": null,
                "Latitude": "25.8465",
                "LocationUpdated": "11:01:05 AM",
                "Longitude": "-80.2417",
                "RouteID": "297",
                "Service": "NB",
                "ServiceDirection": "Northbound",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "297 - 27th AVE ORG MAX NW 207 ST / 27 AVE",
                "TripID": "3346277"
            },
            {
                "BusID": "1112",
                "BusName": "06146",
                "Direction": "S",
                "Latitude": "25.91803",
                "LocationUpdated": "11:02:29 AM",
                "Longitude": "-80.2445",
                "RouteID": "297",
                "Service": "SB",
                "ServiceDirection": "Southbound",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "297 - 27 AVE ORG MAX AIRPORT STATION",
                "TripID": "3346240"
            },
            {
                "BusID": "1626",
                "BusName": "06127",
                "Direction": null,
                "Latitude": "25.7977",
                "LocationUpdated": "10:59:06 AM",
                "Longitude": "-80.2584",
                "RouteID": "297",
                "Service": "SB",
                "ServiceDirection": "Southbound",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "297 - 27 AVE ORG MAX AIRPORT STATION",
                "TripID": "3346227"
            },
            {
                "BusID": "1913",
                "BusName": "AT5775",
                "Direction": "N",
                "Latitude": "25.37654",
                "LocationUpdated": "11:02:29 AM",
                "Longitude": "-80.46355",
                "RouteID": "301",
                "Service": "NB",
                "ServiceDirection": "Northbound",
                "ServiceName": "WEEKDAY",
                "TripHeadsign": "301 - FL CITY WALMART",
                "TripID": "3346319"
            }
        ]
    }
}
```

Only provides data for buses _actively running trips_ on the following routes: 

* Route 34 Busway Flyer
* Route 95 Dade‐Broward Express
* Route 123 South Beach Local
* Route 150 Miami Beach Airport Flyer
* Route 200 Cutler Bay Local
* Route 288 Kendall Cruiser
* Route 297 27th Ave Orange Max
* Route 301 Dade-Monroe Express
* Route 302 Card Sound Express

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/Buses.json](http://miami-transit-api.herokuapp.com/api/Buses.json)

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
BusID | 
BusName  | 
RouteID  | 
Dir | 

### Response Attributes

Attribute | Description
--------- | -----------
BusID | 
BusName | 
Latitude | 
Longitude | 
RouteID | 
TripID | 
Direction | 
ServiceDirection | 
Service | 
ServiceName | 
TripHeadsign | 
LocationUpdated | 

## BusParkRide

```shell
$ curl http://miami-transit-api.herokuapp.com/api/BusParkRide.json
```

> Response: HTTP/1.1 200 OK

```json
{
    "RecordSet": {
        "Record": [
            {
                "Description": "Near Target",
                "Latitude": "25.576458",
                "Longitude": "-80.372736",
                "ParkRideID": "5",
                "ParkRideName": "Busway - SW 112 Ave",
                "svHeading": "332",
                "svLatitude": "25.576093",
                "svLongitude": "-80.372957"
            },
            {
                "Description": null,
                "Latitude": "25.628599",
                "Longitude": "-80.342213",
                "ParkRideID": "3",
                "ParkRideName": "Busway - SW 152 St",
                "svHeading": "179",
                "svLatitude": "25.628853",
                "svLongitude": "-80.342631"
            },
            {
                "Description": null,
                "Latitude": "25.614523",
                "Longitude": "-80.348682",
                "ParkRideID": "4",
                "ParkRideName": "Busway - SW 168 St",
                "svHeading": "26",
                "svLatitude": "25.613872",
                "svLongitude": "-80.348861"
            },
            {
                "Description": null,
                "Latitude": "25.53975",
                "Longitude": "-80.408812",
                "ParkRideID": "6",
                "ParkRideName": "Busway - SW 244 St",
                "svHeading": "213",
                "svLatitude": "25.540114",
                "svLongitude": "-80.408712"
            },
            {
                "Description": null,
                "Latitude": "25.492989",
                "Longitude": "-80.453364",
                "ParkRideID": "7",
                "ParkRideName": "Busway - SW 296 St",
                "svHeading": "353",
                "svLatitude": "25.492355",
                "svLongitude": "-80.453565"
            },
            {
                "Description": null,
                "Latitude": "25.628101",
                "Longitude": "-80.381529",
                "ParkRideID": "8",
                "ParkRideName": "Coral Reef Drive / Florida's Turnpike",
                "svHeading": "354",
                "svLatitude": "25.62741",
                "svLongitude": "-80.381316"
            },
            {
                "Description": "Broward Blvd",
                "Latitude": "26.122503",
                "Longitude": "-80.171946",
                "ParkRideID": "13",
                "ParkRideName": "Ft. Lauderdale Tri-Rail Station",
                "svHeading": "297",
                "svLatitude": "26.122772",
                "svLongitude": "-80.170513"
            },
            {
                "Description": "I-95, US 441, and Palmetto Intersection",
                "Latitude": "25.922772",
                "Longitude": "-80.212023",
                "ParkRideID": "14",
                "ParkRideName": "Golden Glades - East Lot",
                "svHeading": "52",
                "svLatitude": "25.921681",
                "svLongitude": "-80.213093"
            },
            {
                "Description": "I-95, US 441, and Palmetto Intersection",
                "Latitude": "25.920813",
                "Longitude": "-80.215114",
                "ParkRideID": "10",
                "ParkRideName": "Golden Glades - West Lot",
                "svHeading": "183",
                "svLatitude": "25.921288",
                "svLongitude": "-80.215091"
            },
            {
                "Description": "SW 104 St / 152 Ave",
                "Latitude": "25.67112",
                "Longitude": "-80.441878",
                "ParkRideID": "9",
                "ParkRideName": "Hammocks Town Center",
                "svHeading": "27",
                "svLatitude": "25.671027",
                "svLongitude": "-80.443724"
            },
            {
                "Description": null,
                "Latitude": "25.685305",
                "Longitude": "-80.436294",
                "ParkRideID": "2",
                "ParkRideName": "Kendall Drive and SW 150 Ave",
                "svHeading": "148",
                "svLatitude": "25.685783",
                "svLongitude": "-80.436581"
            },
            {
                "Description": "Miami Gardens Drive & NW 73 Ave",
                "Latitude": "25.940926",
                "Longitude": "-80.319741",
                "ParkRideID": "11",
                "ParkRideName": "Miami Gardens Drive Park and Ride",
                "svHeading": "189",
                "svLatitude": "25.941573",
                "svLongitude": "-80.320318"
            },
            {
                "Description": null,
                "Latitude": "26.031716",
                "Longitude": "-80.167773",
                "ParkRideID": "12",
                "ParkRideName": "Sheridan Street Tri-Rail Station",
                "svHeading": "251",
                "svLatitude": "26.032142",
                "svLongitude": "-80.166768"
            },
            {
                "Description": "9155 SW 162 Ave",
                "Latitude": "25.680958",
                "Longitude": "-80.456699",
                "ParkRideID": "1",
                "ParkRideName": "West Kendall Transit Terminal",
                "svHeading": "136",
                "svLatitude": "25.681529",
                "svLongitude": "-80.457371"
            }
        ]
    }
}
```

List bus 'Park & Ride' locations

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusParkRide.json](http://miami-transit-api.herokuapp.com/api/BusParkRide.json)

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
ParkRideID | 

### Response Attributes

Attribute | Description
--------- | -----------
ParkRideID |
ParkRideName |
Description | 
Latitude | 
Longitude | 
svLatitude | 
svLongitude | 
svHeading | 

## BusRouteDirections

```shell
$ curl http://miami-transit-api.herokuapp.com/api/BusRouteDirections.json
```

> Response: HTTP/1.1 200 OK

```json
{
    "RecordSet": {
        "Record": [
            {
                "Direction": "Northbound",
                "RouteID": "1"
            },
            {
                "Direction": "Southbound",
                "RouteID": "1"
            },
            {
                "Direction": "Northbound",
                "RouteID": "2"
            },
            {
                "Direction": "Southbound",
                "RouteID": "2"
            },
            {
                "Direction": "Northbound",
                "RouteID": "3"
            },
            {
                "Direction": "Southbound",
                "RouteID": "3"
            },
            {
                "Direction": "Northbound",
                "RouteID": "6"
            },
            {
                "Direction": "Southbound",
                "RouteID": "6"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "7"
            },
            {
                "Direction": "Westbound",
                "RouteID": "7"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "8"
            },
            {
                "Direction": "Westbound",
                "RouteID": "8"
            },
            {
                "Direction": "Northbound",
                "RouteID": "9"
            },
            {
                "Direction": "Southbound",
                "RouteID": "9"
            },
            {
                "Direction": "Northbound",
                "RouteID": "10"
            },
            {
                "Direction": "Southbound",
                "RouteID": "10"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "11"
            },
            {
                "Direction": "Westbound",
                "RouteID": "11"
            },
            {
                "Direction": "Northbound",
                "RouteID": "12"
            },
            {
                "Direction": "Southbound",
                "RouteID": "12"
            },
            {
                "Direction": "Northbound",
                "RouteID": "16"
            },
            {
                "Direction": "Southbound",
                "RouteID": "16"
            },
            {
                "Direction": "Northbound",
                "RouteID": "17"
            },
            {
                "Direction": "Southbound",
                "RouteID": "17"
            },
            {
                "Direction": "Northbound",
                "RouteID": "19"
            },
            {
                "Direction": "Southbound",
                "RouteID": "19"
            },
            {
                "Direction": "Northbound",
                "RouteID": "21"
            },
            {
                "Direction": "Southbound",
                "RouteID": "21"
            },
            {
                "Direction": "Northbound",
                "RouteID": "22"
            },
            {
                "Direction": "Southbound",
                "RouteID": "22"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "24"
            },
            {
                "Direction": "Westbound",
                "RouteID": "24"
            },
            {
                "Direction": "Northbound",
                "RouteID": "27"
            },
            {
                "Direction": "Southbound",
                "RouteID": "27"
            },
            {
                "Direction": "Northbound",
                "RouteID": "29"
            },
            {
                "Direction": "Southbound",
                "RouteID": "29"
            },
            {
                "Direction": "Northbound",
                "RouteID": "31"
            },
            {
                "Direction": "Southbound",
                "RouteID": "31"
            },
            {
                "Direction": "Northbound",
                "RouteID": "32"
            },
            {
                "Direction": "Southbound",
                "RouteID": "32"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "33"
            },
            {
                "Direction": "Westbound",
                "RouteID": "33"
            },
            {
                "Direction": "Northbound",
                "RouteID": "34"
            },
            {
                "Direction": "Southbound",
                "RouteID": "34"
            },
            {
                "Direction": "Northbound",
                "RouteID": "35"
            },
            {
                "Direction": "Southbound",
                "RouteID": "35"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "36"
            },
            {
                "Direction": "Westbound",
                "RouteID": "36"
            },
            {
                "Direction": "Northbound",
                "RouteID": "37"
            },
            {
                "Direction": "Southbound",
                "RouteID": "37"
            },
            {
                "Direction": "Northbound",
                "RouteID": "38"
            },
            {
                "Direction": "Southbound",
                "RouteID": "38"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "40"
            },
            {
                "Direction": "Westbound",
                "RouteID": "40"
            },
            {
                "Direction": "Northbound",
                "RouteID": "42"
            },
            {
                "Direction": "Southbound",
                "RouteID": "42"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "46"
            },
            {
                "Direction": "Westbound",
                "RouteID": "46"
            },
            {
                "Direction": "Northbound",
                "RouteID": "48"
            },
            {
                "Direction": "Southbound",
                "RouteID": "48"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "51"
            },
            {
                "Direction": "Westbound",
                "RouteID": "51"
            },
            {
                "Direction": "Northbound",
                "RouteID": "52"
            },
            {
                "Direction": "Southbound",
                "RouteID": "52"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "54"
            },
            {
                "Direction": "Westbound",
                "RouteID": "54"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "56"
            },
            {
                "Direction": "Westbound",
                "RouteID": "56"
            },
            {
                "Direction": "Northbound",
                "RouteID": "57"
            },
            {
                "Direction": "Southbound",
                "RouteID": "57"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "62"
            },
            {
                "Direction": "Westbound",
                "RouteID": "62"
            },
            {
                "Direction": "Northbound",
                "RouteID": "70"
            },
            {
                "Direction": "Southbound",
                "RouteID": "70"
            },
            {
                "Direction": "Northbound",
                "RouteID": "71"
            },
            {
                "Direction": "Southbound",
                "RouteID": "71"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "72"
            },
            {
                "Direction": "Westbound",
                "RouteID": "72"
            },
            {
                "Direction": "Northbound",
                "RouteID": "73"
            },
            {
                "Direction": "Southbound",
                "RouteID": "73"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "75"
            },
            {
                "Direction": "Westbound",
                "RouteID": "75"
            },
            {
                "Direction": "Northbound",
                "RouteID": "77"
            },
            {
                "Direction": "Southbound",
                "RouteID": "77"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "79"
            },
            {
                "Direction": "Westbound",
                "RouteID": "79"
            },
            {
                "Direction": "Northbound",
                "RouteID": "87"
            },
            {
                "Direction": "Southbound",
                "RouteID": "87"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "88"
            },
            {
                "Direction": "Westbound",
                "RouteID": "88"
            },
            {
                "Direction": "Northbound",
                "RouteID": "93"
            },
            {
                "Direction": "Southbound",
                "RouteID": "93"
            },
            {
                "Direction": "Northbound",
                "RouteID": "95"
            },
            {
                "Direction": "Southbound",
                "RouteID": "95"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "99"
            },
            {
                "Direction": "Westbound",
                "RouteID": "99"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "101"
            },
            {
                "Direction": "Westbound",
                "RouteID": "101"
            },
            {
                "Direction": "Northbound",
                "RouteID": "102"
            },
            {
                "Direction": "Southbound",
                "RouteID": "102"
            },
            {
                "Direction": "Northbound",
                "RouteID": "103"
            },
            {
                "Direction": "Southbound",
                "RouteID": "103"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "104"
            },
            {
                "Direction": "Westbound",
                "RouteID": "104"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "105"
            },
            {
                "Direction": "Westbound",
                "RouteID": "105"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "107"
            },
            {
                "Direction": "Westbound",
                "RouteID": "107"
            },
            {
                "Direction": "Northbound",
                "RouteID": "108"
            },
            {
                "Direction": "Southbound",
                "RouteID": "108"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "110"
            },
            {
                "Direction": "Westbound",
                "RouteID": "110"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "112"
            },
            {
                "Direction": "Westbound",
                "RouteID": "112"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "113"
            },
            {
                "Direction": "Westbound",
                "RouteID": "113"
            },
            {
                "Direction": "Clockwise",
                "RouteID": "115"
            },
            {
                "Direction": "CntrClockwise",
                "RouteID": "117"
            },
            {
                "Direction": "Northbound",
                "RouteID": "119"
            },
            {
                "Direction": "Southbound",
                "RouteID": "119"
            },
            {
                "Direction": "Northbound",
                "RouteID": "120"
            },
            {
                "Direction": "Southbound",
                "RouteID": "120"
            },
            {
                "Direction": "Clockwise",
                "RouteID": "123"
            },
            {
                "Direction": "CntrClockwise",
                "RouteID": "123"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "132"
            },
            {
                "Direction": "Westbound",
                "RouteID": "132"
            },
            {
                "Direction": "Northbound",
                "RouteID": "133"
            },
            {
                "Direction": "Southbound",
                "RouteID": "133"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "135"
            },
            {
                "Direction": "Westbound",
                "RouteID": "135"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "136"
            },
            {
                "Direction": "Westbound",
                "RouteID": "136"
            },
            {
                "Direction": "Northbound",
                "RouteID": "137"
            },
            {
                "Direction": "Southbound",
                "RouteID": "137"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "150"
            },
            {
                "Direction": "Westbound",
                "RouteID": "150"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "183"
            },
            {
                "Direction": "Westbound",
                "RouteID": "183"
            },
            {
                "Direction": "Northbound",
                "RouteID": "195"
            },
            {
                "Direction": "Southbound",
                "RouteID": "195"
            },
            {
                "Direction": "Clockwise",
                "RouteID": "200"
            },
            {
                "Direction": "Northbound",
                "RouteID": "202"
            },
            {
                "Direction": "Southbound",
                "RouteID": "202"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "204"
            },
            {
                "Direction": "Westbound",
                "RouteID": "204"
            },
            {
                "Direction": "Clockwise",
                "RouteID": "207"
            },
            {
                "Direction": "CntrClockwise",
                "RouteID": "208"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "211"
            },
            {
                "Direction": "Westbound",
                "RouteID": "211"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "212"
            },
            {
                "Direction": "Westbound",
                "RouteID": "212"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "238"
            },
            {
                "Direction": "Westbound",
                "RouteID": "238"
            },
            {
                "Direction": "Northbound",
                "RouteID": "246"
            },
            {
                "Direction": "Southbound",
                "RouteID": "246"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "249"
            },
            {
                "Direction": "Westbound",
                "RouteID": "249"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "252"
            },
            {
                "Direction": "Westbound",
                "RouteID": "252"
            },
            {
                "Direction": "Clockwise",
                "RouteID": "254"
            },
            {
                "Direction": "Northbound",
                "RouteID": "267"
            },
            {
                "Direction": "Southbound",
                "RouteID": "267"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "272"
            },
            {
                "Direction": "Westbound",
                "RouteID": "272"
            },
            {
                "Direction": "Northbound",
                "RouteID": "277"
            },
            {
                "Direction": "Southbound",
                "RouteID": "277"
            },
            {
                "Direction": "Loop",
                "RouteID": "286"
            },
            {
                "Direction": "Northbound",
                "RouteID": "287"
            },
            {
                "Direction": "Southbound",
                "RouteID": "287"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "288"
            },
            {
                "Direction": "Westbound",
                "RouteID": "288"
            },
            {
                "Direction": "Northbound",
                "RouteID": "297"
            },
            {
                "Direction": "Southbound",
                "RouteID": "297"
            },
            {
                "Direction": "Northbound",
                "RouteID": "301"
            },
            {
                "Direction": "Southbound",
                "RouteID": "301"
            },
            {
                "Direction": "Northbound",
                "RouteID": "302"
            },
            {
                "Direction": "Southbound",
                "RouteID": "302"
            },
            {
                "Direction": "Eastbound",
                "RouteID": "338"
            },
            {
                "Direction": "Westbound",
                "RouteID": "338"
            },
            {
                "Direction": "Northbound",
                "RouteID": "344"
            },
            {
                "Direction": "Southbound",
                "RouteID": "344"
            },
            {
                "Direction": "Northbound",
                "RouteID": "500"
            },
            {
                "Direction": "Southbound",
                "RouteID": "500"
            }
        ]
    }
}
```

List bus route directions

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusRouteDirections.json](http://miami-transit-api.herokuapp.com/api/BusRouteDirections.json) 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
RouteID | 

### Response Attributes

Attribute | Description
--------- | -----------
RouteID |
Direction |

## BusRoutes

List bus routes

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusRoutes.json](http://miami-transit-api.herokuapp.com/api/BusRoutes.json)

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
RouteID | 

### Response Attributes

Attribute | Description
--------- | -----------
RouteID | 
RouteAlias | 
RouteAliasLong | 
RouteDescription | 
Bike | 
Wheelchair | 
Metrorail | 
Airport | 
SortOrder | 
RouteColor | 
￼￼￼￼￼￼￼
## BusRouteService

List bus route service

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusRouteService.json](http://miami-transit-api.herokuapp.com/api/BusRouteService.json) 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
RouteID |

### Response Attributes

Attribute | Description
--------- | -----------
RouteID | 
ServiceID | 
ServiceName  | 
ServiceOrder | 

## BusRouteShape

Latitude and longitude coordinates of a bus route shape

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusRouteShape.json?ShapeID=](http://miami-transit-api.herokuapp.com/api/BusRouteShape.json?ShapeID=) 

### Query Parameters (Required)

Parameter | Description
--------- | -----------
ShapeID | Required 

### Response Attributes

Attribute | Description
--------- | -----------
Latitude |
Longitude |

## BusRouteShapesByRoute

List of bus route shapes per route and service direction

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusRouteShapesByRoute.json?RouteID=&Dir=](http://miami-transit-api.herokuapp.com/api/BusRouteShapesByRoute.json?RouteID=&Dir=)

### Query Parameters (Required)

Parameter | Description
--------- | -----------
RouteID | Required
Dir | Required

### Response Attributes

Attribute | Description
--------- | -----------
ShapeID |

## BusRouteShapesByTrip

Returns the Bus Route ShapeID for a specific TripID

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusRouteShapesByTrip.json?TripID=](http://miami-transit-api.herokuapp.com/api/BusRouteShapesByTrip.json?TripID=)

### Query Parameters (Required)

Parameter | Description
--------- | -----------
TripID | Required

### Response Attributes

Attribute | Description
--------- | -----------
ShapeID | 

## BusRouteStops

Bus stops for a route and direction

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusRouteStops.json?RouteID=&Dir=](http://miami-transit-api.herokuapp.com/api/BusRouteStops.json?RouteID=&Dir=) 

### Query Parameters (Required)

Parameter | Description
--------- | -----------
RouteID | Required
Dir | Required

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
TripID |
Sequence |

### Response Attributes

Attribute | Description
--------- | -----------
StopID |  
StopName | 
Sequence | 
Latitude | 
Longitude | 

## BusSchedules

List the scheduled times for the specified bus stop and route. If the optional variables are provided the travel time between the two stops is listed.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusSchedules.json?RouteID=&Service=&Dir=&StopID=&StopID2=&TripID=&Sequence=](http://miami-transit-api.herokuapp.com/api/BusSchedules.json?RouteID=&Service=&Dir=&StopID=&StopID2=&TripID=&Sequence=)
￼￼￼￼￼￼￼￼
### Query Parameters (Required)

Parameter | Description
--------- | -----------
RouteID | 
Service | 
Dir | 
StopID | 
Sequence | 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
StopID2 |
TripID | 

### Response Attributes

Attribute | Description
--------- | -----------
SchedTime | 
TripID | 
Destination |

## BusStopRoutes

Listing of all routes that services the bus stop

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusStopRoutes.json?StopID=](http://miami-transit-api.herokuapp.com/api/BusStopRoutes.json?StopID=) 

### Query Parameters (Required)

Parameter | Description
--------- | -----------
StopID |

### Response Attributes

Attribute | Description
--------- | -----------
RouteID | 
RouteName | 

## BusTracker

Returns Bus Tracker times for a particular stop

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/BusTracker.json?RouteID=&Dir=&StopID=&Sequence=](http://miami-transit-api.herokuapp.com/api/BusTracker.json?RouteID=&Dir=&StopID=&Sequence=)

### Query Parameters (Required)

Parameter | Description
--------- | -----------
StopID |

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
RouteID | 
Dir | 
Sequence | 

### Response Attributes

Attribute | Description
--------- | -----------
StopName | 
RouteID | 
Direction | 
Time1 | 
Time1_Est | 
Time1_Arrival | 
Time1_Bus_ID | 
Time1_Bus_Name | 
Time1_Headsign | 
Time2 | 
Time2_Est | 
Time2_Arrival | 
Time2_Bus_ID | 
Time2_Bus_Name | 
Time2_Headsign | 
Time3 | 
Time3_Est | 
Time3_Arrival | 
Time3_Bus_ID | 
Time3_Bus_Name | 
Time3_Headsign | 

## ConnectingRoutes

Returns a listing of all connecting Routes with another Route, a Rail Station, a Mover Station, or a Bus Park and Ride Lot.
(Rail and Mover are grouped together as they share some stations.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/ConnectingRoutes.json?ID=&type=](http://miami-transit-api.herokuapp.com/api/ConnectingRoutes.json?ID=&type=)

### Query Parameters (Required)

Parameter | Description
--------- | -----------
Type | bus, rail, mover or busparkride 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
ID | route, station ID, or busparkride ID 

### Response Attributes

Attribute | Description
--------- | -----------
ConnectingID |
RouteID |
￼￼￼
## Facilities

Returns a listing of all Elevators and Escalators that are currently Out of Service in on Metrorail and Metormover stations.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/Facilities.json](http://miami-transit-api.herokuapp.com/api/Facilities.json)

### Response Attributes

Attribute | Description
--------- | -----------
ID | 
LocationID | 
LocationName | 
Description | 
Type | 
Other | 
Rail | 
Mover | 
DateUpdated | 
DownDate | 

## HurricaneCenters

Returns a listing of all Hurricane Centers

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/HurricaneCenters.json?CenterID=](http://miami-transit-api.herokuapp.com/api/HurricaneCenters.json?CenterID=) 

### Query Parameters (Required)

Parameter | Description
--------- | -----------
CenterID |

### Response Attributes

Attribute | Description
--------- | -----------
CenterID | 
CenterName | 
Address | 
City | 
State | 
Zip | 
Zone | 
Latitude | 
Longitude | 

## HurricaneEvacuationPoints

Returns a listing of all Hurricane Evacuation Bus Pickup Locations.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/HurricaneEvacuationPoints.json?EvacID=](http://miami-transit-api.herokuapp.com/api/HurricaneEvacuationPoints.json?EvacID=) 

### Query Parameters (Required)

Parameter | Description
--------- | -----------
EvacID |

### Response Attributes

Attribute | Description
--------- | -----------
EvacID | 
EvacName | 
Address | 
City | 
State | 
Zip | 
Zone | 
Latitude | 
Longitude | 

## MoverMapShape

Listing of Metromover Map Shape Latitude and Longitude coordinates

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/MoverMapShape.json?LoopID=](http://miami-transit-api.herokuapp.com/api/MoverMapShape.json?LoopID=) 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
LoopID | 

### Response Attributes

Attribute | Description
--------- | -----------
LoopID | 
OrderNum | 
Latitude | 
Longitude | 

## MoverMapShapeLoops

Returns the different Metromover Shape LoopIDs.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/MoverMapShapeLoops.json](http://miami-transit-api.herokuapp.com/api/MoverMapShapeLoops.json)

### Response Attributes

Attribute | Description
--------- | -----------
LoopID | 

## MoverStations

Returns a listing of Metromover Stations

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/MoverStations.json](http://miami-transit-api.herokuapp.com/api/MoverStations.json) 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
StationID |

### Response Attributes

Attribute | Description
--------- | -----------
StationID | 
StationIDshow | 
Station | 
Address | 
City | 
State | 
Zip | 
ConnectingOther | 
PlacesOfInterest | 
Other | 
Latitude | 
Longitude | 
svLatitude | 
svLongitude | 
svHeading | 

## MoverTracker

Returns Mover Tracker times for each station.  If the ServiceTypeID is 1 then it is an out of service train.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/MoverTracker.json](http://miami-transit-api.herokuapp.com/api/MoverTracker.json) 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
StationID |

### Response Attributes

Attribute | Description
--------- | -----------
StationID | 
StationName | 
firstLoopID | 
firstLoopName | 
firstDirection￼￼￼￼ | 
firstTime1 | 
firstTime1_Est | 
firstTime1_Arrival | 
firstTime1_Train | 
firstTime1_ServiceTypeID | 
firstTime2 | 
firstTime2_Est | 
firstTime2_Arrival | 
firstTime2_Train | 
firstTime2_ServiceTypeID | 
secondLoopID | 
secondLoopName | 
secondDirection | 
secondTime1 | 
secondTime1_Est | 
secondTime1_Arrival | 
secondTime1_Train | 
secondTime1_ServiceTypeID | 
secondTime2 | 
secondTime2_Est | 
secondTime2_Arrival | 
secondTime2_Train | 
secondTime2_ServiceTypeID | 
thirdLoopID | 
thirdLoopName | 
thirdDirection | 
thirdTime1 | 
thirdTime1_Est | 
thirdTime1_Arrival | 
thirdTime1_Train | 
thirdTime1_ServiceTypeID | 
thirdTime2 | 
thirdTime2_Est | 
thirdTime2_Arrival | 
thirdTime2_Train | 
thirdTime2_ServiceTypeID | 
forthLoopID | 
forthLoopName | 
forthDirection | 
forthTime1 | 
forthTime1_Est | 
forthTime1_Arrival | 
forthTime1_Train | 
forthTime1_ServiceTypeID | 
forthTime2 | 
forthTime2_Est | 
forthTime2_Arrival | 
forthTime2_Train | 
forthTime2_ServiceTypeID | 

## MoverTrains

Returns listing of all active Metromover trains.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/MoverTrains.json](http://miami-transit-api.herokuapp.com/api/MoverTrains.json)

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
TrainID |

### Response Attributes

Attribute | Description
--------- | -----------
TrainID | 
Cars | 
Latitude | 
Longitude | 
Direction | 
ServiceDirection | 
Service | 
LoopID | 
LoopName | 
LocationUpdated |

## Nearby

Returns listing of nearest stops and or station to a specific Latitude and Longitude.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/Nearby.json?Lat=&Long=](http://miami-transit-api.herokuapp.com/api/Nearby.json?Lat=&Long=)

### Query Parameters (Required)

Parameter | Description
--------- | -----------
Lat | Required
Long | Required

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
Type | Bus, Mover, or Rail
 
### Response Attributes

Attribute | Description
--------- | -----------
NearbyID | 
NearbyName | 
NearbyType | 
Address | 
Address2 | 
Descr | 
Distance | 
Latitude | 
Longitude | 

## PointsOfInterest

Returns a list of Points of interest around Miami‐Dade County that are accessible via Transit.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/PointsOfInterest.json](http://miami-transit-api.herokuapp.com/api/PointsOfInterest.json) 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
PointID |
CategoryID |

### Response Attributes

Attribute | Description
--------- | -----------
PointID | 
CategoryID | 
CategoryName | 
PointName | 
Address | 
State | 
Zip | 
Latitude | 
Longitude | 
svLatitude | 
svLongitude | 
svHeading | 

## PointsOfInterestCategories

Returns a list of Points of interest Categories.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/PointsOfInterestCategories.json](http://miami-transit-api.herokuapp.com/api/PointsOfInterestCategories.json)

### Response Attributes

Attribute | Description
--------- | -----------
CategoryID | 
CategoryName | 
OrderNum |
￼￼￼￼￼￼
## PointsOfInterestTransit

Returns listing of modes of transportation available from this Point of Interest.

`GET` [http://miami-transit-api.herokuapp.com/api/PointsOfInterestTransit.json?PointID=](http://miami-transit-api.herokuapp.com/api/PointsOfInterestTransit.json?PointID=) 

### Query Parameters (Required)

Parameter | Description
--------- | -----------
PointID |

### Response Attributes

Attribute | Description
--------- | -----------
TransitID | 
TransitName | 
TransitMode | 

## RiderAlerts

Returns a listing of all currently active Rider Alerts

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/RiderAlerts.json](http://miami-transit-api.herokuapp.com/api/RiderAlerts.json)

### Response Attributes

Attribute | Description
--------- | -----------
MessageID | 
Message | 
MessageStamp | 
TypeID | 
Type | 

## SalesOutlets

Returns a listing of all Sales Outlets where Easy Cards can be bought/reloaded. If SalesParking is a 1 then this location has the ability to buy monthly parking.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/SalesOutlets.json](http://miami-transit-api.herokuapp.com/api/SalesOutlets.json)

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
OutletID |

### Response Attributes

Attribute | Description
--------- | -----------
OutletID | 
OutletName | 
Address | 
State | 
Zip | 
Location | 
SalesParking | 
Longitude | 
Longitude | 

## ServiceUpdates

Listing of all current Service Updates in our system.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/ServiceUpdates.json](http://miami-transit-api.herokuapp.com/api/ServiceUpdates.json)

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
ServiceUpdateID | 
Type | Bus, Mover, or Rail

### Response Attributes

Attribute | Description
--------- | -----------
ServiceUpdateID | 
InEffect | 
ServiceUpdateType | 
ServiceUpdateTypeID | 
Title | 
ServiceUpdate | 

## TrainMapShape

Listing of Metrorail Map Shape Latitude and Longitude coordinates

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/TrainMapShape.json](http://miami-transit-api.herokuapp.com/api/TrainMapShape.json)  

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
LineID |

### Response Attributes

Attribute | Description
--------- | -----------
LineID | 
OrderNum | 
Latitude | 
Longitude | 

## TrainMapShapeLines

Returns the different Metrorail Shape LineIDs.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/TrainMapShapeLines.json](http://miami-transit-api.herokuapp.com/api/TrainMapShapeLines.json)

### Response Attributes

Attribute | Description
--------- | -----------
LineID |

## Trains

```shell
$ curl http://miami-transit-api.herokuapp.com/api/Trains.json
```

> Response: HTTP/1.1 200 OK

```json
{
    "RecordSet": {
        "Record": [
            {
                "Cars": "123-124-167-168",
                "Direction": "SW",
                "Latitude": "25.688998",
                "LineID": "ORG",
                "LocationUpdated": "11:17:14 AM",
                "Longitude": "-80.308852",
                "Service": "Southbound",
                "ServiceDirection": "SB",
                "TrainID": "251"
            },
            {
                "Cars": "219-220-215-216-169-170",
                "Direction": "E",
                "Latitude": "25.845286",
                "LineID": "GRN",
                "LocationUpdated": "11:17:24 AM",
                "Longitude": "-80.264088",
                "Service": "Southbound",
                "ServiceDirection": "SB",
                "TrainID": "256"
            },
            {
                "Cars": "199-200-221-222",
                "Direction": "N",
                "Latitude": "25.789862",
                "LineID": "ORG",
                "LocationUpdated": "11:16:56 AM",
                "Longitude": "-80.214988",
                "Service": "Northbound",
                "ServiceDirection": "NB",
                "TrainID": "262"
            },
            {
                "Cars": "139-140-227-228",
                "Direction": "S",
                "Latitude": "25.797868",
                "LineID": "ORG",
                "LocationUpdated": "11:16:30 AM",
                "Longitude": "-80.2587",
                "Service": "Northbound",
                "ServiceDirection": "NB",
                "TrainID": "263"
            },
            {
                "Cars": "201-202-107-108",
                "Direction": "S",
                "Latitude": "25.789475",
                "LineID": "GRN",
                "LocationUpdated": "11:17:09 AM",
                "Longitude": "-80.215015",
                "Service": "Southbound",
                "ServiceDirection": "SB",
                "TrainID": "265"
            },
            {
                "Cars": "109-110-177-178",
                "Direction": "NE",
                "Latitude": "25.732909",
                "LineID": "ORG",
                "LocationUpdated": "11:17:24 AM",
                "Longitude": "-80.254556",
                "Service": "Northbound",
                "ServiceDirection": "NB",
                "TrainID": "266"
            },
            {
                "Cars": "193-194-179-180",
                "Direction": "E",
                "Latitude": "25.812667",
                "LineID": "ORG",
                "LocationUpdated": "11:17:24 AM",
                "Longitude": "-80.241029",
                "Service": "Southbound",
                "ServiceDirection": "SB",
                "TrainID": "267"
            },
            {
                "Cars": "121-122-103-104",
                "Direction": "N",
                "Latitude": "25.763994",
                "LineID": "GRN",
                "LocationUpdated": "11:17:04 AM",
                "Longitude": "-80.195311",
                "Service": "Northbound",
                "ServiceDirection": "NB",
                "TrainID": "268"
            },
            {
                "Cars": "233-234-151-152",
                "Direction": "W",
                "Latitude": "25.839756",
                "LineID": "GRN",
                "LocationUpdated": "11:17:19 AM",
                "Longitude": "-80.304249",
                "Service": "Northbound",
                "ServiceDirection": "NB",
                "TrainID": "272"
            },
            {
                "Cars": "115-116-231-232",
                "Direction": "W",
                "Latitude": "25.812513",
                "LineID": "GRN",
                "LocationUpdated": "11:17:25 AM",
                "Longitude": "-80.22672",
                "Service": "Northbound",
                "ServiceDirection": "NB",
                "TrainID": "274"
            },
            {
                "Cars": "127-126-153-154-175-176",
                "Direction": "SW",
                "Latitude": "25.684969",
                "LineID": "GRN",
                "LocationUpdated": "11:16:16 AM",
                "Longitude": "-80.313806",
                "Service": "Southbound",
                "ServiceDirection": "SB",
                "TrainID": "275"
            },
            {
                "Cars": "111-112-149-150",
                "Direction": "S",
                "Latitude": null,
                "LineID": "ORG",
                "LocationUpdated": "11:15:06 AM",
                "Longitude": null,
                "Service": "Southbound",
                "ServiceDirection": null,
                "TrainID": "279"
            },
            {
                "Cars": "187-188-161-162",
                "Direction": "S",
                "Latitude": "25.763525",
                "LineID": "ORG",
                "LocationUpdated": "11:16:59 AM",
                "Longitude": "-80.19541",
                "Service": "Southbound",
                "ServiceDirection": "SB",
                "TrainID": "284"
            },
            {
                "Cars": "145-146-223-224",
                "Direction": "SW",
                "Latitude": "25.718203",
                "LineID": "GRN",
                "LocationUpdated": "11:17:30 AM",
                "Longitude": "-80.272768",
                "Service": "Southbound",
                "ServiceDirection": "SB",
                "TrainID": "285"
            }
        ]
    }
}
```

Returns listing of all active Metrorail trains.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/Trains.json](http://miami-transit-api.herokuapp.com/api/Trains.json) 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
TrainID | 

### Response Attributes

Attribute | Description
--------- | -----------
TrainID | 
LineID | 
Cars | 
Latitude | 
Longitude | 
Direction | 
ServiceDirection | 
Service | 
LocationUpdated | 

## TrainSchedules

Lists all the scheduled times for the specified station. If the optional variables are provided the travel time between the two stations is listed.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/TrainSchedules.json?StationID=&StationID2=&Dir=&Service=&TripID=](http://miami-transit-api.herokuapp.com/api/TrainSchedules.json?StationID=&StationID2=&Dir=&Service=&TripID=) 

### Query Parameters (Required)

Parameter | Description
--------- | -----------
StationID |
Dir | northbound or southbound

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
Service | Today, Weekday, Saturday or Sunday. If blank defaults to Today.
StationID2 |  
TripID |

### Response Attributes

Attribute | Description
--------- | -----------
SchedTime | 
TripID | 
Destination | 

## TrainStations

```shell
$ curl http://miami-transit-api.herokuapp.com/api/TrainStations.json
```

> Response: HTTP/1.1 200 OK

```json
{
    "RecordSet": {
        "Record": [
            {
                "Address": "3501 NW 12 Avenue",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.808705",
                "LongTermParking": "0",
                "Longitude": "-80.215403",
                "NB_OrderNum": "14",
                "Other": null,
                "Parking": "Parking spaces available for transit users: 69.  \n",
                "PlacesOfInterest": null,
                "SB_OrderNum": "10",
                "State": "FL",
                "Station": "Allapattah",
                "StationID": "ALP",
                "StationIDshow": "ALP",
                "TriRail": "0",
                "Zip": "33127",
                "svHeading": "68",
                "svLatitude": "25.80849",
                "svLongitude": "-80.215728"
            },
            {
                "Address": "801 SW First Avenue",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": "Metromover",
                "Latitude": "25.763735",
                "LongTermParking": "0",
                "Longitude": "-80.195469",
                "NB_OrderNum": "08",
                "Other": null,
                "Parking": "No parking available \n",
                "PlacesOfInterest": "Brickell business district, Financial centers",
                "SB_OrderNum": "16",
                "State": "FL",
                "Station": "Brickell",
                "StationID": "BLK",
                "StationIDshow": "BKL",
                "TriRail": "0",
                "Zip": "33130",
                "svHeading": "218",
                "svLatitude": "25.764556",
                "svLongitude": "-80.195242"
            },
            {
                "Address": "5200 NW 27 Avenue",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.822028",
                "LongTermParking": "0",
                "Longitude": "-80.240729",
                "NB_OrderNum": "17",
                "Other": null,
                "Parking": "Park and Ride has 100 parking spaces available on the ground floor. \n",
                "PlacesOfInterest": "Joseph Caleb Community Center (NW 22 Ave), Family Health Center (NW 22 Ave), Brownsville Renaissance (Laundromat, retail shops)",
                "SB_OrderNum": "07",
                "State": "FL",
                "Station": "Brownsville",
                "StationID": "BVL",
                "StationIDshow": "BVL",
                "TriRail": "0",
                "Zip": "33142",
                "svHeading": "355",
                "svLatitude": "25.821705",
                "svLongitude": "-80.240793"
            },
            {
                "Address": "1501 NW 12 Avenue",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.789686",
                "LongTermParking": "0",
                "Longitude": "-80.215124",
                "NB_OrderNum": "12",
                "Other": null,
                "Parking": "No parking available\n",
                "PlacesOfInterest": "Jackson Memorial Hospital, Bascom Palmer Eye Institute, Veterans Hospital, Miami-Dade County Jail, Miami-Dade Justice Building/Courts, Florida State Building, Cedars Medical Center, Miami-Dade County Health Department, University of Miami Hospitals and Clinics",
                "SB_OrderNum": "12",
                "State": "FL",
                "Station": "Civic Center",
                "StationID": "CVC",
                "StationIDshow": "CVC",
                "TriRail": "0",
                "Zip": "33136",
                "svHeading": "187",
                "svLatitude": "25.790086",
                "svLongitude": "-80.214936"
            },
            {
                "Address": "2780 SW 27 Avenue",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.739809",
                "LongTermParking": "0",
                "Longitude": "-80.238819",
                "NB_OrderNum": "06",
                "Other": null,
                "Parking": "Parking spaces available for transit users: 204. Disabled spaces: 5 \n",
                "PlacesOfInterest": "Cocowalk, Streets of Mayfair, Dinner Key Auditorium, Miami City Hall",
                "SB_OrderNum": "18",
                "State": "FL",
                "Station": "Coconut Grove",
                "StationID": "CGV",
                "StationIDshow": "CGV",
                "TriRail": "0",
                "Zip": "33133",
                "svHeading": "322",
                "svLatitude": "25.739613",
                "svLongitude": "-80.238551"
            },
            {
                "Address": "701 NW 11 Street",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.784551",
                "LongTermParking": "0",
                "Longitude": "-80.207646",
                "NB_OrderNum": "11",
                "Other": null,
                "Parking": "120 spaces. 20 next to the station and 100 south of the station (across the street)",
                "PlacesOfInterest": "Overtown, NW 7 Avenue",
                "SB_OrderNum": "13",
                "State": "FL",
                "Station": "Culmer",
                "StationID": "CUL",
                "StationIDshow": "CUL",
                "TriRail": "0",
                "Zip": "33136",
                "svHeading": "2",
                "svLatitude": "25.784167",
                "svLongitude": "-80.207633"
            },
            {
                "Address": "8300 South Dixie Highway",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.69199",
                "LongTermParking": "0",
                "Longitude": "-80.305102",
                "NB_OrderNum": "02",
                "Other": null,
                "Parking": "Total parking spaces available to transit users: 1,963. Disabled spaces: 69\n",
                "PlacesOfInterest": "Dadeland Station (Bed Bath & Beyond, Best Buy, Michaels, Sports Authority, Target), Dadeland Mall",
                "SB_OrderNum": "22",
                "State": "FL",
                "Station": "Dadeland North",
                "StationID": "DLN",
                "StationIDshow": "DLN",
                "TriRail": "0",
                "Zip": "33143",
                "svHeading": "285",
                "svLatitude": "25.692216",
                "svLongitude": "-80.304181"
            },
            {
                "Address": "9150 Dadeland Boulevard ",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.685244",
                "LongTermParking": "0",
                "Longitude": "-80.313352",
                "NB_OrderNum": "01",
                "Other": null,
                "Parking": "Spaces available to transit users: 1,254 spaces. Disabled spaces: 20 \n",
                "PlacesOfInterest": "South Miami-Dade Busway",
                "SB_OrderNum": "23",
                "State": "FL",
                "Station": "Dadeland South",
                "StationID": "DLS",
                "StationIDshow": "DLS",
                "TriRail": "0",
                "Zip": "33156",
                "svHeading": "295",
                "svLatitude": "25.685106",
                "svLongitude": "-80.312951"
            },
            {
                "Address": "111 Ruiz Avenue",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": "Coral Gables Trolley",
                "Latitude": "25.732773",
                "LongTermParking": "0",
                "Longitude": "-80.254778",
                "NB_OrderNum": "05",
                "Other": null,
                "Parking": "Surface parking: 226 spaces \n",
                "PlacesOfInterest": "Coconut Grove",
                "SB_OrderNum": "19",
                "State": "FL",
                "Station": "Douglas Road",
                "StationID": "DRD",
                "StationIDshow": "DRD",
                "TriRail": "0",
                "Zip": "33133",
                "svHeading": "167",
                "svLatitude": "25.733129",
                "svLongitude": "-80.254852"
            },
            {
                "Address": "6205 NW 27 Avenue",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.83241",
                "LongTermParking": "0",
                "Longitude": "-80.241212",
                "NB_OrderNum": "18",
                "Other": null,
                "Parking": "Parking spaces available to transit users: 63. Disabled: 2\n",
                "PlacesOfInterest": null,
                "SB_OrderNum": "06",
                "State": "FL",
                "Station": "Dr. Martin Luther King, Jr. Plaza",
                "StationID": "MLK",
                "StationIDshow": "MLK",
                "TriRail": "0",
                "Zip": "33147",
                "svHeading": "185",
                "svLatitude": "25.832684",
                "svLongitude": "-80.241108"
            },
            {
                "Address": "2100 NW 41 Street",
                "Airport": "1",
                "City": "Miami",
                "ConnectingOther": "Green Line / Orange Line",
                "Latitude": "25.812453",
                "LongTermParking": "1",
                "Longitude": "-80.229909",
                "NB_OrderNum": "15",
                "Other": null,
                "Parking": "Parking spaces available for transit users: 350. Disabled spaces: 2 \n",
                "PlacesOfInterest": null,
                "SB_OrderNum": "09",
                "State": "FL",
                "Station": "Earlington Heights",
                "StationID": "EHT",
                "StationIDshow": "EHT",
                "TriRail": "0",
                "Zip": "33142",
                "svHeading": "333",
                "svLatitude": "25.812272",
                "svLongitude": "-80.229374"
            },
            {
                "Address": "101 NW First Street",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": "Metromover",
                "Latitude": "25.776025",
                "LongTermParking": "0",
                "Longitude": "-80.196118",
                "NB_OrderNum": "09",
                "Other": null,
                "Parking": "Privately-owned parking available to the public \n",
                "PlacesOfInterest": "Miami Art Museum, Historical Museum of Southern Florida, Miami-Dade Library System, Main Library, Stephen P. Clark Government Center, Miami-Dade County Courthouses, Federal Courthouse Square, Dade County Bar Association, Miami Parking Authority  and Miami Dade County Parking System, Downtown Bus Terminal, School Board Building (Exit Metrorail at Government Center Station; take Metromover to School Board Station via the Omni leg on the outer loop.)",
                "SB_OrderNum": "15",
                "State": "FL",
                "Station": "Government Center",
                "StationID": "GVT",
                "StationIDshow": "GVT",
                "TriRail": "0",
                "Zip": "33128",
                "svHeading": "278",
                "svLatitude": "25.77602",
                "svLongitude": "-80.195214"
            },
            {
                "Address": "125 East 21 Street",
                "Airport": "0",
                "City": "Hialeah",
                "ConnectingOther": null,
                "Latitude": "25.841149",
                "LongTermParking": "0",
                "Longitude": "-80.278977",
                "NB_OrderNum": "21",
                "Other": null,
                "Parking": "Parking spaces available for transit users: 238. Disabled spaces: 9\n",
                "PlacesOfInterest": "Hialeah Park and Race Track, Hialeah Hospital (six blocks east on E. 24 Street)",
                "SB_OrderNum": "03",
                "State": "FL",
                "Station": "Hialeah",
                "StationID": "HIA",
                "StationIDshow": "HIA",
                "TriRail": "0",
                "Zip": "33010",
                "svHeading": "356",
                "svLatitude": "25.840924",
                "svLongitude": "-80.279017"
            },
            {
                "Address": "100 NW 6 Street",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.780986",
                "LongTermParking": "0",
                "Longitude": "-80.196306",
                "NB_OrderNum": "10",
                "Other": null,
                "Parking": "Privately owned parking available to the public\n",
                "PlacesOfInterest": "Ninth Street Pedestrian Mall, Overtown's Historical Lyric Theatre",
                "SB_OrderNum": "14",
                "State": "FL",
                "Station": "Historic Overtown/Lyric Theatre",
                "StationID": "OVT",
                "StationIDshow": "OVT",
                "TriRail": "0",
                "Zip": "33136",
                "svHeading": "217",
                "svLatitude": "25.781799",
                "svLongitude": "-80.196154"
            },
            {
                "Address": "3800 NW 25th St",
                "Airport": "1",
                "City": "Miami",
                "ConnectingOther": "Airport",
                "Latitude": "25.797805",
                "LongTermParking": "0",
                "Longitude": "-80.258625",
                "NB_OrderNum": "16",
                "Other": null,
                "Parking": "No Parking Available. Please note that the TVMs at this station allow passengers to load $2.65(one way) and $5.30(round trip) on an EASY Ticket for those wishing to travel on the Miami Beach Airport Flyer - Route 150\n",
                "PlacesOfInterest": "Miami International Airport",
                "SB_OrderNum": "08",
                "State": "FL",
                "Station": "Miami International Airport",
                "StationID": "MIA",
                "StationIDshow": "MIA",
                "TriRail": "0",
                "Zip": "33142",
                "svHeading": "236",
                "svLatitude": "25.79889",
                "svLongitude": "-80.258197"
            },
            {
                "Address": "3150 NW 79 Street",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.845784",
                "LongTermParking": "0",
                "Longitude": "-80.248861",
                "NB_OrderNum": "19",
                "Other": null,
                "Parking": "Parking spaces available to transit users: 291. Disabled spaces: 5\n",
                "PlacesOfInterest": "Northside Shopping Plaza, USA Flea Market, People's National Bank",
                "SB_OrderNum": "05",
                "State": "FL",
                "Station": "Northside",
                "StationID": "NSD",
                "StationIDshow": "NSD",
                "TriRail": "0",
                "Zip": "33147",
                "svHeading": "132",
                "svLatitude": "25.845708",
                "svLongitude": "-80.249065"
            },
            {
                "Address": "2005 West Okeechobee Road",
                "Airport": "0",
                "City": "Hialeah",
                "ConnectingOther": null,
                "Latitude": "25.839807",
                "LongTermParking": "1",
                "Longitude": "-80.301561",
                "NB_OrderNum": "22",
                "Other": null,
                "Parking": "Parking spaces available: 1,180 Disabled spaces: 27 \n",
                "PlacesOfInterest": "Hialeah Warehouse/Factory District, Okeechobee Road, City of Miami Springs, Town of Medley",
                "SB_OrderNum": "02",
                "State": "FL",
                "Station": "Okeechobee",
                "StationID": "OKE",
                "StationIDshow": "OKE",
                "TriRail": "0",
                "Zip": "33010",
                "svHeading": "352",
                "svLatitude": "25.83892",
                "svLongitude": "-80.301192"
            },
            {
                "Address": "7701 NW 79 Avenue",
                "Airport": "0",
                "City": "Medley",
                "ConnectingOther": null,
                "Latitude": "25.84337",
                "LongTermParking": "0",
                "Longitude": "-80.323845",
                "NB_OrderNum": "23",
                "Other": null,
                "Parking": "Parking spaces available for transit users: 700. Disabled spaces: 20 \n",
                "PlacesOfInterest": "Animal Services Shelter/Adoption Center, Town of Medley",
                "SB_OrderNum": "01",
                "State": "FL",
                "Station": "Palmetto",
                "StationID": "PAL",
                "StationIDshow": "PAL",
                "TriRail": "0",
                "Zip": "33166",
                "svHeading": "255",
                "svLatitude": "25.843803",
                "svLongitude": "-80.322634"
            },
            {
                "Address": "2050 NW 12 Avenue",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.795747",
                "LongTermParking": "0",
                "Longitude": "-80.215114",
                "NB_OrderNum": "13",
                "Other": null,
                "Parking": "Parking at the Santa Clara Metrorail station is available on the ground level in the parking garage of the 17-story apartment building, \"Santa Clara Apartments II.\" Transit users can access the 61 spaces reserved for transit customers by entering via NW 13 Ave. between NW 20 and 21 streets. Disabled spaces: 4\n",
                "PlacesOfInterest": "Miami-Dade Community College Medical Center Campus, Lindsey Hopkins Technical Education Center",
                "SB_OrderNum": "11",
                "State": "FL",
                "Station": "Santa Clara",
                "StationID": "SCL",
                "StationIDshow": "SCL",
                "TriRail": "0",
                "Zip": "33142",
                "svHeading": "173",
                "svLatitude": "25.796029",
                "svLongitude": "-80.215248"
            },
            {
                "Address": "5949 Sunset Drive",
                "Airport": "0",
                "City": "South Miami",
                "ConnectingOther": null,
                "Latitude": "25.705075",
                "LongTermParking": "1",
                "Longitude": "-80.289014",
                "NB_OrderNum": "03",
                "Other": null,
                "Parking": "Total parking spaces available for transit users: 1,774. Disabled spaces: 28 \n",
                "PlacesOfInterest": "South Miami Hospital, Shops at Sunset Place",
                "SB_OrderNum": "21",
                "State": "FL",
                "Station": "South Miami",
                "StationID": "SMI",
                "StationIDshow": "SMI",
                "TriRail": "0",
                "Zip": "33143",
                "svHeading": "82",
                "svLatitude": "25.704536",
                "svLongitude": "-80.289261"
            },
            {
                "Address": "1125 E. 25 Street",
                "Airport": "0",
                "City": "Hialeah",
                "ConnectingOther": "Tri-Rail",
                "Latitude": "25.845446",
                "LongTermParking": "0",
                "Longitude": "-80.259687",
                "NB_OrderNum": "20",
                "Other": "The Address also known as 1125 NW 79 Street 1125 E. 25 Street, Hialeah, FL 33013 (This station is located between East 11 Ave and NW 37 Ave in Hialeah)",
                "Parking": "Parking spaces available to transit users: 42. Disabled spaces: 2\n",
                "PlacesOfInterest": "Amtrak Train Station (NW 37 Avenue), North to Broward/Palm Beach counties, South to Miami International Airport, Hialeah Hospital (five blocks west)",
                "SB_OrderNum": "05",
                "State": "FL",
                "Station": "Tri-Rail",
                "StationID": "TRI",
                "StationIDshow": "TRI",
                "TriRail": "1",
                "Zip": "33013",
                "svHeading": "123",
                "svLatitude": "25.84568",
                "svLongitude": "-80.260109"
            },
            {
                "Address": "5400 Ponce de Leon",
                "Airport": "0",
                "City": "Coral Gables",
                "ConnectingOther": null,
                "Latitude": "25.714849",
                "LongTermParking": "0",
                "Longitude": "-80.27689",
                "NB_OrderNum": "04",
                "Other": null,
                "Parking": "Parking spaces available for transit users: 230. Disabled spaces: 7\n",
                "PlacesOfInterest": "University of Miami, Lowe Art Museum, Gusman Hall, Doctors Hospital",
                "SB_OrderNum": "20",
                "State": "FL",
                "Station": "University",
                "StationID": "UNV",
                "StationIDshow": "UNV",
                "TriRail": "0",
                "Zip": "33146",
                "svHeading": "281",
                "svLatitude": "25.714983",
                "svLongitude": "-80.276439"
            },
            {
                "Address": "3201 SW First Avenue",
                "Airport": "0",
                "City": "Miami",
                "ConnectingOther": null,
                "Latitude": "25.749705",
                "LongTermParking": "0",
                "Longitude": "-80.211825",
                "NB_OrderNum": "07",
                "Other": null,
                "Parking": "Parking spaces available for transit users: 120. Disabled spaces: 5\n",
                "PlacesOfInterest": "Miami Museum of Science, Space Transit Planetarium, Vizcaya Museum and Gardens, Mercy Hospital",
                "SB_OrderNum": "17",
                "State": "FL",
                "Station": "Vizcaya",
                "StationID": "VIZ",
                "StationIDshow": "VIZ",
                "TriRail": "0",
                "Zip": "33129",
                "svHeading": "152",
                "svLatitude": "25.749967",
                "svLongitude": "-80.211989"
            }
        ]
    }
}

```

Listing of all Metrorail Stations.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/TrainStations.json](http://miami-transit-api.herokuapp.com/api/TrainStations.json) 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
StationID |

### Response Attributes

Attribute | Description
--------- | -----------
StationID | 
StationIDshow | 
Station | 
SB_OrderNum | 
NB_OrderNum | 
Address | 
City | 
State | 
Zip | 
Parking | 
ConnectingOther | 
PlacesOfInterest | 
Other | 
Airport | 
TriRail | 
LongTermParking | 
Latitude | 
Longitude | 
svLatitude | 
svLongitude | 
svHeading | 
￼￼￼￼￼
## TrainTracker

Returns Mover Tracker times for each station.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/TrainTracker.json](http://miami-transit-api.herokuapp.com/api/TrainTracker.json) 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
StationID |

### Response Attributes

Attribute | Description
--------- | -----------
StationName | 
StationID | 
NB_Time1 | 
NB_Time1_Est | 
NB_Time1_Arrival | 
NB_Time1_Train | 
NB_Time1_LineID | 
NB_Time2 | 
NB_Time2_Est | 
NB_Time2_Arrival | 
NB_Time2_Train | 
NB_Time2_LineID | 
NB_Time3 | 
NB_Time3_Est | 
NB_Time3_Arrival | 
NB_Time3_Train | 
NB_Time3_LineID | 
SB_Time1 | 
SB_Time1_Est | 
SB_Time1_Arrival | 
SB_Time1_Train | 
SB_Time1_LineID | 
SB_Time2 | 
SB_Time2_Est | 
SB_Time2_Arrival | 
SB_Time2_Train | 
SB_Time2_LineID | 
SB_Time3 | 
SB_Time3_Est | 
SB_Time3_Arrival | 
SB_Time3_Train | 
SB_Time3_LineID | 
￼￼￼
## Updated

Returns a listing of when static listings have been updated.

### HTTP Request

`GET` [http://miami-transit-api.herokuapp.com/api/Updated.json](http://miami-transit-api.herokuapp.com/api/Updated.json) 

### Query Parameters (Optional)

Parameter | Description
--------- | -----------
UpdateType | 

### Response Attributes

Attribute | Description
--------- | -----------
UpdateType | 
DateUpdated | 

# City of Miami

Trolley Service.  Coming soon.