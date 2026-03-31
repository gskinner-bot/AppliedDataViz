# AppliedDataViz
Excessive Drinking Among Rural Counties and Risk Areas

The interactive Folium map was created by integrating multiple datasets: facility information filtered for specific services (such as BIA, CBT, MI), geographic data for Michigan counties from a shapefile, excessive drinking rates, and community resilience data (3+ risk factors).

To build the map, I performed the following steps:

Data Loading and Preparation: Loaded facility data, county geographic boundaries, and additional metrics for excessive drinking and social risk factors.

Standardization and Merging: Standardized county names across all datasets to enable accurate merging of facility counts, drinking rates, and social risk factors with their respective geographic areas.

Rural Classification: Defined rural and non-rural counties, including specific user-driven classifications for ambiguous counties.

Need Score Calculation: A composite 'need score' was calculated for each county by normalizing and combining excessive drinking rates and social risk factors, then subtracting normalized facility counts. This score identifies areas with the highest strategic investment need.

Folium Visualization: Used the Folium library to render an interactive map with several layers:
A choropleth layer showing the excessive drinking rate in rural counties.
Circle markers indicating the count and location of filtered facilities, with larger circles representing more facilities.
A non-rural overlay with hatching to visually distinguish non-rural areas.
Special warning icons (exclamation-triangle) highlighting 'High-Need' counties, defined as those in the top 15th percentile of the calculated 'need score'.
