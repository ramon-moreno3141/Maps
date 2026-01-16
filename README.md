# Maps
<strong>Files Worked On: abstractions.py, recommend.py, utils.py</strong>

<strong>Description:</strong> Maps is a python program that creates a visualization of restaurant ratings using machine learning and a Yelp academic dataset. In this visualization, the city of Berkeley is segmented into regions, where each region is shaded by the predicted rating of the closest restaurant (yellow is 5 stars, blue is 1 star). The visualization being constructed is a <a href="https://en.wikipedia.org/wiki/Voronoi_diagram">Voronoi diagram</a> such as the example below. In the map below, each dot represents a restaurant. The color of the dot is determined by the restaurant's location. For example, downtown restaurants are colored green. The user that generated this map has a strong preference for Southside restaurants, and so the southern regions are colored yellow. They appear to dislike Northside restaurants which is why those regions are more blue. The program will create visualizations based on known ratings of restaurants provided to it and it will try to predict what rating a user will give a restaurant for those without ratings. The prediction is done using simple least-squares linear regression.

<img width="505" height="337" alt="voronoi" src="https://github.com/user-attachments/assets/31b629e3-313c-4b9f-864a-ebd298e82154" /><br>

<strong>How to run the program:</strong>
<ol>
  <li>You can create a visualization for one of the preconstructed users in the <strong>users</strong> directory. You can use the command below and replace "test_user" with a user of your choice.
    <ul>
      <li><strong>python3 recommend.py -u test_user -k 2 -p</strong></li>
    </ul>
  </li>
  
  <li>You can also create a visualization for your own Berkeley restaurant ratings. In the <strong>users</strong> directory, you'll see a few <strong>.dat</strong> files. Copy the contents of one of them to a new file and name it <strong>firstname_lastname.dat</strong>. For example, <strong>john_doe.dat</strong>. In the new file, you'll see something like the following:<br><br>

```python
make_user(
    'John Doe',     # name
    [               # reviews
        make_review('Gomnaru Restaurant', 2.5),
        ...
    ]
)
```

Replace the name on the second line (<strong>John Doe</strong> in the example above) with your name as a string. Then, replace the existing reviews with reviews of your own. You can get a list of Berkeley restaurants with the following command:
    <ul>
      <li><strong>python3 recommend.py -r</strong></li>
    </ul>
    
After rating a couple of your favorite or least favorite restaurants, use the following command to predict ratings for you:
    <ul>
      <li><strong>python3 recommend.py -u test_user -k 2 -p</strong></li>
    </ul>
    
Replace "test_user" with the name of the new file you created with your reviews ("firstname_lastname"). You can play around with the number of clusters (the -k option) used in the k-means algorithm.
  </li>
</ol>
