DeepDotWeb.com is proud to present the “Jolly Roger’s Security Guide for Beginners.” T
his Guide was made by the Jolly Roger — we found the publication on the hub forums
on this thread:
http://thehub7dnl5nmcz5.onion/index.php?topic=52.0
We obtained the Original Poster’s permission to re-post this guide. If you want to
contact the Original Poster, this is his profile on the hub forums:
http://thehub7dnl5nmcz5.onion/index.php?action=profile;u=114
Donations
Jolly Roger has spent countless hours putting this thread together. If you gaine
d some value and want to give back, He is accepting Bitcoin donations.
Address: 1PkJ928QWC5BuQAsHoNQzRV5wfnveJSRCp
Enjoy and stay safe!
Enjoy and keep safe DeepDotWeb.com Team
INTRODUCTION TO SECURE COMMUNICATION – TOR, HTTPS, SSL
PGP, TAILS, VIRTUAL BOX
PGP CONTINUED
WHOLE DISK ENCRYPTION AND FILE SHREDDING
JAVASCRIPT VULNERABILITIES AND REMOVING PERSONAL METADATA FROM FILES
GENERAL SECURITY PRECAUTIONS WHEN POSTING ONLINE, LEARN FROM OTHERS’ MISTAKES
EXIF DATA
RETAINING A LAWYER, HOW TO HANDLE GETTING CAUGHT OR INTERROGATED
COMBINING TOR WITH A VPN
COMBINING TOR WITH A VPN CONTINUED
CONNECTING TOR -> VPN FOR WINDOWS USERS
TRACKING COOKIES
LEARNING FROM OTHERS’ MISTAKES. LIBERTAS, DPR, SABU, LULZSEC
HOW FAR WILL LAW ENFORCEMENT GO?
FRAUDULENT PRIVATE MESSAGES
LEARNING FROM OTHERS’ MISTAKES. HOW THEY BUSTED SABU
LEARNING FROM OTHERS’ MISTAKES. SABU BECAME FBI INFORMANT AND BETRAYED JEREMY HAMM
OND
WHERE YOU MIGHT CONSIDER RUNNING TO, IF YOU HAD NO OTHER CHOICE
SECURING YOUR ACCOUNT FROM FBI MONITORING
INVINCIBILITY MINDSET, FEDERAL GOVERNMENT BULLYING TACTICS
HOW TO CONNECT TO TOR OVER TOP OF TOR
HOW TO VERIFY YOUR DOWNLOADED FILES ARE AUTHENTIC
VERIFYING SIGNED MESSAGES WITH SIGNATURES AND SIGNING YOUR OWN MESSAGES
AN EXAMPLE OF REALLY BAD OPSEC – SMARTEN UP!
TOR CHAT!
OBTAINING, SENDING AND RECEIVING BITCOINS ANONYMOUSLY
CLEARNET VS HIDDEN SERVICES – WHY YOU SHOULD BE CAREFUL
THEY ARE WATCHING YOU – VIRUSES, MALWARE, VULNERABILITIES!
MONITORING YOU WITH AN ANTENNA!
COOKIES & JAVASCRIPT REVISITED, PLUS FLASH COOKIES AND OTHER BROWSER TRACKING
A FEW SIMPLE RECOMMENDATIONS
COLD BOOT ATTACKS, UNENCRYPTED RAM EXTRACTION
THE STRENGH OF CRYPTOGRAPHY AND ANONYMITY WHEN USED PROPERLY PGP/GPG EMAIL ADDRESSES
ANOTHER SCAM EMAIL – BEWARE
AN INTRODUCTION TO AN EXPERT ON OPSEC, PLUS MD5 & SHA-1 CHECKSUMS
IT IS OBVIOUS WHEN YOU ARE USING TOR
ARE YOU USING SAFE-MAIL.NET ?
YET ANOTHER EXAMPLE OF HOW STRONG CRYPTOPGRAPHY AND PROPER OPSEC CAN PROTECT EVE
N PEDOPHILES
LOCALBITCOINS PART 1 – POLICE ARE WATCHING IT!

LOCALBITCOINS PART 2 – THIEVES, SCAMMERS AND COUNTERFEIT BILLS!
LOCALBITCOINS PART 3 – MORE SCAM STORIES
LOCALBITCOINS PART 4 – SELLERS BUSTED FOR MONEY LAUNDERING
HIDING TOR FROM YOUR ISP – PART 1 – BRIDGES AND PLUGGABLE TRANSPORTS
CAPABILITIES OF THE NSA
WHY YOU SHOULD ALWAYS BACK UP YOUR DRIVES, ESPECIALLY ENCRYPTED DRIVES
BITCOIN CLIENTS IN TAILS – BLOCKCHAIN AND ELECTRUM

INTRODUCTiON TO SECURE COMMUNICATION – TOR, HTTPS, SSL
Greetings comrades.
Through my research I have put together some security measures that should be co
nsidered by everyone. The reason I put this together is mainly for the newbies o
f this forum. But if I can help anyone out, then I am grateful for this. I would
like to start out by saying, if you are reading like, you are likely a Silk Roa
d user. If this is the case, then the #1 thing you must be using to even access
this form is Tor. Tor will provide you with a degree of anonymity by using an 12
8-bit AES (Advanced Encryption Standard). There has been some debate as to wheth
er or not the NSA can crack this code, and the answer is likely yes. This is why
, you should never send anything over Tor that you aren’t comfortable sharing with
the entire world unless you are using some sort of PGP encryption which we will
talk about later.
Communication from your computer, to the internet relies on an entry node which
basically “enters your computer” into the Tor network. This entry node communicates
with your computer, this entry node knows your IP address. The entry node then p
asses your encrypted request onto the relay node. The relay node communicates wi
th the entry node and the exit node but does not know your computer’s IP address.
The exit node, is where your request is decrypted and sent to the internet. The
exit node does not know your computer’s IP, only the IP of the relay node. Using t
his model of 3 nodes it makes it harder, but not impossible to correlate your re
quest to your original IP address.
The problem comes obviously when you are entering plain text into TOR because an
ybody can set up an exit node. The FBI can set up an exit node, the NSA, or any
other foreign government, or any malicious person who may want to steal your inf
ormation. You should not be entering any sensitive data into any websites, espec
ially when accessing them over TOR. If any of the nodes in the chain are comprom
ised, and some likely are, and the people in charge of those compromised nodes h
ave the computing power to decrypt your request, then you better hope it wasn’t an
ything sensitive.
So what can we do to fix this? Well, luckily we are now having more and more ser
vers that are offering something called Hidden services. You can easily recogniz
e these services by the address .onion. These services offer what’s called end-toend encryption. What this does is take the power out of the compromised exit nod
es and put them back in your hands. The web server of the hidden service now bec
omes your exit node, which means the website you are visiting is the one decrypt
ing your message, not some random exit node ran by a potential attacker. Remembe
r, the exit node has the key to decrypt your request. The exit node can see what
you are sending in clear text once they decrypt it. So if you are entering your
name and address into a field, the exit node has your information. If you are p
utting a credit card, a bank account, your real name, even your login informatio
n, then you are compromising your identity.
Another step you can take, is to only visit websites that use something called H
TTP Secure. You can tell if the website you are visiting is using HTTP Secure by
the prefix at the beginning of the address. If you see https:// then your websi
te is using HTTP Secure. What this does is encrypts your requests so that only t
he server can decrypt them, and not somebody eavesdropping on your communication
such as a compromised Tor exit node. This is another form of end-to-end encrypt
ion. If somebody were to intercept your request over HTTP Secure, they would see

encrypted data and would have to work to decrypt it.
Another reason you want to use HTTPS whenever possible, is that malicious Tor no
des can damage or alter the contents passing through them in an insecure fashion
and inject malware into the connection. This is particularly easier when you ar
e sending requests in plain text, but HTTPS reduces this possibility. You must b
e made aware however, that HTTPS can also be currently cracked depending on the
level of the key used to encrypt it. When you visit a website using HTTPS, you a
re encrypting your request using their public key and they are decrypting it usi
ng their private key. This is how cryptography works. A public key is provided t
o those who want to send an encrypted message and the only one who can decrypt i
s the one with the private key.
Unfortunately, many websites today are still using private keys that are only 1,
024 bits long which in today’s world are no longer enough. So you need to make sur
e you find out which level of encryption the website you are visiting uses, to m
ake sure they are using at a minimum 2,048, if not 4,096 bits. Even doing all of
this unfortunately is not enough, because we have another problem. What happens
if the web server itself has become compromised? Maybe your TOR nodes are clean
, maybe you have used HTTPS for all your requests, but the web server itself of
the website you are visiting has been compromised. Well then all your requests a
re again, as good as plain text.
With that being said, this will conclude the first post in this series of the st
eps we can take to protect our privacy online, to remain anonymous and maintain
our freedom.
PGP, TAILS, VIRTUAL BOX
inShare
PGP, TAILS, VIRTUAL BOX
So keep in mind that if you are a user of Silk Road, or any other form of activi
sm, you never want to enter any identifying details about yourself online. Make
it so that even if the NSA intercepted and decrypted, or compromised Silk Road t
hat the only information they have against you is your username and password. Ho
w safe is that username and password? Does your password contain any identifying
information? Is it the same password that you use for your personal email? Does
it contain a name of somebody you know personally? Always keep all of these fac
tors in mind.
Another step you must take, especially when communicating with other users on si
tes such as Silk Road is using PGP encryption. This is not always possible, such
as in cases when you are logging into a website, filling out a form, logging in
to an email, etc.. Consider any type of information you enter into a website usi
ng plain text possibly compromised. Never put anything sensitive is any type of
plain text format online. PGP comes into play because it uses a very strong meth
od of encryption called cryptography. PGP stands for Pretty Good Privacy, and it
is used for encrypting, decrypting and signing texts, e-mails, files, directori
es, and whole disk partitions and to increase the security of e-mail communicati
ons.
For the more technical users, it uses a serial combination of hashing, data comp
ression, symmetric-key cryptography, and finally public-key cryptography. For th
e less technical users, the process of encrypting messages using PGP is as follo
ws. You create a private key and a public key. The public key is the key you giv
e out to people you want to send you encrypted messages. Your private key, is ke
pt privately by you. This private key is the only key that can unlock messages t
hat were previously locked with your public key.
If you are still confused, think about it like this. Think about a public key th
at can go around locking boxes that are intended for you. Anyone can lock a box
that is intended for you, but you are the only one with the key to unlock the bo
x. Either if the person who sent you a message locked a box (message) with your
public key, they themselves can not unlock it. Only the person possessing the pr
ivate key can unlock it. If you wish to respond to this person, you must use the

ir public key to encrypt the message you intend to send to them. And they themse
lves, use their own private key to decrypt the message you sent them.
If you are still with me, I am glad I haven’t lost you yet. This is called cryptog
raphy and was designed so that anybody intercepting your message could not decry
pt the message without your private key. Even if you yourself, lose your private
key, there is no method of key recovery. You can consider that message locked f
orever. So how do you use PGP?
Well before we get to that, I want to introduce you to a Live Operating System,
which makes using PGP encryption and decryption very easy. A live operating syst
em is an operating system that you can run on top of your current operating syst
em. So for example, if you are a Windows user, you have 2 choices. You can downl
oad the live operating system, burn it to a CD or DVD and then boot your compute
r from that DVD or CD. This will make sure your computer run as if you have this
operating system installed on your computer. However, if you remove the CD or D
VD and reboot, then your computer will boot as normal. You can also use a USB dr
ive to perform this same feature.
Secondly, you can run this live operating system in what’s called a Virtual Box. T
he benefits of this are that you can run Windows simultaneously as you run this
other operating system and you can easily switch back and forth between them wit
hout rebooting the computer. Both methods have their pros and cons. The pros of
running a live CD boot, are that reduce the risk of having your computer comprom
ised by viruses, malware and keyloggers that rely on Windows vulnerabilities to
run.
If you are going to run this OS from a Virtual Box, I suggest downloading Virtua
l Box from Oracle. Note the https:// :)
https://www.virtualbox.org/
Next, the live operating system I would encourage you to use is Tails. Tails can
be found at the following website.
https://tails.boum.org/
The reason I choose Tails, is because it has many of the security features that
you require to stay anonymous already installed. Some users are not happy with T
ails, but it really is a great operating system loaded with security features. M
any I will talk about in this series on security including PGP encryption and de
cryption. Make sure you download the Tails ISO file from the official Tails webs
ite and you can either load it into Virtual Box or burn it to a DVD or load it o
nto a USB and booting your computer from that drive.
There are plenty of tutorials on how to load Tails into Virtual Box, so I won’t go
into much detail other than, make sure you run Virtual Box and Tails from a USB
drive or SD card. I would suggest a USB drive however for reasons I will explai
n later. But basically when when Virtual Box runs directly on your hard drive, i
t creates a virtual hard drive that is uses as a temporary hard drive while Tail
s is running. Once Tails is closed, this virtual drive is deleted, but it’s not pe
rmanently deleted. As we know from the power of recovery tools, deleted files ar
e easily recoverable with the right tools. I will talk about how to protect your
files from data recovery tools in future posts but for now, just keep Virtual B
ox and Tails OFF of your hard drive, and load it either on a USB drive or SD car
d.
The same goes when booting your computer directly into Tails from a DVD or USB s
tick. Your hard drive will be used to store files used by Tails, so make sure an
y files that are saved or accessed using Tails are done from a USB stick or SD c
ard, otherwise they will be recoverable. This is why I prefer using a Virtual Bo
x and running both the Virtual Box and Tails inside of it, off of a USB stick. K
eep as much as possible off of your actual hard drive. It is possible to shred f
iles beyond recovery, but it’s much easier to do this on a 16gb flash drive, then
it is a 1 TB hard drive.
Next post we will get back on topic and start learning how to use PGP. The reaso
n I have to take a detour to using Tails is because we will be using Tails for m
any of the features from here on out, including PGP.
PGP CONTINUED

inShare
Ok, so by now I am assuming you have Tails running. Let’s learn how to use PGP wit
hin Tails. First thing you are going to want to do is create your own personal k
ey, which consists of your public key that you can give out to people or post in
your profiles online. As mentioned before, this is the key people use to encryp
t messages to send to you. Your personal key also consists of your private key w
hich you can use to decrypt messages that are encrypted using your PGP public ke
y.
If you look up to the top right area, you will see a list of icons, and one o th
em looks like a clipboard. You need to click on that clipboard and click Manage
Keys
Next click File -> New
Select PGP Key and click Continue
Fill out your full name (I suggest you use your online name, not your real name)
Optionally fill out an email and a comment as well.
Next, click Advanced Key Options.
Make sure Encryption type is set to RSA and set key strength to 4096.
Once you have done this, click Create and it will generate your key.
Once you have done this, you can view your personal key by clicking the tab My P
ersonal Keys. You have now created your personal key! To find your PGP public ke
y, you right click on your personal key and click Copy and it will copy your PGP
public key to your clipboard, in which you can paste anywhere you wish. A PGP p
ublic key will look something like this.
—–BEGIN PGP PUBLIC KEY BLOCK—–
mQINBFLLWDcBEADEzn3mnLsezUDDAS5Q0lm1f6JdkI534WPuRlAN8pnuQsCSwUQU
hPEAgNCUNhxN4yCJ1mDt9xpXpX8QzsMIcofCHeE9TMLAnHzbmXLLi+D8sPZpLpDN
6jEIFvmBD4dvp5adimvRl8Ce49RpO345VUz8Ac0qLSmsv2u+kQviDQXZkrrxXHnA
IalvgDopXTISa9Sh7J3HHYYQazOZt9mfAjjuuRdaOqmAAtEe9dl43nrx+nSd/fqH
13XvMKhqJhIoJ02CBFfRBm86vtx5yiXqHZX438M9kbASqU0A2jAfRd+IZG5Z9gCI
W6FTror+F4i+bEdAuGTG1XFsQSgjKTIG0vgYiTJ93C2MZxrLvNnJp0g2zD0URyk8
Y2IdyCDfIL10W9gNMqLmjD0z/f/os66wTJkflSGaU9ZsrKHUKFN5OSfOZtNqktWn
fCpY4bigkJ8U/5C8mtr9ZE3Tv+RV4rPY0hAOtZucnhlRmYKVFNjvbS0MjqA1188c
wzBNG0XcpCNtmM5UsSvXwnDoUaEMXe50Hikxdk3d+CJzqYnor72g/WmIDROCiXl6
2D9rJ2JuLpl9bQLM+KCbXJf3kUSvzszZGXL/AwmynvqlruaXqr5975sCdfqXVexx
1sxsLofOzE01xSDEJRWwHQPlxTKPZFnXD709Xumjdinjv1w4onLk04Z96wARAQAB
tC5Kb2xseSBSb2dlciAoVGhleSB3b3VsZCBsaXZlIGFuZCBkaWUgdW5kZXIgaXQp
iQI3BBMBCgAhBQJSy1g3AhsDBQsJCAcDBRUKCQgLBRYCAwEAAh4BAheAAAoJEPuh
6tSg81nyzNsP/2ayrAz4InCK/ZnyRnnsjSHIXMv7t2uDTbYomA/0B6v/S6wHMNZX
G6+sYg41mfMuZEimgavNb0Uc2r6mI7UyWy5lp1Gd/D+all81X7bm5EBpvl1isPgJ
EqjehEdh9FQjrTiRIJafM1m254hIAaZ1RvAphI0tM2lpudk+tNKq+ivV8PpsN9TP
0mg5ZAu1lIKtG9k5vS9HAQ0grJ01TFMEjlifrf7eRyJ1+dmRJ+Xtoy2js8UwS+wM
RrIi3G39P2BfEZFQka3EmQ2JgN4pDWFoI0hODGhTba8Z0XSnVtabOTi1TOWIFmFu
yqA9bNtuOt3KhIC/O+mEATRsc/VPbTY+80kf45LwlDBfKO3PcOXSOG7ygibzEqXn
Ms/Rfe1kNEBeR9Wx2NMJSdxypqGij17CLJwNLC3KypTIQrhzy3YAndeDG4TadW2P
v/FJxhz+MX+s+9VeX2fGC0Fsfp8JbeWMAznp8Rf6O/tzEYW+pbLoLRPdi/DvFBZV
yWGPspzt3Qspm+BHbeW9iFjvCyvP2/DrKmQM7ABuRh/TMZR7uQ5na11L8rf3nzrS
Al/lSul42xLzxG+h9mDixXd1Vh6rVGMbCjL7wO25TUneFo13U5J+klo1blQWV/DL
FZUwhh2utWNCMCtcdRW0HYa14Wdyy7H68WmsJqBWUsbyD9PZ2gSawBy7uQINBFLL
WDcBEACg3IOme+sg0OZN349UYRr9/O6uW2vC5x9/azZrFNSNYh/LFJTt3XI/FsjN
gCj6NxRxbfdyLjL1gxSlJyFtclkFGS0lC0GIz7lINvemkewjde/bHXChz2IIaIli
L2A6Z6w3fP4jlQCw8NoGGJ360WMkZVTDDakYYkb50BrZSx4TVLjrHfFuLMXTE255
gQrId02jYO6240EDIhHITuiSwUQvHtXlOrHSohN83TD1I4H7iH/FLae9gYh4C/Ix
VLkzLUqvpf72Q/xogCZAJl4WEMmWD6dXufvyvhCXQnbjiLuAdQas0ef/t652LPw/
vJFDSDmguw9PXWpv3vFOe13UNU//+nw3kIGxaVWGvazXk8IFiDv9USgEGjcNn4zo
8HQlQrYz9/gyI3XojGV6L8iecWpHSweqR3NxKJmWKWEG1wwnWPL8M+z6OwEvRdxV
spy+eG0Zs+6igbw3tk6gJ4cq5ehdlmD6py27AhRhlj7uLlZxmK3uFV19QjtX/Dyt
73ZNX16krXqufl0HAJRd1PwhITPCtSviW3L2qKF2Pdak3j97A656EcInCcAyOUC/
mUNUDtXJik6uwFgFFn9/pnFr+acY7ppsWPG5rr7jRj+Lgjnjkckpkjo8jN1hZE17

CfJyrYrSqdglCcIgTHteIEZdPfPUmnbbSoyeufkyEW1AoIKatQARAQABiQIfBBgB
CgAJBQJSy1g3AhsMAAoJEPuh6tSg81ny4nIP/2lVf0DTp1n5xPEBZEUlgzcMNeh5
FTIS3J44g5a+OlkRVgHFtu7K/MUsftlUzkvMMa0sXllhKc6syxcytoD7LAt9tbQh
62yEzijTliU2QFgWJSS6IfbtC2IyRouAns3KD6XouKTFUs/i0n/QpwhnM+Ya/SAg
c/oroM7SE/T4g+v6EeRCq7In/TMgc74j+25zUF1rVSCenbZKkYezxqZ33cXLwl7l
IUBcK2uNHDBUB5G853NR0OkBm5i+KC8vM3K1/MZ+P/lK0xOcTGXZH/A7GrEsI4FJ
nw5i6zJZb8gmDt44Tp/1Ujxnm5xhVWgnOQeSVSyiRsHQ/gTCL1PqsZhW7yulwL05
yxZgN+oYVx4pNtLJMigRjoCY9IKEmZhY75cWXXA19j14Wnxu8IrwwSk1WyzMQcjj
7onP4OEhbPuotqWqVAc0M/+MV5oMGIG0Qepy6XpZOCCpZw/p1rDrZSYP5eQMd/4x
LB7xch6GjbWsnKhA1wGdjdclBodixorVfCRn4s5jTgXx7wWz/opM4ix/CPAkify7
4Sf0BdJ5YtFILZc5StED4WC5pljJbdEWVsb9rn6egvFn7W/ZlDJAerS6Mt5LJGAh
Aude0Kz2HJwDtOBF4nXeTzRCK5BrBnCYPHAtO2aqfowirzjMTd9A/ADoPmIbIJAm
04mA6krRiH909Bnx
=Az2N
—–END PGP PUBLIC KEY BLOCK—–
Next, you are going to want to save the private key on a secondary USB drive or
SD card. If you are running Tails from a USB drive, then you must use a separate
drive to store your key on. If you are running Virtual Box, you want to right c
lick on the icon in the bottom right corner that looks like a USB drive, and sel
ect your separate drive that you will be using to store your keys on. Again, nev
er store your private keys on your hard drive, keep them OFF your computer.
To save your private key, you are going to right click on your personal key and
click Properties. I know you probably saw where it says Export, but this is not
what you want to do. Clicking export will ONLY export your public key and will n
ot save your private key. If you lose your private key, you can never recover it
even if you create another personal key using the exact same password. Each pri
vate key is unique to the time it was created and if lost, is lost forever. So o
nce you have clicked Properties, go over to the tab Details and click Export Com
plete Key.
Once you have done this, you have saved your personal key for future use once yo
u restart Tails. Remembering that Tails is not installed on your hard drive, so
every time you restart Tails you lose all your keys. By saving your keys onto a
USB drive or SD card, you can import your keys for use every time you restart it
.
Next you are going to want to learn how to encrypt and decrypt messages using yo
ur key. Well, luckily for me, Tails has already made a tutorial on how to do thi
s, so I will refer you to their webpage. But before I do that, I need to mention
that you need to find somebody else’s PGP public key, or you can practice by usin
g your own. Needless to say, the way you import other people’s keys into what’s call
ed your key ring is by loading them into a text file. You do this with the progr
am called gedit Text Editor.
Click Applications -> Accessories -> gedit Text Editor and enter in someone’s publ
ic key and hit save. Next you can return to your key program from the clipboard
icon and click File -> Import and select that file. It will import that person’s p
ublic key into your key ring. To add future public keys to your key ring, I sugg
est reopening the same file and just adding the next key below the previous key
and each time you open that file it will load all keys within that file. This wa
y you can keep all the PGP public keys together in one file and save it on your
SD card or USB drive for future use.
Finally you can use the following 2 pages to learn how to encrypt and decrypt me
ssages using PGP.
https://tails.boum.org/doc/encryption_and_privacy/gpgapplet/public-key_cryptogra
phy/index.en.html
https://tails.boum.org/doc/encryption_and_privacy/gpgapplet/decrypt_verify/index
.en.html
Until next time. Have fun with your new found ability to communicate in PGP!
WHOLE DISK ENCRYPTION AND FILE SHREDDING
inShare

Welcome back again!
Now that we have PGP figured out, hopefully, I want to remind you that using PGP
whenever possible, is very very very important. One of the pitfalls of Silk Roa
d 1, is that some of the administrators, including Ross himself did not always c
ommunicate using PGP encryption. Once Ross was busted, they had access to his se
rvers and his computers and anything that wasn’t encrypted was wide open for them
to look at. Most users on Silk Road 2 believe that Ross had stored personal info
rmation about some of Admins and Moderators on his computer in plain text that w
as used to make 3 more arrests of Silk Road users.
One of the reasons why I would suggest for you to store your PGP keys and other
sensitive data on a SD card, is that if that day comes when you are compromised
and you get a knock at your door, you have time to dispose of that SD card or US
B drive quickly. Even better, if you have a micro SD card that plugs into an SD
adapter, then you can snap it with your fingers or at the very least hide it. US
Bs would need to be smashed into pieces and it might not be easy to do this in t
he heat of the moment, so do what you feel best about. But always prepare for th
e day they might come for you.
But our next topic brings us to something called Whole Disk Encryption or Full D
isk Encryption. From here on out I will refer to it as FDE (Full Disk Encryption
). Tails has a FDE feature built into it, which is another reason why I encourag
e the use of Tails. It has many of these features to protect you. Essentially FD
E will protect your drive, whether SD or USB from the people who may come for yo
u one day. The method in which it does this is it formats your drive and rewrite
s the file system in an encrypted fashion so that it can be only be accessed by
someone who has the pass phrase.
If you lose your passphrase, just like in PGP, there is no recovery. Your only c
hoice is to format the drive and start over again. So make sure you remember it!
And please for the love of God, Allah, Buddah, etc… don’t store the passphrase on y
our hard drive somewhere. The tutorial on how to do this is located at the follo
wing webpage.
https://tails.boum.org/doc/encryption_and_privacy/encrypted_volumes/index.en.htm
l
Again, always prepare for the day they come knocking, encrypt everything. Use PG
P when communicating with others and always shred your files when finished with
them. Which brings me to my next topic. File shredding.
File shredding is extremely important and here is why. If you delete a file from
your computer, you are only deleting where it is located on the drive. It is st
ill on the actual drive, just it’s location data has been removed. If you take a f
ile recovery tool you can recover virtually any file that you have recently remo
ved. File shredding combats this by overwriting files instead. The idea is that
instead of removing the file’s location, you need to overwrite the file with rando
m data so that is becomes unrecoverable.
There are a lot of debate happening on whether you can overwrite a file once, or
if you need to do it multiple times. Supposedly the NSA recommends 3 times, sup
posedly the Department of Defense recommends 7 times, and an old paper by a man
named Peter Gutmann written in the 90’s recommended 35 times. Needless to say, I p
ersonally think between 3-7 times is sufficient, and several people out there be
lieve 1 time will get the job done.
The reasoning behind this is that some people believe the drive may miss some fi
les the first time it over writes them and to be more complete, you should do mu
ltiple passes. Do what you feel most comfortable with, but I even think 3 passes
would be sufficient, although it wouldn’t hurt every now and then to run 7 passes
and just leave it overnight.
The programs that can do file shredding are ones you will want to run from Windo
ws or whatever operating system your computer is running. These programs can del
ete your files from your Recycling Bin, delete your temporary internet files and
even Wipe your free disk space to make sure everything gets cleaned up. You alw
ays need to think, did I have any sensitive material on my hard drive? If so, ma
ybe I need to shred my free disk space. When empting your Recycle Bin, you shoul

d always use a shredder. When only deleting under 1gb at a time, you can easily
do 7 passes pretty quickly.
To put this in perspective, the leader of a group called LulzSec name Topiary ha
s been banned as part of his sentence from using any type of file shredding appl
ications so that if the FBI wants to check up on him, they can. File shredding k
eeps your deleted files actually deleted.
Here are some file shredding applications you can use.
http://www.dban.org/
http://www.fileshredder.org/
https://www.piriform.com/ccleaner
Next we’re going to talk about removing harmful metadata from files, and some othe
r topics as well.
JAVASCRIPT VULNERABILITIES AND REMOVING PERSONAL METADATA FROM FILES
inShare
Welcome Back.
Before I get into removing harmful meta data from your files, I want to talk abo
ut another vulnerability to our browsing capabilities called Javascript.
In mid 2013, a person in Ireland was providing hosting to people that hosted hid
den services including a secure email platform called Tor Mail. Unfortunately th
ey busted him on an unrelated charge relating to child pornography and seized al
l his servers. Whether or not he was related to child porn or not, is unknown to
me, or it could be a silly charge the feds slapped him with but either way, the
feds ended up injecting malicious Javascript into his servers so that when user
s would visit certain sites, this malicious code would execute on their computer
s and reveal information about their computers to the feds. I suggest you read t
he following article to learn more about this.
https://openwatch.net/i/200/
With that being said, you may want to disable Javascript in your browsers, espec
ially when visiting certain websites like Silk Road that may become compromised
one day. Many users refuse to visit the original Silk Road website and forums wi
th Javascript enabled because the feds likely injected it with malicious Javascr
ipt to identify users.
In Tails, the browser is called Iceweasel and when Tor in ran in Windows, it use
s Firefox. Both browsers can disable Javascript using the exact same method. Ope
n up a Window and type the following command in the address bar, “about:config” and
click the button that says “I’ll be careful, I promise.”
This will bring up a bunch of settings including a search bar at the top. Enter
javascript in the search bar and look for the following two entries, “javascript.e
nabled” and “browser.urlbar.filter.javascript”. Right click on these and click “Toggle” an
d you will see the Value changed to false. If you want to enable Javascript agai
n, just click Toggle again and you will see the value change back to true.
Again, remember that every time you restart Tails you will have to do this again
, so get into a habit of doing this every time. You never know when your favorit
e website could become compromised.
Moving onto meta data. There is a bit of a famous story about an online hacker n
amed w0rmer that would take pictures of his girlfriend and post them online afte
r he would deface a webpage. What he either forgot, or didn’t know was that photos
taken with the iPhone and other smart phones save the GPS coordinates of where
the picture was taken and store it in the meta data of the picture. Check out th
is article below.
https://encyclopediadramatica.es/W0rmer
You need to remove this meta data! Otherwise you could end up in federal prison
with w0rmer. Luckily Tails has a solution for this! See why I love Tails?
Applications -> Accessories -> Metadata Anonymisation Toolkit
Please get a more clear idea of how this works by reading the following page.
https://mat.boum.org/
Please note the currently supported formats. In terms of pictures, jpg, jpeg and

