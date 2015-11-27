#Installation Guide - Arduino
***
This is an installation guide for Hack Western Students. These installations were tested the weekend before and are therefore very likely to be stable at the time of hacking. We hope you enjoy the event! If you have any trouble, please do not hesitate to [ask for help](http://mentors.hackwestern.com).

## Download 
Visit this [link](https://www.arduino.cc/en/Main/Software) to download the Arduino Software for Windows, Mac, and Linux. 

Note: Examples are built into the Arduino download. 

## Getting Started
Follow the tutorial [here](https://www.arduino.cc/en/Guide/HomePage) to get started on learning Arduino. 

## Reference
Documentation for all commands can be found [here](https://www.arduino.cc/en/Reference/HomePage).

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
