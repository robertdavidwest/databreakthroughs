# Creating a Wordpress blog using Amazon Linux LAMP Stack

I'm setting myself up with a wordpress.org site using an Amazon EC2 LAMP Stack and recorindg the steps I've taken along the way!

## Getting Setup:
	
### 1. Getting Started with Amazon EC2 Linux Instances

* [Amazon Full guide - EC2 Get Started ](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html)

### 2. Installing a LAMP Server on Amazon Linux

* [Amazon Full guide - Install LAMP](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/install-LAMP.html)

### 3. Associating the EC2 with an existing domain on godaddy:

* I followed [these](http://andnovar.tech/2014/05/03/pointing-godaddy-domain-aws-ec2-instance/) simple instructions.

### 4. Hosting a WordPress Blog with Amazon Linux

http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/hosting-wordpress.html 

and that's it! You should now have a working site!

## On going Access:

#### Connecting to the EC2 using ssh

* [Amazon Full guide - Accessing Instances Linux](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html)

Easy Steps I've extracted to avoild viewing the full post everytime:

1. In a command-line shell, change directories to the location of the private key file that you created when you launched the instance, e.g.
		
		cd ~/Documents/Github/databreakthroughs
		
* Use the chmod command to make sure that your private key file isn't publicly viewable. For example, if the name of your private key file is my-key-pair.pem, use the following command

    	chmod 400 databreakthroughs.pem
    
* Use the ssh command to connect to the instance. You specify the private key (.pem) file and user_name@public_dns_name. For Amazon Linux, the user name is ec2-user. If you already associated a domain with the EC2 instance then you would use that domain instead of the public_dns_name. e.g.

        ssh -i "databreakthroughs.pem" ec2-user@databreakthroughs.com
        
       
### Using Github to move between local and production development 

This guide shows how to move between a local MAMP set up to the server using Gitub. ** *I still need to check this out but it's here for safekeeping* **

* [wordpress-github](http://45royale.com/blog/wordpress-github/)

 


