# Jenkins Pipelines on AWS
A Udacity project to create and run an instance on AWS, configure Jenkins, and create a pipeline to deploy a static website on S3.

## Known Issues with Jenkins install when following guide on AWS
Key from jenkins site is not properly added, thus when running `sudo apt update` it produces GPG error. Please note the PUB keys in the error.

To fix the GPG error, run the following commands;
* Start by importing the GPG keys:

`wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -`
* Add to sources list

`sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'`
* Now use this key in the command below. Replace <????> with the PUB key in your GPG error message

`sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys ????`
* Re-run update command

`sudo apt-get update`

Alternatively, try install direction [here](https://phoenixnap.com/kb/install-jenkins-ubuntu). 
