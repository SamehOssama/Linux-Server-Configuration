
#  Linux Server Configuration
_*by Sameh Koleid*_
## Project Description
This is the 3nd project from Udacity's fullstack nanodegree program. It consists 
of taking a baseline installation of a Linux server and prepare it to host our web applications from project 2. Wou will secure our server from a number of attack vectors, install and configure a database server, and deploy one of your existing web applications onto it.

##  Server Information
. IP address = 18.197.138.245
. Server url = http://ec2-18-197-138-245.eu-central-1.compute.amazonaws.com
. To connect: ssh grader@18.197.138.245 -p 2200 -i ~/.ssh/graderkey

## summary of software installed and configuration changes made
1.  Set up Ubuntu 18.04 server on AWS Lightsail
2. Updated and upgrade all currently installed packages
3.  Added a new user "grader" and gave him sudo permission
4.  Set up ssh-key using a local computer (From windows)
5.  Added public key to the server
6. Made sure no one can connect to root remotely
7. Changed the line in `/etc/ssh/sshd_config` From`#Port 22` To `Port 2200` (The new ssh port)
8.  Set up a firewall in the server and in the AWS Lightsail to open ports (80, 123, 2200) for (http, ntp, ssh)
9.  Configured local timezone to UTC
10.  Installed Apache2, mod_wsgi
11. Installed Git
12.  Installed PostgreSQL applications
13. Created a user to be used as role in PostgresSQL 
14. Created a database with limited access permissions
15.  Clone the project [Item-Catalog](https://github.com/SamehOssama/Item-Catalog.git) from Github
16. change the name oof the `project.py` file to `__init__.py`
17.  Installed the libraries: flask, sqlalchemy, psycopg2, google-auth, httplib2, requests
18.  Made and configure the WSGI file
19.  Changed the path of databases for each python file (`python engine = create_engine('postgresql://catalog:PW-FOR-DB@localhost/catalog')`)
20. Added the new url to developer google app credentials
21.  Executed the python file`` __init__.py ``to launch the app

## References:
. Udacity's FSND course for linux security
. [How To Deploy a Flask Application on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
. [How To Install and Use PostgreSQL on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04)
.[Flask: installing WGSI and configuring Apache](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/)

##### Notes:
some lines of code may differfrom the one in the github repository to accommodate for the database and the environment change.
