# Developer's Documentation
This page discuss what a new developer needs to know in order to improve the code. (Explain more here...)

# Program Dependencies
The program uses these technologies from Microsoft. 
* .Net Framework 4.5
* Prism (For MVVM)
* Enterprise Library (For logging)

Additionally, the program needs these files in order to work.
* FFACE.dll (Reads memory from Final Fantasy XI game instances)
* FFACETools (A wrapper for FFACE that makes development easier)

# How the program works
The program is actually very simple. The finite state machine and state classes execute the program's behavior. Any game data you need is stored globally in the App class's FarmingTools object. 

# Program Classes
* Ability - Represents a spell or ability in the game. It contains information about spell cast times, mp costs, tp costs, etc. 

## Ability Service
Provides methods for retrieving abilities from the resource files. This class can return abilities, spells or both by name. 

### Creates an ability service object.
`var abilService = new AbilityService();`

### Retrieves all abilities with the name Dia. `
`List<Ability> abilities = abilService.GetAbilitiesWithName("Dia");`

# Adding new behavior to the program. 
In order to add new behavior to the class (like healing or resting) you will need to create a new state and add it to the finite state machine. There are two steps to this process. 

1. Create a new state inheriting StateBase. 
2. In the finite state machine class, create an instance of your state and add it to the "brains" of the finite state machine.

# Adding a new view
There are three steps you need to take to add a new view.

1. Create the view.
2. Create a new view model inheriting ViewModelBase.
3. Set the view's data context to the view model in the view's code behind. 
4. In the main view's xaml file add a new tab and set it's content to that of your new view. 



