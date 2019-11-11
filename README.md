# World_Wide_Weather_pdouglass

# Weather_Database write-up

## Notes
After performing an API from the Open Weather site, we created a dateframe that provided ~575 worldwide cities with various weather attributes and current characteristics. For cities with no current (<3  hr) precipitation events, those cities were assigned 0" of rain/snow.

## Insights
From the Weather pull, zero cities had experienced snow in the previous 3 hours. For future datapulls, it's unlikley this would occur again. 
By using the .loc method and an "or" operator, we were able to determine that 64 of the cities had experienced rain or snow in the previous 3 hours. A newly created Hotel field is created to be populated with available lodging (if any) within 5000 meters of the longitude-latitude of city center. If no lodging is available, that city is futher removed from the available travel cities. 

# Vacation Search Summary

## Notes
After incorporating the dataset from the Weather_Database the user provides weather, rain and snow preferences to determine a filtered travel cities. 
Map and markers are provided for global destination cities. 


# Vacation Itinerary Summary

## Notes
Potential global destinations with available lodging is used from the Vacation Search output. A coordinate tuple was created to pair the longitude-latitude coordinates and assigned to newly created dataframe column. 
Filtering cities for a travel itinerary was performed by establishing longitude-latitude boudaries and assigning to a new dataframe. Reindexing dataframe allowed for ease in retrieving coordinate tuples for travel stops. Directions_layer performs the routing between cities. 


## Other considerations
For the Travel Itinerary section I was not able to find a way to display both the itinerary and lodging markers on the same map, hence the dual display. Additionally, the marker' info box is not displayed on the downloaded screenshot. 
