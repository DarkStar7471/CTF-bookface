****

# bookface

![alt text](https://i.imgur.com/lbYrx0Y.png)
![alt text]()

**Source:** Created by ben on TryHackMe

***Description:***
	
​	Are you able to root this machine?

***Related Hosting Links***

- TryHackMe
- 	Hosted as a subscriber only room at the time of writing.
- 	Link: https://tryhackme.com/room/bookface

***Special Notes:***

​	*Scanning this specific box is a little different from most rooms. I highly recommend coming into this room with having set up Nessus or a similar higher-end scanning tool in order to produce better overall recon. Additionally, at the time of writing, this box has a fair amount of brute-forcing. Be prepared to solve this box over the series of several hours to a few days.* 



***Instructions:*** 

- As we start most boxes, let's begin with some scanning! For this, let's use nmap.
  - ![alt text](https://i.imgur.com/pKgOHHo.jpg)
  - ![alt text](https://i.imgur.com/mypkUn4.jpg)
- Well that's odd. After allowing this scan to run to completion, I found that every port on this box is reporting as open. Within this instance, if we allow nmap to complete we can see this isn't entirely true, but nmap clearly isn't helping us in this case.
- 









***Flags:***

1. On the FTP server, specifically within the flag1 file.
2. Within the DNS txt records, listed as a txt record along with some port information.
3. UNKNOWN
4. UNKNOWN
