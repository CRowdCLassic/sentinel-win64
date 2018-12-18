# CRowdCLassic Masternode Windows Hot Wallet Guide + Sentinel
Sentinel for using with masternode in 64-bit Windows 

First go to https://github.com/CRowdCLassic/crowdclassic-core/releases and download the wallet
after it Synchronizes go to Receive Tab and created an address

Step 1: Sent exactly 1000* CRCL to your address
·	You must account Transaction Fee
·	You should have more than 1000 CRCL in your wallet before sending
Step 2: Wait For at least 15 Confirmations
Step 3: Go to: Tools-> Open Wallet configuration file (It will be empty)
Step 4: Copy the below code into the file (let it open)

masternode=1
masternodeprivkey=
externalip=

Step 5: Go to Tools-> Debug Console -> Type masternode genkey and press enter
Step 6: Copy the Masternode key in to the masternodeprivkey=
It will look like that

masternodeprivkey= 124FqareKkDeXE5NstcVG4xpjvXAgGRA5n4SeeRjTmRn2z9BY8h

Step 7: Copy your external IP (IPv4) address in to the externalip lane
It should look like this

externalip= 79.285.230.52

If you don’t know your IPV4 just go to http://whatismyip.host/
NOTE*: You must have Port 12875 Open
If you don’t know how to do it google: How to open ports in “your router” and see the guide
If Ports are not open it will not work so be sure to open the ports
So this is how It should look like but of course remember that you should add your Masternode key and your Ip not the ones provided in the guide
Step 8: Save the crowdclassic.conf file and Close the wallet.

Wait 10 Seconds
Start The wallet

Step 9: Go to Tools-> Debug console and Type masternode start

OK That’s IT

FAQ

Q: How do I add nodes?
A: Go to Ann thread and select the node List copy it and paste it in the wallet confirmation file
Then Save and restart the wallet
Your file should look like this:

masternode=1
masternodeprivkey=12TrUZkRjw2X34BBBCoZXuCYvd8FdrMV8SGgg3aAf8ctoXZGh1R
externalip=79.204.230.52

addnode=212.237.55.250
addnode=80.211.87.193

Q: when I enter “masternode start” is says
“Not capable masternode: Could not connect to 79.204.230.52:12865“
A: This problem occurs when the port is not open or you put false IPV4
Q: Ok port is opened IP is correct still the same message
A: Try the same process on another location with a different Router if you succeed then the problem lies with your router
For some reason some Routers don’t allow the Masternode to work correctly or not at all.
Q: It says masternode not found on the list
A: This occurs when you have not properly send the coins at the number of 1000 exactly.
Just be sure do it in a clean wallet and make a new address and send exactly 1000 CRCL
Q: Where do I see my Masternode
A: Go to Masternode Tab and then to All masternodes and search your IP or Wallet address
If you can’t see a Masternode tab go to Settings-> Option-> Wallet-? Check the Show Masternode tab

SENTINEL

Ok you have your Masternode started But on status it is as WATCHDOG_EXPIRED
You need to run sentinel and this is how you do it
Pre assumption you completed the steps and have your masternode started successfully
Now let the wallet run Download the exe here :

https://github.com/CRowdCLassic/sentinelLinux/releases

Step 1. Tools -> Open Wallet Configuration File

masternode=1
masternodeprivkey=7qt9zSJWu******G943kK825pnuGPwEDZRjN7ohUdmJUynSK5Qc
externalip= your IP is here !--

The above is what you should see and the below is what you are should add
Change only the rpcuser and a rpcpassowrd, rest left the same

rpcuser=superuser
rpcpassword=superpassword
server=1
rpcport=	9917
rpcconnect=127.0.0.1

So it should look like this

masternode=1
masternodeprivkey=7qt9zSJWu******G943kK825pnuGPwEDZRjN7ohUdmJUynSK5Qc
externalip= your IP is here !--
rpcuser=supercrowdclassicuser
rpcpassword=supercrowdclassicuser
server=1
rpcport=	9917
rpcconnect=127.0.0.1

Now Save and Restart the wallet Let it sync
Now the Sentinel you downloaded the file put in in a folder of your wish
Right click and create shortcut in the same file
Right click properties
Go to the path and just after the .exe hit space
And paste this:	( this is the path of the crowdclassic.conf that you have edited)

"--config=C:\Users>USER<\AppData\Roaming\CRowdCLassicCore\crowdclassic.conf"

** note USER is your username so you should add your own

Final it looks like this:

C:\Users>USER<\Desktop\sentinel-win64.exe "--config=C:\Users>USER<\AppData\Roaming\CRowdCLassicCore\crowdclassic.conf"

Now press ok and double click the short cut you should see this

OK that’s it let the sentinel running minimize after the Pre-enabled mode I now See Enabled status

Have fun
