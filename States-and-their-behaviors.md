# Pre-Battle
The player enters this state when there's an attackable mob in the area. 
* Start - Perform buffing actions before battle. 
* Summon - Summons trust companions. 
* Pull - Launches an attack to make the target aggressive. 

# Battle
The player enters this state when there is an aggressive, attackable mob in the area. 
* Approach - Approaches an attackable mob, optionally engaging them. 
* Battle - Launches attacks at the target during battle. 
* Weaponskill - Launches a weaponskill at the target during battle. 

# Post-Battle
The player enters this state when all mobs are defeated in the current area. 
* End - Performs actions after all enemy mobs are defeated. 

# Injured
The player enters this state when the player's health drops below a specified amount. 
* Rest - Sits down and rests to recover hp / mp
* Healing - Performs healing actions to cure statuses and recover hp / mp. (can be used in battle)

# Hunting
The player enters this state when there are no attackable mobs in the current area. 
* Travel - Walks the given route to search for new, attackable mobs. 