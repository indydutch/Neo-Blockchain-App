# <p align="center">**<u>Neo Blockchain App</u>**</p>

### **Description:** Demo Neo Blockchain Application for Senior Design at Florida Polytechnic University. 

#### **Code Organization:** 

- Main.java: driver for the program. Contains onMessageReceived() which constantly checks for a command and creates a corresponding object then calls a function with any input parameters.

- FetchFunctions.java: a list of functions used for each command. When a command is called, any parameters are gathered and used to generate a return message to the user. Once exception is for the `!list` command which creates another object and calls a function.

- ListFunctions.java: a list of functions used for the database. As mentioned above in FetchFunctions.java, if the `!list` command is called, it will gather the passed parameters and work with the corresponding function to send a response back to the user. This file relies heavily on the second parameter.

- FindGifs.java: a separate (optional) file for using the Tenor GIFs API. This section is called if a certain substring is detected within a message string. If the specified substring is found, then a message coupled with a link gathered from the API will be sent back to the corresponding user/channel.

- IsInteger.java: a generic file used within multiple other files. When a command is called that needs to check if a string or substring is made up exclusively of integers, the function isInteger() is called using a created IsInteger object. It returns a boolean-like response to the calling section.

  

#### **Code Building:** 

- build.gradle: please ensure that your build.gradle file has all the necessary dependencies that are required by the various APIs and the database
- JDA (Discord bot API): used for running the bot on a Discord server.
- JSON (for parsing): used in each API to gather information that is queried.
- JDBC (SQLite Database): 

Before running the code, add the bot token "ODA0NzY4MTM3MzMyMzkxOTQ4.YBRIuw.QYiFCgQJdnngsWP2J7Ne6Jll1PA"  to the "Program Requirements" text box in the "Edit Configurations" for the "Main" program file. **<u>*CRITICAL*</u>**



#### **Team Contributions:**

Note: all team members worked and contributed as equally as possible with coding and researching for what we needed for this project. For formality's sake, here is a list of team members and what we are each contributing:

- Matthew Dutchess (Team Lead): Java Programming, Team Management, SQLite Database Management, QA Testing.

- Cameryn Costanzo: Java Programming, Document Organization, Research, QA Testing.

- Calvin Hariprasad: Java Programming, QA Testing, Timeline Organization.

  

#### **Imported Libraries:** 

- DV8FromTheWorld JDA: used for basic bot functions such as creating any intents and detecting any messages or users within a Discord.
- Javax.security.auth.login: for handling any login exceptions.
- JSON.org: used for parsing through a given JSON string when using an API.
- Java.net: used for creating a URL connection.
- Java.util: used for creating random variables and for scanning through string content.
- Java.sql: used for connecting to a SQLite database, creating or deleting a table, and then adding or removing items from said table.
