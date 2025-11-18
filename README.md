**Overview**

This project determines the orientation (North, East, South, West, etc.) of residential properties using GNAF coordinates and the road network. Orientation is a valuable factor for buyers and investors because it influences light, comfort, and energy efficiency.

**Approach**

Loaded GNAF points and road geometries into GeoPandas.

Reprojected to a metric CRS for accurate distance calculation.

Found the nearest road segment for each property.

Calculated the bearing of the road and mapped it to a compass direction.

Produced a dataset with address, latitude, longitude, and orientation.

**Output**

A CSV file with 2,000 processed properties, including orientation values.

**Findings**

104 properties were North-facing, 66 North-East, and 4 North-West. Orientation can be used directly for pricing insights, filters, or quality scoring.

**Visualization**

A bar chart showing orientation distribution is included as a screenshot.

**Limitations**

Assumes each home faces the nearest road. Corner lots or cul-de-sacs may reduce accuracy. With more time, cadastre boundary analysis would increase precision.

**Future Improvements
**
Use parcel frontage instead of the nearest road.

Add sunlight/shadow scoring.

Scale processing with spatial indexing and parallel batch processing.