png. But unfortunately MAT is not perfect and I wouldn’t solely rely on it, so a
better idea would be to never upload pictures of yourself or your significant ot
her online, especially bragging about a hack you committed. Please read the site
provided above for more information.
GENERAL SECURITY PRECAUTIONS WHEN POSTING ONLINE, LEARN FROM OTHERS’ MISTAKES
inShare
Next I want to talk about good practices when using TOR, Tails and other hidden
services.
First of all, it is highly recommended that you use multiple identities online f
or different things. Perhaps if you are a buyer and a seller on Silk Road, you m
ay want to have separate logins for this. And then possibly a third login for th
e forums. Then maybe you want to be part of another marketplace, then you might
want a fourth login.
Well, Tails has another good program offered by Tails is called KeePassX. When y
ou have multiple logins, it is hard to keep track of them all, so it might be a
better idea to keep them all in 1 document that is encrypted with a strong passw
ord. KeePassX can help you with this.
https://tails.boum.org/doc/encryption_and_privacy/manage_passwords/index.en.html
You never want to use nicknames or locations, or anything else that is related t
o yourself online when you post or create usernames. And another thing you need
to adopt are new ways of conducting yourself. If you are generally a messy typer
, who makes the same grammar mistakes, or the same spelling mistakes all the tim
e, this can be used to identify you. Always proof read anything you post publicl
y, or privately because the feds will always find ways to correlate things to yo
u.
With Ross Ulbricht, they found an old post he posted on a forum when he first st
arted Silk Road asking people if they had heard of a marketplace called Silk Roa
d. Obviously this is an old trick used by people trying to spread awareness abou
t a new project of theirs. Later he identified himself by saying he was looking
for programmers and gave out his private email address on the same forum under t
he same name.
But if you always misspell the same words, if you always use the same slang term
s, capitalize the same words, use a certain amount of periods after an etc…. or al
ways use the same number of !!!!! then all of these things give them reasonable
suspicion and it becomes easier to tie things to you. Once they have you under t
heir radar, like they had Ross, it only took a few slip ups and he was theirs. R
emember, you only have to make one mistake. So talking about your local election
is a really dumb idea, get it?
Think about the time you use your computer. Is it easy to correlate your timezon
e based on the time you go online? Or is it more random? Do you have patterns th
at are predictable? Always think about these things when you post online. Always
think about what type of personality you are putting out there about your onlin
e name.
Expect that every single word you type online is being read by the Feds. To them
, this is much easier than tracking drug lords on the streets. They sit in an of
fice and read forum posts and try and make connections. Don’t underestimate the fe
ds. Always treat everything as compromised, always treat everybody as compromise
d and don’t ever think anybody will ever go to jail for you. If somebody can avoid
10-20 years by ratting you out, they will do it in a heart beat.
The perfect example is Sabu from LulzSec. After he was busted and facing 112 yea
rs in jail, they made him a deal to help them rat out his friends and he ended u
p getting many of his “friends” arrested. Even people who are your friends will turn
their backs on you when it comes down to their freedom.
EXIF DATA
inShare

I forgot to mention above when talking about metadata, that when it comes to pho
tos, there is another risk involved called EXIF data, this is another form of me
ta data specifically related to images and may not be properly removed by Metada
ta Anonymisation Toolkit mentioned before.
EXIF data stands for Exchangeable image file format and affects JPG, JPEF, TIF a
nd WAV files. A photo taken with a GPS-enabled camera can reveal the exact locat
ion and time it was taken, and the unique ID number of the device – this is all do
ne by default – often without the user’s knowledge.
In December 2012, anti-virus programmer John McAfee was arrested in Guatemala wh
ile fleeing from alleged persecution in Belize, which shares a border. Vice maga
zine had published an exclusive interview with McAfee “on the run” that included a p
hoto of McAfee with a Vice reporter taken with a phone that had geotagged the im
age. The photo’s metadata included GPS coordinates locating McAfee in Guatemala, a
nd he was captured two days later.
To avoid this, only take photos that use PNG because it does not store EXIF data
. To check if your photo has any revealing EXIF data attached to it, check out t
his site.
http://www.viewexifdata.com/
or you can download a tool by doing a quick search online to see what EXIF data
may be contained in your photos before you upload them. Be very careful with any
files that you upload online, because you never know what type of harmful data
could be attached in them. It helps to use Tails, but always consider everything
you put online as a potential piece of evidence to be used against you and alwa
ys prepare for the day the feds come to your door.
RETAINING A LAWYER, HOW TO HANDLE GETTING CAUGHT OR INTERROGATED
inShare
Next entry into the series on security is how to handle getting caught.
Let us face it. We are all human and we make mistakes. Unfortunately, you only n
eed to make one mistake, and the Law Enforcement, commonly referred to as LE on
these forums can bust you. Maybe they will wait for you to do something more ser
ious before they nab you, but if you slip up and they feel you are worth going a
fter, you can expect them to get you no matter where you live, with rare excepti
on.
The first thing I want to do is link you to another thread I just came across on
these forums.
https://silkroad5v7dywlc.onion/index.php?topic=13093.0
The main question is, should I keep an emergency lawyer fund on hand? And how mu
ch should it be. The response I think was most appropriate for this question was
the following.
Give your lawyer 50k and put him on a retainer.
Don’t have a emergency fund ‘stash’ lying around if that is what you mean…. you should a
lready have your lawyer paid + plus extra in case he needs to post bond for you
and they seize the majority of your drug funds.
Once you get arrested by LE, they can seize your money based on the assumption t
hat it is drug related. So you need to have a lawyer paid for ahead of time. Tha
t way, in the unfortunate case that you get a visit from the feds, you have a la
wyer ready to go. The agreed upon amount was around $50,000.
Next I want to talk to you about what to do in case you get interrogated by LE.
There is a great thread about this.
https://silkroad5v7dywlc.onion/index.php?topic=4461.0
The take homes from this thread are basically. Keep your moouth shut. The feds a
re going to try all types of tactics on you to get you to admit to guilt of the
crimes you are being accused of. They will likely use the good cop, bad cop on y
ou. First they will tell you that they want to help you, and that they are after
the big guys. They just need your help to put away the big guys. Do not listen
to this, I have never cooperated with a good cop LE and have it end up working i

n my favor. Once you admit to being guilty, you can kiss your freedom good bye.
Secondly, if you refuse to cooperate, their attitude will change to bad cop. The
y will say, “OK fine, you do not want to cooperate? I tried to help but now you ar
e going to be in a lot of trouble. Do you have any idea what kind of charges you
are facing? You are going away for a long time unless you start talking.”
They are going to try and scare you into admitting guilt. Again, keep your mouth
shut and continue to ask for a lawyer, hopefully the one you put on a $50,000 r
etainer prior to this happening. Never speak without a lawyer present and never
do anything you do not have to do legally. If you have the right to remain silen
t, then exercise that right. I know there are some circumstances in which you do
not have that right, but unless that is the case, you are better off staying qu
iet.
Third, drop the attitude. Do not argue with the cops about having nothing on you
, or something for that matter. Act scared, anxious and confused. Act like you h
ave no idea what is going on and that you are scared for your life. Tell the cop
s they are scaring you and you want to see your lawyer because you do not know w
hat this is about. They need evidence, and solid evidence at that, to charge you
with a crime.
They are going to try and correlate posts you made on forums, phone numbers you
called, perhaps a package shipped to your home, all forms of communication, bank
transfers, and so forth, until they can find a way to link you to the crime you
are being accused of. But the biggest piece of evidence will always be your wil
lingness to admit your guilt for a lesser sentence.
When Sabu found that he was facing 112 years in federal prison, he quickly spill
ed everything and started working for the feds. Again, talk to your lawyer, find
out the evidence against you and only answers questions your lawyer advises you
to answer, and answer them in a way your lawyer advises you to answer them.
Try and be as honest as possible with your lawyer. Your lawyer can not and will
not share any admittance of guilt you have with the prosecutors or LE, this is c
alled Attorney-client privilege. Please note there are a few instances where thi
s does not apply.
https://en.wikipedia.org/wiki/Attorney%E2%80%93client_privilege#When_the_privile
ge_may_not_apply
COMBINING TOR WITH A VPN
inShare
Welcome back readers!
Today I want to talk about a greatly debated topic.
Should I use a VPN with TOR?
Should I use TOR to connect to a VPN, or use a VPN to connect to TOR?
Let me say first of all, that when you are browsing the internet without TOR, yo
u should probably be using a VPN regardless of whether or not you are using TOR.
And make sure that the VPN uses some form of encryption as well. For those of y
ou who are very beginner, think about when you connect to a public wifi network
at a coffee shop, or an airport and you get all these warnings that your request
s sent over this network are vulernable.
All networks, but especially public wifi networks are vulnerable to traffic anal
ysis. Put this together with the fact that some internet service providers monit
or your activity to some level, and you can see why it might be a good idea to a
lways use an encrypted method of using the internet. At the very least to protec
t your personal information when you are entering credit cards, usernames and pa
sswords, as well as other personal data online. Again, especially if you are usi
ng a public wifi network.
Choosing a VPN that uses at least 128 bit encryption like TOR is good practice,
and will stop the majority of eavesdroppers. But if you can get 256 bit encrypti
on, you are even safer. Before we get into whether or not we should be using a V
PN together with TOR, I want to give you a few warnings regarding how you should
be using a VPN.

If you are going to be using a VPN for any type of freedom fighting, make damn s
ure that your VPN does not keep logs. This is actually a lot harder than you mig
ht think. Many VPN providers will claim to not keep logs of your activity in ord
er to gain you as a customer, because they have to compete with the other provid
ers out there. Customers are going to trend towards providers who offer no ident
ifying data retention. Unfortunately, this claim of theirs is not always the rea
l case and I will give you an example.
There is a well known VPN provider named HideMyAss that previously claimed not t
o keep logs of its users. Unfortunately, when met with a court order from their
government in the UK, they handed over evidence of a suspected hacker from an in
ternet group LulzSec which helped lead to his arrest. The story can be found bel
ow.
http://www.theregister.co.uk/2011/09/26/hidemyass_lulzsec_controversy/
One of the take home quotes from this article is the following.
Quote
We are not intimidated by the US government as some are claiming, we are simply
complying with our countries legal system to avoid being potentially shut down a
nd prosecuted ourselves.
A very smart man that goes by the online handle The Grugq, said when doing your
freedom fighting online that nobody is going to go to jail for you, and he is 10
0% correct. When it comes down to it, no VPN provider is going to risk jail to p
rotect a $20 a month subscriber. No matter how tough they sound, no matter how m
uch they claim to care about protecting their customers, when faced with a choic
e to give you up or go to jail, they will always choose freedom.
Another thing to consider however, is using a VPN does hide your internet activi
ty from your internet service provider. It can also hide the fact that you are u
sing TOR, which may flag some suspicion when the feds start asking ISPs to provi
de data about their users. This may or may not be relevant, since many people us
e TOR and you can argue there are many legitimate reasons to use TOR and nothing
suspicious about TOR. But it is just another factor to arouse suspicion that ma
y or may not come into play and should be considered.
If you choose to use TOR over a VPN, the benefits are that you would be again, h
iding from your ISP the fact that you are using TOR. Also, your VPN would only b
e able to see that you are connecting to TOR nodes and that you are sending encr
ypted data. The VPN would not be able to see what data you are sending over TOR
unless they decrypted it, because remember, all information relayed over TOR is
encrypted.
The downsides of course, as mentioned are that VPN providers may or may not log
everything that you do in the form of meta data or even content if they have the
storage capacity, and keep those logs on hand for a long time. In this case, it
is no better than connecting to TOR through an ISP. Another thing to mention to
those who will use VPNs when not using TOR, but also use VPNs when using TOR is
remember when you are, and are not connected to your VPN. Sometimes VPNs can un
expectedly drop connections and you may not even be aware of it. If the reason y
ou are using a VPN is to hide TOR activity from your ISP, then if your VPN drops
, your ISP will start seeing your TOR traffic instead.
Or, maybe you forget that you are connected to your VPN and end up punching in y
our address on Google Maps to find directions somewhere. Well guess what Google
does with all data entered into their system? They keep it. And they likely keep
it indefinitely. So if one day the NSA identifies you on the TOR network by occ
upying a large number of nodes and using traffic analysis to identify you based
on statistical analysis, it will link them to your VPN IP address.
At this point, they will likely ask the VPN to turn over data on their users, bu
t if the VPN refuses to comply because they are not subject to US law, or the la
ws of other countries, they may check some of the big surveillance websites out
there to see if you slipped up and used that IP address for anything else online
. They will check logs from Google, Yahoo, Facebook, Twitter, Netflix and other
big data collection companies to see who has been using that IP address to conne
ct to their servers.
If you accidentally punched in your address on Google when connected to that VPN

, you are now a suspect. So always keep things like this in mind. Just because y
ou are covered behind a VPN does not mean you are not traceable by human error.
The benefits of TOR, are that you get a new identity every time you connect. Thi
s may or may not be the case with your VPN, so please check and make sure.
Next post we will talk about the advantages and disadvantages of using TOR to co
nnect to a VPN.
COMBINING TOR WITH A VPN CONTINUED
inShare
Ok, now let us talk about why you may want to connect to a VPN over TOR.
The data flow would look like this. You -> Tor -> VPN -> Internet
The benefits of doing that are as follows. You are more anonymous to your VPN in
case they happen to keep logs, or if you do something using the VPN that you ar
e not supposed to and a website or server grabs your VPN IP address. In the case
of this happening, even if the VPN manages to keep logs of everything you do, t
hey can only identify you as an anonymous TOR user as long as you did not purcha
se the service like an idiot with your credit card or Paypal account. If you use
Bitcoin, and made sure the the Bitcoin trail is not easily traceable you should
be okay. Some websites block TOR users from connecting to their websites or ser
vers, by using your VPN to appear as the exit node, you are hiding your TOR acti
vity from the website you are visiting and hopefully bypassing their filters.
Another advantage, is that if your VPN connection does drop, your fall back will
be your TOR IP address instead of your real IP address. And finally, if you are
passing through a compromised TOR exit node, your information will remain encry
pted through the VPN’s encryption protocol until it reaches the exit node of the V
PN. This is a good thing if you are passing through a compromised exit node, but
do not forget that the VPN could be logging everything you are doing anyways. D
o not trust anybody who has access to your unecrypted data!
A few of the downsides of doing things this way, as mentioned in the previous po
st are that your ISP knows you are using TOR, when and for how long. This may or
may not matter to you, but it is just something to consider. Second, you will b
e unable to visit hidden services websites. Remember those .onion sites we talke
d about in the beginning? You need to be connected to the TOR network to visit t
hose hidden service websites.
But I am connected to TOR aren’t I? Yes you are, but your final method of communic
ating with the internet does not come from the TOR network, it comes from your V
PN. And your VPN is likely not configured for TOR. In order for you to be able t
o connect to a hidden services, you must either be connected directly to TOR, or
use a VPN to connect to TOR. TOR must be your final node of connectivity in ord
er to visit onion websites.
The choice is ultimately up to you, and every person in every state, province an
d country will have different reasons for wanting to do VPN to TOR or TOR to VPN
, or just TOR, or just VPN. Whatever choice you make, please keep all the things
mentioned in this post and the previous post in mind. None of these methods wil
l save you if you enter anything identifying about yourself online. Do not log i
nto your Facebook account using your VPN. Do not check your email or search a ne
arby address on Google using your VPN. In fact, stay away from Google altogether
unless absolutely necessary.
There are two other search engines out now that do not store information about t
heir users.
#1 – DuckDuckGo. They have both a clearnet URL and a hidden services URL for both
types of users.
https://www.duckduckgo.com
http://3g2upl4pq6kufc4m.onion/ – Please note the hidden services mirror is not HTT
PS
#2 – StartPage. This server also does not store any information about its users.
https://www.startpage.com
Before we move on, I want to go back to how to choose a good VPN. When looking f

or a VPN provider, you will most likely come across two protocols to choose from
. Find out which one your VPN provider is using before you sign up with them. PP
TP and OpenVPN. At this time, I am going to highly recommend that you avoid PPTP
and stick with OpenVPN providers. Check out this site for a quick comparison.
http://www.goldenfrog.com/vyprvpn/openvpn-vs-pptp
As you can see, PPTP uses a weaker encryption, 128-bit versus 160-bit to 256-bit
for OpenVPN. It offers basic security versus a high level of security using som
ething called digital certificates. This is basically a way to make sure they da
ta coming in is sent from your VPN provider and not injected by some malicious t
hird party because the incoming and outgoing data are signed using specially obt
ained certificates, similar to showing your ID to get into a a restricted area.
The only downside is that setting up OpenVPN can be a little challenging for the
less technical users, but there are plenty of great tutorials online to set up
OpenVPN providers and your VPN provider itself will likely help you get set up a
s well. PPTP has been abandoned by those who demand the highest level of securit
y, so I would recommend to avoid it. A third option for VPN providers is L2TP/IP
sec, but many users now believe it has also been compromised by the NSA due to i
ts weaker levels of encryption and should be avoided as well. Stick with OpenVPN
.
Lastly, if you want to know how to connect to TOR over a VPN. If you are using O
penVPN like I recommended, then you it is really quite simple. Make sure you are
connected to your VPN, check your IP address to on any website such as WhatIsMy
IpAddress.com to make sure it has changed. Then, open TOR or open TAILS and star
t using TOR and you are now connected to TOR over a VPN.
Connecting to a VPN over TOR is a more tricky and currently above my skill set s
ince OpenVPN reconfigures your network routes so Tor can’t be running on the same
host. As soon as I figure it out, I will post a tutorial, and if anybody can sha
re an easy way to connect a VPN over TOR, then please share it with this thread.
UPDATE
A method of connecting to a VPN over TOR has been added to this thread but is cu
rrently only able to be used by Windows users. You can read it about it at the l
ink below.
CONNECTING TOR -> VPN FOR WINDOWS USERS
inShare
After a long search, I have found a way you can connect TOR -> VPN. It is not pe
rfect, and some might not agree with doing things this way, but it works and I a
m giving it to you as an option, but it only works for Windows users at this tim
e.
If you look back at my previous posts regarding combining VPN and TOR then you w
ill find the reasons why you would want to do so, and some of the reasons why yo
u might not want to do it. But I was unable to provide you with a way to connect
to a VPN using TOR so that the VPN does not know who you are. When it comes to
TOR -> VPN, if you cannot trust your VPN, which you rarely should, then keeping
your identity anonymous from your VPN is a good idea. Also, with more and more p
eople using TOR, but with only around 4000 TOR exit nodes, many of the exit node
IP addresses are being flagged as spammers on popular websites and limiting the
usage of well meaning TOR users to post on message boards like Stack Exchange a
nd so forth.
The way that I found you can do TOR -> VPN is by using a virtual machine, prefer
rably Virtual Box and running another instance of Windows, preferrably one that
uses less memory than your current version. You also want to run TOR Expert and
Tortilla on your host OS. I talk about how to do this in previous posts. Next se
t your Virtual Box to route all it’s network traffic through Tortilla (bridge adap
ter), which routes it all through TOR. Currently Tortilla is only supported by W
indows, which is why this option is only available to Windows users at this time
. Doing this also makes it easier to do things like watch videos on YouTube.
Now that you have your Windows Virtual Machine running on TOR, you can install a

VPN of your choice, preferrably one using OpenVPN on your Windows Guest OS and
connect to it. Check your IP address before connecting and after and you should
see a different IP address. If all went well, you now have a virtual machine run
ning TOR -> VPN. Then if you want to add another layer, you can download TOR bro
wser bundle onto your virtual machine and run that as well giving you TOR -> VPN
-> TOR for another layer of security. Also you have the option using this meth
od to use a VPN on your host OS, then Tor Expert with Tortilla, then another VPN
on your guest OS, then TOR browser, giving you VPN -> TOR -> VPN -> TOR.
I am not advocating any whcih method, you need to make that decision on your own
, I am just giving you the knowledge necesary to make an informed decison and yo
u can ultimately choose which method you feel most comfortable with. Sometimes d
oing TOR -> VPN is necessary because of the spam filter reasons I mentioned abov
e and other times having TOR as your last node to the internet is necessary like
when accessing the onion network. It is completely up to you and I know that we
are trying to shy away from Windows usage because of all the exploits and other
reasons spoken about in the previous posts, but if you have no other way of sta
ying anonymous from your VPN than this, then I think it is a good compromise unt
il we have something like Tortilla that is compatible with Linux distributions.
TRACKING COOKIES
inShare
Next time I want to talk about is something that most people completely forget a
bout. Tracking Cookies.
A recent article explains how the NSA uses things like Google Ads and other trac
king cookies to identify users over TOR when doing so by other means is not poss
ible.
http://www.washingtonpost.com/blogs/the-switch/wp/2013/12/10/nsa-uses-google-coo
kies-to-pinpoint-targets-for-hacking/
For those of you who do not know what I am talking about, let me ask you this. H
ave you ever noticed that certain ads seem to follow you around from website to
website? Perhaps something you searched for on Google or Yahoo is now showing up
in ads on other pages? This was originally designed to market things to you bas
ed on your preferences by installing tracking cookies into your browser.
Luckily TOR clears its cookies every time you restart the browser, and yes Tails
does too, but that does not mean you are not vulernable within the same TOR ses
sion. What I mean by this is, let us say you went and did some freedom fighting
on a forum somewhere and then after, using the same Tor session, visited another
website with Google Ads on it. Then you went to another site with more Google A
ds on it. You would be surprised how many sites now have Google Ads on them, by
the way.
Google can use these tracking cookies to learn about your browsing behavior. You
r search terms, your preferred sites, and so forth. Some people are even stupid
enough to use the same TOR IP address and go check their Facebook news feed or t
heir email. Guess who is in bed with the feds? Google, Yahoo, Facebook, MSN, and
all of their email providers as well. Remember, when you start leaving patterns
behind, they will start looking for similarities that start with just a suspici
on.
Perhaps they correlated the freedom fighting forum posts with you because you lo
gged into your email, and now they start noticing that you always misspell the s
ame words, make the same grammar mistakes, the same slang terms. Perhaps you vis
ited a website belonging to somebody local to you with Google Ads on it. It is n
ot entirely sure how they are able to use these tracking cookies to identify you
, but the point is, they keep everything. And if you happen to do something stup
id like Google a local restaurant or what movies are playing in your local area
on the same IP address that you did something you should not have earlier on, th
en Google can put 2 and 2 together.
Once they are on your trail, you are screwed. So do not give them anything to co
rrelate to you, ever! So then you might ask, can not I just disable cookies all

together? Yes you could, but, cookies are required for things like login session
s. Without cookies, you are unable to maintain a state of being logged in on cer
tain websites, because they use that cookie ID to identify the session on the se
rver. Again, you can certainly disable cookies, but you will not be able to main
tain a login anywhere.
LEARNING FROM OTHERS’ MISTAKES. LIBERTAS, DPR, SABU, LULZSEC
inShare
A little change of pace for this next post. I want to talk about one of our fall
en moderators Libertas.
It has finally been confirmed, what we all were hoping for that Libertas, one of
the 3 arrested moderators was released on bail recently according to an article
.
http://techcrunch.com/2014/01/07/the-silk-roads-libertas-is-free-to-the-annoyanc
e-of-us-authorities/
Quote
The Silk Road moderator Gary Davis, aka Libertas, is officially free on bail and
awaiting an extradition hearing on February 13.
The FBI flew to Ireland that night for the express purpose of taking Davis into
custody and interrogating him in Ireland, with regard to his position and functi
ons “being a moderator on a website allowing transactions to facilitate the sale o
f drugs online.”
So as you can see, just because Libertas was a moderator on the site, he is bein
g charged with allowing transactions to faciliate sales of drugs. He is basicall
y being charged as a drug dealer.
Quote
However, Davis was found in possession of illicit substances which could result
in a minimum sentence.
He unfortunately was found with drugs on him at the time of his arrest, which ma
de things much easier to keep him in custody. And it turns out that the alleged
former owner of Silk Road, Ross Ulbricht is fully complying with law enforcement
to attempt to identify senior vendors on Silk Road. According to the article, R
oss communicated with the vendors frequently and likely in plain text (is my gue
ss).
The reason I bring this up, is that we need to remind every user on here of the
mistakes that were made by Ross, and the other three moderators so that we can h
opefully learn from them. We need to avoid these types of mistakes, never ever E
VER give anybody any personal information about yourself online. The story goes,
that Ross required moderators to give him copies of their IDs in order to becom
e moderators of Silk Road, and he likely kept a record of these on his computer.
Unfortunately, these are now in the hands of the FBI and 3 moderators have been
arrested as a result since. And now, according to the article, they are after s
enior vendors as well.
A few take homes are; Always use PGP encryption in all your communications, whic
h unfortunately in this case would not have mattered because Ross ended up givin
g up his private keys to the feds. But it is still another hurdle in their way t
o protect you from them taking away your freedom. Never give out any personal in
formation to anybody online about yourself. Never put your trust in somebody els
e’s hands, because at the end of the day, nobody is going to go to jail for you. R
oss found an opportunity to possibly reduce his sentence and he is fully taking
advantage of the opportunity.
This exact same scenario happened with Sabu from LulzSec was threatened with 112
years in prison, he quickly turned on all his friends and worked with the feds
to get them all locked up to help reduce his sentence. Sabu has 2 kids and obvio
usly decided he would rather snitch out his friends and have a chance at being a
father rather than spend the rest of his life locked up in jail. Again, nobody
is going to go to jail for you.

HOW FAR WILL LAW ENFORCEMENT GO?
inShare
Today we are going to talk about the lengths that law enforcement (LE) will go t
o try and catch you slipping.
The thread that inspired this post was the following SR thread.
http://silkroad5v7dywlc.onion/index.php?topic=8788.0
The first question is, can LE ship drugs to buyers to try and set them up for dr
ug charges? Let us just say, that they have done it to a Silk Road user before w
ho went by the name of Flush aka Chronicpain aka Curtis Green
http://www.usatoday.com/story/news/nation/2013/11/07/vendor-administrator-pleadguilty-in-silk-road-case/3469751/
Quote
In April 2012, a DEA undercover agent in Maryland posing as a drug smuggler bega
n communicating with “Dread Pirate Roberts” on Silk Road about selling a large amoun
t of illegal drugs. “Dread Pirate Roberts” instructed [Curtis] Green to help the smu
ggler find a drug dealer who could buy a large amount of drugs, court papers say
. Green found a buyer and agreed to act as the middleman for a $27,000 sale of a
kilogram of cocaine. Green gave the DEA agent his address.
An undercover U.S. Postal Service inspector delivered the cocaine to Green’s house
in Utah on Jan. 17.
So as you can see, whether you view it as entrapment or not, once they have evid
ence against you, they will eventually figure out a way to get something on you
and bust you for it like they did to Curtis Green.
The Secret Service posed as a vendor for fake IDs online for 5 years and actuall
y shipped fake IDs that they made to buyers on an online Russian forum.
http://www.tested.com/tech/456882-how-secret-service-sold-fake-ids-catch-identit
y-crooks/
Quote
The US Government’s “Operation Open Market” resulted in indictments against 55 defenda
nts. According to Wired, Special Agent Mike Adams shipped out more than 125 fake
IDs over about five years of activity while going by the username Celtic. Amazi
ngly, the entire scheme started when the government arrested the real Celtic, a
Nevada man who got caught shopping at a Whole Foods where he’d previously used a f
ake credit card.
Law enforcement discovered counterfeiting equipment among his possessions and le
arned about his online activities. Adams assumed his online identity and even im
proved Celtic’s cred, shipping near-flawless IDs and becoming a trusted seller on
Carder.ru.
As you can see in this article, the Secret Service again sold illegal items to p
eople online in order to bust them. Several of the buyers used their real addres
ses and sent real photos of themselves to this officer to have their IDs made, r
esulting in being arrested by the feds.
And in this particular case, the feds charged all the defendants under something
called the RICO act.
Quote
“The main indictment is noteworthy because, in addition to the usual mix of credit
card fraud and false identification charges, the 39 defendants have been charge
d under the mob-busting RICO act – a first for a cybercrime prosecution.
Enacted in 1970 to help the FBI crack down on the mafia, the Racketeer Influence
d and Corrupt Organizations Act lets the feds hold every member of a criminal or
ganization individually responsible for the actions of the group as a whole. The
losses collectively inflicted by the Carder.su members are easily enough to giv
e every RICO defendant 20 years in prison.”
When you commit crimes online, especially in an online community, the feds may b
e able to hold you accountable for the actions of other users on that same commu
nity. So make sure when you do your freedom fighting, or whatever you choose to
do, that you take this into considering. Always weigh out the worst case scenari
o, should you get busted, because the LE will try and set you up.

