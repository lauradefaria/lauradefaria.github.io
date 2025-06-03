<a href='https://github.com/shivamkapasia0' target="_blank"><img alt='Python' src='https://img.shields.io/badge/Python-100000?style=for-the-badge&logo=Python&logoColor=white&labelColor=3776AB&color=3776AB'/></a>

# Heat Map with Geotag Photos in João Pessoa
This project aims to identify the most visited places in João Pessoa using the Flickr platform to collect geotagged photos. These photos serve as the data source to generate a heat map highlighting the most frequented areas, and to segment it, allowing for more detailed analysis of regions of interest.

## Data Collection
Data Collection
The Flickr API provides access to data and functionalities from the Flickr platform. One of the most useful methods is flickr.photos.search, which allows for searching photos based on specific criteria.

```
- Timeframe: April 1, 2002 – April 1, 2024 

- Location: The area of interest is centered on the Mata do Buraquinho (João Pessoa), using a search radius of 8 km to cover a significant portion of the city.
```

## Identification

A 40-day temporal criterion was established based on the photo capture date.

```
- Tourist: If a user does not post new photos within the same region during the next 40 days.

- Resident: If a user continues to contribute photos in the region after this period.
```

## Vizualization
A blank map is created, centered on João Pessoa, to serve as the base for plotting data points. The photo data collected is organized into a DataFrame, allowing for efficient handling and iteration. Each photo is then plotted as a point on the map, with its color indicating the user type either a resident or a tourist. 

## Heat Map
A separate lists of geographic coordinates are generated for tourists and residents. Using the HeatMap() function, these coordinates are transformed into a heat map that visually represents the density of photos across different locations, highlighting hotspots of activity.

## Clustering
 The latitude and longitude coordinates of the photos are normalized to prepare the data for K-Means clustering. The K-Means algorithm then groups the data into five distinct clusters based on spatial proximity. A radius parameter is applied to smooth the density of points on the map, making the visualization more coherent. These density layers are added to the existing map, and for each cluster, a separate heat map is created

## Segmantation
Finally, the image is divided into distinct parts or regions based on color to separate tagged users from the rest of the image. This segmentation facilitates further analysis or the extraction of specific information. Following the initial segmentation, groupings and region growing algorithms are applied to refine and enhance the delineation of the marked regions.

---   
## Author

|<a href="https://www.linkedin.com/in/lauradefaria/" target="_blank">**Laura de Faria Maranhão Ayres**</a> |
|:-----------------------------------------------------------------------------------------:|
|                   <img src="https://avatars.githubusercontent.com/u/45434515?v=4" width="100px"> </img>                            |           
|               <a href="http://github.com/lauradefaria" target="_blank">`github.com/lauradefaria`</a>      | 


## Clone

- Clone this repo to your local machine using
    > https://github.com/lauradefaria/HeatMap_GeoTag.git

---
## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**