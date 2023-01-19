# Maps
<strong>Files Worked On: abstractions.py, recommend.py, utils.py</strong>

<strong>Description:</strong> Maps is a python program that creates a visualization of restaurant ratings using machine learning and a Yelp academic dataset. In this visualization, the city of Berkeley is segmented into regions, where each region is shaded by the predicted rating of the closest restaurant (yellow is 5 stars, blue is 1 star). The visualization being constructed is a <a href="https://en.wikipedia.org/wiki/Voronoi_diagram">Voronoi diagram</a> such as the example below. In the map below, each dot represents a restaurant. The color of the dot is determined by the restaurant's location. For example, downtown restaurants are colored green. The user that generated this map has a strong preference for Southside restaurants, and so the southern regions are colored yellow. They appear to dislike Northside restaurants which is why those regions are more blue. The program will create visualizations based on known ratings of restaurants provided to it and it will try to predict what rating a user will give a restaurant for those without ratings. The prediction is done using a simple least-squares linear regression.

<img src="https://inst.eecs.berkeley.edu/~cs61a/fa18/proj/maps/visualize/voronoi.png" alt="A sample Voronoi diagram">

<strong>How to run the program:</strong>
<ol>
  <li>You can create a visualization for one of the preconstructed users in the <strong>users</strong> directory. You can use the command below and replace "test_user" with a user of your choice.
    <ul>
      <li><strong>python3 recommend.py -u test_user -k 2 -p</strong></li>
    </ul>
  </li>
  
  <li>You can also create a visualization for your own Berkeley restaurant ratings. In the <strong>users</strong> directory, you'll see a few <strong>.dat</strong> files. Copy one of them and rename the new file to <strong>yourname.dat</strong> (for example, <strong>john.dat</strong>). In the new file (e.g. <strong>john.dat</strong>), you'll see something like the following:
  
  <strong>make_user(<br>
  &emsp;'John Doe', &emsp;&emsp;# name<br>
  &emsp;[           &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;# reviews<br>
  &emsp;&emsp;&emsp;make_review('Jasmine Thai', 4.0),<br>
  &emsp;&emsp;&emsp;...<br>
    &emsp;]</strong>
    
  Replace the second line with your name (as a string). Then, replace the existing reviews with reviews of your own. You can get a list of Berkeley restaurants with     the following command:
    <ul>
      <li><strong>python3 recommend.py -r</strong></li>
    </ul>
    
After rating a couple of your favorite or least favorite restaurants, use the following command to predict ratings for you:
    <ul>
      <li><strong>python3 recommend.py -u test_user -k 2 -p</strong></li>
    </ul>
    
Replace "test_user" with your name. You can play around with the number of clusters (the -k option) used in the k-means algorithm.
  </li>
</ol>
