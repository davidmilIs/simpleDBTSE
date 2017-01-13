# Hands on with a database engine: SimpleDB 

This project is a fork (mavenized) from [SimpleDB](http://www.cs.bc.edu/~sciore/simpledb/intro.html).

## Setting up the environment

 * Import the project in Eclipse (import-> check out existing Maven project from SCM)
 * Start the server by running: simpledb.server.Startup 
 * On the console tab, deselect the icon "show console when standard output changes"
 
Execute in the following order the main files contained in src/client/java to ensure that the system is working correctly:

 * CreateStudentDB => Create the student database
 * FindMajors => Return the majors in the database 
 ## Your work
 
 In this lab, we want to analyze the structure of the code of a Database engine, identify its components and their interactions.
 
 The various components of a database system are presented in Figure 1 of [the following paper](http://db.cs.berkeley.edu/papers/fntdb07-architecture.pdf). This simple database engine does not contain all the components describe in this Figure. Please note that this paper is fundamental in this course and you may refer to it, whenever required.
 
 Your work is to identify which of them are present and which are missing. For each block, also give the name of the associated packages in the project.
 
 **How to process ?**
 
You will use the debugger to follow the path of execution of both query and updates:

For this purpose, you will start the server in debug mode, not after adding breakpoints into the following classes:
* simpledb.remote.RemoteStatementImpl  line 30 and 48
* simpledb.remote.RemoteConnectionImpl line 57
This will setup breakpoints when update, query and commit are called on the server. 

Then start one of the following class:
* Creation of the database and insertion of values, using CreateStudentDB
* Selection of entries from the Database, using FindMajors
To the follow the execution, use F5 (mostly) to dive into the calls, use F7 to return from a function (hashcode() or other Java API functions)

## Expected result

A document (doc,pdf) uploaded on mootse. Do not hesitate to produce figures whenever required.

