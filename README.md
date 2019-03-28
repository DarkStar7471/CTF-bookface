****

# bookface

![alt text](https://i.imgur.com/lbYrx0Y.png)
![alt text]()

**Source:** Created by ben on TryHackMe

***Description:***
	
​	Are you able to root this machine? Jerry is a new developer and has made a few mistakes!

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
- Well that's odd. After allowing this scan to run to completion, I found that every port on this box is reporting as open. Within this instance, if we allow nmap to complete we can see this isn't entirely true, but nmap clearly isn't helping us in this case. Let's go ahead and try Nessus. 
-	 ![alt text](https://imgur.com/tLDPafd)
- Nessus is a commonly used scanning tool within the field of penetration testing. Nessus is installed as a server and offers a free home version, which, for our use case is incredibly useful. For more information, check out this link: https://www.tenable.com/products/nessus-home
- Since nmap isn't giving us great results with our typical scan, we'll go ahead and run a basic network scan with Nessus. I'll be using the following settings for this scan:
- 	Scan Type: Basic Network Scan
- 	Discovery: All Ports
- 	Advanced: Scan low bandwidth links*
- 		*This is useful for our case as we are scanning over a vpn connection
- Let's go ahead and take a look at the results of this scan
- 	![alt text](https://i.imgur.com/IYtcKF3.jpg)
- Interesting, it looks like both DNS and FTP services are reporting on the target box. We'll revisit DNS later, for now let's try and brute force the FTP credentials. For this, we'll be using hydra. Additionally, we'll be using jerry as our test user since he was listed above as the developer.
- 	![alt text](https://i.imgur.com/NWEVh9O.jpg)
- 	![alt text](https://i.imgur.com/U4B82Eq.jpg)
- Success! We have our FTP password!
- 	Let's go ahead and log in:
- 	![alt text](https://i.imgur.com/I2TljWj.jpg)
- There's our first flag and a lovely note. Let's check out that note
- 	![alt text](https://i.imgur.com/nBlENjB.jpg)
- Looks like we'll need to revisit that DNS service. Let's try a dig lookup against the box
- 	![alt text]()
- And there's our second flag with some interesting ports listed in an odd order. Let's giving port knocking this a try! For a good port knocking script, check out my knock.sh repository. *This isn't originally my script but I've reposted it here for my own use and for others to clone.*
- 	![alt text]()









***Flags:***

1. On the FTP server, specifically within the flag1 file.
2. Within the DNS txt records, listed as a txt record along with some port information.
3. UNKNOWN
4. UNKNOWN

