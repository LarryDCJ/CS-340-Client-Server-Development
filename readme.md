Grazioso Salvare Rescue Training
Turning The Rescued to Rescuers!
About
This application was commissioned by Grazioso Salvare, a company focused on turning rescued pups into rescue pups. The software we’ve created in collaboration with them allows them to leverage data provided from animal shelters in proximity to Austin, TX to find viable candidates for their program leveraging the Dash package to provide a usable front-end with data organization, additional statistical insights, and a map to help locate these animals.

Specifically, this application provides CRUD capabilities with MongoDB with data provided by local shelters.

It it primarily written in Python and currently in active development. We opted to use MongoDB, a document-based database. We understood data may be derived from many independent entities with (potentially) little uniformity. MongoDB allows us to store data without a schema, instead using  as unstructured documents. This provides the use of aggregation and pipelines to build the data view we desire. 



















Getting Started
Tools
Mongo Shell
The “mongod_ctl start” command starts the local mongo server with authorization based on prior configuration. Developers can use either remote or local servers depending on their use case.
/usr/local/bin/mongod_ctl start



Following starting the server, the next step allows a registered user to login and perform operations consistent with their current permissions.

mongo --authenticationDatabase "AAC" -u "aacuser" -p


"mongo" - This command starts the authentication process for a server that's been properly configured. If no permissions have been set, this command logs the user in without the need for additional flags.

"--authenticationDatabase" - This flag specifies the database the user will initially authenticate with with "AAC" being the database in this example.

"-u" - This command specifies the user to authenticate as.

"-p" - This command prompts the user for a password, preventing the need to enter it in plaintext.


Example






Python 3.8
	* A consistent Python version ensures any dependencies are compatible regardless of the system we use to run this software.

PyMongo
	* PyMongo serves as the connection between our Python code and the Mongodb server.

Configuration

Import the csv containing the Animal Shelter data from shelters serving Houston, Texas.



Create the “admin” user account




Ensure the user was created successfully by loggin in as “admin” to confirm the password.



Create the “aacuser” account


View the aacuser account to verify creation.
Note: You cannot verify the password with this method. Log in as the user to verifiy the password.






Usage Examples
This example shows the “aacuser” connecting with the database driver, creating new documents, reading the database, updating a document with new information as well as deleting a document from the collection.

















The example below shows the completed application with a front-end for users to interact with the data, making data searching as easy as clicking the type of rescue role you are looking to fill! 

A user can select up to 5 rows to display on the map, dropping a pin for each selected animal.
You can further divide the animals up based on the recommended breed/rescue type via the radio buttons above the chart.



Roadmap

* Implementing update and delete capability - DONE!
* Checking to avoid duplicate entries 
* Ability to interact with non-secure databases
Known Issues

There are no KNOWN issues, but feel free to report any you run in to!

Read The Docs!
https://pymongo.readthedocs.io/en/stable/

Contact
Larry D. Cawley Jr.
larry.cawley@snhu.edu

