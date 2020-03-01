# Change-the-hostname-on-Debian-10
For example, to change the system hostname to example.com in Debian 10

Now you know how to view the current hostname. It is time to change it as per your needs. A hostname is nothing but a name that identifies your Debian box on a network. Typically for the server, you set it as FQDN (fully qualified domain name) such as example.com The syntax is as follows:
hostnamectl set-hostname {name-here}

For example, to change the system hostname to example.com in Debian 10, you can use the following command:
sudo hostnamectl set-hostname example.com

Next, edit the /etc/hosts file, run:
sudo nano /etc/hosts

127.0.0.1       localhost
127.0.1.1       example.com     example
192.168.233.167 example.com  www.example.com
# The following lines are desirable for IPv6 capable hosts
::1     localhost ip6-localhost ip6-loopback
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters


Verify the change

How do you know that hostname was successfully changed? You use the same command without any arguments. In other words, type the following command:
hostnamectl
