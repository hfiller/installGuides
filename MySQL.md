#Installation Guide - MySQL
***
This is an installation guide for Hack Western Students. These installations were tested the weekend before and are therefore very likely to be stable at the time of hacking. We hope you enjoy the event! If you have any trouble, please do not hesitate to [ask for help](http://mentors.hackwestern.com).
##Installing MySQL
Well, you don't ever really install MySQL (well, you shouldn't), but you're going to use it, and there's some configuring to be done!
##Installing MySQLWorkbench
Probably the most important tool (unless you REALLY like command line). It gives you a good overview of data, has excellent database creation and planning tools, and is an industry standard. [Download](http://dev.mysql.com/downloads/workbench/) and install the program.
Then, connect it up to your database.

If you are using an external server, there is a chance that external connections are not allowed. In that case, either see the section below, or use *Connection Method: Standard TCP/IP over SSH*.
##Allowing External Connections
We're going to modify some config files. Oh yeah, for realsies. First open terminal/PuTTY and shell into your server. The file you are looking for is called
