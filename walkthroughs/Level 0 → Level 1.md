# Objective

This level introduces the basics of Secure Shell (SSH), a protocol used to establish an encrypted connection to a remote machine. SSH allows users to access and interact with remote systems securely over a network.

In this challenge, the goal is to connect to the Bandit server using SSH with the provided hostname, port, username, and password.

# Approach

start an encrypted connection using #ssh by specifying the user (**<span style="color:lightgreen; font-size: 20px">bandit0</span>**) password (**<span style="color:lightgreen; font-size:20px;">bandit0</span>**) to the domain name **<span style="color:lightblue;">bandit.labs.overthewire.org</span>** with port number **<span style="color:lightblue;">2220</span>** 

# Commands Used

``` bash
	~ ssh <user_name>@<domain_name> -p <port_number>
	~ yes # you will need it in the first time you connecet to the target
	~ <type_the_password>
	~ cat <file_to_Read> #(the Readme file which containg the password for the 
						 #next level)
```

``` bash
	~ ssh bandit0@bandit.labs.overthewire.org -p 2220
	~ yes
	~ bandit0
	~ cat readme
```

# Explanation

#### ssh --> used to establish a remote connection using the ssh protocol running on port 22 by default how ever our target is running on 2220 we use the `-p` parameter to use the ssh with the new port

#### <user_name>@<domain_name> --> specifying the exact user we want to log in exactly on what device and we can use a domain name or an ip both will work with no problems

#### yes --> when we try to connect to a remote machine the first time we do it the machine will ask us if we trust to make a connection with the other device

#### \<password> --> if we chose yes then it prompt us to type a password of the user we try to connect to

#### cat <file_name> --> to read the contents of the readme file to get the password for the next level
# Key Concepts

- **SSH (Secure Shell):** An encrypted protocol used to access and manage remote machines securely over a network.
    
- **Connection Parameters:** SSH uses a username, hostname or IP address, and port number to identify the account and server to connect to. Port `22` is the default, but custom ports can be specified.
    
- **Host Verification and Authentication:** SSH may ask us to accept the server's host key on the first connection, then authenticates the user using credentials such as a password.

# lessons learned

- What is ssh and how to use it
	
- what parameters and flow we need to specify to make the connection
	
- how to chose what port we want to connect to how ever ssh run by default on port 22

# Screenshots

![level-0-to-1-part-1](../photos/level-0-to-1/level-0-to-1-part-1.png)

![Level 0 - Part 1](level-0-to-1-part-2.png)