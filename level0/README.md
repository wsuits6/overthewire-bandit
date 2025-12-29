
===============================================================
The Goal of this level is to connect to the badit SSH server 
for the first time using the password and username provided 
===============================================================

domain
bandit.labs.overthewire.org,
Ip
51.21.210.216


# WHAT I DID
-------------

Since I nned the ip Adress of the server before i canuse ssh tool oninux to onnect to the servier I wll ping the server soo i get ICMP echo response with the Ip addres in it 

Now after getting the ip address of the server I need to connect to the server usingthe normal SSH method 
Since i am giving the credentials 

on my first try to log in I get to relaiase that overthewire sepcified the port to connect to on SSH which is PORT 2220 not the defalt SSH port 22
### syntaxt
ssh username@target_ip

TO specify whch port to conenct using ssh  I usethe -p argument

ssh -p username@target_ip

After logging in succesfully I will now try to find some files might probabilily fins soem files witht he flag in it  

listed out all the file susing the command 
ls -la

found reade file whoch reminds me of MR ROBOT 

I READ the contnents of the file using the cat comand 
cat readme

and found a flag in it 
FLAG : ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If


## credentials
--------------

username : bandit0 
password : bandit0
 