One last example of how LE will try and set you up, but not relating to online c
ommunities is when they put together a fake sweepstakes in Los Angeles.
http://www.nbclosangeles.com/news/local/La-Mirada-Inspired-by-the-Simpsons-to-Ca
tch-Criminals-78093912.html
Quote
Sheriff’s deputies in La Mirada attempted a rope-a-dope on some alleged criminals
by offering them a fake sweepstakes prize. Out of the 960 letters sent to these “p
eople of interest” only eight showed up at the La Mirada Holiday Inn to collect th
eir prize, according to the Whittier Daily News.
Posing as the “Pelican Marketing Group,” deputies sent letters last week to people t
hroughout the county wanted in connection with crimes ranging from misdemeanor w
arrants to murder.
According to the report, the suspects were advised to bring their letter and ide
ntification to the Holiday Inn, and told that they were guaranteed a prize worth
at least $100, and would be one of 200 people with a chance to win a 2010 BMW 2
38i sedan.
They were all smiles when they showed up to collect their prizes, Deputy Janet R
amirez told the newspaper. “Once they tell them they’re under arrest, the smile fade
s quickly,” she said.
So the reason I made this post, was for those of you who think that LE will not
go to certain lengths to try and set you up for charges. They will do it if they
want you bad enough, and if you fall for it, they might get you on some tough c
harges. Curtis Green is facing up to 40 years for the sting operation by the DEA
on him and the users who purchased fake IDs on the Russian forum could face up
to 20 years each since they can be charged under the RICO act. Always keep these
things in mind when conducting activities online and always take the worst case
scenario into account.
It only takes one mistake to get caught and the government has unlimited resourc
es and super computers to try and catch you slipping. You may only have a few la
ptops, desktops, servers, but nothing compared to the what they have. Be careful
everyone.
FRAUDULENT PRIVATE MESSAGES
inShare
Be careful with private messages (PM) online, because one thing that comes with
anonymity, is plenty of scammers.
Silk Road users have been reporting supsicious and outright fraudulent messages
from users posing as Moderators asking them to download files to their computers
. Here is an actual message received by another member.
Quote
This message is to inform you that the version of Tor Bundle you are using may b
e vulnerable to a remote execution attack through a flaw in Javascript’s onreadyst
atechange event. This vulnerability may disclose a users actual identity and oth
er sensitive information transmitted over the tor network.
As of Janurary 2nd 2014 the following vulnerability was found
Title: Execution of unmapped memory through onreadystatechange event
Impact: Critical
An attack that exploits a Firefox vulnerability in JavaScript has been observed
in the wild. Specifically, Windows users using the Tor Browser Bundle (which inc
ludes Firefox plus privacy patches) appear to have been targeted.
Please note: If you are using Linux or Tails (bootable) this vulnerability does
not apply to you, please disregard this message.
We are advising all of our community members to upgrade to the patched version T
or Bundle (3.5)
http://www34.zippyshare.com/v/xxxxxxxx/file.html (Latest Tor Bundle 3.5)
Mirror: http://xxxxxxxxxxxxxxx.onion/files/torbrowser-install-3.5_en-US.zip
Note: You do not need to remove your current Tor Bundle before installing. This
will overwrite the previous installation and upgrade you to the latest 3.5 versi

on.
If you are unsure of which version you have it is best to upgrade anyways, it wi
ll preserve your bookmarks and preferences during the upgrade.
Also…Don’t Forget to Click the “Forbid Scripts Globally” after clicking on the S …..
The rest….Do Not mess with….this is a relatively simple thing to do….you must do this
all before accessing any DarkWeb Site. Point …Blank & Period….
This is your Safety and Security that you’re Dealing with here….TAKE THIS SERIOUSLY!
!
I don’t mean to sound harsh or an asshole…i believe we’re all Family here….and from here
on out if you cannot do as told to ensure that your security and safety is not
compromised…..well then you don’t need to be here….Period….
Any questions? Please feel free to message any mod and we will do our best to re
ply Asap
Happy New Year & Stay safe in 2014!
-SR Staff
They then provide a link for you to download an “updated” version of TOR, which has
been removed for security purposes. But this message is not coming from any Silk
Road staff, it is coming from a random account and the files are likely to be v
iruses or possibly even from law enforcement.
If you get any suspicious messages from anybody claiming to be a Silk Road moder
ator asking you to download software to your computer, report it to a moderator
immediately so that they can ban the accounts. Do not under any circumstances do
wnload any software to your computer unless it comes from an official website su
ch as;
https://torproject.org
https://tails.boum.org/
Again, stay safe everyone!
LEARNING FROM OTHERS’ MISTAKES. HOW THEY BUSTED SABU
inShare
This next post I want to focus on more mistakes that other hacktivists and freed
om fighters have made which ultimately led to their arrests. This is more proof
that you only need to screw up once.
You have probably heard me talk about somebody named Sabu multiple times and may
be you are new to the online communities and you have no idea who I am talking a
bout. Sabu was the leader of a self proclaimed hacktivist group called LulzSec.
They were responsible for taking advantage of security exploits in online server
s and posting the information online on a website called PasteBin. They had done
this many times.
https://www.informationweek.com/attacks/lulzsec-leader-sabu-unmasked-aids-fbi-ha
cker-sweep/d/d-id/1103214?
Quote
The men have been charged with hacking Fox Broadcasting Company, Sony Pictures E
ntertainment, and the Public Broadcasting Service (aka PBS).
During the time all this was happening, the members of this group maintained an
online Internet Relay Chat (IRC) channel in which they regularly discussed and t
ook credit for their attacks and exploits. The agreed upon ring leader for these
attacks, and this group went by the online handle Sabu. Sabu had also been link
ed to selling stolen credit cards on Facebook through his online handle, not his
real one, which carries a charge of aggravated identity theft.
The group had leaked identities of law enforcement, Sony users, and all wreaked
all types of havoc online including DDos attacks on the CIA. The FBI wanted Sabu
, they wanted the ring leader, who would eventually be facing charges that could
lead to 112 years in prison. But as I mentioned in previous threads, it only ta
kes one mistake to get caught. That is all they need.
http://www.foxnews.com/tech/2012/03/06/exclusive-unmasking-worlds-most-wanted-ha
cker/
Quote

Sabu had always been cautious, hiding his Internet protocol address through prox
y servers. But then just once he slipped. He logged into an Internet relay chatr
oom from his own IP address without masking it. All it took was once. The feds h
ad a fix on him.
However, this was not his first actual slip up, but it was his first slip up whe
re the feds actually discovered his mistake. His identity was actually discovere
d, or “doxed” previously by another online hacking group called Backtrace who posted
his identity and general location online weeks prior to this in an attempt to d
ox members of LulzSec.
http://arstechnica.com/tech-policy/2012/03/doxed-how-sabu-was-outed-by-former-an
ons-long-before-his-arrest/
Quote
Sabu occasionally mentioned ownership of a domain called prvt.org in his chats,
including those in Backtrace’s “consequences” document. Every domain registration is a
ssociated with corresponding information in the WHOIS database. This information
is supposed to include the name and address of the domain’s owner.
Often this information is incorrect (most domain registrars do nothing to valida
te it) or anonymized (many firms offer “proxy” domain registration, so the WHOIS dat
abase contains the details of the proxy registrar, rather than the person using
the domain). Monsegur appeared to use one of these anonymizing services, Go Dadd
y subsidiary Domains By Proxy, for registering the prvt.org domain.
The registration for the domain was due to expire on June 25, 2011, requiring Mo
nsegur to renew it. But for some reason—error on Monsegur’s part perhaps, or screw-u
p by the registrar—the renewal was processed not by Domains By Proxy but by its pa
rent, Go Daddy. Unlike Domains By Proxy, Go Daddy uses real information when it
updates the WHOIS database, so on 24th June (the day before it was due to expire
), Monsegur’s name, address, and telephone number were all publicly attached to hi
s domain name.
Monsegur quickly remedied the mistake, changing the WHOIS registration to use va
rious other identities—first to that of Adrian Lamo (who reported Bradley Manning
to authorities) and then to “Rafael Lima” and subsequently to “Christian Biermann”. This
attempt to mislead those relying on the WHOIS information successfully misled s
ome would-be doxers. But not all: by August there were extensive dossiers on Sab
u’s true identity.
Two mistakes that we know of, is all that it took to bring down at one time, the
World’s Most Wanted Hacker. If you are familiar with the story of LulzSec, there
was a time they were receiving mainstream news coverage and Sabu had gained a re
putation of being this mystical untouchable hacker. Unfortunately for him, he ma
de two small yet very costly mistakes which ended up putting him away. But we ar
e not done yet on this story about Sabu.
Sabu had a weakness, that the feds used as leverage against him when he got bust
ed.
Quote
An unemployed computer programmer, welfare recipient and legal guardian of two y
oung children.
“It was because of his kids,” one of the two agents recalled. “He’d do anything for his
kids. He didn’t want to go away to prison and leave them. That’s how we got him.”
Monsegur was quietly arrested on aggravated identity theft charges and released
on bail. On Aug. 15 he pleaded guilty to a dozen counts of hacking-related charg
es and agreed to cooperate with the FBI.
So when you are doing your freedom fighting online, you need to ask yourself. Wh
at do I have to lose? Do I have a wife? Children? What would happen if I were to
lose everything and be thrown away for 10 to 20 years, could I handle that? If
you decide that you are willing to risk all that, then you again need to learn f
rom the mistakes of those who have fallen before you. Ask yourself, if put in a
hard place, where you had to choose between life in prison, and cooperation, in
order to see your own family, you may think you will not talk now, but you may s
tart talking when the feds are threatening to take them away from you forever.
Once the FBI had the leader of the group LulzSec working for them, they wasted l
ittle time getting the former hacker to turn on his friends and aid in their arr

ests.
Continued next post.
LEARNING FROM OTHERS’ MISTAKES. SABU BECAME FBI INFORMANT AND BETRAYED JEREMY HAMM
OND
inShare
We are continuing the subject of how others were taken down after Sabu was compr
omised and started cooperating with the FBI. According to this article.
http://arstechnica.com/tech-policy/2012/03/stakeout-how-the-fbi-tracked-and-bust
ed-a-chicago-anon/
Quote
The day after Christmas, sup_g had another online chat about the Stratfor hack a
nd about some 30,000 credit card numbers that had been taken from the company. H
is interlocutor, CW-1, engaged in a bit of gallows humor about what might happen
should they all get caught.
But the raid had, in fact, already happened. CW-1 was “Sabu,” a top Anon/LulzSec hac
ker who was in real life an unemployed 28-year old living in New York City publi
c housing. His sixth-floor apartment had been visited by the FBI in June 2011, a
nd Sabu had been arrested and “turned.” For months, he had been an FBI informant, wa
tched 24 hours a day by an agent and using a government issued laptop that logge
d everything he did.
So we see here Sabu is chatting with a user sup_g to try and engage him about th
e hacks that took place.
Quote
Sabu suddenly addresses sup_g by a new name, “anarchaos.” It would turn out that sup
_g went by many names, including “anarchaos,” “burn,” “yohoho,” “POW,” “tylerknowsthis,” and
threat.”
CW-1: if I get raided anarchaos your job is to cause havok in my honor
CW-1: <3
CW-1: sup_g:
@sup_g: it shall be so
Normally, the attempt to link his various names would have raised the hacker’s gua
rd; as he confided to Sabu, someone else had once tried to link the names “yohoho” a
nd “burn,” but the hacker “never answered… I think he picked up some language similariti
es I’ve worked with [REDACTED] on other ops in the past.” But this was Sabu, a sort
of hacker demigod in the world of Anonymous. If you couldn’t trust him, who could
you trust? Sabu had even provided a server to store the stolen Statfor data, so
he couldn’t be a fed (in reality, he had done so at the FBI’s direction).
And more details on how they looked through copious amounts of logs to correlate
this user sup_g to his real identity.
Quote
To identify sup_g, the Bureau first turned to the voluminous chat logs stored on
Sabu’s computer. They went through every comment that could be plausibly linked t
o sup_g or one of his aliases. The goal was to see if the hacker had slipped up
at any point and revealed some personal information.
He had. On August 29, 2011 at 8:37 AM, “burn” said in an IRC channel that “some comrad
es of mine were arrested in St. Louis a few weeks ago… for midwestrising tar sands
work.” If accurate, this might place “burn” in the Midwest. FBI Chicago agents were a
ble to confirm that an event called Midwest Rising was attended by Chicago resid
ent Jeremy Hammond’s twin brother. (Hammond had a history with anarchism and viole
nt protest.)
“Anarchaos” once let slip that he had been arrested in 2004 for protesting at the Re
publican National Convention in New York City. Much later, “yohoho” noted that he ha
dn’t been to New York “since the RNC,” nicely tying both online handles to the same pe
rson. The FBI went to New York City police and obtained a list of every individu
al detained at the 2004 convention; they learned that Jeremy Hammond had in fact
been detained, though he had not been arrested. The pieces were starting to fit
.

“Sup_g” and “burn” both indicated later that they had spent time in prison, with “burn” indi
cating that he had been at a federal penitentiary. A search of Hammond’s criminal
records revealed that he had been arrested in March 2005 by the Chicago FBI and
had pled guilty to hacking into a “politically conservative website and stealing i
ts computer database, including credit card information,” according to an FBI affi
davit. Hammond was sentenced to two years in prison for the action.
In yet another chat, “Anarchaos” told Sabu that he had once spent a few weeks in a c
ounty jail for possession of marijuana. He also asked Sabu not to tell anybody, “c
ause it could compromise my identity,” and he noted that he was on probation. Both
matched Hammond, who was placed on probation in November 2010 after a violent p
rotest against the Olympics coming to Chicago. When the FBI ran a criminal histo
ry check on Hammond, it also revealed two arrests for marijuana possession.
The FBI was so thorough that it even followed up on a “POW” comment saying “dumpster d
iving is all good i’m a freegan goddess.” (“Freegans” scavenge unspoiled, wasted food fr
om the trash of grocery stores and restaurants.) The FBI went to Chicago authori
ties, who had put Hammond under surveillance when they were investigating him ba
ck in 2005. As part of that earlier surveillance, “agents have seen Hammond going
into dumpsters to get food.”
Now that they had a suspect, it was time to put him under surveillance.
This is why you all need to be extra paranoid with every single thing you say ab
out yourselves on this forum. I have seen people talking about what country they
live in, some even talking about which state they live in. If you think that th
e FBI will never put the pieces together, you may be sadly mistaken as Jeremy Ha
mmond found out.
Quote
Watching the WiFi network revealed the Media Access Control (MAC) addresses of e
ach device connected to the network. Most of the time there was only one, an App
le Computer—and sup_g had told Sabu that he used a Macbook.
On March 1, the agents obtained a court order allowing them to use a “pen register
/trap and trace” device that could reveal only “addressing information” and not conten
t. In other words, if it worked, agents could see what IP addresses Hammond was
visiting, but they would see nothing else.
His Macbook’s MAC address was soon seen connecting to IP addresses known to be par
t of the Tor anonymizing network.
And while this definitely sounded like their man, the Bureau went to even greate
r lengths to double-check their target. The main technique was to observe when H
ammond left his home, then to call Sabu in New York and ask if any of Hammond’s su
spected aliases had just left IRC or the Jabber instant messaging system.
If this does not open your eyes to some of the mistakes many of you have been ma
king online, then you need to reevaluate how you handle yourselves online. Read
the entire article to get a better picture, but remember, I do not care if it is
your best friend from elementary school, do not, under any circumstances ever a
dmit anything online to anybody. Never under any circumstances take credit for a
ny freedom fighting or hacktivism you have participated it online. And for chris
t’s sake, NEVER log into a server, especially one that keeps logs with your real I
P address!
WHERE YOU MIGHT CONSIDER RUNNING TO, IF YOU HAD NO OTHER CHOICE
inShare
In the case that you may have to run, here are some things to consider.
I am not an expert on evading extradition, or how to evade the federal governmen
t, NSA or other super powers, but I do have some recommendations that you might
want to consider if you decide that you have no other choice but to run. The fol
lowing countries do not currently have an extradition treaty to the United State
s.
Quote
Afghanistan, Algeria, Andorra, Angola, Armenia, Bahrain, Bangladesh, Belarus, Bo
snia and

Herzegovina, Brunei, Burkina Faso, Burma, Burundi, Cambodia, Cameroon, Cape Verd
e, the Central
African Republic, Chad, China, Comoros, Congo (Kinshasa), Congo (Brazzaville), D
jibouti, Equatorial
Guinea, Eritrea, Ethiopia, Gabon, Guinea, Guinea-Bissau, Indonesia, Ivory Coast,
Kazakhstan,
Kosovo, Kuwait, Laos, Lebanon, Libya, Macedonia, Madagascar, Maldives, Mali, Mar
shall Islands,
Mauritania, Micronesia, Moldova, Mongolia, Montenegro, Morocco, Mozambique, Nami
bia, Nepal,
Niger, Oman, Qatar, Russia, Rwanda, Samoa, São Tomé & Príncipe, Saudi Arabia, Senegal,
Serbia,
Somalia, Sudan, Syria, Togo, Tunisia, Uganda, Ukraine, United Arab Emirates, Uzb
ekistan, Vanuatu,
Vatican, Vietnam and Yemen.
This does not mean that these countries will not extradite you, but if you are g
oing to pick a country to flee to, it would be favorable to your chance to choos
e from this list. One noteable country on this list, which is famous for extradi
ting one of the owners of the Pirate Bay, Gottfrid Svartholm to Sweden, is Cambo
dia. Although no treaty exists between the two countries, he was extradited by t
he government.
We all know that Edward Snowden fled to Russia from Hong Kong after leaving the
US from Hawaii and has remained there since without being extradited by the gove
rnment and was granted a 1 year temporary asylum. It is unclear if Snowden will
be able to stay longer than his 1 year temporary asylum grants, but as of right
now he is badly wanted by the US government, and Russia is refusing to hand him
over.
Another person involved in the Pirate Bay named Fredrik Neij fled to Laos in Asi
a following being convicted of “assisting in making copyright content available” and
was sentenced to one year in prison and ordered to pay damages of 30 million SE
K (approximately €2,740,900 or US$3,620,000). This is of course between Laos and S
weden, but Laos has not extradited Fredrik, so Laos may be a valid option.
I often hear people from the US claim that if “shit ever pops off” they would just f
lee to Canada. Do not even try it, you would not even make it through the border
. Canada is like the baby brother of the United States. When the United States s
ays jump, Canada says “how high?”. Stay away from Canada if you are running from the
United States. Even a pot activist named Mark Emery who was a Canadian citizen,
lived in Canada, but sold marijuana seeds over the internet to people in the US
was extradited to the US to serve a 5 year sentence. According to the other see
d vendors in the area, those who only sold within Canada had never been arrested
, but because Emery sold to the US, he was arrested and extradited. And of cours
e, we know that Ireland and Australia will likely be extraditing two of the mode
rators from Silk Road to the United States soon enough.
Although not on the list above, a woman, wanted in the US for parental kidnappin
g, named Chere Lyn Tomayko was granted asylum in Costa Rica.
http://www.usatoday.com/news/topstories/2008-07-25-3841863361_x.htm
Quote
Tomayko’s claims that her actions were justified by domestic violence she suffered
were taken into account by the Costa Rican authorities.
Assata Shakur was charged with murder, attempted murder, armed robbery, bank rob
bery, and kidnapping by the US and fled to Cuba. Cuba actually has an extraditio
n treaty with the US, but the relations between the two countries have not been
good since the cold war between the US and the Soviet Union and thus the request
s were not honored, even for someone with such serious charges. Cuba may be an o
ption for you, but again this is only something to consider as I am no expert in
any way.
And finally according to a previous post of mine explaining how the Secret Servi
ce sold fake IDs online to people on a forum, several of the members of that for
um were able to evade capture due to being in Eastern European countries, althou
gh not specified by the feds for obvious reasons, and remain at large to this da

y.
http://www.tested.com/tech/456882-how-secret-service-sold-fake-ids-catch-identit
y-crooks/
Quote
The government made its move in 2012, arresting dozens of fraudsters in the US a
nd in countries where extradition is easy. But many more, including the founder
of Cards.ru, remain at large. Those in Eastern European countries, especially, a
re largely out of the government’s reach.
SECURING YOUR ACCOUNT FROM FBI MONITORING
inShare
I just had another realization that you may want to consider.
I noticed that certain some people on the forum were never shown as Online, even
when they clearly were, and others were shown as online at times. I then realiz
ed to myself there must be a way to never show your status as Online.
The way you do this is to open up Account Settings and unselect the box that say
s Show others my online status.
So why would you want to do this anyways? For reasons we spoke about earlier, yo
u do not want to give any law enforcement the ability to see when you log on and
log off. It is bad practice, it can leave a trail, leave a pattern, and if you
are a person of interest and they are able to connect the time you sign off on t
he forum with the time you leave your house, or go to sleep, it gives them more
reason to be suspicious and more evidence to be used against you in court.
Consider disabling this option.
INVINCIBILITY MINDSET, FEDERAL GOVERNMENT BULLYING TACTICS
inShare
Some people have an invincibility mind set that nothing will ever be able to be
tied to them or derived from their online communications.
Well guess what? They do not have to use your online communications to find out
who you are. All that needs to happen, is for you to do something stupid and bec
ome a person of interest and they will be monitoring your activities online to t
he best of their abilities. Remember you only need to screw up once.
For example, maybe you become a person of interest and the FBI gains a subpoena
to your Facebook account where you stupidly bragged to a friend of yours about p
articipating in certain online activities. This happened to one of the members o
f LulzSec who transferred a data dump that he obtained through SQL injection exp
loits to a friend of his using his own Facebook in his own name. So do not ever
talk about Silk Road or any of your online activities on any social media platfo
rm.
Even if a company does not currently keep logs, a court order may perhaps be use
d to force a company to start keeping logs. Hush Mail was forced to hand over 12
CDs worth of e-mails from three Hushmail accounts, following a court order obta
ined through a mutual assistance treaty between the U.S. and Canada. According t
o the following article.
http://www.wired.com/threatlevel/2007/11/encrypted-e-mai/
When it comes to being threatened by a court order from the federal government,
99.99% of all companies will comply to avoid either prosecution themselves, or s
hutting down their business as we saw previously with Hide My Ass.
But one company decided to stand up to this type of bullying that you may have h
eard of called LavaBit as seen in the following article.
http://www.theguardian.com/world/2013/oct/03/lavabit-ladar-levison-fbi-encryptio
n-keys-snowden
Quote
The email service used by whistleblower Edward Snowden refused FBI requests to “de
feat its own system,” according to newly unsealed court documents.
The founder of Lavabit, Ladar Levison, repeatedly pushed back against demands by

the authorities to hand over the encryption keys to his system, frustrating fed
eral investigators who were trying to track Snowden’s communications, the document
s show.
Levison is now subject to a government gag order and has appealed against the se
arch warrants and subpoenas demanding access to his service. He closed Lavabit i
n August saying he did not want to be “complicit in crimes against the American pe
ople”.
In July, the authorities obtained a search warrant demanding Lavabit hand over a
ny encryption keys and SSL keys that protected the site. Levison was threatened
with criminal contempt – which could have potentially put him in jail – if he did no
t comply. Such a move would have given the government access to all of Lavabit u
sers’ information.
The court ordered Levison to be fined $5,000 a day beginning 6 August until he h
anded over electronic copies of the keys. Two days later Levison handed over the
keys hours after he shuttered Lavabit.
You see what I am talking about? The federal government ordered this man to hand
over all his encryption keys and SSL keys which compromised the privacy of 400,
000 users just so they could gain more data on one man, Edward Snowden. And they
used bullying tactics and attempted to bankrupt the owner of Lavabit by fining
him $5,000 per day until he handed over the keys. Unfortunately Levison had no c
hoice but to hand over the keys or lose everything.
An interview on Reddit with Levison revealed what he claimed that other secure e
mail providers who threatened to shut down were forced to stay up.
http://www.theregister.co.uk/2013/11/19/lavabit_analysis/
Quote
Lavabit’s founder has claimed other secure webmail providers who threatened to shu
t themselves down in the wake of the NSA spying revelations had received court o
rders forcing them to stay up.
There you have it. Anyone who tries to stand up to the government, especially in
the United States will be met with swift justice, court orders and outrageous f
ines unless they comply and on top of it, slapped with gag orders so they cannot
tell anybody about what the government is doing.
HOW TO CONNECT TO TOR OVER TOP OF TOR
inShare
Here is another fun tip that may or may not interest you, but I figured I would
throw it in for you anyways.
I figured this out while trying to figure out an effective way to do a TOR -> VP
N connection. You can do TOR -> TOR connection with Tails by using a program cal
led Tortilla, thus adding another layer for your adversaries to crack. Whether o
r not this is worth it, is completely up to you, but I am sharing in case it is
something you want to do. This however currently only works for those using Wind
ows because it was designed to be used by Windows users. Please note as well tha
t this will noticeably slow down your connection since you are going through TOR
twice. Here is the official homepage of Tortilla.
https://github.com/CrowdStrike/Tortilla
And the official download page for the prebuilt standalone exe below. There is a
link to it on the home page if you do not trust me.
http://www.crowdstrike.com/community-tools/
The way you do this is very simple actually. You need to first download TOR Expe
rt Bundle from the TOR Project download page and install it on your computer or
better yet your USB drive.
https://www.torproject.org/download/download.html.en
Next open the tor.exe and just let it run until it says Bootstrapped 100% Done.
Next you want to run the tortilla.exe file and make sure you run it with Adminis
trator privileges. Also, if you are running Windows Vista or later, you will lik
ely get an error that this program does not have a valid certificate, because it
is actually signed with something called a test-signed ceritifcate. In this cas
e you need to allow test-signed drivers to run on your computer.

To do this, simply go to your Start Menu and type in the search box “command”. When
command comes up, you right click it, and click run as Administrator and it will
open up a command prompt. Next type in the following command. Bcdedit.exe -set
TESTSIGNING ON and this will allow Windows to install test-signed drivers. Resta
rt your computer and you will see in the bottom right hand corner after you rest
art Test Mode Windows. Now you can run Tortilla. And let it connect to TOR. Reme
mber to have tor.exe from TOR Expert Bundle open first.
Finally, you open up Virtual Box or whatever Virtual Machine software you are us
ing and click Settings on the Tails virtual machine. Click on the Network tab an
d change the drop down menu where it says Attached To: to Bridged Adapter and in
the drop down menu below it called Name: Select Tortilla Adapter. Now your Virt
ual Machine, in this case Tails, will always connect to the internet through Tor
tilla, which connects through TOR. And since Tails establishes its own connectio
n to TOR, you will be running TOR over top of TOR. Again, you may or may not wan
t to do this, but I am giving you the option should you want to.
If anyone is interested in learning more about the creator of Tortilla, he did a
PowerPoint presentation at the 2013 Black Hat USA conference. Feel free to watc
h his talk at the YouTube link below. Please note however that YouTube is owned
by Google and there are only about 57 views on the video, so the government will
likely correlate users who watch that video with users from this forum. Make su
re you do not watch the video on YouTube with your real IP address. At the very
least use a VPN or find another site that has it hosted. Always be extra paranoi
d.
HOW TO VERIFY YOUR DOWNLOADED FILES ARE AUTHENTIC
inShare
I just had a realization about something that is pretty important and I wanted t
o share it with you, regarding security. Verifying your downloads
As a general rule of thumb, you should always download files from the home pages
of their respective developers.
TOR: https://www.torproject.org
Tails: https://www.tails.boum.org
Virtual Box: https://www.virtualbox.org/
The reason this is so important, is that there are people who host maliciously m
odified versions of these programs and will host legitimate looking sites to try
and get you to download their version, which can install things like backdoors
into your computers, keyloggers, and all types of nasty surprises. Sometimes dev
elopers will offer mirrors for their projects, which are simply just alternative
links to download from in case the main server is too slow, or down. Sometimes
these mirrors can become compromised without the knowledge of the developers.
Maybe you do not have TOR or Tails on your laptop and you are traveling out of t
he country and the hotel that you are staying at has TOR’s homepage blocked. There
are times when you may need to find an alternative mirror to download certain t
hings. Then of course there is the infamous man-in-the-middle attack where an at
tacker can inject malicious code into your network traffic and alter the file yo
u are downloading. The TOR developers have even reported that attackers have the
capability of tricking your browser into thinking you are visiting the TOR home
page when in fact you are not.
So what do you do about it? You can verify that the file you downloaded is in fa
ct legitimate. The best tool for this is GnuPG. The TOR developers recommend you
get it from the following page (Windows Users).
http://www.gpg4win.org/download.html
You can install this program on your USB drive or on your actual computer, you w
ill hear your actual computer’s operation system referred to as your Host OS. So d
ownload it, run it, install it and we will start showing you how to use GnuPG.
If you remain on the GnuPG download page you will see something under the big gr
een box that is called OpenPGP signature. Download that into the same folder as
the GnuPG file, this is the file that the download was signed with. Basically so

