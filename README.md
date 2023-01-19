# Maps
<strong>Files Worked On: abstractions.py, recommend.py, utils.py</strong>

<strong>Description:</strong> Maps is a python program that creates a visualization of restaurant ratings using machine learning and a Yelp academic dataset. In this visualization, the city of Berkeley is segmented into regions, where each region is shaded by the predicted rating of the closest restaurant (yellow is 5 stars, blue is 1 star). The visualization being constructed is a <a href="https://en.wikipedia.org/wiki/Voronoi_diagram">Voronoi diagram</a> such as the example below. In the map below, each dot represents a restaurant. The color of the dot is determined by the restaurant's location. For example, downtown restaurants are colored green. The user that generated this map has a strong preference for Southside restaurants, and so the southern regions are colored yellow. They appear to dislike 

<img src="https://inst.eecs.berkeley.edu/~cs61a/fa18/proj/maps/visualize/voronoi.png" alt="A sample Voronoi diagram">
