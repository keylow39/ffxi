# Feature Ideas
This is a list of feature ideas that may be incorporated into the program. 

## Player Detection
* The program should either pause when a player is nearby or run its waypoint path to escape the player. If the program runs the waypoint path but reaches the end and a player is still nearby then pause the program. 

* If the program is allowed to run without pause on player detection it should target mobs that are far away from opposing players. 

## Combat Enhancements
* When a you cannot see the target message appears and then player is close to a monster have the player back up a small distance. 

## Travel Enhancements
* When traveling to a mob from the waypoint path find the two closest points to that mob. Generate a list of points between the two closest points and pick the one that is closest from that list. Go to this point and then travel to the mob. This will reduce the program from becoming stuck on environmental objects a little (same method could be applied to moving from a mob to the waypoint path). 

* If we could find a way to determine when the program is stuck on an object we could map areas which areas are traversal or not. We could first make a view that display x, z coordinates and then have the program try to decide when its stuck or not. Having a debugging aid like that will enable us to figure out the variables needed to determine when the bot is stuck. 