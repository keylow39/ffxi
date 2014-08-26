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

# Program Architecture
This program has quite a simple architecture. There are a few main pieces to the program...

* FarmingTools - Provides global access to game environment data and user settings. 