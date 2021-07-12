---
layout: post
title: "Recent Earthquakes Worldwide Past 24 Hours"
subtitle: ""
background: '/img/posts/Global_EarthQuakes/earth.jpeg'
---

## Quick Overview
This was a fun project to work on since this was one of my first interactive visualizations. 
A simple but very informative scatter plot (**Figure 1**) was the result of the code that is shown below. The plot allows you to zoom in/out and displays the magnitudes and locations for all earthquakes. Each circle represents an earthquake, varying in size and color. The larger and the closer to red, the higher the magnitude. 

The plot shows all earthquakes in the past day (at the time when this blog was written). 
*My original Scattergeo plot consisted of all recent earthquakes from the past month, but the plot file was too large. I decided to stick with the past 24 hours instead.* Please feel free to explore the scattergeo plot below! 



<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://larrys19.github.io/globalearthquakes/" height="525" width="100%"></iframe>


## General Setup
````python
import json

from plotly.graph_objs import Scattergeo, Layout
from plotly import offline
````
Make sure to import the necessary modules and packages.  Additionally, import the offline module. The offline module allows you to render the scattergeo map as a local HTML file. You can find all the necessary files for this project within the projects' [GitHub repository](https://github.com/LarryS19/globalearthquakes){:target="_blank"}.
If you are interested in exploring recent earthquake data, you can visit the official [USGS website](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php){:target="_blank"}. 

## Analyzing and Storing Data from USGS JSON File
````python
# Analyze the structure of data for the following file
filename = 'eq_data_july5.json' # JSON file path
with open(filename) as f:
    all_eq_data = json.load(f)

# Accessing the lists of earthquake data and metadata
all_eq_dicts = all_eq_data['features']
metadata = all_eq_data['metadata']

# Create lists and store magnitudes, locations and coordinates
magnitudes = [each_dic['properties']['mag'] for each_dic in all_eq_dicts]
approx_loc = [each_dic['properties']['title'] for each_dic in all_eq_dicts]
longitudes = [each_dic['geometry']['coordinates'][0] for each_dic in all_eq_dicts]
latitudes = [each_dic['geometry']['coordinates'][1] for each_dic in all_eq_dicts]
````

The JSON file comes with a lot of information. So it's necessary to understand the structure of the file to extract only what is relevant for this project. The [USGS website](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php){:target="_blank"}, does a good job explaining the structure. 
In order to work with the file, I had to import it using the JSON module. Once loaded, I created a list of all earthquakes and stored them in **all_eq_dicts**. **metadata** will also be necessary for an automated plot title, which will be used when defining **my_layout**.

The list **all_eq_dicts** is essentially a list composed of several dictionaries. Each dictionary represents an earthquake.
The code above has several for loops, each of which extracts data from each dictionary within **all_eq_dicts** (magnitudes, location of earthquake, longitude, and latitude). To keep the code simple, I used list comprehensions to extract and store data in lists in one shot. 

## Plotting Data
````python
# Prepare and format data for scatter plot
data = [{'type': 'scattergeo',
         'lon': longitudes,
         'lat': latitudes,
         'text': approx_loc,
         'marker': {
             'size': [5 * mag for mag in magnitudes],
             'color': magnitudes,
             'colorscale': 'portland',
             'colorbar':{'title': 'Magnitude'},
         },
         }]

# Plot Data
my_layout = Layout(title=f"{metadata['title']}"
                         f"\n (July 5th 2021)")
fig = {'data': data, 'layout': my_layout}
offline.plot(fig, filename='index.html')
````
Since plotly offers several ways to customize plots, one can express each feature as a key-value pair. Any keys with nested dictionaries are features in which one can further customize. In this case, the key **data['marker']** is a good example. I wanted the size and color of each circle to correspond to the magnitude. So I multiplied each magnitude by a scale factor of five to make it easier to see the size differences. Furthermore, I instructed python to relate each magnitude to a specific color in the color scale *portland*. 
Finally, I used **Layout()** to set the title and offline to render the scattergeo map!

[GitHub repository](https://github.com/LarryS19/globalearthquakes){:target="_blank"}

