# Behavioral Ideas
This section will discuss potential ways a certain feature should act. We should pick the best ways for a feature to act, and we can only do this if we can list all the possible ways to implement a behavior. Afterwards, we can pick the best way or create a new method from many alternatives. It's important to record these ideas since no developer can remember everything about a project, and without this knowledge in the forefront of your mind can destroy the way the program behaves. 

## Pulling
Pulling is where we are trying to get the mob to fight us, and we can use multiple approaches to do this: 

| Strategy | Description |
|----------|-------------|
| Always pull mobs | Use a move on every mob that we have as a target and is not fighting. |
| Pull when mob exceeds distance threshold | Use a move only when a mob is beyond a certain number of yalms. |
| Pull when recasts a low | Use a move when our pulling wait time is low. |

Of course, we could always use any combination of strategies. One where we'll only pull when a mob exceeds a certain distance and we'll only have to wait a minimum of two seconds for the next pull attempt. 

## Buffing
Buffing is used to buff the player before battles so that they are prepared to fight. Buffing moves do not target mobs and are only used on the player. 

| Strategy | Description |
|----------|-------------|
| Buff only before battles | only use buffs when we're just about to fight. | 
| Keep buffs on the whole time | Maintain buffs even before a battle. | 
| Maintain high duration buffs | Maintain buffs that last a long time like seigan. | 
| Buff before buffs with low durations | Only use buffs with a low duration before battles. | 

Once again, we can combine these strategies. Ideally we would want to keep buffs on the whole time minimizing time spent casting before engaging. Seigan (duration=5m, recast=1m) can be kept up full time, but Third Eye (duration=30s, recast=1m) should be cast just before. 

Now, if Seigan wears off during battle and we only use buffs before battle, the effectiveness of Seigan will be lowered. Maybe we should have one list of buffs to maintain at all time and one to use before battles. 

## Healing
How can we most effectively cure?
| Strategy | Description |
| Heal target when hp low | Use cure when a player's health is below a certain percent |