# Project 1

For this project, we wanted to see the correlation between California Geography and Solar Installations. California is the national leader in solar panel installations, and understanding this correlation could help to inform the current state of the solar industry.

# Requirements to run code:

In order to run the code that we worked on, several dependencies must be installed:
1. Matplotlib
2. Pandas
3. Numpy
4. Seaborn (download here: https://jakevdp.github.io/PythonDataScienceHandbook/04.14-visualization-with-seaborn.html)
4. Gmaps (download here: https://developers.google.com/maps/documentation/)
    - In order to get the Google Maps API to run, you must:
        a. Register for an API Key
        b. Create a file called keys.py
        c. Create a variable called gkey, and input your Google Maps API key 
            (ex. gkey = "your API key")

# Where we found our data:

1. Number of Solar Installations: https://openpv.nrel.gov/search
2. Climate Zone Data: California Energy Commission. California Climate Zone Descriptions for New Buildings. July 1995.
3. Climate Zone Details: California Energy Commission. California Climate Zone Descriptions for New Buildings. July 1995.
4. Sunny Days: https://www.currentresults.com/Weather/US/average-annual-sunshine-by-city.php
5. Population data: https://factfinder.census.gov/faces/tableservices/jsf/pages/productview.xhtml?src=CF
6. Electricy Consumption by County: http://ecdms.energy.ca.gov/elecbycounty.aspx

# Jupyter notebook analysis overview

Look at "open_pv_california_2015_V2" to see the initial data cleaning.

Look at "open_pv_california_2015_V3", "open_pv_california_2015_V4", and "ClimateZonevsSize" to see the analysis and visualizations.

Look in the "Images" folder to see the graphs that we created, and that will be referenced below.

Main idea: The geography of California will have an effect on the number of solar installations in the state.

1. Hypothesis: Climate zones with the higher temperature recorded will have more installations.

2. Hypothesis: Cities in the Central Valley of California will have more solar installations.
    The idea here was that homes in the central valley are often in remote areas. These areas are often not connected to the grid. Thus, homes need another source of energy, and solar energy seems like a viable alternative. The Central Valley of California is one of the most productive agricultural regions in the world, and as such, we figured must receive enough sunlight to make solar installations cost effective, especially when paired with the fact that it is hard to connect the statewide electric grid to homes in remote regions.

    I used a combination of data from:
        - The Open PV project: a source of data for over 1 million residential and commercial solar installations across the US
        - US Census: housing units data for each county in California
    We merged the data for this using the County as the common factor
    From this, I found 3 different Climate Zones: 11, 12, and 13, which include the cities of Red Bluff, Stockton, and Fresno, had by far the highest percentage of solar installations per number of housing units (3.5 - 4%). The heatmap on the right visually shows that our hypothesis was true, since the red corresponds with the Central Valley of California.

3. Hypothesis: Climate zones with more sunny days will have a higher percentage of solar installations per number of housing units.
    Our hypothesis was that Climate Zones with more sunny days will have a higher % of solar installations. This is a more specific look at one aspect of climate zones, which is the sunny days factor, and does not take into account other effects such as access to the grid.

    I graphed sunny days vs solar installations per number of housing units, and based off this graph there does not appear to be much correlation. Two counties with some of the most sunny days actually have the lowest number of solar installations. This leads us to believe that there are other factors that affect solar installations.

4. Hypothesis: Climate zones with more sunny days will have smaller solar installations.
    We also wanted to see if the number of sunny days affected the installation size. The idea here was that the more sun an area receives, the smaller the installation size, since the solar panels will be more effective at converting solar energy into electricity in these areas. This graph again appears to disprove this hypothesis.

5. Hypothesis: Climate zones with more sunny days will have a lower cost per watt for solar installations.
    The final angle here was to see if areas with more sun had a lower installation cost per watt. Again, this was disproved by the results on this graph. There does not appear to be much correlation between these two.


# Our final presentation:

https://docs.google.com/presentation/d/12u-A6Y91gxWVugpeC02APJudTuzyL4Vv0-MEjxn-Fxs/edit?ts=5c7c2bf8#slide=id.g51bfa45bb1_0_11

