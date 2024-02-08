0x00. AirBnB clone - The console

##Project description
The project is based on the console using command interpreters.
Data is stored in json files and accesses using the json module.

##Command interpreter description
it has a limited number of accepted commands that work specifically for the purpose of the AirBnB website.
Some of the commands are; show, create, update, destroy, count.

##How to start it
Installation - by cloning the repo on your user interface.
After successfully cloning the repo, cd into AirBnB_clone and create the several files containing the code neded for specific tasks.
/console.py - main executable file, command interpreter
models/engine/file_storage.py - class that serializes instances to json files and deserializes json files to instances
models/__init__.py - unique filestorage instance
models/base_model.y - defines all common methodes for other classes
models/user.py - user class that inherits from BaseModel
models/state.py - state class that inherits from BaseModel
models/city.py - city class that inherits from BaseModel
models/amenity.py - amenity class that inherits from BaseModel
models/place.py - place class that inherits from BaseModel
models/review.py - review class that inherits from BaseModel

##How to use it
It can be used in both the interactive and non-interactive mode.
1) Interactive mode
A prompt will appear whereby the user will have to type in a command and after it is processed the prompt will appear again and the user will have to type in another command, and this goes on.
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$

2) Non-interactive mode
The command will have to be piped in so that it runs as soon as the shell is run. No prompt will appear and no input is required from the user.
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$

If a command is successful, it will run, but if it isn't an error message will pop up, to exit the user will have to exit using **CTRL + D** or **CTRL + C** or the commands **quit** or **EOF**

##Commands and their use
**quit** or **EOF** - exits program
**usage** - by itself
**help** - provide description on how to use command
**create** - creates a new instance of a valid class, saves it to the json file, and prints the ID.
Valid classes are; BaseModel, User, State, City, Amenity, Place, Review.
**show** - prints string representation of an instance based on the class name and 'id'
**destroy** - deletes instance based on class name and 'id'
**all** - prints all string representations of all instances on the class name
**update** - updates instance based on the class name and 'id' by adding or updating attribute
**count** - retrieves numb er of instances in a class
