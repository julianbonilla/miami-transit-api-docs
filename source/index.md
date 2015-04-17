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
                "Direction": "Westbound",
                "RouteID": "101"
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
