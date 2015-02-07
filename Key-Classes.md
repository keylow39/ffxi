# Key Classes
This page contains the role definitions used in the [EasyFarm](https://github.com/Mykezero/EasyFarm/wiki) program. There are classes for getting creature data and parsing the resource xmls. 

## Classes
| Class Name | Description | 
|------------|-------------|
| Ability | A class that represents a magic spell, weapon skill or job ability. |
| AbilityService | A class that retrieves Ability objects from the resource files generated by Windower. |
| AbilityExecutor | Provides methods that allow the player to execute Ability objects. |
| ActionBlocked | Determines whether a player can do something based on what status effects they have. |
| CombatService | Contains methods used to interactive with Unit objects around him. |
| RestingService | Provides methods for resting. |
| Unit | A class that represents an friendly or hostile creature. |
| UnitService | A class that allows you to retrieve Unit objects that are around you. |
| Serialization | A helper class that allows you to write an object to file. |
| Constants | Contains constants that are commonly used like max ranged attack distance. |

## Examples
### Creating an FFACE Session
```C#
// Get the first pol process or null
var FFProcess = Process.GetProcessByName("pol").FirstOrDefault();

// Exit out if no process is found
if(FFProcess == null) return;

// Create a new fface session.
var Session = new FFACE(FFProcess.Id);
```
### Casting the cure spell on yourself
```C#
// Creates a new ability service object to get information on 
// spells, weaponskills and job abilities.
var as = new AbilityService();

//Retrieves the information for "Cure V" from the spells resource file.
var CureV = as.CreateAbility("Cure V");

// Create a new ability executor
var ae = new AbilityExecutor(Session);

// Use the Cure V spell on the player.
ae.UseAbility(CureV);
```