# Hamburg-gtfs

Visualizing the trace of a user who travels from different stations in Hamburg City using GTFS data In Neo4j.


# Queries

`` 
CALL spatial.bbox('spatialGeometry',{lon:9.946658,lat:53.561669}, {lon:10.072805, lat:53.584786}) 
``

`` 
CALL spatial.closest('spatialGeometry',{lon:9.946658,lat:53.561669}, 0.001) Yield node
return count(node) 
``

`` 
WITH "POLYGON((9.946658 53.561669, 9.956658 53.57, 9.976658 53.57, 9.976658 53.59,9.946658 53.561669))" as polygon
CALL spatial.intersects('spatialGeometry',polygon) YIELD node RETURN node.name as name 
``


# Javascript

Used Mapbox and leaflet js for visualization purposes