[Page in progress]

# List Descriptions
This page describes what functionality is provided by each list in the battles tab. These are the current understandings on how each list should function and perform. 

## List Types
There are two types of lists: buffing and targeted. For targeted lists, the program will make sure that the player is engaged and in distance of the mob. Buffing lists are not target oriented. Distance and other attributes related to mobs will not be checked. 

## Action Behavior
There are some common characteristics in the way moves are used. Moves will be used when they are off cooldown to increase their usage. Unless the user specifies to only recast it on wear, it will use it whenever it's available. 

## Pull List
This list is used for moves that get a mobs attention. There's no guarantee that all of the moves will be executed and its job is over once the target has become aggressive. Pulling moves will not be used on mobs that are already aggressive. By using the minimum amount of pulling moves, instead of using them all, we avoid the problem of having to melee pull the mob. 

## Start list
This buffing list is used for executing moves right before a fight. Moves like stoneskin should be put in this list since it has a high cast time and would not be ideal to cast in a fight unless necessary. 

## Battle List 
The battles list is a targeted list that is used right after the mob has been pulled or the user specified no pulling moves. You can add a combination of buffing and targeted moves into this list for use.

## End List
This list contains moves that should be used in between battles, and is a buffing list. Moves in the list will be executed when no target is found or the previous target is dead. This list may not execute after every fight since the program will find mobs close to it and reassign its target field before this list's execution. 