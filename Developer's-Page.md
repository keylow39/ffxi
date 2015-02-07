# Developer's Documentation
This document contains the development documentation for the Final Fantasy XI EasyFarm farmbot. It lists program dependencies, explains the program's architecture and describes how to add new behavior and views to the project. 

## Program Dependencies
The program uses these technologies from Microsoft. 
* .Net Framework 4.5
* Prism (For MVVM)
* Enterprise Library (For logging)

Additionally, the program needs these files in order to work.
* FFACE.dll (Reads memory from Final Fantasy XI game instances)
* FFACETools (A wrapper for FFACE that makes development easier)

## Key Classes
The list of the major classes and their roles can be found [here](https://github.com/EasyFarm/EasyFarm/wiki/Key-Classes). It also includes a sample of how they are used within the program. 

## How the program works
The program has a really simple design. The program now uses a component system, which is just a fancy finite state machine. What this allows us to do is to have state machines that can contain other state machines allowing deep nesting of states and more control of behavioral flow. 

User data is contained in the Config class where it can be accessed globally by all classes that depend on it. The MVVM design pattern has been implemented which controls users interactions and pushes settings into the config class to make it available for other classes. 