meone’s signature saying, I made this file. And you also need a PGP public key to
verify the signature. So to sum it up so far, the signature is created from the
PGP private key, and can be verified by the PGP public key. The signature file i
s used to verify the program itself. So let us grab the PGP public key for GnuPG
as well.
If you look on the same download page, under the heading Installation, you will
see a link where it says verify the integrity of the file. It will lead to you t
he following page.
http://gpg4win.org/package-integrity.html
Note where it says the following statement. The signatures have been created wit
h the following OpenPGP certificate Intevation File Distribution Key (Key ID: EC
70B1B8). This is the link to the page that hosts the PGP public key file that yo
u need to download, go there. On the page we just navgiated to, go to the bottom
right where it says Intevation-Distribution-Key (public OpenPGP key for signing
files) and download that file. This is the PGP public key file, save it to the
same place as your signature file for ease of use.
Okay, now that we have both the signature file and the PGP public key, let us no
w verify our download. First thing you need to do is navigate to the PGP public
key file, called Intervation-Distribution-Key.asc, right click it and go to More
GpgEX Options and down to Import Keys. This will import the PGP public key into
your key ring, and now you can verify the file with the signature.
Right click your actual file you want to verify, in this case gpg4win-2.2.1.exe
and go to More GpgEX Options and down to Verify and it should automatically det
ect the signature file where it says Input File, but if it does not, navigate to
the signature file and make sure the box below it where it says Input file is a
detached signature is checked. Look at the bottom and click Decrypt/Verify and
you will likely get the following message.
Not enough information to check signature validity. Check details.
Believe it or not, this is completely fine. Click on show details, you are looki
ng for a specific result.
Signed on 2013-10-07 08:31 by distribution-key@intervation.de (Key ID: 0xEC70B1B
8). The validity of the signature cannot be verified.
If you navigate back to the page from Gpg4Win that says Check Integrity where yo
u found the link to the page that contained the PGP public key you will see on t
hat page.
Intevation File Distribution Key (Key ID: EC70B1B8)
Note the key ID from your decrypt result and the key ID from the Check Integrity
page and note the email address ending in the same URL that we downloaded the P
GP public key from. We have a match! I will explain the reason for this warning
message later.
Now that we verified that our verification program is legit. Let us try and veri
fy our Tails ISO file, since if we have a compromised Tails OS, then nothing we
do will be anonymous. Let us get right to the Tails download page.
https://tails.boum.org/download/index.en.html
Scroll down to where it says Tails 0.22 signature and download that to your Tail
s folder where you have the ISO file that we already downloaded. Next scroll dow
n to where it says Tails signing key, this is our PGP public key. Exact same pro
cedure, import the key, then click Verify and specify the signature file if it h
as not already been specified for you, exact same settings and you will get the
same warning message. As explained by Tails
Quote
If you see the following warning:
Not enough information to check the signature validity.
Signed on … by tails@boum.org (Key ID: 0xBE2CD9C1
The validity of the signature cannot be verified.
Then the ISO image is still correct, and valid according to the Tails signing ke
y that you downloaded. This warning is related to the trust that you put in the
Tails signing key. See, Trusting Tails signing key. To remove this warning you w
ould have to personally sign the Tails signing key with your own key.
In other words, you need to basically promise that the PGP public key you downlo

aded is safe by signing the PGP public key with your own private key, but we do
not really need to do that and I will not be including a tutorial on how to do t
hat. Tails explains that if you are worried about a compromised PGP public key,
just download the key from multiple sources and compare them, if they all match,
it is a good chance you are using a legit PGP key. Now let us finally move on t
o TOR because this one will be a little less straight forward, but once you do t
his one, you should be able to figure out how to verify anything. Navigate to th
eir download page and find the package that you want.
https://www.torproject.org/download/download.html.en
To keep things simple let us choose Tor Browser Bundle 3.5, and under the orange
box you will see a link (sig). This is the link for the signature file, I hope
by now you know what to do with it. Next we need the PGP public key right? Well
it turns out that with so many developers working on TOR, there are multiple PGP
public keys, and certain bundles were signed with different keys than other bun
dles. So we need to find the PGP public key that belongs to our Tor Browser Bund
le. Check out this page.
https://www.torproject.org/docs/signing-keys.html.en
It has a list of all the signing keys that they use and you can certainly use th
ese key IDs to get what we want by simply right clicking on the signature file a
nd click verify. You will get a warning.
Not enough information to check signature validity. Show Details
And in details it will say the following warning.
Signed on 2013-12-19 08:34 with unknown certificate 0x416F061063FEE659
Keep this entire number in mind for later, it is called a fingerprint. But for n
ow if you just compare the last 8 digits to Erinn Clark’s key ID (0x63FEE659) prov
ided on the above page, and since she is the person who signs the Tor Browser Bu
ndles you will see they match. But we want to be a bit more thorough, never sett
le for mediocrity.
Go to your task bar in Windows, and find the program called Kleopatra, it looks
like a red circle with a small white square in it. Right click it and go to Open
Certificate Manager. We are going to import the full keys using this manager. A
lso note, if you go to the tab that says Other Ceriticates you will find the Tai
ls and Intevation (GnuPG) keys we used earlier stored for the future when you ne
ed to download a new version of those programs and verify them again.
We are going to be following the instructions from the verifying signatures page
on the TOR Project website. Feel free to follow along from that page so you kno
w what I am talking about and where I am getting my URL and numbers from.
https://www.torproject.org/docs/verifying-signatures.html.en
In order to import keys, we need to first add an online directory where they are
stored. So let us first add the online directory where the PGP public keys are
stored according to the TOR website. Click Settings then Configure Kleopatra. Ne
xt, click New and we are going to enter the following URL which I took right fro
m the page above. pool.sks-keyservers.net, and leave everything else as default
and click OK.
Finally, click the button that says Lookup Certificates On Server and we will be
searching for Errin Clark’s PGP public key by searching for her fingerprint provi
ded on the TOR website page called Verifying Signatures above, remember, she is
the developer who signs the Tor Browser Bundle. The fingerprint we are entering
is 0x416F061063FEE659, does this number look familiar? It should, it is the numb
er we got back the first time we tried verifying but without the actual PGP publ
ic key. if you get any warnings that pop up when searching just click OK and it
should bring up Errin Clark’s key, select it and click Import. You should now have
her key listed under Imported Certificates.
Now let us go back and verify that signature one more time and see what happens.
You should get something like the following.
Not enough information to check signature validity.
Signed on 201-12-17 12:41 by errin@torproject.org (Key ID: 0x63FEE659).
The validity of the signature cannot be verified.
TOR also explains this warning message in their words in case you are still not
happy with the warning message.

Quote
Notice that there is a warning because you haven’t assigned a trust index to this
person. This means that GnuPG verified that the key made that signature, but it’s
up to you to decide if that key really belongs to the developer. The best method
is to meet the developer in person and exchange key fingerprints.
I do not know about you, but I am happy with the result here, and I am certainly
not going to track down Erinn Clark to get her key fingerprint, and it looks li
ke our TOR Browser Bundle is legitimate as well! Now you know what to do when th
e PGP public key file is not directly hosted on the site itself, you have no mor
e excuses to not verify your downloads.
VERIFYING SIGNED MESSAGES WITH SIGNATURES AND SIGNING YOUR OWN MESSAGES
inShare
Since we just finished a section on verifying downloads with signatures and publ
ic keys, I figured we should do a quick post on verifying messages by using the
same two things, signatures and public keys.
Now for those of you who are members of the Silk Road Forums, you will notice th
at some people, mainly Moderators like to sign their messages with signatures. L
et us look at an example of a signed message from Dread Pirate Roberts. The last
message he left before going on his leave of absence.
Quote
—–BEGIN PGP SIGNED MESSAGE—–
Hash: SHA512
Silk Road has not been compromised even if the allegations are true. Neither had
access to sensitive material. I will make an announcement later to address the
concerns this has raised.
—–BEGIN PGP SIGNATURE—–
iQIcBAEBCgAGBQJStEgqAAoJEMyyOOR8/t+867AP/RpjCq1B3WSYgnscbZU+UZOy
K0AGMM7tmu1DV1pr2S379YjVxQeUWeTbwDYhaYcWkDBDshnlpSd97fwAL1YVrBQx
jWE08tyo1sd1v5F/HajCx0DC2L5NeqD4UTDd6Dl2AOeBI4pZ+Ah/Q4VoB9cOBQGw
lSbjBY2U4redqBeRd1mFR8N+f3XmxYXzmB4Mf8ddvQkl62HmkwRwA27uUExt73uj
f3/EYVc/XjPgKG345S8yUwcGxLQcfoRM7UosbSGeEaDvvWjfZ6qQw4p7CbqIimHu
IOT6dhFcPmoVdiZGDvjtM3jXfF2sTi5mclGp/4axsrvOWZlCbrobE9EuJnGvscU4
ekU90vtcviES9XEJAr9XGOGgzY/OBf1xpj0iRY7rBDHUqA/FjfSULxqanZYhh0Wn
webHldrjylBRKM0PsnQdPn1CVGj8ThwB6SLfd0WEN1FEQt0hXP3uK1zDOri/fIcJ
Pnvf3jxYNcw9Q+2OW6QpZ/7t+S2E0yiifbNCobAMI18mrynuw3pk/xumg6t2WF/j
YHRpbTfFCCsbiPwR8P9CcUNQ5Iqcc2ewq4GOPx053aL/Vo/nfPdu/9hrRpfF3U5E
J7rFvAStaejxH7/vNxZRrTTiwrrc6njsFJHXWVAJjd+fHLI1efptbc8Kzwms9Yl0
0nzLjAJPFZOv6y7gP8tG
=lDZd
—–END PGP SIGNATURE—–
So why should you care about this? What is the significance of signing a message
? The reason is, in case somebody were to compromise DPR’s account, due to having
a weak password or possibly an exploit in the forum’s coding, then the person woul
d not be able to sign the messages without access to DPR’s private key. So let us
look at how we can verify this message left by DPR. First of all you need to vis
it Dread Pirate Roberts’ profile page and grab his PGP public key. I am not going
to post the key here for space reasons, but just visit his page at the following
URL and import that key into your keyring.
http://silkroad5v7dywlc.onion/index.php?action=profile;u=1
Next, highlight the entire PGP signed message from top to bottom and copy it to
your clipboard (Right click, Copy). You will see your little Clipboard icon in t
he top right of Tails turn red. Click on that clipboard and select Decrypt/Verif
y. You should get the following results. One in the window on top and the other
on the bottom.
Quote
Silk Road has not been compromised even if the allegations are true. Neither had
access to sensitive material. I will make an announcement later to address the
concerns this has raised.

gpg: Signature made Fri 20 Dec 2013 01:37:46 PM UTC using RSA key ID 7CFEDFBC
gpg: Good signature from “Dread Pirate Roberts <silkroad6ownowfk.onion>”
gpg: WARNING: This key is not certified with a trusted signature!
gpg:
There is no indication that the signature belongs to the owner.
Primary key fingerprint: 5A48 F5D0 50E9 9052 62B4 799D CCB2 38E4 7CFE DFBC
Again we get the same warning we did when verifying our downloads, saying we hav
e not verified that the PGP public key is authentic. We can see the signature na
me was made by Dread Pirate Roberts and the comment section has the Silk Road UR
L, so far so good. Now remember when we verified TOR? We wanted to check out the
fingerprints to see if they matched. We do this by going to our key ring (Manag
e Keys), and selecting DPR’s key, right clicking it and going to properties. Now m
ove to the tab Details and look under where it says Fingerprint: and compare the
numbers in there to the numbers we got when we verified the signature. They sho
uld be the following.
5A48 F5D0 50E9 9052 62B4
799D CCB2 38E4 7CFE DFBC
We have ourselves a match! So unless DPR’s private key was compromised, we know th
at he himself was the one who wrote that message. So now you see why some people
decide to sign their messages. It is a way of verifying that their account has
not been compromised by verifying that the person in control of the account is t
he same person that is in control of the PGP private key.
Do you want to learn how to sign a message? It is very easy. Open up gedit Text
Editor and type in a message. Next, select the message and copy it to your clipb
oard (Right Click – Copy) and then click on your clipboard icon up top and choose
Sign/Encrypt Clipboard with Public Keys. Do not choose a key from your list of P
GP public keys unless you want to encrypt the message. If you want to encrypt th
e message to send to somebody’s inbox or so that only one person can view it, then
select their name and it will encrypt it with their PGP public key. In our case
, we just want to sign the message without encrypting it, but you can certainly
do both at the same time if you wanted to.
If you look down near the bottom you will see where it says Sign message as: cli
ck on this and select your personal key. It will ask you for your passphrase bec
ause remember you are signing this with your private key. Once you enter it corr
ectly, the PGP signed message will be copied to your clipboard and you can paste
it anywhere (Right Click – Paste) that you want to. Here it what mine looked like
.
—–BEGIN PGP SIGNED MESSAGE—–
Hash: SHA512
This is my PGP signed message for demonstration purposes.
—–BEGIN PGP SIGNATURE—–
iQIcBAEBCgAGBQJS0GiWAAoJEPuh6tSg81nyqXAP/2mEqvk9RP0FEHZi3edH9faV
OmDoOostmzm90nGMGOOu4cuG0M6jgl7R3hfUZBE6zCh59MG8a9EDuUzpIT3U5nfd
zS0GWtzUQKGXPXfJ1OvWlsA6Sm7TsEsviBBz5DJxyVLcJGNU6OLUVm7onxBLwfTq
D1jAATIB43WJbDrq3XY9MF9GCoOLlcLeKNVa4m0JF582IvQJ05mSZXeXCueImvol
FaflpLW5MKyJJ92a8uheB0pLHUQTLr6jZn6TcfKY9dK8puOam5k2TGut/Sm47uqc
aMA1trXw4xntww/8X4QyL5SbSN7QVOFsy/g0b3Grp5OrConsfnsUoeRH5ArnxY0W
ijPl92aTbZazvXspW2REkJ3yq+fWjuGrYHw8m7/YVBig+OSMuBUXhSE5Pjq95fyM
bA1P7rF2fi7eRsl1z0qyETV3Bs1RltwvBUVIwj3SZNeVVoG5cHgpiPgGFq4S9Qke
unIFeHy3YpBk90kLA1n8n61VnkKAUy0Dt9AoTJloeOqPtcgeKHVsFzxdPCBcSwqd
XYnIx4lNeaw4OvHYgZsCMvFlUItSBGnFWLN9foQ8UybAUPGI9Z4sK2WmtyWK4fLl
cXnYY9zt56Ji4DiVsQrEUamNTQEDGxpvBL/kQKRMKN6HviEXW+qr57LAo6t6sTQw
KTV4uJkH1JxuOOhN9tIe
=Nkox
—–END PGP SIGNATURE—–
And if you want to verify it, check out my PGP public key in my profile and veri
fy my PGP signature against my key! It is really that simple. But you might be a
sking, cannot somebody just change the message and copy the signature? No, chang
ing the message will change the signature because the signature depends on both
the message and the PGP private key. So if you change one single character of my
signed message you will get the following error.

gpg: Signature made Fri 10 Jan 2014 09:39:34 PM UTC using RSA key ID A0F359F2
gpg: BAD signature from “Jolly Roger (They would live and die under it)”
So when should you sign a message? And when should you not sign a message? Great
question. The majority of users should probably not sign messages unless they h
ave to because it gives you plausible deniability. It is easier to deny posting
certain things or certain communications you may have had with vendors or other
people including law enforcement if you do not sign your messages, because you c
an always claim somebody else gained access to your account. It is harder to do
this if you signed the message with your PGP private key. If you are dealing wit
h somebody who wants to verify your identity and make sure that your current sig
nature matches the public key they had on file for you from 6 months ago, then m
aybe they might get you to send a signed message. But again, all they really nee
d to do is send you an encrypted message with your PGP public key they had on fi
le, and if you cannot decrypt it, you are not who you say you are.
In real world application, developers can use PGP signed messages in News Announ
cements or perhaps new releases of their programs providing a download URL so th
at users can be sure the developer is the one posting the URL and not some malic
ious attacker who compromised the forum account of the developer and so forth. S
o for the average Silk Road forum user there really is not a lot of times when y
ou should be signing messages unless you are a moderator or making a public anno
uncement and so forth, but it is an option you now have in your arsenal, and now
you can start verifying the signatures of the Administrators and Moderators in
case you believe their accounts may have been compromised.
AN EXAMPLE OF REALLY BAD OPSEC – SMARTEN UP!
inShare
Guys, I am not going to post exactly who started this thread quoted below, but i
t belongs to somebody who is a senior member with 375 posts. And he posted some
very personal details and probably did not realize how very revealing these deta
ils are.
Quote
Track Me If You Can…
Awesome bit I just watched on Netflix. This is not terribly new, done in 2010, b
ut he is quite thorough in his demonstrating how to disappear in modern US cultu
re.
I do have to add that some of the tech he introduced from the other side is quit
e alarming.
The alphabet cops have waaay too much discretionary income. Time to start defund
ing them.
So why is this revealing? Why is this bad you might be asking. Well, Netflix col
lects metadata on its users just like every other big data corporation. If you a
re a Netflix user, you likely have a profile which keeps track of every movie yo
u have ever watched and what you rated it and so forth.
http://www.usatoday.com/story/theoval/2013/12/17/obama-bidenapple-amazon-twitter
-netflix-yahoo-facebook-microsoft-google/4049305/
Quote
Electronic surveillance and the new health care law are on the agenda as Obama a
nd Vice President Biden meet with a group that includes executives from Apple, A
mazon, Twitter, Netflix, Yahoo, Facebook, Microsoft, and Google.
This user stated, that he just watched a specific movie, that he named. And also
stated that this movie has been up since 2010. So how many people do you think
watched this exact movie in the time frame that this guy stated he watched it? P
robably not too many. Under 100 for sure since the movie has been up for almost
3 years. Well, now the federal government has a list of 100 or less suspects, on
e of which is this particular user on Silk Road.
But maybe he was using a VPN to connect to Netflix? Great…. does he use that VPN f
or anything else? Logging into his email, surfing the web, etc… Even if he used a
VPN, maybe they keep logs? Maybe they are US based and are easily subject to sub

poenas, maybe they will spill everything just like HideMyAss did. We just do not
know, but this is exactly the type of information you all should NOT be reveali
ng about yourselves. This is extremely bad OpSec people. Smarten up!
But then I looked even further through this user’s profile and looked at his posts
. I know which country he lives in, I know which drugs he has imported into his
country and I know which countries he has imported those drugs from. This guy ha
s spoken about cooking drugs, he talks about being in a cold part of his country
, which not all parts of that particular country ever even get cold which helps
law enforcement narrow down that list of suspects they got from Netflix.
If you think that law enforcement is not interested in buyers you are sadly mist
aken. Sometimes if they establish that a buyer has been purchasing from a vendor
that they are after, then busting the buyer can help them get to the vendor. Th
ey may take over the user’s online identity and start ordering things from vendors
since he already has established a trust with these particular vendors. If the
vendor slips up because of the trust built up with the buyer, the vendor is in t
rouble.
I want you all to learn a lesson from this! If you are going to talk about which
vendors you buy off of, which country you live in and which countries you have
imported drugs from, then you better make DAMN SURE you do not start giving away
details like which movie you watched last night on Netflix. That is almost as b
ad as logging onto a server with your real IP address. Keep your mouths shut abo
ut your personal lives!
TOR CHAT
inShare
By now if you have been following this thread, you should know that any type of
messaging system is likely compromised or storing your data for an unknown perio
d of time, and if you ever become a person of interest can be looked back upon f
or 5+ years.
This means things like Gmail, Hotmail, Yahoo Mail, Skype Messaging, Facebook Ins
tant/Private Message, Text Messages, and other forms of communication are all li
kely being monitored to some degree, at the very least logging the meta data. Bu
t you should always treat everything as if those who are monitoring it can read
the content of the email as well.
We have talked about communicating with PGP, we have talked about using TOR and
hidden services, and we have talked about good practices of OpSec. But some of u
s want to be able to instant message somebody else. The good news is, you can do
this with something called TorChat.
TorChat is a decentralized anonymous instant messenger that uses Tor hidden serv
ices as its underlying Network, in other words it communicates over the Tor netw
ork through the .onion URL protocol. This provides end to end encryption that we
talked about in previous posts. It provides cryptographically secure text messa
ging and file transfers for business dealings, and confidential communication be
tween two people. The best news, is that you can use TorChat on your Windows, Li
nux and your smart phones. A French developer released a version for MAC users,
but it still in beta and should be used at your own risk. You can get TorChat fo
r the iPhone in the Apple store, you can get TorChat in the Android Market as we
ll, so you can even use it as a means of text messaging somebody else who also h
as TorChat.
In TorChat, every user has a unique alphanumeric ID consisting of 16 characters.
This ID will be randomly created by Tor when the client is started the first ti
me, it is basically the .onion address of a hidden service. TorChat clients comm
unicate with each other by using Tor to contact the other’s hidden service. For ex
ample, the first time you open TorChat your computer might generate d0dj309jfj94
jfgf.onion and from here on out, d0dj309jfj94jfgf will be your TorChat ID that y
ou give out to people that you want to be able to message you. Here is the home
page of TorChat.
https://github.com/prof7bit/TorChat

http://www.sourcemac.com/?page=torchat – MAC users
Unfortunately at this time, TorChat does not run properly in Tails, so you will
either need to run it on your Windows, Linux or MAC system. It is pretty straigh
t forward, download it, unpack it and run it and everything else should happen a
utomatically for you. Once the avatar beside your TorChat ID turns green, you ar
e online and same with your contacts. You can add contains by right clicking and
choosing Add Contact and just enter their TorChat ID.
At this time there is some people debate as to whether or not TorChat is complet
ely safe, and I would say that TorChat is about as safe as Tor is, just make sur
e you practice the same good practices you are used to. Do not give out personal
information, if you are sending sensitive information use PGP encryption and so
forth.
Here is another article on how TorChat works going into a little bit more detail
. You can access it over the onion network.
http://kpvz7ki2v5agwt35.onion/wiki/index.php/Hacking_TorChat
UPDATE
Another user had some additional input that I overlooked when writing this post
that you should be aware of.
Quote from: ldopa on January 13, 2014, 08:43:25 am
Torchat’s security is unknown. It has not undergone a proper security audit, profe
ssional or otherwise, that I know of. It creates a hidden service on your comput
er leaving you vulnerable to deanonymization attacks that apply to all hidden se
rvices. It also seems to be a very basic protocol that looks like netcat over To
r. There is no way to decline a file transfer. It automatically starts the trans
fer, writing the file to /tmp which is a RAM-mounted tmpfs on Linux. Then you ar
e supposed to save the file somewhere. Theoretically an attacker could transfer
/dev/urandom while you are away from your computer until it fills up your RAM an
d crashes your computer. This would be great for inducing intersection attacks.
Not sure though. If the kernel is managing the system correctly, it may just sto
p the transfer when you run out of RAM.
Another thing is that once someone learns your Torchat ID there is no way to pre
vent them from knowing you are online, even if you remove them from your buddy l
ist. The reason is because your Torchat instance is a hidden service that publis
hes a normal hidden service descriptor which anyone can download. There’s no way t
o stop that. If you want to cut off contact with someone, you have to get a new
Torchat ID. So you should be very conservative about handing out your Torchat ID
and only give it to extremely trusted associates.
OBTAINING, SENDING AND RECEIVING BITCOINS ANONYMOUSLY
inShare
This post was inspired by a user who posted the following on the Silk Road forum
s.
Quote from: dusttodust on January 12, 2014, 07:39:43 pm
BEST WAY TO OBTAIN BTC’S? AND HOW DO YOU PROTECT IDENTIY DONIG SO? i just would li
ke to know so i can get over this bump i been learning all this stuff to do shit
on these sites for a month now and this is my last obsticle i think?!!
We have talked about a large amount of ways to maintain your security, but we ha
ve not really talked about how to actually exchange currency. First thing I want
to say as a disclaimer, is that I am not advocating that you do anything illega
l. This is for educational purposes only and my recommendations are made assumin
g you are exchanging currencies anonymously as a means to protect your own priva
cy.
So you have found something online that you want to buy, and they are asking for
Bitcoins as payment. How do you get the Bitcoins, and how do you get the Bitcoi
ns to them? We are going to explore these options to a degree and hopefully by t
hen you can make an educated decision on which method is best for your situation
.
The options of buying Bitcoins are as follows.

1. Sign up at an exchange online. Some popular exchanges are MT Gox, BTC-E, BitS
tamp and Coinbase
The downside of purchasing Bitcoins at these exchanges, are that you need to ver
ify your identity with them by means of submitting documents such as a driver’s li
cense or passport and a utility bill. If you are able to get past this first obs
tacle, then you need to find a way to get money into the account. Exchanges gene
rally only accept wire transfers as a way to fund your account, but some of them
offer a way of transferring money directly from your bank account. You can obvi
ously see that by doing this you are exposing your true identity to the exchange
s in one way or another, if not at the very least your location.
2. LocalBitcoins.com
LocalBitcoins offers a way for you to find a person in your local area, or if yo
u want to go to another state or province to meet up with someone further away f
rom you, you can choose where to look for people in that area selling Bitcoins e
ither online (bank transfer or cash deposit) or meet them for cash in person. Tr
aders have reputation lists, similar to a feedback score on eBay and you can fin
d a trader who has a good reputation to buy off of. You send in a trade request
and once the seller has received the money, he can release the Bitcoins from Loc
alBitcoins and they are sent to your wallet. Some people have expressed concern
that law enforcement may act as buyers and sellers on LocalBitCoins, but it does
not matter if this is the case in my opinion as long as you are not looking to
buy large amounts. You can also, if you want, communicate with the buyer over em
ail, arrive from public transportation, wear a hat, and all sorts of secret agen
t type tricks to try and conceal your identity. Wear a wig if you are super para
noid.
3. Use a Bitcoin ATM
Currently there is only one ATM in the world that I am aware of, and it is locat
ed in Canada. If you do not live in Canada then this does not help you. Luckily
according to the an article, the company who is rolling out these ATMs called Ro
bocoin is launching ATMs in other countries as well coming soon.
http://techcrunch.com/2014/01/02/robocoin-the-bitcoin-atm-is-heading-to-hong-kon
g-and-taiwan/
Quote
The first shipping bitcoin ATM, Robocoin, is landing in Hong Kong and Taiwan as
the company expands its reach this January. They are planning further releases i
n Europe, Canada, and the US but, given Asia’s clout in the BTC markets, this is d
efinitely an interesting development.
There will likely be some way to try and cut down on money laundering by getting
you to verify your identification, but from what I understand, they currently o
nly do this if you are selling Bitcoins for cash using the ATM, and not buying t
hem for cash. The way that it works, is you choose the amount of BTC you want to
buy, and you feed your cash into the ATM machine. You can at that point either
print out a generated paper wallet, or choose a wallet of your own to send the B
itcoins to. This method may be another good way because it takes dealing with an
other human out of the transaction. Something you may need to be aware of is sur
veillance cameras, so maybe wear a hood, hat, wig, sunglasses, and so forth to d
isguise yourself if you are worried about your identity.
4. Craigslist
Believe it or not, there are a decent amount of people on Craigslist that you ca
n meet up with in person and buy Bitcoins off of with cash. Your local area may
not have a large number of listings, but you can always search in other nearby m
etropolitan areas and make a day trip out of it if you want. The same considerat
ions about protecting your identity apply here as above.
5. Mine your own Bitcoins
I am not going to get into how to mine Bitcoins, or whether or not you should, b
ut if you want to get Bitcoins without dealing with other people, this is one of
the ways you can do it. Run your miners over Tor, stay anonymous and you will h
ave yourself some untainted Bitcoins.
Okay, so now you have yourself some Bitcoins, how can you get them to somebody e
lse that you want to buy something off of or trade with? As you probably know by

now, every single transaction is tracked on BlockChain.info. My wallet address
that I have set up for donations for the hours I have spent working on this thre
ad is 1PkJ928QWC5BuQAsHoNQzRV5wfnveJSRCp. You can check out the transactions rel
ated to it by going to the following address.
http://blockchain.info/address/1PkJ928QWC5BuQAsHoNQzRV5wfnveJSRCp
So you have Bitcoins sitting in your wallet, and if you send them to somebody el
se, it will show up on BlockcChain exactly where you sent them. A couple of thin
gs to keep in mind.
1. You purchased your Bitcoins from somebody or something. They may have kept a
record of the wallet those coins were sent to.
2. If you dealt with a law enforcement or somebody trying to track you, then the
y can track where the coins are sent after you forward them to somebody else.
Right now the best method of trying to lose this trail is using something called
a mixer or a tumbler. You can think of this like throwing your Bitcoins into a
giant pile of coins with other users and then withdrawing them at a later time f
rom the mixer. If you threw in 1 Bitcoin and pulled out 1 Bitcoin, think of all
the other people who did the exact same thing. Possibly thousands of others with
drawing 1 Bitcoin from the exact same pile of coins. It has now become much hard
er for you to be linked to those coins. Then on top of that, maybe you do not wi
thdraw 1 Bitcoin, maybe you only withdraw 0.5 Bitcoin right now and leave the ot
her 0.5 Bitcoin in the pile. It becomes even harder to link those Bitcoins to yo
u.
One website that does this is called BitcoinFog and can be found on a clearnet U
RL and a hidden services URL.
http://www.bitcoinfog.com/
http://fogcore5n3ov3tui.onion/
BitcoinFog has been around for a while now and most people seem happy with the s
ervice they provide, so I would come to think that they are a trustworthy servic
e. The way they work is as I mentioned above, and on top of that the service tak
es 1%-3% (randomized for obscurity) fee on each deposit. So you may put in 1.0 B
itcoins and take out 0.97 Bitcoin after fees and it mixes things up. You can als
o decide when you might want to withdraw it, whether it is in a month, week, day
s, and so forth. This is a good service to use and definitely mixes things up fo
r you. The only thing you need to keep in mind, is that there is a trail of you
sending your coins into BitcoinFog, which some people may or may not find suspic
ious. But what you do with your coins after BitcoinFog is going to be extremely
difficult to track, if not impossible due to the vast number of transactions tha
t are occuring in and out of BitcoinFog.
When you withdraw your coins from BitcoinFog, please make sure you send them to
a new wallet, and not the same wallet that you used to deposit them into Bitcoin
Fog. Another option you can have when withdrawing the coins from BitcoinFog, is
to get BitcoinFog to withdraw the coins directly to the person you want to buy s
omething from. This takes the step of creating a new wallet and then having to f
orward it on and will keep things again extremely hard to track. Just keep their
transaction fees in mind to make sure your desired seller is going to receive t
he correct amount of Bitcoins needed for the purchase or exchange.
Two other options you can use are provided by Blockchain.info and can be accesse
d by creating a wallet and logging in to it. Send Shared and Shared Coin. Send S
hared is another way of mixing up coins, the way that it works is, you send you
r money into the giant pot and it gets matched up with somebody else who is send
ing the same amount. An example of this is let us say we have 4 people. A, B and
X, Y. Person A is sending 1 Bitcoin to person B and person X is sending 1 Bitco
in to person Y. Send Shared will match these amounts together, and it will mix t
hem so that person A sends their 1 Bitcoin to person Y and person X sends their
Bitcoin to person B. This way you are breaking the chain that links person A to
person B because there is no record of person A ever sending anything to person
B. This is a very good option to use, and one that many people prefer. Of course
, there are many people using Send Shared, so the likelihood of there just being
4 people mixing up transaction is going to be more like 10,000 or more, making
it pretty much impossible to track.

Shared coin uses a different method called coinjoin. Shared coin hosts a coinjoi
n server which acts as a meeting point for multiple people to join together in a
single transaction. Having multiple people in a transaction improves privacy by
making transactions more difficult to analyse. The important distinction betwee
n traditional mixing services is the server cannot confiscate or steal your coin
s. A sharedcoin transaction will look something like the following.
https://blockchain.info/tx/e4abb15310348edc606e597effc81697bfce4b6de7598347f17c2
befd4febf3b
As you can see multiple inputs and outputs make the determining the actual sende
r and receiver more difficult. Basically it sends the coins in and out of many d
ifferent wallets that are participating in Shared coin at the time and it does t
his to throw hundreds or thousands of transactions in all the wallets participat
ing making it extremely difficult to track. The downside though is that coinjoin
can never completely sever the link between the input and destination address,
there will always be a connection between them, it is just more difficult to ana
lyse. The benefit to Shared Coin is that while this processing is happening, you
can hit cancel and get your coins back. When you send your coins into a traditi
onal mixing service, an untrustworthy mixing service could potentially steal you
r coins.
Now that you have the knowledge to make an educated decision on how to mix up yo
ur coins en route to your intended destination, I feel that you can now put your
mind at ease when looking to buy something with Bitcoins. It should be noted th
at you can reverse the process if you want to cash out your Bitcoins as well.
CLEARNET VS HIDDEN SERVICES – WHY YOU SHOULD BE CAREFUL
inShare
Some of you may have seen links to different websites on these forums. In fact m
y thread is full of them.
As you probably know by now, a hidden service is a website that uses a .onion ad
dress and a clearnet site uses the regular internet. You must be on TOR to acces
s the onion network, whereas clearnet sites can be accessed from any browser. So
why should you be careful when visiting clearnet sites?
When you see an article, link or video posted on the Silk Road forums, please no
te, that you should only be viewing those videos over TOR or possibly but as a l
ast resort use a VPN and here is why. Let us use YouTube for example. YouTube is
owned by Google, Google tracks everything. YouTube keeps track of which IP addr
esses search for what videos, and tons of meta data about it’s users.
When a link to a YouTube video is posted on the SR forums, we likely have to use
our regular browsers to watch it because Tor browser is not good for watching f
lash videos. But the problem is, if a post on SR was written on January 10, 2014
recommending a video, and this video only has 500 views, perhaps this video has
been up for a few months and did not end up being very popular. And then within
the few days that this article was posted, 50 people viewing the Silk Road foru
m watch this video. The number of views just went up in a short period of time.
It is pretty easy to correlate that it is possible, that the people who watched
that YouTube video, especially since it is not a popular video came from Silk Ro
ad, and if you made the mistake of using your real IP address, you have now been
added to a list of people of interest. And if you do this multiple times with d
ifferent YouTube videos, then they start to see a pattern and before you know it
, they are confident that you are coming to watch these videos from Silk Road be
cause every time a video is posted on Silk Road forums, your IP address comes up
to watch this video.
But if you use a VPN, this makes things a little harder in that they are not as
easily going to be able to link the video to you yet. But once they see a VPN ad
dress constantly popping up on those videos being linked from the forums, they m
ight submit a court order to monitor the activities of the users of the VPN. Hid
eMyAss was one of the most well known examples of VPNs being ordered to hand ove
r information on their users.

The same thing goes with all clearnet sites. You never know who is monitoring th
eir activity, and if it is an old article, more than a couple of years, then you
can almost bet that the number of people viewing that article are down. So when
somebody posts a clearnet link on the forums and people visit that link using a
n unprotected IP address, then the LE can start to correlate patterns against yo
u. Of course, these articles and links are not as likely to be visited without T
OR from the SR forums because you need TOR to view the forums, but especially th
ings like YouTube videos since TOR does not work well with YouTube can be proble
matic.
So what can you do to protect yourself? Ask yourself first, do I really need to
watch that YouTube video? Is it something important that I need to see? If it is
, you might consider an option that I spoke about earlier called Tortilla, but i
t is only available to Windows users. I talk it about it at the following articl
e.
http://silkroad5v7dywlc.onion/index.php?topic=14555.msg304569#msg304569
You will run a Virtual Machine such as Debian, but do not connect to TOR using t
he Virtual Machine. The VM uses a bridged apapter and routes all traffic through
Tortilla which routes all traffic through TOR on your Windows host OS without h
aving to use the TOR browser on your VM. MAC users and Linux users may just want
to view the YouTube video in a one time use proxy that does not keep any logs o
r maybe a public wifi network that has lots of users on it daily.
There is an infamous case of a murderer who called the sister of his victim from
his victim’s cell phone. He would call from her Time Square in New York and taunt
her and talk about how she was torturing her sister and the police put a trace
on the phone. Unfortunately because Time Square is such a crowded place, even wi
th all the cameras, they were unable to pinpoint exactly which person was making
the call on that phone and they never ended up catching the guy. He ended up di
tching the phone after he finally killed his victim. They knew he was a guy walk
ing around Time Square on a cell phone but if you have ever been to Time Square,
you know that there are millions of people doing the exact same thing, he just
blended right in.
So you may want to use a public wifi in a crowded area that has many users all d
ay long to watch a video and keep your IP address safe. If you cannot watch vide
os safely without identifying yourself, then do not watch them. It is as simple
as this. Yes I know it is annoying that Tor does not work well with flash videos
, but it is better than being thrown in jail where you will never be able to wat
ch any YouTube videos.
The main reason I wrote this post was to remind you that correlating two users t
ogether on the internet is easier than you think. Once you start developing patt
erns and leaving your footprints behind, the LE have an unlimited storage space
available to them to keep track of everything you do. Remember how Sabu got caug
ht? He just logged onto IRC with his real IP address, one time. One time is all
it takes for them to take you down. Always think before opening a link, what wil
l this website identify about me?
THEY ARE WATCHING YOU – VIRUSES, MALWARE, VULNERABILITIES
inShare
Your computer will always be vulnerable to some sort of attack from those who wa
nt to harm you in some way. Whether it is harm your privacy, steal your informat
ion or throw you in jail.
It should come to no surprise to us that the US government is actually the large
st purchaser of malware.
Quote
According to a new report, the United States government is now in fact the singl
e largest buyer of malware in the world thanks to the shift to “offensive” cybersecu
rity and is leaving us all vulnerable in the process.
In order for the government to exploit vulnerabilities discovered in major softw
are, they cannot disclose those vulnerabilities to the manufacturers or the publ

ic, lest the exploit be fixed.
“My job was to have 25 zero-days on a USB stick, ready to go,” one former executive
at a defense contractor told Reuters. The defense contractor would purchase vuln
erabilities from independent hackers and then turn them into exploits for the go
vernment to use as an offensive cyberweapon.
http://endthelie.com/2013/05/10/report-us-government-now-buys-more-malware-thananyone-else-in-the-world/#axzz2qIjeZ32e
After reviewing the sources in the article and other articles, some of these def
ense contractors expressed concern that the government was essentially funding c
riminal activity. They are paying independent hackers, in some cases blackhats t
o find zero day exploits (ones that have not been publicly announced yet) and bu
y these exploits off of them for huge sums up money, upwards of $100,000.
If you are using a laptop with a built-in microphone and camera, you are extreme
ly vulnerable to an attack as John McAffee, the man who started McAffee Anti Vir
us explains.
Quote
“We don’t have much [security] anymore, and certainly not in the online world,” he sai
d at Saturday’s talk. “If you can give me just any small amount of information about
yourself, I promise you, within three days, I can turn on the camera on your co
mputer at home and watch whatever you’re doing.”
http://abcnews.go.com/Technology/john-mcafees-product-aims-make-internet-users-v
irtually/story?id=20424182
So the first thing you should do right now is go grab some opaque tape and put i
t over your camera. If you are on a desktop and you have a webcam plugged in, un
plug it unless you are using it. There is no reason to give an attacker an open
window into your home. Next is your microphone, again desktops usually do not ha
ve built in microphones, but most laptops do. A microphone can be activated to l
isten to you talking and you need to find a way to physically disable it. The be
st way of course is to physically remove it, but I am not writing a tutorial on
how to do that.
The FBI developed a keystroke logging software called Magic Lantern. Magic Lante
rn can reportedly be installed remotely, via an e-mail attachment or by exploiti
ng common operating system vulnerabilities, unlike previous keystroke logger pro
grams used by the FBI. It has been variously described as a virus and a Trojan h
orse. It is not known how the program might store or communicate the recorded ke
ystrokes.
Quote
The FBI intends to deploy Magic Lantern in the form of an e-mail attachment.
When the attachment is opened, it installs a trojan horse on the suspect’s compute
r. The trojan horse is activated when the suspect uses PGP encryption, often use
d to increase the security of sent e-mail messages. When activated, the trojan h
orse will log the PGP password, which allows the FBI to decrypt user communicati
ons.
Spokesmen for the FBI soon confirmed the existence of a program called Magic Lan
tern. They denied that it had been deployed, and they declined to comment furthe
r
Source: https://en.wikipedia.org/wiki/Magic_Lantern_%28software%29
Then of course we have cell phones which can be activated remotely as well.
Quote
Mobile phone (cell phone) microphones can be activated remotely, without any nee
d for physical access. This “roving bug” feature has been used by law enforcement ag
encies and intelligence services to listen in on nearby conversations
https://en.wikipedia.org/wiki/Covert_listening_device#Remotely_activated_mobile_
phone_microphones
According to a few of the sources in the Wikipedia article, the cell phone can b
e activated to listen to you even when it is off. Pulling the battery will likel
y do the job, but there is no guarantee. So make sure the phone is not in the sa
me room as you if you are talking about anything sensitive. As always, be super
paranoid. Turn on the shower and put the phone in the bathroom if you have to, o
r better yet if you are going somewhere and you do not need your cell phone, lea

ve it at home. Since most people never leave home without their cell phones, if
somebody is snooping on you, they might think you are still at home. The first g
roup of people that went to visit Snowden in Russia were told not to bring any l
aptops or cell phones with them for those reasons.
So we know the government is actively trying to gain remote access to your compu
ter, they can listen to your phones, what should you do about it ?
You need to do the best you can to make sure the computers that you use are not
exposed to the elements of risk. Always disable Javascript when visiting any web
sites unless the website is 100% trusted. Start phasing out the use of Microsoft
Windows and MAC OSX because these closed source proprietary operating systems a
re not open to scrutiny and auditing the way open source Linux distributions are
. There are more Windows users and thus more exploits available for Windows.
Running your operating system in a Virtual Machine, even if your host OS is Linu
x (remember Virtual Box can run on Linux) will help cut down on the retention of
any malware you might pick up when on the internet. Do not go to any potentiall
y harmful sites on your freedom fighting computers. Do not open any emails from
anyone that you do not trust 100%. Regularly format your hard drives to keep the
m clean of any hidden viruses.
If you are unsure if something is safe, test it on a computer only meant for tes
ting and one that is not connected to the internet. If you can reset your boot s
ector on your hard drive from time to time that would be a good idea as well, be
cause you can get master boot sector viruses that would boot up a virus before y
our computer even boots into the OS.
Flash your BIOS, the BIOS is the first thing that runs when you turn on your com
puter, if you have a virus in your BIOS, there is no antivirus that can remove i
t, you would need to flash your BIOS and install a new firmware. Make sure the f
irmware is 100% trustworthy as infected firmware is the most common way to get a
BIOS virus.
In the interest of saving space I will not go into detail on how to do all of th
ese virus removals because there are numerous tutorials online and I am certainl
y not an expert in this field. I am sure there are many other things I have not
covered in this post and if somebody else wants to chime in, please feel free to
do so as long as you can provide sources for the claims you are making. I do no
t want to turn this thread into a bunch of unsubstantiated claims and paranoid c
onspiracy theories. But if you have something valuable to add to this, I am open
to your input.
MONITORING YOU WITH AN ANTENNA
inShare
First thing I want you to do is find a secure way of watching this video. Rememb
er they log everyone who watches these videos and since I am linking you to them
from Silk Road, they will be watched even closer.
This video shows how using a strong antenna, sitting in a van outside your home,
the FBI could be picking up on your keystrokes on a wired keyboard. In fact man
y people speculate that the new smart meters installed in many homes already hav
e this technology to determine everything you are doing in your home electronica
lly. Wired and wireless keyboards emit electromagnetic waves, because they conta
in electronic components. This electromagnetic radiation could reveal sensitive
information such as keystrokes as shown in the video. Every electrmagnetic wave
is unique to the device using it, which gives a person spying on you the ability
to tell the difference between you using your computer versus the dishwasher.
According to the people who did this experiment, they were able to extend the ra
nge up to 20 meters using relatively cheap technology. This was for wired keyboa
rds by the way, and they go on to explain that wireless keyboards and mouses are
even easier. Which brings us to another area of interest, wireless transmission
s. Things like wireless keyboards and wireless mice (or mouses?) are vulnerable
to eavesdropping as well. If they are not using a strong enough encryption to se

nd data to the receiver, anyone can be listening in on your keystrokes and mouse
activity. Probably something most people never thought about either, this is on
top of the electromagnetic waves that can also be picked up.
Quote
Microsoft has upgraded the weak encryption found on today’s mass-market wireless k
eyboards with a new design that uses 128-bit AES to secure communication to and
from the PC.
Hitherto, keyboard encryption has been weak, with keys chosen from a small palet
te of possibilities, with one hacking group claiming in 2009 that it had develop
ed a tool specifically to sniff keystrokes from Microsoft keyboards at a range u
p to a 10 metres.
http://news.techworld.com/security/3284218/new-microsoft-wireless-keyboard-gets128-bit-encryption/
Are you using wireless technology? How old is it? Might be time to upgrade your
equipment. 10 meters is about 33 feet, but remember the technology available to
the government could potentially reach beyond that. Then there are other things
people forget such as wireless monitors which broadcast your screen to a receive
r that can be picked up. Just think about the old antennas people used to have o
n top of their homes, and how far away those could pick up signals from TV stati
ons, if you had one of those pointed at you in a van across the street, there is
no doubt they could be eavesdropping on your activities inside.
One researcher was able to use a wireless signal sent by a smart meter from up t
o 300 meters away (900 feet) to find out which house it was coming from and what
the current power consumption was in plain text. She was then able to use this
information to determine when people were and were not home based on average spi
kes in consumption since the meters pulse every 30 seconds.
Quote
The data sent was in plain text and carried the identification number of the met
er and its reading. The name of the home owner or the address aren’t included, but
anyone motivated enough could quickly figure out the source.
“The meter ID was printed on the front of the meter we looked at, so theoretically
you could read the ID [off a target meter] and try to sniff packets,” Xu said.
In her tests, Xu found she was able to pull packets out of the air from target m
eters between once every 2 to 10 minutes. That’s fast enough to be able to work ou
t the average power consumption of a house and notice start to deduce when someo
ne is at home.
https://www.networkworld.com/news/2012/110512-smart-meters-not-so-clever-263977.
html
Things like automatic timers that flip switches might be worth investing in to a
lways make it look like someone is home until security researchers start looking
into ways to avoid the wide open door we are giving to anyone who wants to find
data about us.
What can you do about these types of eavesdropping? Not a whole lot unless you w
ant to start turning into a tin-foil hat type of person. There are some fun thin
gs you can do if you want to go crazy with it though as recommended by the follo
wing site.
http://www.lessemf.com/smart.html
Quote
Y-SHIELD
YShield High Frequency Shielding Paint
Easy to apply water-based paint for walls, ceilings, doors and other interior OR
exterior surfaces. Very effective for blocking cell phone signals, CB, TV, AM,
FM signals, radiofrequency radiation and microwaves. Tested highly effective up
to 18 GHz!
http://www.lessemf.com/paint.html#290
There are lots of other things on there as well like drapes, curtains, garments,
fabrics and so forth which disrupt the tranmission of these signals. It is comp
letely up to you what you want to do, I am just giving you the options and the e
ducation so you can make an educated decision of how far you want to go to prote
ct your privacy.

COOKIES & JAVASCRIPT REVISITED, PLUS FLASH COOKIES AND OTHER BROWSER TRACKING
inShare
Your browser can reveal an alarming amount of information about you.
Surprisingly enough, or not too surprising, when you visit a website there is a
surprisingly large amount of identifying data being sent to the website you are
communicating with.
Cookies
Cookies are pieces of information that a web site can send to your browser. If y
our browser “accepts” them, they will be sent back to the site every time the browse
r accepts a page, image or script from the site. A cookie set by the page/site y
ou’re visiting is a “second party” cookie. A cookie set by another site that’s just prov
iding an image or script (an advertiser, for instance), is called a “third party” co
okie.
Cookies are the most common mechanisms used to record the fact that a particular
visitor has logged in to an account on a site, and to track the state of a mult
i-step transaction such as a reservation or shopping cart purchase. As a result,
it is not possible to block all cookies without losing the ability to log into
many sites and perform transactions with others.
Unfortunately, cookies are also used for other purposes that are less clearly in
users’ interests, such as recording their usage of a site over a long period of t
ime, or even tracking and correlating their visits to many separate sites (via c
ookies associated with advertisements, for instance).
With recent browsers, the cookie setting that offers users the most pragmatic tr
adeoff between cookie-dependent functionality and privacy is to only allow cooki
es to persist until the user quits the browser (also known as only allowing “sessi
on cookies”). Tails does this automatically by the way with Iceweasel.
Recent Cookie-Like “Features” in Web Browsers
In addition to the regular cookies that web browsers send and receive, and which
users have begun to be aware of and manage for privacy, companies have continue
d to implement new “features” which behave like cookies but which are not managed in
the same way. Adobe has created “Local Stored Objects” (also known as “Flash Cookies”)
as a part of its Flash plug-ins; Mozilla has incorporated a feature called “DOM st
orage” in recent versions of Firefox. Web sites could use either or both of these
in addition to cookies to track visitors. It is recommended that users take step
s to prevent this.
Managing Mozilla/Firefox DOM Storage Privacy. If you use a Mozilla browser, you
can disable DOM Storage pseudo-cookies by typing about:config into the URL bar.
That will bring up an extensive list of internal browser configuration options.
Type “storage” into the filter box, and press return. You should see an option calle
d dom.storage.enabled. Change it to “false” by right-clicking and choosing Toggle.
Managing Adobe Flash Privacy.
Adobe lists advice on how to disable Flash cookies on their website.
http://helpx.adobe.com/flash-player/kb/disable-local-shared-objects-flash.html.
There are some problems with the options Adobe offers (for instance, there is no
“session only” option), so it is probably best to globally set Local Stored Object
space to 0 and only change that for sites which you are willing to have tracking
you. On the Linux version of Adobe’s Flash plugin there does not seem to be a way
set the limit to 0 for all sites and therefore its use should be limited or avo
ided. Luckily Tails does not have flash installed, but in case you are not using
Tails be aware of this.
If you absolutely need to watch a video online, find a way to download the video
to your computer and watch it that way. This takes the browser out of the loop
of processing a video for you and eliminates those Flash cookies which help iden
tify you.
Javascript
Javascript is probably the grand daddy of all vulnerabilities in internet browsi
ng. The majority of exploits, malware, viruses and other computer take overs hap

pen because of Javascript code executing in your browser. Javascript has many us
es. Sometimes it is simply used to make webpages look flashier by having them re
spond as the mouse moves around or change themselves continually. In other cases
, javascript adds significantly to a page’s functionality, allowing it to respond
to user interactions without the need to click on a “submit” button and wait for the
web server to send back a new page in response.
Unfortunately, javascript also contributes to many security and privacy problems
with the web. If a malicious party can find a way to have their javascript incl
uded in a page, they can use it for all kinds of evil: making links change as th
e user clicks them; sending usernames and passwords to the wrong places; reporti
ng lots of information about the users browser back to a site. Javascript is fre
quently a part of schemes to track people across the web, or worse, to install m
alware on people’s computers. It is best to disable Javascript (about:config in UR
L bar search for Javascript and Toggle it to disabled) unless you absolutely tru
st the site or use the browser add-on NoScripts that comes with Tails and is ava
ilable in Firefox to at least selectively block malicious scripts. Disabling Jav
ascript outright is the best option though, and gumby has added a suggestion tha
t can make it even easier to do this.
Quote from: gumby on January 14, 2014, 08:59:57 pm
Supposedly NoScript doesn’t block all Javascript even when it is enabled and no si
tes are on the whitelist. Not sure about that claim but I’ve seen people make it.
There’s a Firefox add-on (which also works in Tor Browser) called toggle_js which
lets you toggle the about:config javascript.enable parameter through a toolbar i
con so you don’t have to go into about:config. I find it quite useful.
Javascript can also reveal an alarming amount of information about you even if y
ou are using TOR or a VPN, including your browser plug-ins, your time zone, what
fonts you have installed (flash does this as well) and of course most browsers
will send your user agent, meaning they tell the website what browser you are us
ing and in some cases your operating system! Some of these details may not seem
very important, but collected as a whole, it can make it easier to identify who
you are online by almost generating a finger print of you with your specific set
tings related to your browser. Then as you hop around from site to site with you
r finger print, correlations and patterns can be drawn from this and eventually
linked to you if you are not extremely careful.
Luckily, Tails and Whonix overrides the majority of this identifying information
, so as long as you use Tails with Javascript disabled, or at the very least wit
h NoScripts (Flash is disabled automatically) then you can cut down on the amoun
t of information you share. Needless to say, it is not always possible to browse
with Tails, so these are things you need to be aware of when you are browsing w
ith regular browsers on your native OS with your browser of choice.
See what your browser is revealing about you at this page below. Do not visit it
from your real IP address, since this page will be linked to the Silk Road foru
ms from the moment I make this post part of my thread. As a result, you may wish
to search online for other sites that check what information your browser is re
vealing about you. If you are confident in your OpSec abilities, use the one bel
ow.
http://browserspy.dk/
A FEW RECOMMENDATIONS
inShare
Here are a few recommendations that may slip by the average user on these forums
.
1. Never leave your computer that you use for your freedom fighting unattended.
This may seem like a no-brainer, but if you have kids, or a spouse or a sibling
that does not understand what you do on the computer and they decide to hop on y
our account and sign into their email, Facebook or doing things that could compr
omise your location while on that computer because they simply did not know, thi
s could potentially cause you problems.

Maybe you are connecting through multiple layers like this TOR -> VPN(1) -> TOR
-> VPN(2), so that is 4 layers and VPN(2) is the IP address that everyone sees.
Then your child or spouse goes on to their email with that IP address, then sign
s off without your knowledge. That VPN is now linked to you. And we remember how
when under pressure, companies will likely give out information about their cus
tomers to avoid fines, shut downs and prosecution.
2. Do not tell your family members what you are doing, just instruct them not to
touch your computer. Keep it passworded. – You should never tell anyone what you
are doing on your computer because if law enforcement ever did show up, they wou
ld question your family and friends about you. If they honestly do not know, the
n they cannot be held in contempt of court, so it is better to keep them in the
dark. Or maybe the police might scare them into giving up all your secrets becau
se they tell your family that if they do not confess that yourself and them will
be going to jail, possibly for a long time. Just password your computer and nev
er leave it unattended with the screen unlocked.
3. If you use multiple layers to connect, make sure you regularly check to make
sure all your layers are in tact. VPNs can drop sometimes without warning and wh
ile you should never set yourself up so that if one layer drops you lose everyth
ing, just keep in mind when one drops that you may need to adjust the way you ha
ndle yourself online until you get that next layer up. This is one of the reaons
I like Tortilla so much, if my TOR layer does not work, it does not bypass it a
nd go to my next layer, instead it just stops working altogether. When VPNs drop
, your computer bypasses the dropped VPN and moves onto the next layer, which in
some cases could be your real IP address. Just something to keep in mind.
4. Do not use the same password for multiple forums, marketplaces, emails and so
forth. – Expect that one or more of the websites you are registered with is stori
ng your password in plain text. This means that if somebody finds an exploit in
the software and is able to dump the entire database, they can find your passwor
d. And if you used the same password for other sites, and god forbid with the sa
me username as well, your entire list of accounts is compromised. Always use dif
ferent passwords and keep them strong. Do not let anything about your password i
dentify how you choose passwords, or identify anything personal about you.
COLD BOOT ATTACKS, UNENCRYPTED RAM EXTRACTION
inShare
Did you know that even if your system is whole disk encrypted, your data can sti
ll be extracted using something called a cold boot attack? Read on.
The first thing we need to talk about is RAM. RAM stands for random access memor
y. All you need to know about RAM is that RAM is the place in a computer where t
he operating system, application programs, and data in current use are kept so t
hat they can be quickly reached by the computer’s processor. RAM is much faster to
read from and write to than the other kinds of storage in a computer, the hard
disk, floppy disk, and CD-ROM. However, the data in RAM stays there only as long
as your computer is running. When you turn the computer off, RAM loses its data
.
When you turn your computer on again, your operating system and other files are
once again loaded into RAM, usually from your hard disk. RAM can be compared to
a person’s short-term memory and the hard disk to the long-term memory. The shortterm memory focuses on work at hand, but can only keep so many facts in view at
one time. If short-term memory fills up, your brain sometimes is able to refresh
it from facts stored in long-term memory. A computer also works this way. If RA
M fills up, the processor needs to continually go to the hard disk to overlay ol
d data in RAM with new, slowing down the computer’s operation. Unlike the hard dis
k which can become completely full of data, RAM never runs out of memory.
Data can be extracted from the RAM using various tools. When you have a text doc
ument open and you are working on it, you are working from the RAM. Meaning that
if you are working on a sensitive document, that document is temporarily stored
in the RAM and is vulnerable to being extracted while the computer is on. When

RAM is being stored, it is being stored without any form of encryption, making i
t very easy to steal and a huge security risk.
Shutting down a computer through its normal shutdown cycle usually goes through
a process of clearing the RAM. However, if the computer loses power abruptly lik
e in a power outage, the computer does not go through its normal shut down cycle
and some information remains on the RAM chips for a few seconds up to a few min
utes. This is one of the ways cold boot attacks can work.
I also want to quickly introduce a type of RAM to you which will help you unders
tand the rest of this article better. Below is a research paper and they used a
type of ram called DRAM. DRAM stands for dynamic random access memory. DRAM is t
he most common kind of random access memory (RAM) for personal computers and wor
kstations. DRAM is dynamic in that, unlike static RAM (SRAM), it needs to have i
ts storage cells refreshed or given a new electronic charge every few millisecon
ds. DRAM is designed to lose its memory quickly after losing power. Then there a
re subsections of DRAM called DDR. This is a way of making the memory more quick
ly available, but it is not really important to fully understand. Wikipedia can
give you all you need to know about DDR. In this article we are focusing on just
the concept of DDR, DDR2 and DDR3.
These are newer versions of DRAM that keep getting better, and I believe we are
currently up to DDR4. But most computers circulating around today have DDR2 and
DDR3 in them unless they are older computers, this includes laptops. DRAM is kno
wn as a type of volatile memory, it is computer memory that requires power to ma
intain the stored information. It retains its contents while powered, but when p
ower is interrupted, stored data is quickly lost. But how quickly is it lost?
In 2008, a group of researchers wanted to see the practicality of extracting une
ncrypted data from the RAM in your computer. They argued that DRAMs used in most
modern computers retain their contents for seconds to minutes after power is lo
st, even at operating temperatures and even if removed from a motherboard. And b
y using an analysis tool they were able to search for key files (such as PGP key
s) held in the RAM that could be used to decrypt encrypted volumes (drives) on y
our computer. They successfully were able to decrypt volumes using BitLocker, Fi
leVault, dm-crypt, and TrueCrypt. Below is the abstract of their research.
Quote
Lest We Remember: Cold Boot Attacks on Encryption Keys
Abstract Contrary to popular assumption, DRAMs used in most modern computers ret
ain their contents for seconds to minutes after power is lost, even at operating
temperatures and even if removed from a motherboard. Although DRAMs become less
reliable when they are not refreshed, they are not immediately erased, and thei
r contents persist sufficiently for malicious (or forensic) acquisition of usabl
e full-system memory images. We show that this phenomenon limits the ability of
an operating system to protect cryptographic key material from an attacker with
physical access. We use cold reboots to mount attacks on popular disk encryption
systems — BitLocker, FileVault, dm-crypt, and TrueCrypt — using no special devices
or materials. We experimentally characterize the extent and predictability of me
mory remanence and report that remanence times can be increased dramatically wit
h simple techniques. We offer new algorithms for finding cryptographic keys in m
emory images and for correcting errors caused by bit decay. Though we discuss se
veral strategies for partially mitigating these risks, we know of no simple reme
dy that would eliminate them.
https://citp.princeton.edu/research/memory/ [Abstract] http://citpsite.s3-websit
e-us-east-1.amazonaws.com/oldsite-htdocs/pub/coldboot.pdf [Full Text]
Here is an FLV video you can download to watch exactly how they did it.
https://anonfiles.com/file/97b5737dba6b96871fd862b8a587b8f0
This was very troubling to most people, and had many people freaking out when th
e research paper was released back in 2008 because even tough encryption tools l
ike TrueCrypt could be rendered useless with an attack like this. Upon further a
nalysis of the paper, I wanted to note that they used SDRAM, DDR and DDR2, and n
ot DDR3 because it was not available at that time. This prompted TrueCrypt to re
lease the following statement on their website.
Quote

Unencrypted Data in RAM
It is important to note that TrueCrypt is disk encryption software, which encryp
ts only disks, not RAM (memory).
Keep in mind that most programs do not clear the memory area (buffers) in which
they store unencrypted (portions of) files they load from a TrueCrypt volume. Th
is means that after you exit such a program, unencrypted data it worked with may
remain in memory (RAM) until the computer is turned off (and, according to some
researchers, even for some time after the power is turned off*). Also note that
if you open a file stored on a TrueCrypt volume, for example, in a text editor
and then force dismount on the TrueCrypt volume, then the file will remain unenc
rypted in the area of memory (RAM) used by (allocated to) the text editor. This
applies to forced auto-dismount too.
Inherently, unencrypted master keys have to be stored in RAM too. When a non-sys
tem TrueCrypt volume is dismounted, TrueCrypt erases its master keys (stored in
RAM). When the computer is cleanly restarted (or cleanly shut down), all non-sys
tem TrueCrypt volumes are automatically dismounted and, thus, all master keys st
ored in RAM are erased by the TrueCrypt driver (except master keys for system pa
rtitions/drives — see below). However, when power supply is abruptly interrupted,
when the computer is reset (not cleanly restarted), or when the system crashes,
TrueCrypt naturally stops running and therefore cannot erase any keys or any oth
er sensitive data. Furthermore, as Microsoft does not provide any appropriate AP
I for handling hibernation and shutdown, master keys used for system encryption
cannot be reliably (and are not) erased from RAM when the computer hibernates, i
s shut down or restarted.**
To summarize, TrueCrypt cannot and does not ensure that RAM contains no sensitiv
e data (e.g. passwords, master keys, or decrypted data). Therefore, after each s
ession in which you work with a TrueCrypt volume or in which an encrypted operat
ing system is running, you must shut down (or, if the hibernation file is encryp
ted, hibernate) the computer and then leave it powered off for at least several
minutes (the longer, the better) before turning it on again. This is required to
clear the RAM.
* Allegedly, for 1.5-35 seconds under normal operating temperatures (26-44 °C) and
up to several hours when the memory modules are cooled (when the computer is ru
nning) to very low temperatures (e.g. -50 °C). New types of memory modules alleged
ly exhibit a much shorter decay time (e.g. 1.5-2.5 seconds) than older types (as
of 2008).
** Before a key can be erased from RAM, the corresponding TrueCrypt volume must
be dismounted. For non-system volumes, this does not cause any problems. However
, as Microsoft currently does not provide any appropriate API for handling the f
inal phase of the system shutdown process, paging files located on encrypted sys
tem volumes that are dismounted during the system shutdown process may still con
tain valid swapped-out memory pages (including portions of Windows system files)
. This could cause ‘blue screen’ errors. Therefore, to prevent ‘blue screen’ errors, Tru
eCrypt does not dismount encrypted system volumes and consequently cannot clear
the master keys of the system volumes when the system is shut down or restarted.
http://www.truecrypt.org/docs/unencrypted-data-in-ram
A few key points to extract from here are that properly shutting down your compu
ter reduces, if not completely enliminates this risk except in the case of encry
pted system disks. What is meant by this is, for example, if your main operating
system is Windows and you have encrypted that drive, this is your system drive
and the master key for that drive is not cleared upon shutdown or restart. The s
olution is simply to never store anything sensitive on your system volume. Wheth
er you use a partitioned drive or a USB stick that is encrypted, just make sure
that your main drive that is booted into does not contain sensitive data. And if
you have no other choice, then you need to separately encrypt the data inside t
he system volume with a different passphrase and private key so that even if the
y get into your system volume, they cannot access the other encrypted data you w
ant to protect.
They can use these same techniques to sniff around for your PGP private key file
s in the RAM, so this is a very real threat in the case that if your computer is

still powered on if they come to get you, they can use these techniques to retr
ieve data from your computer. However, there is a debate about whether or not th
is type of attack can persist even now into 2014 with newer types of RAM. I poin
t to a random blog online and I make no judgement as to whether or not this is a
legitimate claim, but it is interesting nonetheless.
Quote
Now to test the actual cold-boot attack. Fill memory with around 1000 taint mark
ers, just to be sure there are enough.
Now shut down. Ostensibly, the markers could be recognizable in RAM after whole
minutes, but I’m impatient, so I just waited 10 seconds for the first test. Boot u
p, into the minimal linux installation. Load the kernel module: insmod ./rmem.ko
. Run hunter.
Nothing.
That’s ok, though. There should be at least some data corruption. The default mark
er size is 128 bytes, so let’s set the hamming distance to 128, meaning that one b
it out of every byte is allowed to be flipped. (Statistically, that’s equivalent t
o a 25% corruption rate, since a corrupted bit has a 50% chance of remaining the
same).
Nothing.
Looks like in 10 seconds, memory was completely corrupted. Let’s try a shorter int
erval: 2 seconds. Same results. Nothing is left of our “encryption key”.
http://bytbox.net/blog/2013/01/cold-boot-attacks-overrated.html
The user claimed to be using a newer type of RAM called DDR3. which is known to
hold memory for a much shorter time than DDR2. And a newer research paper releas
ed in September 2013 tried to reproduce the findings of the 2008 research but us
ing computers with DDR1, DDR2 and DDR3 and their findings were interesting.
Quote
Even though a target machine uses full disk encryption, cold boot attacks can re
trieve unencrypted data from RAM. Cold boot attacks are based on the remanence e
ffect of RAM which says that memory contents do not disappear immediately after
power is cut, but that they fade gradually over time. This effect can be exploit
ed by rebooting a running machine, or by transplanting its RAM chips into an ana
lysis machine that reads out what is left in memory. In theory, this kind of att
ack is known since the 1990s. However, only in 2008, Halderman et al. have shown
that cold boot attacks can be well deployed in practical scenarios. In the work
in hand, we investigate the practicability of cold boot attacks. We verify the
claims by Halderman et al. independently in a systematic fashion. For DDR1 and D
DR2, we provide results from our experimental measurements that in large part ag
ree with the original results. However, we also point out that we could not repr
oduce cold boot attacks against modern DDR3 chips. Our test set comprises 17 sys
tems and system configurations, from which 5 are based on DDR3.
https://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=6657268&url=http%3A%2F%2F
ieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D6657268
So what does should you do? Number one, always shut down your computer when you
are not around it or put it into hibernation mode, otherwise your sensitive docu
ments could be lingering around in your RAM. Simply locking the screen will do y
ou no good. Make sure your computer is using a DDR3 type of RAM, if possible. So
me of you this means you need to upgrade. If you are unsure what kind of RAM you
r computer has, search online to find a tool that will detect it for you. Never
store anything sensitive on an encrypted system volume, because this attack can
be used to break into the volume and anything unencrypted can be retrieved. If y
ou are using a laptop, pull the battery out so that if you need to quickly pull
the power, it will turn it off immediately. If you have time, shut down the comp
uter, otherwise turn it off immediately so that it is not running. The more time
you can waste are precious seconds where they cannot retrieve any data. So imme
diately shut things off if you do not have enough time to do a proper shutdown.
Consider putting a lock on your computer case, and if you want to go take it a s
tep further, bolt it to the floor. That way the amount of time it would take the
m to get inside your computer would waste valuable minutes and more than likely
render any recoverable memory useless. Some people have even suggested that you

solder the RAM into the motherboard so they cannot take it out. This may help sl
ow things down, but remember that cooling the memory down can preserve things fo
r quite a while if you are using DDR1 or DDR2. With DDR3, you should be good to
go and I believe with this realization, manufacturers will likely start looking
at ways to encrypt RAM, but until that time you do need to be aware of this as a
possible means for stealing your sensitive data and something you should keep i
n the back of your mind and prepare yourself for just in case.
THE STRENGH OF CRYPTOGRAPHY AND ANONYMITY WHEN USED PROPERLY
inShare
This post is meant to serve as an example of how, when cryptography and anonymit
y is used properly, you can evade just about anybody including the police.
By now, everyone has likely heard of someone getting locked out of their compute
r and being forced to pay by the attacker to have it unlocked, this is CryptoLoc
ker. Dell SecureWorks estimates that CryptoLocker has infected 250,000 victims.
The average payout is $300 each, and millions in laundered Bitcoin have been tra
cked and traced to the ransomware’s money runners.
CryptoLocker is a ransomware trojan which targets computers running Microsoft Wi
ndows[1] and first surfaced in September 2013. A CryptoLocker attack may come fr
om various sources; one such is disguised as a legitimate email attachment. A ZI
P file attached to an email message contains an executable file with the filenam
e and the icon disguised as a PDF file, taking advantage of Windows’ default behav
iour of hiding the extension from file names to disguise the real .EXE extension
. When activated, the malware encrypts certain types of files stored on local an
d mounted network drives using RSA public-key cryptography to generate a 2048-bi
t RSA key pair, with the private key stored only on the malware’s control servers.
The malware then displays a message which offers to decrypt the data if a paymen
t (through either Bitcoin or a pre-paid voucher) is made by a stated deadline, a
nd threatens to delete the private key if the deadline passes. If the deadline i
s not met, the malware offers to decrypt data via an online service provided by
the malware’s operators, for a significantly higher price in Bitcoin.
Dell SecureWorks estimates that CryptoLocker has infected 250,000 victims. The a
verage payout is $300 each, and millions in laundered Bitcoin have been tracked
and traced to the ransomware’s money runners. In November 2013, the operators of C
ryptoLocker launched an online service which claims to allow users to decrypt th
eir files without the CryptoLocker program, and to purchase the decryption key a
fter the deadline expires; the process involves uploading an encrypted file to t
he site as a sample, and waiting for the service to find a match, which the site
claims would occur within 24 hours. Once a match is found, the user can pay for
the key online; if the 72-hour deadline has passed, the cost increases to 10 Bi
tcoin.
To date, no one has successfully defeated CryptoLocker. The Swansea, Massachuset
ts police department was hit in November. The officers paid CryptoLocker’s ransom.
Police Lt. Gregory Ryan told press that his department shelled out around $750
for two Bitcoin on November 10. One of the reasons I am posting this, is that Cr
yptoLocker uses 2,048 RSA encryption, and if you remember in the PGP posts earli
er in this thread I recommended to use 4096. Even with 2,048 bit encryption, no
one has successfully defeated CryptoLocker, and this is the power of properly im
plemented cryptography.
And, using the proper methods of anonymity, this person or group has managed to
acquire, according to research done by ZDNet, around 41,928 BTC.
http://www.zdnet.com/cryptolockers-crimewave-a-trail-of-millions-in-laundered-bi
tcoin-7000024579/
Quote
In research for this article ZDnet traced four bitcoin addresses posted (and reposted) in forums by multiple CryptoLocker victims, showing movement of 41,928 B
TC between October 15 and December 18.
Based on the current Bitcoin value of $661, the malware ninjas have moved $27,78

0,000 through those four addresses alone – if CryptoLocker cashes out today.
If CryptoLocker’s supervillans cash out when Bitcoin soars back up to $1000, like
it did on November 27… Well, $41.9 million isn’t bad for three months of work.
As you can see, properly executed cryptography and anonymity allowed this group
of people acquire the Bitcoin equivalent of almost $42 million in just now 4 mon
ths at the time of this post. I am not recommending or advocating that you do th
is, but just giving you a perfect example of how powerful the combination of the
se two very important factors are in protecting anybody online when used properl
y.
PGP/GPG Email Addresses
inShare
This post was created by HonoluluExpress and posted at the following page and I
have decided to add it to my security thread with his permission. The rest of th
e post is written in his words.
http://silkroad5v7dywlc.onion/index.php?topic=19277.msg383130#msg383130
Over the time I’ve been here I’ve been talking to a lot of people. I have also acqui
red a lot of gpg/pgp keys and I see that LOT of people use there real email addr
esses. I would like to remind everyone that when you give someone your pgp/gpg k
ey THEY CAN SEE THE EMAIL ADDRESS THAT YOU ASSOCIATED WITH THAT KEY. You are NOT
suppose to use ANY type of clearnet email service such as: gmail, yahoo, hotmai
l, etc. If you want to use a valid email address then you need to use an email p
rovider that supports Tor and anonymity. For example I use safe-mail. I’m able to
access this email service on Tor which allows me to stay anonymous. You may also
use an email such as “123@123.com”.
DO NOT UNDER ANY CIRCUMSTANCES ASSOCIATE A CLEAR NET EMAIL ADDRESS WITH YOUR PGP
/GPG KEY. THIS WILL COMPROMISE YOUR ANONYMITY.
Definition of DOX: Personal information about people on the Internet, often incl
uding real name, known aliases, address, phone number, SSN, credit card number,
etc.
ANOTHER SCAM EMAIL – BEWARE
inShare
If you have been following my thread for a while now, you will remember the prev
ious email scam going around trying to get people to download an infection versi
on of tor. With Silk Road at the time of this post now boasting over 25,000 memb
ers, it is easy to get that these occurrences are likely going to increase and u
nfortunately some people are going to fall for them. This new one is directed at
vendors, but it nonetheless should serve as an example of the type of scams tha
t people are going to be trying to pull on members of this forum and other forum
s.
Quote
Dear Valued Vendor,
Due to the recent instability of the site, and our programmers inability to reme
dy the problems in a timely manner, we are going to have to temporarily shut dow
n vendor accounts. Since we can’t just stop operation of the site completely, we a
re forced to develop a way for only some of the vendors to go into a temporary v
acation mode. In need of recent server upgrades, as well as this new method we a
re implementing, it has occured to us that the only way to pick which vendors ar
e going to remain in business is by how much sales/profit they are doing, as wel
l as how much being a vendor on our site means to them. Here’s how this is going t
o work:
If you would like to keep vending on the site during our upgrades/repairs, we ar
e going to require that you pay an additional .3BTC bond to us. If you pay this
.3BTC bond, your account will remain active and you will keep vending while we w
ork to fix the problems. If you do not pay this .3BTC bond, your account will be

temporarily put into vacation mode status and you will be unable to vend until
we locate and remedy the problem. We are very sorry for these changes!
In the event you do pay the bond, as soon as the vending opens back up to everyo
ne, you will have your .3BTC bond returned, and you will receive a premium vendo
r account status. You will have a title on your page that displays you as “Hardcor
e Vendor”. We are terribly sorry we have to ask this of all our hardworking vendor
s, but there is really no other way for us to decide WHO gets to keep vending an
d who has to wait until we fix things.
Our team is working hard at the problem, and we estimate it will be no longer th
an a week for the changes to be made and vending to open back up to everyone.
Vendors who will pay bond: Please send .3BTC to BTC Address: 1NbEs2rJgreRUvjp9o7
hUWo3akeLA3EfFY
Vendors who are unable to pay bond: Your accounts will go into vacation mode at
12:01AM UTC February 2nd.
Let us never forget this recent hurdle in our battle for freedom. But let us not
allow it to stop our fight, either – it is now time to simply pick ourselves back
up, dust ourselves off, and continue fighting this revolution like we’ve never fo
ught it before.
I’m proud to have you all at my side.
Yours Loyally
Dread Pirate Roberts
The user who sent out this message actually used the name Dread Pirates Robert,
which is similar but not correct. One thing you should be aware of, is that any
type of announcement like this from a high ranking Administrator like DPR will a
lways be signed with their PGP signature. And remember, we discussed how to veri
fy these signatures in a previous post. I remember when a moderator named Sarge
was in charge of vendor bonds, there was a user with the name Sarrge (two r’s) tha
t was trying to scam vendors into sending their bonds to his address instead and
unfortunately, several people fell for this scam.
Please always check if there is a PGP signature, and if there is not, kindly ask
the Administrator or Moderator to resend the message to you using a signature.
Protect yourself by verifying the name and make sure this user has an Administra
tor or Moderator status on the forum. Be safe!
AN INTRODUCTION TO AN EXPERT ON OPSEC, PLUS MD5 & SHA-1 CHECKSUMS
inShare
ers to people keeping themselves anonymous online. He goes by the online handle,
“The Grugq”, and Grugq has his own blog which can be found at the following webpage
.
http://grugq.github.io/
It should be noted that Grugq was at one time on the payroll of the US governmen
t for finding and selling zero day exploits. If you remember the previous post a
bout how the US federal government is the singlemost purchaser of malware in the
world, well Grugq was one of those who sold malware to the government. Unfortun
ately for him, when he went public about it, they no longer wanted to buy malwar
e from him because they like to maintain their own anonymity when purchasing the
se exploits. And here is a short biography from an online website.
Quote
Biography:
The Grugq is an Information Security Professional who has has worked with digita
l forensic analysis, binary reverse engineering, rootkits, Voice over IP, teleco
mmunications and financial security. He has reported to be an exploit broker for
15% of the sale. Last but not least, he has also spoken at various security con
ferences.
Facts
He developed “userland exec”
He is the author of Hash (hacker shell), a tool to enable people to evade detect
ion while penetrating a system.

He has released a voip attack software.
Claims to have made mad loot on being an exploit broker (middleman).
https://www.soldierx.com/hdb/Grugq
Why are we talking about the Grugq? Who cares? Well, he has some of the best inf
ormation on keeping yourself anonymous and maintaining privacy online and he is
somebody who you should all familiarize yourselves with. He writes blog posts, a
nd he has done video presentations at security and hacker conferences, with his
most famous presentation, at least in the world of Silk Road being the one he di
d on OpSec. Since I know it is hard for Tails users to watch videos on YouTube,
I decided to download it from YouTube and upload it to AnonFiles.com so you all
can watch it. The presentation is about 1 hour long, and an essential to everyon
e who wishes to maintain their anonymity online. Remember, you only have to scre
w up once.
https://anonfiles.com/file/b6de41da8d1fca2fabf725f79d2a90df
SHA1 Sum: 1a9e6c67a527b42a05111e1b18c7a037744bb51e
MD5 Sum: b6de41da8d1fca2fabf725f79d2a90df
Once you have downloaded the file, I want you to check something called the chec
ksum of the file. The checksum is where the contents of the entire file get plug
ged into a mathematical algorithm and output a specific string. You can see the
two strings above. This is something you should all get into the habit of doing
when possible is verifying the checksum of your files. If you remember when we t
alked about signature files and PGP, this is another method of verifying your do
wnloads but not as good as the signature files. It should however, whenever prov
ided be performed to verify your downloads when the signature file + PGP combina
tion is not available.
Once you have downloaded the file in Tails, the first thing you should do, is mo
ve the file you downloaded to your tmp folder. In order to do this, look up at t
he top and click Places -> Computer -> File System -> tmp. This is where you mov
e the file your downloaded to, and to keep things easier, rename the file grugq.
zip and you will see why you want to do that in a second.
Next we are going to open a terminal window (like a DOS prompt) by clicking the
black rectangle icon in the upper left center area of Tails. Once you have opene
d your terminal window, we are going to perform some Linux commands.
cd /tmp – This will change the current directory you are operating within the term
inal to your tmp folder and allow you to more easily access the files in that fo
lder.
sha1sum grugq.zip – This will perform a SHA1 checksum on the file you just downloa
ded, and you can see why you wanted to rename the file. It should give you the s
ame output as the SHA1 sum listed above.
md5sum grugq.zip – This will perform an MD5 checksum on the file you just download
ed, and is another way of checking the file. SHA1 is better because it is harder
produce the same output twice with different file contents using SHA1 versus MD
5, but nonetheless, use both whenever possible and always check your downloaded
files.
Ok, assuming your downloaded video passed the checksum test, you can be assured
that the video file that I uploaded has not been tampered with, or had any malic
ious code injected into it. When even a single character is changed in the sourc
e code of a given file, the checksum output will be completely different. Most p
eople think it may be off by a a few characters, but the difference is always qu
ite large and is why performing checksums is an important way of verifying your
downloads.
Since you now have a 1 hour video presentation that you all need to watch and re
watch (You can do this in Tails), I will end this post and continue with my next
post from the assumption that you can completed watching this highly recommende
d and endorsed (by SR administrators and moderators) video on OpSec. We will sta
rt looking more into the recommendations from the Grugq. He will be an invaluabl
e resource of information for us, and I will mainly be translating some of his p
osts into a more understandable format for those of you who are less technically
capable and also keeping them on the Silk Road forum hidden services.
—–BEGIN PGP SIGNATURE—–

iQIcBAEBCgAGBQJS7wteAAoJEPuh6tSg81nyhyYP/0nFaWRq0GPe6/5XeMUj3yiZ
2fBaJ+7SXOMxnNXPZw9XAN5Hkpp9wPQmk8W27otuIk2N+iom8H0tJcGZi7hiMd45
Dv0NOrt/gS3bst/G37I+tPwdnWxb1pVNCS+3XnuLOo9IA7VdykU8tz6R+68kPB25
9lDguaUYVeGp2AJMezQ01LL60xQvv25TFLgiPrYD611bscVadckhSV5upXlbMW9+
WVzJG1mgY9gmUYQV6D5ErPGIvxm8cC+IVlzwgGHQPd3kq2QlmQF3XJrXqWGPXd8d
ewkD6VnrU8yO6tVMCG57K1xO9a9zPYp6yN1IOe69IsRkK7g266D+cz6Idwt97/Vr
5jgu1Ook8dfFGA3Sxg+qpoARt5diWKchvmqbxRrnFdOtCAawH1+DgNcVdepi7agk
zhIES1drHdIM1uQ9Wg3vegCLrU3HDpRwwyWoSZxH4kxruU7aByOH5ZdAZw9JV6Lk
b5JzVjrvrhayXwiHPQnnjM50RT9jPH44PhNZCN4G7Ln2Rkb7qa/kS5sA4W2dRwXf
SjtYXf+18pCp/7NL09LD+LsabZHEAa/MilWxjsAnLLIrJsnw3YbSUola/ebmnIq8
oUW20yP0fDOHdeSGVq1uLNZIadZHZtmZIGqBigPU3XAKLxYajssglAgcPxD8E4vc
rkKb3PIyz1k1/JXulymR
=zJvP
—–END PGP SIGNATURE—–
IT IS OBVIOUS WHEN YOU ARE USING TOR
inShare
This is going to be a short post about a mistake we can all learn from when a Ha
rvard student emailed a bomb threat to his school while using tor to avoid a fin
al exam.
http://www.forbes.com/sites/runasandvik/2013/12/18/harvard-student-receives-f-fo
r-tor-failure-while-sending-anonymous-bomb-threat/
Quote
…the student “took steps to disguise his identity” by using Tor, a software which allo
ws users to browse the web anonymously, and Guerrilla Mail, a service which allo
ws users to create free, temporary email addresses.
Despite 20-year-old Eldo Kim’s goal of anonymity, his attempts to mask his identit
y led authorities right to his front door. Does that mean that Tor failed a user
looking to delay his “Politics of American Education” exam? Not in the slightest.
While the Harvard student did indeed use Tor, it was his other sloppy security m
easures that led to his arrest. The complaint says the university “was able to det
ermine that, in the several hours leading up to the receipt of the e-mail messag
es … Eldo Kim accessed Tor using Harvard’s wireless network.”
What Kim didn’t realize is that Tor, which masks online activity, doesn’t hide the f
act that you are using the software. In analyzing the headers of the emails sent
through the Guerrilla Mail account, authorities were able to determine that the
anonymous sender was connected to the anonymity network.
Using that conclusion, they then attempted to discern which students had been us
ing Tor on the Harvard wireless network around the time of the threats. Before f
iring up Tor, Kim had to log on to the school’s wireless system, which requires us
ers to authenticate with a username and password. By going through network logs
and looking for users who connected to the publicly-known IP addresses that are
part of the Tor network, the university was able to cross-reference users that w
ere using both Tor and its wireless internet around the time the bomb threats we
re received.
There is not much for me to add other than the fact that, if you are planning on
doing some freedom fighting, activism or just using Silk Road, make sure that y
ou are able to do so where using tor is not going to raise some flags. In the ca
se of this student, he was likely the only student at Harvard using tor at the m
oment this email was sent, and when the authorities came to his dorm he quickly
admitted he was responsible.
He likely never would have been caught, but remember when you use tor, others ca
n be aware that you are using it. A better idea for him would have been to conne
ct to another computer remotely and have that computer connected to tor to send
the email. This way, they never could have seen his computer connected to tor. I
would not worry about using tor on a regular basis from your home, because ther
e are hundreds of thousands of tor users, but it is again, something to be aware
of. tor will not cover your bad OpSec mistakes like in the case of Eldo Kim.

ARE YOU USING SAFE-MAIL.NET ?
inShare
A recent article on Forbes.com talks about a false sense of security users may h
ave when using Safe-Mail.net
http://www.forbes.com/sites/runasandvik/2014/01/31/the-email-service-the-dark-we
b-is-actually-using/
If you are a user of Silk Road, you have likely seen many users advocating the u
se of a service called Safe-Mail.net. This company describes itself as “the most s
ecure, easy to use communication system”, and many Silk Road users have adopted it
. But there are some things you should be aware of.
Quote
Known users of the Safe-mail web service include operators, vendors and customer
s of the dark web’s many drug market sites, journalists writing about the investig
ation into Silk Road, and BTCKing, the vendor who ran an underground anonymous B
itcoin exchange and allegedly worked with BitInstant CEO Charlie Shrem to sell m
ore than $1 million worth of Bitcoins to users of Silk Road.
When I reached out to Safe-mail for comment, Amiram Ofir, Safe-mail’s President an
d CEO, responded in an email that the company and its employees “certainly are not
aware of any criminal activity,” adding that the company does “follow court orders
that are issued in Israel by an Israeli court. Any other law enforcement agency
should contact the Israeli authorities.” It’s worth noting, however, that Israel sig
ned a Mutual Legal Assistance Treaty (MLAT) with the U.S. in 1998. An MLAT reque
st was used to image the Silk Road web server, according to the criminal complai
nt of Sept. 27, 2013.
Ofir told me that communications between users and the web service are SSL prote
cted, and that information stored on the server is encrypted with user-specific
keys. When asked if Safe-mail has received court orders issued by an Israeli cou
rt on behalf of a non-Israeli law enforcement agency, such as the FBI, Ofir repl
ied with a short “Yes.” My followup email, asking if Safe-mail has the ability to de
crypt information without a user’s key, went unanswered.
So, the first time to note is that the FBI is already aware of Safe-Mail.net and
is already receiving court orders from non-Israeli law enforcement agencies. An
d they are likely giving them everything they need in order to read the emails.
Therefore, you should remember that no email service should be trusted. No email
service is going to go to jail for you. And if you are sending anything sensiti
ve over email using plain text, it will likely be read eventually by somebody ot
her than the intended recipients. This is why things such as strong PGP encrypti
on are essential to any type of sensitive communication.
With this, it should be noted that Safe-Mail is no safer than Gmail when it come
s to protecting your privacy with its centralized email service. Never trust any
company with your privacy, always encrypt.
YET ANOTHER EXAMPLE OF HOW STRONG CRYPTOPGRAPHY AND PROPER OPSEC CAN PROTECT EVE
N PEDOPHILES
inShare
Yes, you read the title correctly. Using the same types of techniques taught in
this thread, you can and should remain anonymous no matter what you are doing.
Pedophiles and child pornographers are some of the most wanted people on the pla
net. They are up there with terrorists and serial killers. They are hunted by fe
deral law enforcement agencies, and punished very seriously, as they should. So
the reason for this post is to demonstrate, that if somebody who is as wanted as
much as pedophiles and child pornographers can remain free by using proper OpSe
c, then you can too.
Quote
If your secure communications platform isn’t being used by terrorists and pedophil

es, you’re probably doing it wrong.
http://grugq.github.io/blog/2013/12/01/yardbirds-effective-usenet-tradecraft/
I want to talk to you about a group of child pornographers that operated for sev
eral years online, called YardBird. During a period of 15 months, there were aro
und 400,000 images and 11,000 videos uploaded to a central server run by the gro
up and shared by the members. The reason we know that, is because during that 15
months, the FBI performed an undercover operation to infiltrate the group in ho
pes of apprehending the members. They successfully apprehended 1 in 3 members of
the group. One of those who remain free to date, was the leader of the group, w
ho also went by the online name YardBird.
How is it possible that after so much effort was put in by the American Federal
Bureau of Investigation (FBI), the Australian Federal Police (AFP) and the Austr
alian Queensland Police Service, that people high up on the wanted lists were ab
le to evade capture. They used strong cryptography, and proper OpSec rules. Let
us now talk about the history of the attempted apprehension of this group.
According to the FBI.
Quote
There were approximately 60 members that were loosely identified, and from the 6
0, approximately 20 were positively identified in this group.
There were numerous challenges presented during Operation Achilles. The group ut
ilized an unprecedented level of organization and sophistication. They had a tim
ed test for prospective new members. They had to use encryption technology and I
nternet-based anonymizers, re-mailing services. They also intentionally corrupte
d their own child pornography files and only the new members knew how to reconfi
gure those files to be able to read the pictures or the video. They also had the
uncanny ability to monitor worldwide news pertaining to law enforcement efforts
in child pornography matters in order to better educate themselves to avoid law
enforcement detection.
https://www.fbi.gov/news/podcasts/inside/operation-achilles.mp3/view
As I said earlier, the alleged leader of this ring used the online name “Yardbird”.
Yardbird made a re-appearance on Usenet in both 2009 and 2010 on the date corres
ponding to the first and second anniversaries of the busts in 2008. His intent w
as to show that he was still free, and to answer people’s questions.
One of the most important things Yardbird stated were that everyone in the group
who used Tor and remailers remained free, while those who relied on services su
ch as Privacy.LI were arrested and convicted. Privacy.li is an offshore VPN serv
ice that promises anonymity. They claim from their website the following.
Quote
If you need corporate and/or military strength encrypted networks, then a Virtua
l Private Network is the way to go. All and any traffic from and to your desktop
are within an encrypted tunnel, and your originating IP-address is well conceal
ed.
http://www.privacy.li/services.html
And their privacy policy makes the following promise.
Quote
Yes, we 101% honor your privacy, no logs, no snooping, no profiling. No legal mu
mbo-jumbo to disguise any hidden efforts. We believe in individualism and privac
y, even anonymity.
http://www.privacy.li/privacy-policy.html
Yardbird further commented that several members of the group, including his seco
nd-in-command Christopher Stubbings (Helen) and Gary Lakey (Eggplant) were Priva
cy.LI users — in fact he stated that they used it for everything. (Helen is curren
tly serving a 25-year sentence in the UK, while Eggplant is serving life in an A
rizona prison.)
Eggplant literally became notorious because of his constant promotion of Privacy
.LI — he continually boasted that he could not be caught because Privacy.LI did no
t keep logs, and they were located outside of U.S. jurisdiction.
Quote
I pointed out to anyone who would listen that services such as Privacy.LI
were for /privacy/ — not for anonymity. In an ideal situation, one needs

both to be private as well as anonymous. Essentially, what Privacy.LI
supplied was a type of VPN service, providing an encrypted tunnel for data
to travel between two endpoints–the customer’s computer being one endpoint, while th
e Privacy.LI servers provided the other. While there was a degree of privacy, th
ere was NO anonymity at all–so it really didn’t come as a surprise that Privacy.LI’s
customers were among those arrested.
http://dee.su/uploads/baal.html
At the end of the day, no service provider is going to go to jail for you. A sim
ple court order can get even the toughest VPN providers to roll over on their us
ers, because they would rather betray a $20 per month user than be fined, shut d
own and possibly thrown in jail for interfering with a federal investigation.
What other mistakes were made to lead to the arrest of some members of this grou
p? The Australian police arrested a man on totally unrelated child pornography c
harges, and presumably as part of a plea deal, he revealed the existence of ‘the
group’ and handed over a PGP public/private keypair and password. Having acquired
from the informer the current group PGP public/private keypair, and its passphra
se meant that the police could assume this group member’s identity, and furthermor
e, read all the encrypted traffic posted by members of the group.
Quote
Once the group was penetrated, the police were able to take advantage of a
few factors:
1) They had the informant’s computer, with all its email, PGP keys and the
like. This provided a history, which made it easier to continue the
impersonation.
2) By the time it was penetrated, the group had been operating for about 5
years. By this time, the group had jelled into a community — people were
familiar with each other, they often let their guards down, and would
sometimes reveal tidbits of personal information. This is especially the
case when they thought their messages were secure, and beyond the ability
of the police to intercept–they would say things that they would *never*
say in the open.
http://dee.su/uploads/baal.html
So it is important to note at this time, that you no matter how comfortable you
become with somebody, there is always a chance that they can become compromised.
In fact, the group has a set of rules, that all members were told to abide by,
and if any member was found to be breaking the following rules, they would be ex
pelled.
Quote
Never reveal true identity to another member of the group
Never communicate with another member of the group outside the usenet channel
Group membership remains strictly within the confines of the Internet
No member can positively identify another
Members do not reveal personally identifying information
Primary communications newsgroup is migrated regularly
If a member violates a security rule, e.g. fails to encrypt a message
Periodically to reduce chance of law enforcement discovery
On each newsgroup migration
Create new PGP key pair, unlinking from previous messages
Each member creates a new nickname
Nickname theme selected by Yardbird
http://grugq.github.io/blog/2013/12/01/yardbirds-effective-usenet-tradecraft/
The ones who got caught, were the ones who did not follow the rules by putting t
oo much trust in their online “friends”. We saw this in the arrest of Sabu when he h
elped the FBI bust his “friends” in LulzSec. If someone is given a deal to cut the a
mount of time spent in prison in half, they likely will take the deal at your ex
pense. Below is an example of a plea versus trying to fight the charges in this
exact case.
Quote
…seven of the U.S. subjects pleaded guilty pre-trial to a 40-count indictment and
received federal sentences ranging from 13-30 years in prison. The remaining sev

