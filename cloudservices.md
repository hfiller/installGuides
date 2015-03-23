#Installation Guide - Cloud Services
***
This is an installation guide for Hack Western Students. These installations were tested the weekend before and are therefore very likely to be stable at the time of hacking. We hope you enjoy the event! If you have any trouble, please do not hesitate to [ask for help](http://mentors.hackwestern.com).
##Cloud Services
There are basically two cloud services that are being offered freely for the weekend to programmers: they are [Digital Ocean](#do) and [Microsoft Azure](#az). Both offer free credit to anyone participating in the hackathon, so feel free to make use of them. Alternatively, you can use heroku, which is always free, but I would recommend the previous 2 options.
####Which One's Better?
Both are great services, so their merits will come down to your application. If you are new to servers, and are looking for a quick way to spin up a ready made server, then Digital Ocean is for you. Digital Ocean has pre-installed frameworks and gives you an IP to access your server. However, if you want more options in terms of processors and distributions, or just don't have a credit card, Azure is great for high-performance, specific-purpose servers. Finally, if you really are having trouble deciding; why not both?
###<a name="do"></a>Digital Ocean
>*Did you know?* Hack Western runs on Digital Ocean.

To use this, go to digital ocean's [website](https://www.digitalocean.com/), then create an account. After creating an account, you will be able to use the codes to get credit by visiting the [payment page](https://cloud.digitalocean.com/user_payment_profiles). Once you've done that,you can create a [droplet](https://cloud.digitalocean.com/droplets/new). Name it (this can be anything), select your size ($10 is typically fine), select region, and select additional settings.None are really worth mentioning, but please, do select IPv6. Now, it's time to select an image. While the distribution doesn't really matter (just pick your favorite flavor, we recommend Ubuntu), the Application (which is the stack) is quite important. The most common stacks are: RoR (Ruby on rails build, creates a ready-to-go server), Wordpress (you're better than that!), LAMP( Linux, Apache, MySQL, PHP/Python), LEMP (same as LAMP, except uses Nginx (I know I know...)), and MEAN (Mongo, Express, Angular, Node). If you have any questions about the stacks, and which one is best, please do not hesitate to contact a mentor. This is an important decision.

Finally add an SSH key, trust me it's faster than a password.([how to make an ssh key](https://help.github.com/articles/generating-ssh-keys/)). However, if you should ever decide you want a password, you can get one by going to your droplet, navigating to the "Access" tab, and the second sub-tab is "Reset Root Password". This will take 5-10 minutes depending on how good you are at typing jibberish.(on first time logging in with generated password, you are required to replace it)

**NOTE**: Digital Ocean does require a credit card / Paypal, so if you are a High School student/ do now own a credit card, consider the Azure alternative.

###<a name="do"></a>Azure
>*Did you know?* Azure services are free to try and don't require a credit card.

The codes given out will have instructions prompting you to go to a specific site, and entering the redemption code. At the end of this process, you will be forwarded to the azure [manager](https://manage.windowsazure.com/), here you will see all the things you can create. These include websites, virtual machines, databases of various types and mobile services. However, for most purposes, you will be wanting to create a virtual machine. While websites do allow for web-facing web pages, if you are creating an API, an interactive website, or just need an online server use the virtual machines instead. To create a new one, click the **+**, then **COMPUTE** then **Virtual Machine** then **FROM GALLERY**. At this point, you are given the ability to choose specs for your application. Note: you are not able to pre-install a certain development stack (like, LAMP, RoR or MEAN) like in Digital Ocean, so you will have to do that on your own. If you need help with this, refer to the appropriate install links, or ask a mentor for help.
After decind upon a Distribution, you can customize the quality of your server using the Tiers and Sizes. Then create a user-name (doesn't matter, just don't forget it), and upload an SSH key.([how to make an ssh key](https://help.github.com/articles/generating-ssh-keys/)). Then create a DNS name and (optionally) install a VM agent (shelling agent).
###Accessing your Server
####Linux / mac
>open terminal

For Digital Ocean, look up the IP of your new droplet, then type

```
ssh root@<IP HERE>
```

for example:
```
ssh root@104.131.22.888
```
For Azure, use the username and DNS you specified in configuration, then type
```
ssh <username>@<dns>.cloudapp.net
```
for example:
```
ssh azureuser@testingapplication.cloudapp.net
```

Your computer will then ask you to trust the ECDSA key fingerprint. This is fine. Once that is done, you should be logged in automatically (if not, you may have forgotten to run " ssh-add ~/.ssh/id_rsa" or the ssh on the server is failing). To give the rest of the team access, add their public ssh keys to the .ssh/authorized_keys file.

####Windows
Download [PuTTY](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html) or use the vm agent provided by Azure, but PuTTY is pretty great. Using either software, connect to your server (shell over TCP using port 22). Your computer will then ask you to trust the ECDSA key fingerprint. This is fine. Once that is done, you should be logged in automatically (if not, you may have forgotten to run " ssh-add ~/.ssh/id_rsa" or the ssh on the server is failing). To give the rest of the team access, add their public ssh keys to the .ssh/authorized_keys file.

##Heroku
Install [heroku toolbelt](https://toolbelt.heroku.com/) for your respective OS.
Make an account [here](https://signup.heroku.com/www-home-top). Your free account can have up to 5 projects.
#### Im going to assume that your already have a git repository set up.
Go to your terminal or command prompot and use this command to login to your account:

	heroku login

Create a remote branch for the given application:
	
	heroku create

Add the files from your repository to the remote repository:
	
	heroku push origin master

Provides the address of the hosted service and opens it in your browser:
	
	heroku open

Heroku can be annoying to work with sometimes. I've had success in the past by simply reinitializing my git repository, but this isn't a guarantee.

