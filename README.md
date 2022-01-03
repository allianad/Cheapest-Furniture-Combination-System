# Cheapest-Furniture-Combination-System
Program Description:

This program has been written to serve as an application that searches through a database containing the current inventory of furniture.
It will produce a textfile that contains the ID numbers of the pieces of furniture used to construct the requested furniture at the 
cheapest price, with its corresponding total cost.

This textfile will appear in the same directory that runs the package of code. After returning the information, the database will be 
updated. Note the database must be on for the application to work.

The program will request the user for JBURL, username and password to make a connection to the database. The program will then ask for 
the order details. An example of the questions with answers is given as follows:

Enter a DBURL:
jdbc:mysql://localhost/inventory

Enter a Username:
emily

Enter a Password:
drhsl8974

Enter desired Furniture from the list (Ex. chair, desk, etc):
chair

Enter a type Furniture (Ex. mesh, task, etc):
mesh

Enter the amount:
1

To run all the listed command lines these four jar files will be needed. They are provided in the lib folder:

hamcrest-core-1.3.jar
junit-4.13.2.jar
mysql-connector-java-8.0.23.jar
system-rules-1.19.0.jar

*Note: For the unit tests to run properly, the inventory.sql should not be modified from the file we were given to work with. This is
because some tests have been written specifically to test inventory.sql in its current state.

----------------------------------------------------------------------------------------------------------------------------------------
Useful tips:

To compile the classes on a windows machine, these command lines should be ran:

javac -cp .;lib/mysql-connector-java-8.0.23.jar edu/ucalgary/ensf409/User.java edu/ucalgary/ensf409/Chair.java edu/ucalgary/ensf409/Lamp.java edu/ucalgary/ensf409/Filing.java edu/ucalgary/ensf409/Desk.java edu/ucalgary/ensf409/OrderForm.java edu/ucalgary/ensf409/Main.java
javac -cp .;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar;lib/mysql-connector-java-8.0.23.jar;lib/system-rules-1.19.0.jar edu/ucalgary/ensf409/ProjectTest.java

To run the main application this command line should be ran:

java -cp .;lib/mysql-connector-java-8.0.23.jar edu.ucalgary.ensf409.Main

To run ProjectTest.java (used to run the unit tests), first change the Username and Password in the file to the appropriate values. Then, this command line should be ran:

java -cp .;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar;lib/mysql-connector-java-8.0.23.jar;lib/system-rules-1.19.0.jar org.junit.runner.JUnitCore edu.ucalgary.ensf409.ProjectTest



If you wish to re-load the database with the orignal contents after altering information, the following line can be run in the mySQL command line:

SOURCE file/path/to/inventory.sql