en defendants opted for a joint, simultaneous trial. All seven were convicted by
a jury and subsequently sentenced to life in prison.
https://www.fbi.gov/news/podcasts/inside/operation-achilles.mp3/view
13-30 years versus life in prison, may entice even some of the hardest criminals
, and if you think your online “friend” who you have never met in person is going to
keep their mouth shut to keep you out of jail, you are in for a big surprise.
So, as you can see, the group was pretty much an open book to the police. They w
ere completely and thoroughly penetrated. Despite that, however, the majority o
f the group were still able to remain at large, and were neither positively iden
tified nor arrested. This is due to the privacy tools (pgp, tor, nymservers, rem
ailers) that were employed. Even with everything else being an open book, those
using these tools still managed to evade capture. But you may be saying, Ok, I u
nderstand PGP, I understand tor, but what the heck is a nymserver and a remailer
?
In a nutshell, an anonymous remailer is a server that receives messages (in this
case an email) with embedded instructions on where to send them next, and that
forwards them without revealing where they originally came from. A nymserver als
o referred to as a pseudonymous remailer assigns its users a user name, and it k
eeps a database of instructions on how to return messages to the real user. Thes
e instructions usually involve the anonymous remailer network itself, thus prote
cting the true identity of the user.
Some of the advantages of using these services are to protect the intended recip
ient from an adversary, and also protect the sender of the message. Some of thes
e services use what is called a common mailbox, in which all messages are stored
in a central mail box with no “To and From” headers. It is up to the users who use
the service to attempt to use their PGP keys to try and decrypt all of the messa
ges stored in the central message box and see if they can decrypt any of them. I
f they can, this message is intended for them. This way it rules out again, the
sender and receiver. This system of remailers, can also form a chain, in which t
he message is bounced off of multiple remailers before making it to its intended
reicipient to widen the gap between the sender and receiver.
Another effective option some services offer is the ability to delay when the me
ssage gets sent on to the next server in the chain, or the recipient itself. If
you are found to be sending out PGP encrypted traffic through some type of analy
sis at 5:00PM, and another person being monitored receives it at 5:01PM, it is e
asier to correlate that this message may be from you to the other person being m
onitored. At this time I have no recommendations for service to use, but I am li
kely to post about them in the future. In the meantime, let us get back to the r
ing of pedophiles shall we?
Quote
Leaving aside my personal feelings about pedophiles, I brought up this case
as an example for several reasons:
1) Child pornography is a serious crime in virtually every jurisdiction.
As this example demonstrates, police will work together, even across
national boundaries, to investigate these crimes. They are willing
to invest considerable time, manpower and money in pursuit of these
suspects. The only other crimes which usually merit this type of
approach are drug/gun-running or terrorism. The level of effort
expended in pursuing this group can be seen in that even FBI
executive assistant director J. Stephen Tidwell was involved.
Normally one would not expect FBI personnel that highly placed
to be involved — this shows the level of importance placed on
this particular investigation. (A year or so after the busts,
Yardbird himself expressed astonishment that the FBI would
consider his group such a priority.)
2) This case is the only one that I’m aware of, where suspects were
using sophisticated tools like PGP, Tor, anonymous remailers and
nymservers.
3) This case underscores the effectiveness of these tools even against
well-funded, powerful opponents like the FBI, Europol, and Interpol.

