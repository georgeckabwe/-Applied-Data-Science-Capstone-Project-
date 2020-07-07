The-Battle-of-Neighborhoods
PIZZA IN NEW YORK OR SAN FRANCISCO?
Data Science Capstone - IBM Data Science Professional Certificate on Coursera
Introduction
We all love pizza! Right? This project focuses on comparing pizza places in New York to San Francisco. Imagine your choice of which city to visit depends on which city has the best pizza. The decision is to choose a place with a high density of Pizza places as most of people love to change places where they eat pizza from until they find their best and favorite place. To solve this problem, an analysis of the Pizza stores’ locations in New York and San Francisco will be conducted to find the best place for anyone who loves changing pizza places and anyone who wants to find the best place from . 
Data section
The FourSquare API will be used to collect data about locations of Pizza stores in New York, NY and San Francisco, CA. These are two of the most populated US cities and they should contain some of the best Pizza places in the US.
Methodology
The target here is to asses which city would have the highest Pizza store density. The Four Square API through the venues channel will be utilized together with the near query to get venues in the cities. Also, the CategoryID will be used to set it to show only Pizza Places. An Example of the requests:
https://api.foursquare.com/v2/venues/explore?&client_id=&client_secret=&v=20180605&New York, NY&limit=100&categoryId=4bf58dd8d48988d1ca941735
The 4bf58dd8d48988d1ca941735 is the Id of the Pizza Place Category. Also, Foursquare limits us to maximum of 100 venues per query.
This request will be repeated for San Francisco to get its top 100 venues. The name and coordinate data will then get saved from the result and plotted on the map for visualization.
Next, to get an indicator of the density of Pizza Places, the center coordinate of the venues will be calculated to get the mean longitude and latitude values. Then the mean of the Euclidean distance from each venue to the mean coordinates will be calculated. This will be the indicator; mean distance to the mean coordinate.
