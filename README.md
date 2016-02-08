This repository is meant to hold datasets from DARTs bus schedules.

2/8/16 - First Commit - Uploaded large datasets. (DISCLAIMER - I'm not 100% sure of this)

DART_data.csv:
route_id: This is the bus route number. These are the numbers that the buses 
are colloquially referred too.
route_name: The name of the route.
trip_id: Every bus runs multiple times per day. These numbers represent that.
It is important to note that a bus "route" may include more than one trip. This
is because trips can be thought of as segments of a route. Sometimes the same
route takes alternate paths, ie. the express that takes the highway. 
This distinction is clear in the relationship of "shape_id"s to "trip_ids" 
shape_id: This is the key reference to the other dataset.  The "shape" is a set of coordinates that more granularly describes a vehicles path as it drives.
While the "trip" + "route" are concerned with the bus stops, the "shape" is
concerned with traffic patterns.  For instance, if a bus stopped at 1st & A and
2nd & B, a line between the two would cross diagonally through the city block.
The shape, in this example, may contain at least three coordinates. A point at
1st & A, a point at 2nd & A, and a point at 2nd & B.
stop_sequence: This is the order in which the bus stops are approached. This 
combined with the "trip_id" will describe the stops a bus makes.
stop_id:This field is a numeric reference to the stop. This is a relic of 
combining raw data sets.
stop_name:The literal value of the bus stop.
latitude: A measure of distance from the Equator.
longitude: A measure of distance from the Prime Meridian.
arrival_time: The time at which the bus arrives at the stop.
departure_time: The time at which the bus departs the stop.