(N.B.: FWIW, those who were caught used either inappropriate and/or
ineffective tools and techniques to protect themselves.
4) I fully understand most people’s disgust at the types of crimes/
criminals being discussed here. That said, it is important to
remember that one simply cannot design a system that provides
protection for one class of people, but denies it for another.
You can’t, for example, deploy a system that provides privacy/
anonymity for political dissidents, or whistle blowers, and yet
denies it to pedophiles — either *everyone* is safe, or NO ONE
is safe. This may not be palatable, but these are the facts.
http://dee.su/uploads/baal.html
To summarize. We have seen that even the most hunted criminals, can evade captur
e when using strong cryptography and proper OpSec. The ring leader of one of the
most investigated child pornography rings still remains at large today because
those who followed the rules.
LOCALBITCOINS PART 1 – POLICE ARE WATCHING IT!
inShare
I have a few stories to share from people who used LocalBitCoins to sell their B
itcoins.
Quote
In September and October, I sold 213 BTC (gradually) to some random guy on local
bitcoins. Everything went fine, each time I got the money, I sent the bitcoins.
5 days after the last transaction, I get arrested by the police. “Where does this
money come from?” I explain about bitcoins, and tell them all I know about the ran
dom guy, I volunteer my phone to analyse my emails and check my story. Once they
were sure that the guy contacted me and not the other way around, I was finally
free to go. Later they told me that the money was stolen and they thought I was
doing money laundering.
Now after almost 3 months and a lot of back and forth with the police, they are
now suggesting that I send back the money. I would gladly do that if they arrest
ed the criminal and found out he can not repay. Right now if I send back the mon
ey, the innocent person who got his money stolen gets it back, but then I become
the innocent person who got his money stolen, so that makes no sense to me.
Edit: I just saw a lawyer. According to him I already won the case. But it’s going
to cost me some serious money in lawyer’s fees… More than my cumulated profits. I t
ake that as the cost of a great life lesson and a wake-up call.
He also told me I can disclose the info that the police already knows. So here w
e go. I’m in Brisbane, Australia. The reason the police froze my account and not t
he criminal’s account is that they wanted to know where the money was going. The p
olice are regularly checking my house to make sure the criminal is not seeking r
evenge (he has my full address and I have 2 kids).
http://www.reddit.com/r/Bitcoin/comments/1to08d/arrested_by_the_police_for_local
bitcoins_business/
This guy, likely a BTC miner, was arrested and questioned by police for selling
BTC to a buyer over several transactions. They must have assumed that the buyer
was using fraudulent funds and this shifted suspicion onto the seller as well. I
do not know if this story is true, but I am tending to believe it is. Police ar
e monitoring these transactions, so you better make sure you have a reasonable e
xplanation as to where you obtained the Bitcoins you are trying to sell.
This next story was removed by the original poster (OP), but luckily somebody in
the replies quoted the entire post and therefore I was able to grab it.
Quote
So, as a few of you guys know, I’m moving to another country soon enough. When I g
et over there I won’t have access to my bank account, so a few weeks ago I decided
it might be a good idea to sell some of my BTC for cash. I had done this a coup
le of times before and had a positive experience, so had no whims about doing it
again.

