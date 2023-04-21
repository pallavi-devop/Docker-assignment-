# Docker-assignment-
<h1>Steps To Install Nginx On Docker Container</h1>

<b>Step 1 :</b>

Create Docker Environment On Operating System, i used Ubantu hear 

Requirements Check:
- Check Kernel version
	$ uname -a Or -r

NOTE: Kernel can also be upgraded.

- Check OS name:
	$ lsb_release -a / -cs
	$ cat /etc/os-release	


Installation Steps:
===========	==========	
# Update apt-get cache
	$ sudo apt-get update

# Install docker dependencies
	$ sudo apt-get install apt-transport-https ca-certificates curl software-properties-common

# Add GPG key to apt repository
	$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

# Setup Stable repository:
	$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
	
# Update apt package index:
	$ sudo apt-get update
	
# Install Latest version of Docker
	$ sudo apt-get install docker-ce

#Installation Check
sudo docker --version

<b>Step 2</b>

Create Dockerhub account, use this link
<link>https://hub.docker.com</link>

Create github account 

<link>https://github.com</link

<b>step 3</b>
<h3> this is we will perform in terminal </h3>
Create Repository in GitHub and clone it on ubantu envirement by using this cmd 

$git clone repourl

enter into repository 

$cd directory-name

<b>step 4</b>

create DockerFile 

$vim Dockerfile 

On This DockerFile Write this 

<div>
# Pull the minimal Ubuntu image
FROM nginx

# update lib
RUN apt-get update && apt-get upgrade -y

# Copy the Nginx config
COPY index.html /usr/share/nginx/html

# Run the Nginx server
ENTRYPOINT service nginx start && bash

</div>

<h5>after this customise your nginx default page with your customised page 
by editing in the index.html file </h5>

<div>

<html>
<h1>Hello Welcome To Nginx world</h1>
 </body> 
</html>

~    <div>                                                                           
~        
