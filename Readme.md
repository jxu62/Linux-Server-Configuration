Linux Server Configuration
This is the last project of Full Stack Web Dev Nanodegree. It is a baseline installation of a Linux server and prepare it to host my web applications. I have secured my server from a number of attack vectors, install and configure a database server, and deploy the Item Catalog web applicatons onto it.

Skills Horned
A deep understanding of exactly what your web applications are doing, how they are hosted, and the interactions between multiple systems are what define you as a Full Stack Web Developer. In this project, you’ll be responsible for turning a brand-new, bare bones, Linux server into the secure and efficient web application host your applications need.

Usage Instrtcution
Ip Adress: 18.206.119.139
Alias Name: 18.206.119.139.xip.io
SSH port: 2200
URL of the hosted web app: http://18.206.119.139.xip.io/

To access the instance:
1. Copy the SSH key to a new file named grader_key and put it in ~/.ssh
2. From terminal, run sudo ssh -i ~/.ssh/grader_key -p 2200 grader@18.206.119.139
3. You will be prompted by - 

Enter passphrase for key '/Users/haomeng/.ssh/grader_key':

4. The passphrase is 'password' without quotes
5. You are in!

Walk through of the configuration and references
1. New Instance with Ubuntu Linux Server on Amazon Lightsail

2. Update and upgrade installed packages

3. Change the SSH port from 22 to 2200

4. Configure the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).

References
TechRepublic, How to install and use Uncomplicated Firewall in Ubuntu. https://www.techrepublic.com/article/how-to-install-and-use-uncomplicated-firewall-in-ubuntu/
Official Ubuntu Documentation, UFW - Uncomplicated Firewall. https://help.ubuntu.com/community/UFW

5. Use Fail2Ban to ban attackers

References
Fail2Ban Official website. http://www.fail2ban.org/wiki/index.php/Main_Page
DigitalOcean, How To Protect SSH with Fail2Ban on Ubuntu 14.04.https://www.digitalocean.com/community/tutorials/how-to-protect-ssh-with-fail2ban-on-ubuntu-14-04

6. Set up Automatically install updates

References
Ubuntu Wiki, AutomaticSecurityUpdates.https://help.ubuntu.com/community/AutomaticSecurityUpdates
Official Ubuntu Documentation, Automatic Updates.https://help.ubuntu.com/lts/serverguide/automatic-updates.html

7. Updated packages to most recent versions
This is what I got when logging in as of 10/02/2018 4:14 pm EDT
Welcome to Ubuntu 16.04.5 LTS (GNU/Linux 4.4.0-1069-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.

New release '18.04.1 LTS' available.
Run 'do-release-upgrade' to upgrade to it.


Last login: Tue Oct  2 20:01:13 2018 from 66.170.97.7

Reference
DigitalOcean, Updating Ubuntu 14.04 -- Security Updates.https://www.digitalocean.com/community/questions/updating-ubuntu-14-04-security-updates

8. Create a new user account named grader

9. Give grader the permission to sudo

10. Create an SSH key pair for grader using the ssh-keygen tool

References
Ubuntu Wiki, SSH/OpenSSH/Keys. https://help.ubuntu.com/community/SSH/OpenSSH/Keys
DigitalOcean, How To Set Up SSH Keys. https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2

11. Configure the local timezone to UTC and disable Root Login

12. Install and configure Apache to serve a Python mod_wsgi application

13. Install and configure PostgreSQL and git

Reference
DigitalOcean, How To Secure PostgreSQL on an Ubuntu VPS.https://www.digitalocean.com/community/tutorials/how-to-secure-postgresql-on-an-ubuntu-vps

14. Deploy the Item Catalog project

Resource
Flask documentation, Working with Virtual Environments http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/#working-with-virtual-environments

15. Launch the Web Application with http://18.206.119.139.xip.io/

16. Troubleshooting
 - useful log: sudo nano /var/log/apache2/error.log
 - useful command: sudo service apache2 restart

Other References:
Many help from Udacity Forum
Many help from Udacity Online Chat Help
Many help from GitHub Repositories