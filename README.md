# Sparta Node Sample App

## Running Vagrant

Firstly, install vagrant from:
```
https://www.vagrantup.com/downloads.html
```

Choose the right version depending on your operating system.

---------------

Secondly, install VirtualBox from:
```
https://www.virtualbox.org/wiki/Downloads
```
---------

Then, download Git bash from:
```
https://git-scm.com/downloads
```

----------

Once all of these are installed, download the Vagrant files from this repo:
```
https://github.com/chpoullet/node-sample-app/tree/master/vagrant-lab-1
```

----------

Go into vagrant-lab-1 folder and right click and open Git Bash
or cd into this directory. Once in Git Bash and in the correct directory, run these commands one line at a time:
```
vagrant plugin install vagrant-hostsupdater
vagrant up
```


Finally, run all these commands. Copy and paste each line one at a time:
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get upgrade -y
sudo apt-get install nginx -y
sudo systemctl start nginx
```


## Description

This app is intended for use with the Sparta Global Devops Stream as a sample app. You can clone the repo and use it as is but no changes will be accepted on this branch. 

To use the repo within your course you should fork it.

The app is a node app with three pages.

### Homepage

``localhost:3000``

Displays a simple homepage displaying a Sparta logo and message. This page should return a 200 response.

### Blog

``localhost:3000/posts``

This page displays a logo and 100 randomly generated blog posts. The posts are generated during the seeding step.

This page and the seeding is only accessible when a database is available and the DB_HOST environment variable has been set with it's location.

### A fibonacci number generator

``localhost:3000/fibonacci/{index}``

This page has be implemented poorly on purpose to produce a slow running function. This can be used for performance testing and crash recovery testing.

The higher the fibonacci number requested the longer the request will take. A very large number can crash or block the process.


### Hackable code

``localhost:3000/hack/{code}``

There is a commented route that opens a serious security vulnerability. This should only be enabled when looking at user security and then disabled immediately afterwards

## Usage

Clone the app

```
npm install
npm start
```

You can then access the app on port 3000 at one of the urls given above.

## Tests

There is a basic test framework available that uses the Mocha/Chai framework

```
npm test
```

The test for posts will fail ( as expected ) if the database has not been correctly setup.




