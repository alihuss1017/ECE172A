# A* Swarms Algorithm

In my algorithm, I find all unexplored areas in the explore map by looking for all locations in explore_map where the value is equal to the unmapped_value, which is 0. Once a robot reaches a destination, I set the next destination to be the closest point in unexplored_areas to the current position of the robot. I find the closest point by using a Euclidean distance metric, and every time I find a distance less than the threshold, I set that threshold as that distance, and destination as the corresponding coordinate pair. 

I update my explore map by looking at every location in the route matrix as well as the destination pair through the explore_map, and check if it is unmapped. If so, I set it as planned so the robot will eventually explore it. Next, to update the position of the robot, I set curPos to the first element of route, and then pop that same element from route so the robot will eventually move. I make sure to initialize that updated position of the robot as mapped in the explore_map. Finally, I check if the updated position is the same as the destination, and if so, I make destination an empty list so I can make a new destination location. 

## - Number of Iterations
<h3>

- bots = 5: 920 iterations <br>
- bots = 10: 503 iterations <br>
- bots = 15: 376 iterations

</h3>

Video Demonstration: https://www.youtube.com/watch?v=rWbQpkYX8D0