So I received a request from someone who wanted to buy 500euro worth of BTC in a
f2f transaction. I drove down to meeting spot, met the guy, he gave me the 500e
uro and basically ran back to his car and drove off. I obviously found this stra
nge, but it was an escrow tx, so I released escrow from my phone and went back t
o my car.
On my drive back, I noticed that there was a Ford Mondeo behind me (the kind of
car that is usually used by undercover police in my city). It seemed to be follo
wing me, I didn’t have all my paperwork on my car in order, so I decided to take
a detour down some local back-roads and shake it.
So anyways, I lost the car, drove home and thought nothing of this strange encou
nter.
Over the next few days, I noticed strange needle marks and tiny tears in all of
my mail, I also noticed a really strange parked car outside my house one day, wh
en I walked over to it to ask them what they were doing there, they drove off at
speed. I probably should’ve been suspicious then, but I had done nothing wrong an
d shrugged it off.
A couple of days later, I wake up to the sound of my door being smashed in. I ru
n down to find 5 police officers in my house. They showed me a search warrant un
der the misuse of drugs act. The national drugs unit were parked outside with sn
iffer dogs ready, they left after a few minutes though and didn’t come inside with
the dogs. The police told me the person I met on localbitcoins was an undercove
r police officer, and they had copied the registration number off of my car and
got my address from it.
They stripped the whole house down, turned everything upside down looking for dr
ugs. They found 1 joint of weed and they also seized a clock which they thought
was a digital scale (it wasn’t) and informed me that they were going to prosecute
me for intent to supply, even though I wasn’t selling, and I showed them a prescri
ption from a doctor in another country (that isn’t valid here) and told them the s
uperintendant of the local police station had informally told me that they would
n’t prosecute me for possession if it was medical use even though I was technicall
y breaking the law. They also found padded envelopes and accused me of selling d
rugs through the post (a complete lie with no evidence).
They then told me that if I didn’t give them all the messages & phone numbers of e
veryone I had met to sell BTC that they were going to seize all my bitcoin miner
s, computers etc and have them “analyzed”. I was about to move country in the next f
ew days and didn’t want the hassle of having to deal with this, so I told them tha
t I had deleted all the messages (which I did) but that I would be able to get t
hem back if they left my computers there, and that I would co-operate fully (I’m o
bviously not going to co-operate). They then left and I changed my flight date a
nd basically fled the country the next day, luckily I was planning on moving in
a week anyways.
So, a warning to you guys, be careful doing f2f transactions or buying/selling B
TC in general, even though we’re not breaking the law it doesn’t mean you won’t get un
wanted attention from the police.
https://bitcointalk.org/index.php?topic=174918.msg1820363#msg1820363
This story above, I do not know if it is true either, but it is something to thi
nk about. According to the OP, law enforcement wanted all his messages and phone
numbers, obviously to try and find other people involved in money laundering an
d the drug trade. He was scared enough to have deleted the original post, but as
I mentioned, some other people quoted it and I was able to grab it.
To summarize, the police are likely watching these Bitcoin transactions to some
degree and you need to establish a buyer or seller that you can trust. Once you
find a good one, stick with them, even if their rates go up. Try to search for p
eople with established feedback, ask for ID if you want, and make sure you have
nothing incriminating on you, or at your home around the time of these transacti
ons. You never know when you could be trying to offload your BTC to a cop!
LOCALBITCOINS PART 2 – THIEVES, SCAMMERS AND COUNTERFEIT BILLS!
inShare

This post is a continuation from the last one. The threat of being ripped off or
scammed on LocalBitcoin is a very real threat. One that you need to be aware of
.
I want to share a few stories with you.
Quote
Going to keep it short and simple. I live in a major metropolitan city, and do a
lot of business of craigslist. Meet in person, public location, inspect the ite
m, hand cash and be on my way. I’m sure I have 25+ transactions, never been scamme
d.
Today, I saw someone include just as a footnote “I also accept bitcoins”. Not “I only
accept bitcoins” or “plz send bitcoins i mail” just a little footnote that they are fi
ne with it.
Contacted, mentioned purchasing in cash, that was fine, and at the end decided t
o do it in bitcoins. Brought my laptop, public wifi, took a seat at a McDonalds.
Inspected the headphones – Perfect condition, as described, everything was lookin
g good.
He hands me a paper cutout with a wallet address, I key it into blockchain, he i
s looking at the address on screen. I confirm the price (80 USD, was .8xxbtc), h
e says good, I hit send, the little blockchain beep plays over the speakers.
He casually stands up, has the headphones, and walks away. I stand up pretty qui
ck, and shout after to him, accusing him of theft. He says a quick comment aroun
d the lines of “If you can’t pay the price don’t waste my time, I said $80″ and walks ou
t.
I contemplate chasing after him, calling the police, or fuck maybe getting some
public attention, then I realized I didn’t have a leg to stand on.
Cameras would show a guy sitting down at a table, showing me headphones, me insp
ecting them, then playing on a computer for a bit, with him walking off. I attem
pt to accuse him of theft, he probably didn’t even have $80 in his wallet, nothing
would show me handing him cash, and the worst part, as I sat there with a mixtu
re of adrenaline, rage and frustration – is that It was impossible for me to get t
hat money back.
Can you imagine trying to talk to the police about this? So yeah officer, I sent
him bitcoins, a virtually currency for this craigslist transaction, and then he
walks off – Sir, do you have any proof of this? Well, he gave me this address of
random letters, but I swear it’s his, but it isn’t there anymore, it’s gone to a mixin
g service where it gets puYou get the point. I have a decently hard time explaining bitcoins to my eager,
willing to learn friends. I can’t imagine trying to explain it to an officer who t
hinks I just tried to give someone WoW gold for headphones.
So, is there any safety precaution out there I didn’t take, or should you just kee
p BTC and Craigslist as far apart as possible?
Thanks for reading the rant. Sorry for the wall of text. I guess I just kinda ne
eded to get it out there.
http://www.reddit.com/r/Bitcoin/comments/1b89wm/i_just_got_robbed_blind_of_bitco
ins_in_person_im/
Remember, the risk of something like the above happening increases with the amou
nt of Bitcoin being traded for FIAT currency (Government paper or electronic cur
rency). So if you are trying to unload a few Bitcoins to a seller, you may find
yourself in a similar situation from time to time and it is best to prepare your
self in case this happen. Bring a friend with you, have them wait at the door in
case the person tries to run away, or better yet, multiple friends. If you live
in a country or state where it is legal to carry a concealed weapon, then you m
ight want to consider doing this as well.
Quote
A dangerous new scamming trend? £15,000 too close
So it appears that unfortunately scammers have changed their tactics. I have bee
n advised by police not to disclose the username or details of the person concer
ned until their investigation is complete but I am ok to disclose the story as a
warning to others. Today I went to meet a buyer who was looking for £15,000 worth

of bitcoins and wanted to pay in cash but this particular user had a good buyer
history so although cautious I agreed to meet him in London in a place I knew t
here would be CCTV and security for my own safety. Arriving there today in a pub
lic place, all went fine initially from chatting with him but when I pulled out
a quick form to comply with AML’s he seemed very uncomfortable which although I di
dn’t show it, it sent alarm bells ringing in my head as he kind of covered his ID
whilst in terrible handwriting filled out the form and done a completely unreada
ble signature looking nothing like the name. At this point, I was very tempted t
o call the deal off simply because my gut instinct was really telling me to back
out of this but he brought up he had to withdraw another £200 from his bank and s
o I asked him what bank he was with, which was Nationwide, which I am too, so I
went with him to the branch with the cash and forms etc in my bag and said I wou
ld just sit in the branch since it had air conditioning and was only 5 stores aw
ay. In my head at this point, I was trying to get into the branch and see if I c
ould overhear the name he was withdrawing from and also to see if he actually ow
ned the card he had in his hand so I could match the details up with what was on
the form.
Upon arrival at the branch, he handed his card over and the bank teller gave eve
rything a quick glance and asked him for further ID and a security check so whil
st he done that, I thought I would ask the teller next to him who was free if th
ey could put it on their cash counting machine and showed all the relevant docum
entation. The cash went behind the counter when she agreed and put it straight o
n the machine without even looking at the documents surprisingly. Immediately as
this happened, the male buying the bitcoins said to me “What are you doing?” lookin
g terrified and visibly sweating and shaking and I was absolutely certain someth
ing was very wrong at this point and before I could turn to the cashier and ask
her to keep hold of the documents & cash and call security and the police for me
(I was planning to write it on the piece of paper in my hand to be subtle), I h
eard a loud beeping sound from behind the desk which was the cash machine, rejec
ting every note in the pile because they were counterfeit notes, £15,000 worth of
them. As you can imagine, we had 3 security guards onto us in seconds and police
arrived only 2 minutes later and as myself and the other male sat there in hand
cuffs, the police began to ask questions to me and the other male was taken into
another room inside the branch.
Fortunately this day I had my CSV dumps of recent transactions, a letter from my
HMRC communications recently as per my other post and also a bank statement to
verify the recent transactions, plus copies of the emails I had exchanged with t
he male concerned as I bring them to every meeting in my bag for reference purpo
ses if anything arises. Soon enough, having went back to the original place we m
et and reviewing CCTV footage of the whole thing, I was released but they kept e
verything in my bag, all the money of course and frozen my accounts whilst they
investigate which I complied with voluntarily. The male who passed the counterfe
it notes has been taken to the police station and will be in court tomorrow and
I was advised by the Inspector he will probably be referred to the crown court o
n the matter and is being held in custody until his trial.
The bank and police were both present for this and the bank strongly recommended
I be careful in future and transactions that large can be run through the bank
if need be and they can be the third party to sign it and check everything out f
or £35, which will completely cover me for the AML’s over £10,000 and the buyer doesn’t
need to go on the bank records but the bank will verify the ID is real for me in
some branches too. Whilst I was there I also was given a 10 pack of pens to che
ck notes with for future deals and police have asked me to cease trading until t
his case is resolved and be prepared to be asked to come to court to present tes
timony if required.
Again I can’t name and shame the individual due to a police request, but for what
it is worth, that is the story and lesson I have learned from today and despite
the many big deals I have done in the past and the many shady characters, this o
ne has really rattled me up.
https://localbitcoins.com/forums/#!/regional/uk#a-dangerous-new-scamming-tr
So, another recommendation if you are dealing with cash often is to get yourself

some currency detection pens and a black light to check the bills for hidden lo
gos. A quick search online will give you an idea of what to look for in the curr
ency your country uses. Here is one more story about counterfeit money.
Quote
I occasionally trade bitcoins via localbitcoins.com, to ensure that I have a goo
d feel for the liquidity of the market and the ability to exit at will. I’ve never
had any problems before.
Last week, I responded to a request to buy $500 worth of bitcoin, via a local bu
yer here in San Francisco.
Nothing unusual about the meet, or the buyer, other than the fact that he wanted
to find a contact for regular and higher amount buys. I think he was trying to
get me to increase the amount.
Anyhow, I had funded $500 in bitcoins, in escrow with localbitcoins.com and we s
at down to do the trade. He gave me 25 x $20 bills, which I counted. The bills f
elt a bit stiff, like brand new bills from an ATM. I looked at them carefully (o
r so I thought) and they seemed real. I pocketed the money and moved on.
Fast forward three days later, I go out with a friend. Just before leaving the h
ouse, I grab a few $20s and put them in my wallet. At the first bar I paid for a
drink, the bartender cam running out 5 min later into the bar area to find me.
He showed me the bill I had given him, said “this is fake, it fell apart when it g
ot wet”. True enough, the bill had not held up to water like a normal bill. I show
ed him the other money I had on me and he confirmed it was all fake, except for
one $20 I had from before. So I paid for my drink with the real money and left.
For those wondering, the bills are indistinguishable from real $20s unless you k
now exactly what to look for. The smell and texture are slightly off. The most i
mportant clue is that the iridescent “20” on the side that changes from red-green to
black-green depending on the angle you look at it. On the fake bills it does no
t change color.
For my next bitcoin sale, I will be carrying a UV light and pen and will be more
careful in scrutiny of the bills. As always, I will only meet in public and I a
m never unarmed, but now I also have counterfeit detection gear.
Seller Beware – Counterfeit money being passed to bitcoin sellers in San Francisco
Edit: I will be writing an article about this for letstalkbitcoin.com and will p
rovide links to detection tips and products to help with detection. Will also pr
ovide a more detailed story and pictures of the notes. Standby a few days for th
at…
Edit 2: I will be reviewing the following products against these counterfeit not
es, in an upcoming article for letstalkbitcoin.com:
Dri-mark and sharpie brand pens
UV light + magnifying combos
Magnetic testers
http://www.reddit.com/r/Bitcoin/comments/1nj88k/i_was_given_counterfeit_20_bills
_in_exchange_for/
If this is not enough to make you feel a bit uncomfortable, then you need to rea
d them again. But what you can do is simply learn how to inspect bills for authe
nticity. Again, get yourself a handheld black light, a currency marker and anyth
ing else that applies to your country’s currency and you can likely protect yourse
lf against this. If the person buying the Bitcoins off of you seems nervous, or
like they are in a hurry to get away, then take greater caution with this buyer.
Always try to find buyers with good feedback (although this is not perfect), po
ssibly ask for ID if you would feel more comfortable, and bring a friend with yo
u, but do not make it obvious that you brought a friend with you. Getting scamme
d, robbed or ripped off sucks, and you need to do whatever you can to avoid it h
appening to you.
LOCALBITCOINS PART 3 – MORE SCAM STORIES
inShare
This post is more stories about people being scammed or robbed on LocalBitcoins.

Quote
AmbysWorld:
just got robbed in Oklahoma City – Edmond, a kid about 20 years old, brownish-blon
de hair, 6 ft tall, 150-160lbs
$950.00 –
be careful doing bitcoin trades. I know it’s tough to get trust, so my advice is
start small and after you have gained trust, make sure the money is in your pock
et before you release the coins!!
I guess it is just the price to pay to learn a lesson.
realestone:
can you give more details what happened exactly?
AmbysWorld:
We met, inside a coffee shop, introduced myself, asked him if he had done trades
before. He said he had done several. I wanted to make sure he was familiar wi
th how the site worked and then to see if he had any questions about bitcoins in
general. I released the coins, and we started to shake hands as he was handing
me the envelope. He jerked the envelope out of my hand and took off running.
Every person I have met has been awesome and excited about bitcoins. So I let m
y guard down. Showed up wearing flip flops. I started to pursue after he had a
lready taken 3 steps, but then realized I would not be able to run in flippers f
or very long and stopped after about 100 yards.
The worst part is that I had my 14 year old daughter with me. There is a specia
l place in hell for people like this!
https://bitcointalk.org/index.php?topic=288053.0
Here is a story from a group of people trying to test out LocalBitcoins for the
first time and ended up losing their Bitcoins due to their own ignorance. But th
e buyer could have done the right thing, and did not.
Quote
Bitcoin in hand, we decided to take a look at Localbitcoin and see how easy the
system is for someone who does not know the lingo and does not have much experie
nce with computers to see, what the difficulties could be.
So we found a buyer and proceeded to do an exchange of a small amount of Bitcoin
s. Everything looked great at first as we signed up, got verified and then proce
eded to transact with the trader. We sent our Bitcoins and where confronted with
some windows which began to confuse our tester, who mistakenly confirmed the tr
ansaction, minutes after sending the Bitcoins. Our tester was not sure if they n
eeded to click the confirmation to advise the trader that the coins where sent,
so spent some time in the FAQ to find out what to do next. No information was fo
und by our tester, who then guessed that since there was no mention of it, then
it must be a trivial issue and confirmed the transaction anyway. What happened n
ext worried out tester as the transaction was marked as closed and they had sent
the Bitcoins to the trader without knowing if the fiat money would be deposited
into the bank account. We waited 24 hours to confirm a cash transaction into a
designated account and lo and behold, its not there.
Next we proceeded to contact the trader and as of writing, we have not heard fro
m them. We contacted Localbitcoin support and began a ticket. Shortly afterwards
, we received an email from Localbitcoin support staff and explained the situati
on and where told that the confirmation did need to be done AFTER we confirmed t
he funds had been placed into our designated account by the trader.
After a few emails to the support staff, we did explain that we where testing th
e system useability for the everyday mom and pop situation, because if Bitcoin i
s to be used properly, it needs to have an easy (dumbed down) system so the inex
perienced user can make a trade without making mistakes like our tester did.
http://mentaso.com/bitcoin-news/item/224-localbitcoins-scammed-on-our-first-test
-of-the-system.html
This next one is an attempt at a phishing scam. A phishing scam is when somebody
sends you to a URL that looks like the real URL, but it is actually set up so t
hat when you login, it steals your login credentials and the attacker takes over
your account. In this case, take over the LocalBitcoin account and steal the Bi
tcoin

Quote
User requested nearly $2k CAD worth of bitcoins using my localbitcoins ad.
Immediately asked to move the conversation to text messaging, asked me “how many c
oins I have in there (localbitcoins wallet)” then (after some dawdling and chitcha
t) asked me to “check out and read his other localbitcoins ad first”.
Included was a URL to localbitcoinis.com with an ad url long enough I know this
was copy/pasted and not a typo.
A quick WHOIS reveals a domain by proxy, but some google-fu on the contact telep
hone number registered to the domain reveals that domains related to this phone
number have been involved in other scams.
http://bitcoinviews.com/scam-alert-localbitcoinis-com-scammer-contacting-localbi
tcoins-com-users/
Luckily for the seller, he did not fall for the scam. But anybody not careful en
ough could fall victim to this scam. Always make sure you read the url closely.
LOCALBITCOINS PART 4 – SELLERS BUSTED FOR MONEY LAUNDERING
inShare
Here is a simple copy and paste story you should be aware of:
Quote
State authorities in Florida on Thursday announced criminal charges targeting th
ree men who allegedly ran illegal businesses moving large amounts of cash in and
out of the Bitcoin virtual currency. Experts say this is likely the first case
in which Bitcoin vendors have been prosecuted under state anti-money laundering
laws, and that prosecutions like these could shut down one of the last remaining
avenues for purchasing Bitcoins anonymously.
Working in conjunction with the Miami Beach Police Department and the Miami-Dade
State Attorney’s office, undercover officers and agents from the U.S. Secret Serv
ice’s Miami Electronic Crimes Task Force contacted several individuals who were fa
cilitating high-dollar transactions via localbitcoins.com, a site that helps mat
ch buyers and sellers of the virtual currency so that transactions can be comple
ted face-to-face.
One of those contacted was a localbitcoins.com user nicknamed “Michelhack.” Accordin
g to this user’s profile, Michelhack has at least 100 confirmed trades in the past
six months involving more than 150 Bitcoins (more than $110,000 in today’s value)
, and a 99 percent positive “feedback” score on the marketplace. The undercover agen
t and Michelhack allegedly arranged a face-to-face meeting and exchanged a singl
e Bitcoin for $1,000, a price that investigators say included an almost 17 perce
nt conversion fee.
According to court documents, the agent told Michelhack that he wanted to use th
e Bitcoins to purchase stolen credit cards online. After that trust-building tra
nsaction, Michelhack allegedly agreed to handle a much larger deal: Converting $
30,000 in cash into Bitcoins.
Investigators had little trouble tying that Michelhack identity to 30-year-old M
ichell Abner Espinoza of Miami Beach. Espinoza was arrested yesterday when he me
t with undercover investigators to finalize the transaction. Espinoza is charged
with felony violations of Florida’s law against unlicensed money transmitters – whi
ch prohibits “currency or payment instruments exceeding $300 but less than $20,000
in any 12-month period” — and Florida’s anti-money laundering statutes, which prohibi
t the trade or business in currency of more than $10,000.
Police also conducted a search warrant on his residence with an order to seize c
omputer systems and digital media. Also arrested Thursday and charged with viola
ting both Florida laws is Pascal Reid, 29, a Canadian citizen who was living in
Miramar, Fla. Allegedly operating as proy33 on localbitcoins.com, Reid was arres
ted while meeting with an undercover agent to finalize a deal to sell $30,000 wo
rth of Bitcoins.
Documents obtained from the Florida state court system show that investigators b
elieve Reid had 403 Bitcoins in his on-phone Bitcoin wallet alone — which at the t
ime was the equivalent of approximately USD $316,000. Those same documents show

