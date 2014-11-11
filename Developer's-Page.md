# Developer's Documentation
This document contains the development documentation for the Final Fantasy XI EasyFarm farmbot. It lists program dependencies, explains the program's architecture and describes how to add new behavior and views to the project. 

## Program Dependencies
The program uses these technologies from Microsoft. 
* .Net Framework 4.5
* Prism (For MVVM)
* Enterprise Library (For logging)
* [XI-Tools library](https://github.com/Mykezero/XI-Tools/wiki)

Additionally, the program needs these files in order to work.
* FFACE.dll (Reads memory from Final Fantasy XI game instances)
* FFACETools (A wrapper for FFACE that makes development easier)

## How the program works
The program is actually very simple. The finite state machine and state classes execute the program's behavior. Any game data you need is stored globally in the App class's FarmingTools object. 
[Out of Date: Please update for current code. ]

## Adding new behavior to the program. 
In order to add new behavior to the class (like healing or resting) you will need to create a new state and add it to the finite state machine. There are two steps to this process. 

1.Create a new state inheriting StateBase. 
2.In the finite state machine class, create an instance of your state and add it to the "brains" of the finite state machine.

## Adding a new view
There are three steps you need to take to add a new view.

1. Create the view.
2. Create a new view model inheriting ViewModelBase.
3. Set the view's data context to the view model in the view's code behind. 
4. In the main view's xaml file add a new tab and set it's content to that of your new view. 