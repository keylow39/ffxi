[Page in progress]

# List Descriptions
This section defines what each list is suppose to do in the battle's tab. 

## List Types
There are two types of lists: buffing and targeted. For targeted lists, the program will make sure that the player is engaged and in distance of the mob. Buffing lists are not target oriented. Distance and other attributes related to mobs will not be checked. 

## Pull List
This list is used for moves that get a mobs attention. There's no guarantee that all of the moves will be executed and its job is over once the target has become aggressive. Pulling moves will not be used on mobs that are already aggressive. 

## Start list
This buffing list is used for executing moves right before a fight. 

## Battle List 
This list is used to execute moves during battle. 

## End List
This list contains moves that should be used in between battles, and is a buffing list. Moves in the list will be executed when no target is found or the previous target is dead. This list may not execute after every fight since the program will find mobs close to it and reassign its target field before this list's execution. 