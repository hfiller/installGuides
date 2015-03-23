#Installation Guide - Environment Variables
***
This is an installation guide for Hack Western Students. These installations were tested the weekend before and are therefore very likely to be stable at the time of hacking. We hope you enjoy the event! If you have any trouble, please do not hesitate to [ask for help](http://mentors.hackwestern.com).

## Windows
This [link](http://www.computerhope.com/issues/ch000549.htm) is great.

To view your current path variable use this command
	
	echo %PATH%

## Linux/Mac
To add things to your path, you can modify 1 of 2 files. Either modify ~/.bash_profile (to add path only for that user) or modify /etc/profile. In either case, open the file
```
nano ~/.bash_profile
```
or
```
nano /etc/profile
```
Then go to the end of that file, there you want to add your new included path to the end. You can do this using:
```
PATH=$PATH:/path/to/script
export PATH
```
Once this is done, run the file you just modified using either **source** or **.**
```
source ~/.bash_profile
. /etc/profile
```