that the undercover agent told Reid he wanted to use the Bitcoins to buy credit
cards stolen in the Target breach.
Nicholas Weaver, a researcher at the International Computer Science Institute (I
CSI) and at the University of California, Berkeley and keen follower of Bitcoinrelated news, said he is unaware of another case in which state law has been use
d against a Bitcoin vendor. According to Weaver, the Florida case is significant
because localbitcoins.com is among the last remaining places that Americans can
use to purchase Bitcoins anonymously.
“The biggest problem that Bitcoin faces is actually self-imposed, because it’s alway
s hard to buy Bitcoins,” Weaver said. “The reason is that Bitcoin transactions are i
rreversible, and therefore any purchase of Bitcoins must be made with something
irreversible — namely cash. And that means you either have to wait several days fo
r the wire transfer or bank transfer to go through, or if you want to buy them q
uickly you pay with cash through a site like localbitcoins.com.”
One very popular method of quickly purchasing Bitcoins — BitInstant — was shuttered
last year. Last month, BitInstant CEO Charlie Shrem was arrested for money laund
ering, following allegations that he helped a man in Florida convert more than a
million dollars in Bitcoins for use on the online drug bazaar Silk Road.
It’s still unclear how the defendants Espinoza and Reid were able to obtain so man
y Bitcoins for sale, although a review of Michelhack’s profile suggests little mor
e than arbitrage — that is, buying Bitcoins for $700 apiece and selling them for a
couple hundred dollars more.
There is nothing that links either defendant to the Silk Road trade. But it’s nota
ble that a third individual charged with money laundering as part of this invest
igation — 28-year-old Canadian citizen Vincente Loyola — is currently serving a 12-m
onth sentence at a U.S. federal detention center for narcotics trafficking.
In any case, Weaver said he anticipates that more states will soon seek to crack
down on high-dollar Bitcoin sellers on localbitcoins.com. “I’d expect many more sta
te cases like this one because it will act to strangle the lifeblood of the onli
ne dark markets,” such as Silk Road, Weaver said. “If you want a significant amount
of anonymous Bitcoins, right now this community is about the only mechanism stil
l available.”
News of the Florida actions comes on the heels of the arraignment of Ross Ulbric
ht — the alleged onetime owner of the Silk Road. Ulbricht was scheduled to be arra
igned in New York today.
The court documents in this case also offer a great example of the traceability
of Bitcoin transactions — a potential danger for both those seeking anonymous paym
ents and for law enforcement officials posing as criminals as part of an underco
ver investigation. The ICSI’s Weaver noted that, by examining the times and transa
ctions in the criminal complaint, it appears that this is the Bitcoin wallet ass
ociated with the undercover officer.
https://krebsonsecurity.com/2014/02/florida-targets-high-dollar-bitcoin-exchange
rs/
As you can see, the cops are watching LocalBitcoins. Laundering Bitcoins is like
laundering real money. You need to have a way to justify where the money came f
rom. Back in the day, the Mafia had small legitimate businesses it would run tha
t it could claim as an income, and they might fix the numbers a bit and say they
made more money than they really did. This would provide an income they could u
se as a reason for having money. If you are somebody who does not work, and only
sell drugs on Silk Road, and are trying to cash out your coins, then I hope you
have a legitimate reason for holding that many BItcoins, otherwise you could en
d up like these two guys.
HIDING TOR FROM YOUR ISP – PART 1 – BRIDGES AND PLUGGABLE TRANSPORTS
inShare
This post is going to talk about something that has been commonly discussed on t
he forums recently. How can I hide my tor usage from my ISP ?
People are more worried about hiding their tor usage from their ISP, than hiding

it from a VPN. There seems to be a back and forth debate about whether using a
VPN will or will not protect you. Whether or not the VPN can be convinced to log
your connection, and so forth. A few of my previous posts regarding LulzSec an
d the YardBird pedophile rings have shown that those who rely on VPNs to protect
them are historically known to end up in jail. Even our friend we were recently
introduced to, The Grugq says, TOR -> VPN is ok, but VPN -> TOR, go to jail.
In my previous posts about VPN -> TOR and TOR -> VPN, I tried to remain neutral
in that you should be able to make your own decisions about how you wish to prot
ect yourself. But just remember, at the end of the day, nobody is going to go to
jail for you. If you simply want to hide the fact that you are using tor from y
our ISP, then we have other options than a VPN. We have bridges, and several dif
ferent pluggable transports. What are these, and how can we use them in Tails?
Quote
What bridges are and when to use them
When using Tor with Tails in its default configuration, anyone who can observe t
he traffic of your Internet connection (for example your Internet Service Provid
er and perhaps your government and law enforcement agencies) can know that you a
re using Tor.
This may be an issue if you are in a country where the following applies:
1. Using Tor is blocked by censorship: since all connections to the Internet are
forced to go through Tor, this would render Tails useless for everything except
for working offline on documents, etc.
2. Using Tor is dangerous or considered suspicious: in this case starting Tails
in its default configuration might get you into serious trouble.
Tor bridges, also called Tor bridge relays, are alternative entry points to the
Tor network that are not all listed publicly. Using a bridge makes it harder, bu
t not impossible, for your Internet Service Provider to know that you are using
Tor.
https://tails.boum.org/doc/first_steps/startup_options/bridge_mode/index.en.html
The first thing we are going to do is get some bridges. Let us do this before we
configure Tails to use bridges, because once Tails is in bridge mode, we will n
ot be able to connect to tor without working bridges. So the first thing we want
to do is visit the following webpage.
https://bridges.torproject.org/bridges
Enter the impossibly difficult captcha, and click “I am human”, and you should get a
list of bridges that look like this. These are actual bridges pulled from the t
or bridges page.
Quote
5.20.130.121:9001 63dd98cd106a95f707efe538e98e7a6f92d28f94
106.186.19.58:443 649027f9ea9a8e115787425430460386e14e0ffa
69.125.172.116:443 43c3a8e5594d8e62799e96dc137d695ae4bd24b2
These bridges are publicly available on the Tor Project website, so they may or
not may be the best choice to use, but they are a good start. Another option is
to send an email to bridges@bridges.torproject.org with a message in the body sa
ying “get bridges” without the quotes. This will only work if sent from a Gmail acco
unt or Yahoo, unfortunately. If you want to use this, set up the email account u
sing tor and you will receive a list of around 3 bridges shortly thereafter. Sa
ve them somewhere you can use them the next time you boot up Tails, or write the
m down.
Ok, so now we have our bridges. How do we use bridges in Tails? This is an optio
n we need to activate when we boot up Tails. To activate the bridge mode, we wil
l be adding the bridge boot option to the boot menu. The boot menu is the first
screen to appear when Tails starts. It is the black screen that says Boot Tails
and gives you two options. 1. Live, 2. Live (Fail Safe). When you are on this sc
reen, press Tab and a list of boot options will appear in the form of text at th
e bottom of the screen. To add a new boot option, add a Space then type “bridge” wit
hout the quotes and press enter. You have now activated bridge mode.
Once Tails boots up completely, you will get a warning that you have entered bri
dge mode and not to delete the default IP address in there, which is 127.0.0.1:*
. This is advice we will follow, so just click OK and the settings window for to

r will pop up. At this point you need to add your bridges. So you are going to t
ake the three bridges you got, and enter the IP address and the port. If we were
going to use the example above this is what we would enter.
Quote
5.20.130.121:9001
106.186.19.58:443
69.125.172.116:443
For each bridge you add, type it in the available text box where it says “Add A Br
idge” and then click the green + button to add that bridge. You will need to add o
ne bridge at a time. Once you are finished adding your bridges, you can click OK
. At this point, your yellow tor onion icon in the top right should turn green s
hortly after and you will be connected to the tor network using a bridge. Again,
since these bridges are less likely to be known by your ISP, they are less like
ly to know that you are using tor when you use bridges.
You may wish to look up your bridge before you use it however. Maybe you want to
find out where your bridge is located, maybe you want to see who is hosting the
bridge, and you can do this by looking for a IP look up service online, by doin
g a search and typing in the IP address. The three listed above are located in t
he following locations.
Quote
5.20.130.121 – Country: Lithuania
106.186.19.58:443 – Country: Japan
69.125.172.116:443 – Country: New Jersey, United States
And with that, you can decide which bridge would be a better choice for you to u
se. I suggest however, that you go and get new bridges and do not use the ones I
listed above for obvious reasons that they are now linked to Silk Road users by
me posting them on this forum. I should note that the way bridges hide the fact
that you are using tor from your ISP, is that you are connected to an IP addres
s that is likely not known to your ISP to be affiliated with tor entry nodes.
While bridges are a good idea, unfortunately they may not be enough. According t
o Jacob Applebaum, (a tor developer) bridge traffic is still vulnerable to somet
hing called DPI (deep packet inspection) to identify internet traffic flows by p
rotocol, in other words they can tell you are using tor by analyzing the traffic
. While tor uses bridge relays to get around a censor that blocks by IP address,
the censor can use DPI to recognize and filter tor traffic flows even when they
connect to unexpected IP addresses. This is less likely to be done by your ISP,
and more likely to be done by the NSA, or other oppresive governments like in C
hina and Iran, so you can choose if this is an issue for you.
Quote
Lately, censors have found ways to block Tor even when clients are using bridges
. They usually do this by installing boxes in ISPs that peek at network traffic
and detect Tor; when Tor is detected they block the traffic flow.
To circumvent such sophisicated censorship Tor introduced obfuscated bridges. Th
ese bridges use special plugins called pluggable transports which obfuscate the
traffic flow of Tor, making its detection harder.
https://www.torproject.org/docs/bridges#PluggableTransports
Pluggable transports are a more new, but less talked about technology being impl
emented by tor to disguise the fact that you are using tor to your ISP and other
censors. As mentioned above, it attempts to transform your tor traffic into inn
ocent looking traffic that would hopefully be indistinguishable from normal web
browsing traffic. Currently the most popular pluggable transports are obfuscated
bridges. Obfuscation by definition, is the hiding of the intended meaning in co
mmunication, making communication confusing, wilfully ambiguous, and harder to i
nterpret. Obfuscated bridges actually transform the traffic to look like random
packets of data. Obfuscated bridges currently have 2 protocols.
1. obfs2
2. obfs3
Obfs2 (The Twobfuscator) is talked about at length at the following official pag
e.
https://gitweb.torproject.org/pluggable-transports/obfsproxy.git/blob/HEAD:/doc/

obfs2/obfs2-protocol-spec.txt
But for the laymans out there, basically obfs2 uses a protocol that disguises yo
ur traffic to look like random data, whereas tor has a more distinct structure t
o it. However, it should be noted in the case of obfs2, that if an attacker snif
fs the initial handshake between your computer and the obfuscated bridge, they c
ould get the encryption key used to disguise your traffic and use it to decrypt
the disguised traffic which would reveal it as tor traffic. They would not be ab
le to decrypt your tor traffic, but they would be able to see you are using tor.
This is not likely something your ISP would do, but it may be something law enf
orcement or the NSA would do. So if you are only worried about your ISP, then ob
fs2 would likely suffice.
Obfs3 (The Threebfuscator) is talked about at length at the following official p
age.
https://gitweb.torproject.org/pluggable-transports/obfsproxy.git/blob/HEAD:/doc/
obfs3/obfs3-protocol-spec.txt
Obfs3 uses a very similar protocol to disguise your traffic as obfs2, however it
uses a more advanced method of an initial handshake called the Diffie Hellman k
ey exchange. They however found some vulnerabilities in the protocol and had to
go a step further and customize the Diffie Hellman key exchange to make it an ev
en more robust method of establishing that initial handshake. Using obfs3 would
be a better bet to disguise your traffic if your adversary is the NSA or other l
aw enforcement.
So how do you get these obfuscated bridges? They are not as easy to get, but the
y can be obtained from tor through email. However, you need to request those bri
dges specifically to get them. You need to use a Gmail or Yahoo account and send
an email to bridges@bridges.torproject.org and enter in the body of the email “tr
ansport obfs2″ without the quotes, and for obfs3, simply enter “transport obfs3″. Plea
se note that you can only send one request to tor per email, every 3 hours. Whic
h one you should use, is entirely your choice, I am just giving you the informat
ion necessary to make an informed choice. Enter them in this format so that Tail
s knows which protocol to use.
obfs3 83.212.101.2:42782
obfs2 70.182.182.109:54542
tor also provides a few obfuscated bridges on their home page which you can use
as well, and I will list them below. If you send a request to tor and get a resp
onse containing bridges without obfs2 or obsf3 at the beginning of the lines, th
en these are normal bridges, not obfuscated, and they are likely to be out of ob
fuscated bridges at the moment. You will have to try again another day. So if yo
u get a response with bridges that are without obfs2 or 3 at the beginning of ea
ch line, please again, be aware these are normal bridges, unlike the ones below.
obfs3 83.212.101.2:42782
obfs3 83.212.101.2:443
obfs3 169.229.59.74:31493
obfs3 169.229.59.75:46328
obfs3 209.141.36.236:45496
obfs3 208.79.90.242:35658
obfs3 109.105.109.163:38980
obfs3 109.105.109.163:47779
obfs2 83.212.100.216:47870
obfs2 83.212.96.182:46602
obfs2 70.182.182.109:54542
obfs2 128.31.0.34:1051
obfs2 83.212.101.2:45235
I have a feeling that some of you reading this will be inclined to go out and ge
t yourself some obfs3 bridges right away, because you think they are the best ch
oice out there for staying anonymous. And right now they have the potential of b
eing what you hope for in that regard, except for one huge flaw. The number of o
bfs3 bridges is small. Last report I read put it at around 40 bridges running ob
fs3, and obfs2 was around 200. So while obfs3 is the most secure option out ther
e, its limited number of available bridges would pool you into a smaller group o

f people making connections to the 40 available bridges and may not provide any
more anonymity for you. tor is in depserate need of more obfs2 and obfs3 bridges
at this time and these factors should be taken into account when using obfuscat
ed bridges.
One of the solutions to this shortage problem, is to run your own obfuscated bri
dge. I am not going to go into it, but if you are interested in doing this, you
should visit the following page to set up an obfuscated proxy, or better yet, pu
rchase a few VPS and set them up as obfs2 or obfs3 proxies. One of the best thin
gs about doing it this way, is that you can configure it (with the instructions
provided) to be a private obfuscated bridge, and therefore tor will not give it
out to the public. You can then connect to your own private obfs3 bridge. You ca
n also use a friend’s computer, or use a server that you know is secure. But again
, make sure that you trust the computer you are using, otherwise it is no more s
ecure than a VPN.
Another possible solution to the lack of obfuscated bridges may be another plugg
able transport option, something called a flash proxy. This is brand new and not
perfectly implemented yet, and please be aware that this is basically still in
beta. When thinking about a flash proxy, think about the characteristics of a fl
ash, quick and short lived. This protocol was developed by a tor developer who a
ttended Stanford University, and the idea is that the IP addresses used are chan
ged faster than a censoring agency can detect, track, and block them. This metho
d is similar to using normal bridges, in that, it hides the fact you are connect
ing to IP addresses known to be related to tor, including when the bridge’s IP add
resses listed by tor are discovered by your ISP or law enforcement. This does no
t however, hide the fact you are using tor if somebody is analyzing your traffic
using DPI (deep packet inspection).
The main benefit to this option is that the proxies are run by many people all o
ver the world. They are run when random internet users visit a webpage with a sp
ecific plugin that turns their browser into a proxy as long as they are on that
page. You are basically using somebody else’s connection through their browser to
connect to a tor relay. You are only using 1 active connection at any time, but
you have around 5 established connections to different proxies in case your acti
ve connection drops off, then you can start using another proxy in its place. Be
low is another explanation of how this process works.
Quote
In addition to the Tor client and relay, we provide three new pieces. The Tor cl
ient contacts the facilitator to advertise that it needs a connection (proxy). T
he facilitator is responsible for keeping track of clients and proxies, and assi
gning one to another. The flash proxy polls the facilitator for client registrat
ions, then begins a connection to the client when it gets one. The transport plu
gins on the client and relay broker the connection between WebSockets and plain
TCP. (Diagram below)
https://crypto.stanford.edu/flashproxy/arch.png
A sample session may go like this:
1. The client starts Tor and the client transport plugin program (flashproxy-cli
ent), and sends a registration to the facilitator using a secure rendezvous. The
client transport plugin begins listening for a remote connection.
2. A flash proxy comes online and polls the facilitator.
3. The facilitator returns a client registration, informing the flash proxy wher
e to connect.
4. The proxy makes an outgoing connection to the client, which is received by th
e client’s transport plugin.
5. The proxy makes an outgoing connection to the transport plugin on the Tor rel
ay. The proxy begins sending and receiving data between the client and relay.
In other words, you end up going from your computer, to the proxy, then the prox
y to the tor relay. – JR
The whole reason this is necessary is because the client cannot communicate dire
ctly with the relay. (Perhaps the censor has enumerated all the relays and block
ed them by IP address.) In the above diagram, there are two arrows that cross th
e censor boundary; here is why we think they are justified. The initial connecti

on from the client to the facilitator (the client registration) is a very low-ba
ndwidth, write-only communication that ideally may happen only once during a ses
sion. A careful, slow, specialized rendezvous protocol can provide this initial
communication. The connection from the flash proxy to the client is from an IP a
ddress the censor has never seen before. If it is blocked within a few minutes,
that’s fine; it wasn’t expected to run forever anyway, and there are other proxies l
ined up and waiting to provide service.
I know this might be a bit complicated, but you really do not need to understand
how it works to benefit from it. You also might be asking about somebody just b
locking your ability to connect with the facilitator (the supplier of the proxie
s). But, the way you actually connect to the facilitator is in a very special wa
y that tor has designed, and this is built into the flash proxy pluggable transp
ort. This explanation is just for your comfort, not to help you make it work.
Quote
The way the client registers with the facilitator, is a special rendezvous step
that does not communicate directly with the facilitator, designed to be covert a
nd very hard to block. The way this works in practice is that the flash proxy cl
ient transport plugin makes a TLS (HTTPS) connection to Gmail, and sends an encr
ypted email from an anonymous address (nobody@localhost) to a special facilitato
r registration address. The facilitator checks this mailbox periodically, decryp
ts the messages, and inserts the registrations they contain. The result is that
anyone who can send email to a Gmail address can do rendezvous, even if the faci
litator is blocked.
https://trac.torproject.org/projects/tor/wiki/FlashProxyFAQ
Two questions you should be asking. 1) Can I trust the proxies, and/or facilitat
or? 2) How do I use this?
Well, the facilitator is chosen and currently only run by tor, so you can take t
hat at face value. As far as the proxies go, the proxies themselves may or may n
ot be trustworthy, and this is the risk you run every time you use tor. Your bri
dges that you use may be compromised, your entry nodes, your exit nodes, every s
ingle possible hop along your way to the internet can be compromised at any give
n time. Luckily, even if the proxy is compromised and logging your traffic, they
are only going to be able to see encrypted tor traffic. And as I mentioned abov
e, anybody who visits a webpage with a specific plugin on it, becomes a flash pr
oxy as long as they are on that site. This means, some people will be a flash pr
oxy without their knowledge, and others will be flash proxies because they want
to be one. The idea behind this is to have multiple users, tens of thousands, if
not hundreds of thousands of flash proxies available at all times to increase t
he number of possible IP addresses you rotate between to keep your ISP and possi
bly the NSA guessing.
So do you use this? It actually currently is not supported in Tails. But it can
be used with Tor Pluggable Transports Tor Browser Bundle outside of Tails. You c
an get it at the following page and it will run on your normal operating system,
whether it is Windows, MAC, or Linux. Get the package at the following page.
https://www.torproject.org/docs/pluggable-transports.html.en#download
Next follow the following tutorial, which is pretty straight forward and has pic
tures of exactly what you need to do, and will probably do a better job than I w
ould at explaining how to set it up.
https://trac.torproject.org/projects/tor/wiki/FlashProxyHowto
Essentially it comes down to, enable port forwarding for port 9000, add “bridge fl
ashproxy 0.0.1.0:1″ without the quotes, to your torrc, and leave everything else a
lone unless you need to use a different port, which is unlikely. You may need to
make an exception in your firewall for the flashproxy plugin if it asks you. As
long as you are using the Tor Pluggable Transports Tor Browser Bundle, it shoul
d be pretty easy to get this feature working. But until Tails adds support for i
t, this is the only option you have if you want to use flash proxy bridges.
Ok, so you have a lot of information right now and maybe are left a bit confused
, but read over this one a few times and try to extract as much out of it as pos
sible at once. Try setting up normal bridges, then try doing the obfuscated brid
ges, and once you get those working, then maybe consider doing the flash proxies

if you are okay without using Tails. Tails will likely implement support for th
is later. Ask yourself some questions, do I just want to hide the fact that I am
using tor from my ISP? Or am I hiding from somebody much bigger than that?
Consider whether it is plausible for you to run a private obfuscated proxy, or e
ven a private bridge. Hopefully now you have enough information to make an infor
med decision.
Currently there are other pluggable transports currently under developed, but no
t yet deployed. Here is a list of upcoming projects.
Quote
ScrambleSuit is a pluggable transport that protects against follow-up probing at
tacks and is also capable of changing its network fingerprint (packet length dis
tribution, inter-arrival times, etc.). It’s part of the Obfsproxy framework. See i
ts official page. Maintained by Philipp Winter.
http://www.cs.kau.se/philwint/scramblesuit/
Status: Undeployed
StegoTorus is an Obfsproxy fork that extends it to a) split Tor streams across m
ultiple connections to avoid packet size signatures, and b) embed the traffic fl
ows in traces that look like html, javascript, or pdf. See its git repository. M
aintained by Zack Weinberg.
https://gitweb.torproject.org/stegotorus.git
Status: Undeployed
SkypeMorph transforms Tor traffic flows so they look like Skype Video. See its s
ource code and design paper. Maintained by Ian Goldberg.
http://crysp.uwaterloo.ca/software/SkypeMorph-0.5.1.tar.gz
http://cacr.uwaterloo.ca/techreports/2012/cacr2012-08.pdf
Status: Undeployed
Dust aims to provide a packet-based (rather than connection-based) DPI-resistant
protocol. See its git repository. Maintained by Brandon Wiley.
https://github.com/blanu/Dust
Status: Undeployed
Format-Transforming Encryption (FTE) transforms Tor traffic to arbitrary formats
using their language descriptions. See the research paper and web page.
https://eprint.iacr.org/2012/494
https://kpdyer.com/fte/
Status: Undeployed
Also see the unofficial pluggable transports wiki page for more pluggable transp
ort information.
https://trac.torproject.org/projects/tor/wiki/doc/PluggableTransports
Source: https://www.torproject.org/docs/pluggable-transports.html.en
WHY YOU SHOULD ALWAYS BACK UP YOUR DRIVES, ESPECIALLY ENCRYPTED DRIVES
inShare
This is an embarrassing story of something that happened to me in the past few d
ays, and it was a lesson well learned, for some of the things I have lost are no
t recoverable. – Jolly Roger
Do you have your Bitcoin wallets saved on a flash drive? What would happen if yo
u lost your flash drive? Do you have a backup? What would happen if your files b
ecame corrupted and were not able to be recovered, could you live with that? Do
you have certain things that would absolutely cause a huge problem if you lost t
hem? Then you better start backing up your drives regularly, better yet, do it d
aily!
I am the type of person who usually backs up his files regularly, but unfortunat
ely do to the large amount of strange events occuring online lately with Utopia
being brought down, BMR forums being seized, Silk Road being robbed and so forth
, I had not backed up my files in about 2 weeks. I had all of my most recent fil
es, including a few new Bitcoin wallets with balances on them on my main portabl
e drive, and on top of it, this drive was encrypted.
Then, without warning, I suddenly received an error that the file system was cor

rupted and my disk could not be read. No matter, if you have an unencrypted driv
e, you can simply run a data recovery program such as testdisk. Open up your ter
minal and type the following. Make sure you started Tails with a login at the bo
ot up when it asks you.
sudo apt-get install testdisk
Using this program (follow documentation online) you can likely recover most of
your files because it ignores file system headers and other types of file organi
zation required to identify the way the files are stored. There are many other p
rograms as well. The problem in my case, was that all my files were encrypted. T
his means, that in order to decrypt the files, I needed a key file that is store
d on the drive to unlock my files. If this key file gets damaged, then even if y
ou have the password for your files, you will not be recovering your files.
The key is unique to that particular instance when you encrypted the drive. Mean
ing that even if I tried to recreate the key file with the same password, the re
sult would be a different key file. This means essentially that my data is unrec
overable, because my key file was somehow corrupted. Technology is delicate, dat
a is stored in the form of magnetic frequencies and there is no guarantee that f
iles will not become corrupted one day for seemingly no reason. Here are some th
ings that could ruin your data.
Flood, hurricane, power surge, fire, moisture damage, accidentally stepping on y
our drive, a family member (usually a child) breaks it, you lose it, spill water
on it, over heats, and so forth.
All of these could result in your data or drive getting damaged and losing all o
f your data. This is why you need a minimum of 2 backups. Not 1, but 2. And have
one of your backups preferrably stored outside of your home. If you work, store
one at work, or in your car, or somewhere you can access regularly, and try to
back up your data as often as possible. If your house burns down and you kept al
l your backups at home, then you lose everything. If you kept a copy at work, th
en you can recover it. The more backups the better, as long as they are encrpypt
ed. Any time you create a new wallet and transfer Bitcoin into it, back it up. A
ny time you set up a new account or a new email with a unique password (which sh
ould be every time), back it up. You need to be backing up everything.
Luckily for myself my main wallet was recoverable with the majority of my coins,
but I did lose some coins, which can never be recovered, trust me, I tried. Get
ting extra USB drives or SD cards are very cheap and inexpensive, so you owe it
to yourself to spend a few extra dollars to have multiple backups just in case y
ou wind up in my situation where you had not backed up your drive in a couple of
weeks and end up losing data that could cost you a lot more than what it would
have costed to have a few extra drives laying around as back ups.
BITCOIN CLIENTS IN TAILS – BLOCKCHAIN AND ELECTRUM
inShare
In this post I want to talk about 2 options for trading your Bitcoins.
#1 – Blockchain
#2 – Electrum
By now, hopefully you know how to use BlockChain. If not, you simply go to http:
//blockchain.info and press the button “Wallet” and you can open up your existing wa
llet or create a new account. Very straight forward and can be done all from you
r web browser.
But what about Electrum? Electrum is an easy to use Bitcoin client. It protects
you from losing coins in a backup mistake or computer failure, because your wall
et can be recovered from a secret phrase that you can write on paper or learn by
heart. There is no waiting time when you start the client, because it does not
download the Bitcoin blockchain. If you use the normal Bitcoin client from https
://bitcoin.org then you would need to download the entire blockchain, which is s
everal GB of data. In Tails, we are trying not to download too much to our compu
ters. Downloading the entire BlockChain can take over 24 hours.
So how do we set up Electrum in Tails? First thing we need to do is download it.

https://download.electrum.org/Electrum-1.9.7.tar.gz
Now extract it (right click -> Extract here) and rename the folder to electrum t
o make things easier. (Right click -> Rename). You might also want to move the f
older to the tmp directory so it is easier to find. (Places -> Computer -> File
System -> tmp)
Next open up a terminal and type the following command
cd /tmp/electrum
You can replace /tmp/electrum with whatever directory electrum is currently in,
but this is why we put it in tmp, to make things easier for us. Next type the fo
llowing command.
./electrum -s 56ckl5obj37gypcu.onion:50001:t -p socks5:localhost:9050
This will allow your electrum to connect through Tor, to make sure it does not c
onnect over clearnet. You will get a warning when you do this that electrum is a
ttempting to connect in an unsafe manner, but this is expected, and do not worry
, it is safe to do this. This step was recommended on the Tails web page at the
following URL.
https://tails.boum.org/forum/Report:_the_electrum_bitcoin_client_in_tails/
Since you are likely going to want to reuse your wallet that is generated in Ele
ctrum, you can specify where your wallet is kept by replacing the above command
with the following command.
./electrum -s 56ckl5obj37gypcu.onion:50001:t -p socks5:localhost:9050 -w /tmp/el
ectrum.dat
You would replace /tmp/electrum.dat with whatever the path to your wallet is, an
d you can rename electrum.dat to whatever you want to call your wallet, like srw
allet.dat or whatever you want. Or leave it the way that it is. Then each time y
ou want to start up electrum, reuse the same command, and make sure you copy ele
ctrum.dat into /tmp or whatever directory you wish to use. Then when you are fin
ished, make sure to back up electrum.dat onto your USB drive or SD card, especia
lly if you do not have Tails persistence. This way you can reuse the same wallet
and you will not lose your balance.
Electrum is likely going to be the Bitcoin client of choice for Tails users. And
you can read more about how to use Electrum by visiting the home page at the fo
llowing link.
https://electrum.org
