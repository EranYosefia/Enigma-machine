# Enigma-machine
Enigma machine simulator implemented in Java
BREAKING THE ENIGMA - Part.1

In this exercise we created 2 modules: UI, Engine

Engine Module - includes 6 packages.

Components : Contains the machine components implementation.

class Rotor - we chose to implement the rotor class with two ArrayList<Character> one for left and the other for right, used for representing the character mapping of each rotor. Rotor class also contains notch, index of window, rotor id and a boolean variable flag if the next rotor should be advanced.

Class Rotors - used to contain the collection of rotors, used in the enigma, the collection implemented as a map where the key is integer rotor id, and the value is the rotor object itself, there are also data members of the amount of all rotors, and another to arraylist contains the chosen rotors, and rotors starting position.

Class Reflector - used for implementing the reflector component in the enigma machine, contains a map with an integer key and value for the mapping of the reflector, and also two more data members, the amount of mapping used by the reflector and roman number as the ID.

Class Reflectors- used to contain the collection of reflectors, implemented by a map with the roman number reflector Id as the key and the reflector itself as the value. contains also the roman number of the current reflector in use and the amount of total reflector available to choose from.

Class PlugBoard- used to represent the plugboard component on the machine, an array list of pair of char that contains all available plugs, and a map of character key and value, represents the chosen inuse plugs.

Class Machine- represents the machine itself, assembles and contains objects of type plugboard,rotors, reflectors, and two maps used for the initial mapping of the letters in the machine abc. also contains machine language and the number of rotors as data members.

Enigma Machine- class contains only an object instance of the machine.

exceptions - we wrote 4 classes of exceptions under this package.

generated - Package contains the auto-generated CTE classes.

resources - Package contains the XSD file and some XML files.

utils - a package contains two enum classes - Roman numbers and direction right to left or left to right.

operation package - contains two classes, Tests and operator. Test is the class handling most of the logic input and machine details validation. Operator is the class handling the connection between the UI and the Engine models by moving back and forth dto objects.

UI Module - contains two packages.

uiUtils package contains enum of the menu options.

enigmaUI package contains 3 classes.

Class Menu- class handling the menu of the enigma and his validity using boolean data members

Class ConsoleUI- class contains instances of the menu and the operator classes as data members. gets all the information the user has entered through the menu, managing, handling and checking it using the class operator instance.

