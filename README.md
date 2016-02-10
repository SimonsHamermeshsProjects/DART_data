This repository is meant to hold datasets from DARTs bus schedules.

2/8/16 - First Commit - Uploaded large datasets. (DISCLAIMER - I'm not 100% sure of this)
2/10/15 - Made some updates the the README file.


DART_data.csv:

route_id: This is the bus route number. These are the numbers that the buses are colloquially referred too.

route_name: The name of the route.

trip_id: Every bus runs multiple times per day. These numbers represent that. It is important to note that a bus "route" may include more than one trip. This is because trips can be thought of as segments of a route. Sometimes the same route takes alternate paths, ie. the express that takes the highway. This distinction is clear in the relationship of "shape_id"s to "trip_ids" 

shape_id: This is the key reference to the other dataset.  The "shape" is a set of coordinates that more granularly describes a vehicles path as it drives. While the "trip" + "route" are concerned with the bus stops, the "shape" is concerned with traffic patterns.  For instance, if a bus stopped at 1st & A and 2nd & B, a line between the two would cross diagonally through the city block. The shape, in this example, may contain at least three coordinates. A point at 1st & A, a point at 2nd & A, and a point at 2nd & B.

stop_sequence: This is the order in which the bus stops are approached. This combined with the "trip_id" will describe the stops a bus makes.
 
stop_id: This field is a numeric reference to the stop. This is a relic of combining raw data sets.

stop_name: The literal value of the bus stop.

latitude: A measure of distance from the Equator.

longitude: A measure of distance from the Prime Meridian.

arrival_time: The time at which the bus arrives at the stop.

departure_time: The time at which the bus departs the stop.



DART_shape_22595.csv:

shape_id: the key referenced from DART_data.csv (all 22595 in this table)

shape_pt_sequence: an integer that represents the order of the stops (?)

latitude: A measure of distance from the Equator.

longitude: A measure of distance from the Prime Meridian.


DART_shape_22603.csv:

shape_id: the key referenced from DART_data.csv (all 22603 in this table)

shape_pt_sequence: an integer that represents the order of the stops (?)

latitude: A measure of distance from the Equator.

longitude: A measure of distance from the Prime Meridian.


DART_shapes.csv:

shape_id: the key referenced from DART_data.csv (this table seems to contain all of the shape_id's' and has ~150k rows)

shape_pt_sequence: an integer that represents the order of the stops (?)

latitude: A measure of distance from the Equator.

longitude: A measure of distance from the Prime Meridian.


mini_DART_data.csv:

Contains the same columns as DART_data.csv but only has 10 rows from route 1.


mini_DART_shape_22595.csv:

Same as DART_shape_22595.csv but with only 36 rows of data.     (Q: does this represent a single trip?)


mini_DART_shape_22603.csv:

Same as DART_shape_22603.csv but with only 36 rows.         (Q: does this represent a single trip?)


mini_DART_shapes.csv:

Save as DART_shapes.csv but with only 10 rows from shape_id 22591.