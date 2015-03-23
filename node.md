#Installation Guide - MEAN
***
This is an installation guide for Hack Western Students. These installations were tested the weekend before and are therefore very likely to be stable at the time of hacking. We hope you enjoy the event!
##Installing The MEAN Stack
The MEAN stack is a very popular web development platform that allows fast development using ONLY javascript, and thus is very popular at hackathons. Installing is also quite easy, just follow these steps.
##Installing Node - Linux/Mac
Perhaps the most important step here is actually installing the library. Luckily for linux/mac, this is exceedingly simple.
>open terminal

```
sudo apt-get install nodejs
```
and
```
sudo apt-get install npm
```

That's it! Now let's get into the thick of it. The first thing you want to do is create a package.json file, click [here](http://browsenpm.org/package.json) to see how those work. Create this file in your folder, then run this to create your project.
```
npm install
```
Note: node_modules folder should be git ignored, you *are* using git *right?*


Then you're ready to start! Create yourself a node file (.js) and start building!([example](http://expressjs.com/starter/hello-world.html)).

##Installing Node - Windows
[click here](http://cwbuecheler.com/web/tutorials/2013/node-express-mongo/)
(Ignore the mongo part, doing mongo locally is silly).

##Installing Mongo
The short version here is "don't", this is what [mongo-lab](https://mongolab.co)/cloud services are there for.

To get set-up with mongo lab, go to the website and create your account.


Once you're login in your will want to click on the "Create New" button.
Once you are re-directed, under that "Plan" tab select "Single-Node" and the "Sandbox" radio button (this makes the database free).
Name the database and select "Create new MongoDB Deployment".
Select the database, you'll be redirected. Select the "Users" and create a user. Do NOT select the "Make Read-only" checkbox.
Now to access your database with a URI, do something similar to this: (you MUST copy the specific URI from the top of the mongolab page)

	mongodb://userNameGoesHere:passwordGoesHere@ds031541.mongolab.com:31541/nameOfDatebase


For how to use mongo, see the link under Installing Node - Windows.


##Installing Express
```
npm install express
```
Yes really.

##Installing Angular

	<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.3.14/angular.min.js"></script>

Put this into your header tag (alongside jQuery if you want, they play nice!)