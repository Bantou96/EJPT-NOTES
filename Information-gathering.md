# Overview
The aim is to collect lots of but very useful informations about individual, company, website...

There are two types of information gathering : Passive & Active

info : this course requires a basic understanding of Command Line Interface using linux operating systems. So you have to be familiar with linux commands and the distribution Kali-linux. 

### What are we looking for ?

- IP adresses
- Directories
- Email and/or phone
- physical adresses
- web technologies used

# Passive information gathering
In this section we will learn about different methods that we can use to gather useful information about our target. This is the first step and it is very important because without this kind of informations we could not proceed for the penetration testing. This is called passive because we will just look for legal informations that we can find in the internet without compromising the target system. 

For all the commands enumerate here you can use **whatis** for a better understanding. 

### Gather basic informations of a specific website
This two commands give us information about ip addresses and dns information
```
host yourwebsite.org

whois yourwebsite.org
```
### informations about infrastructures
the website netcraft.com give us more information about domain names, domain ownership and the infrastructure structure

### DNS reconnaissance
This one gives us more informations about name servers and all other useful information about the dns protocol
```
dnsrecon -d yourwebsite.org
```
We can also use the website dnsdumpster.com to get all the informations developped upstream and identify subdomains. 

### Directory organization 
robot.txt file shows restricted directory in a search engine

sidemap(s).xml is a file that contains the entire directory organisation of a specific website.

We can also use **addons** like : 
- Builtwith : gives us informations about technologies used
- wappalyzer : is a web technology profiler

For comprehensive view we can use :
```
whatweb yourwebsite.org 
```
To download an entire website we can use HTTrack :
```
webhttrack yourwebsite.org
```
### Detect a web application filter 
This one is called wafdetection and we will use the following command :
```
wafw00f -a yourwebsite.org 
```
we can use the option -l to list all waf supported by the command.
