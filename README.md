# Table of content: Agent Sudo
- [AgentSudo](#agentsudo)
    + [Learning objectives](#learning-objectives)
- [Glossary](#glossary)
- [Walkthrough](#walkthrough)
  * [How many open ports?](#how-many-open-ports-)
  * [How you redirect yourself to a secret page?](#how-you-redirect-yourself-to-a-secret-page-)
  * [What is the agent name?](#what-is-the-agent-name-)
  * [FTP Password](#ftp-password)
  * [ZIP file password](#zip-file-password)
  * [Steg password(Which text is  needed to encrypt in  order to get the Steg password?)](#steg-password-which-text-is--needed-to-encrypt-in--order-to-get-the-steg-password--)

### Learning objectives
I learned several things from this container. For example I used FTP for the first time.Some elements were already known such as brute force and reading files. Although some elements were new such as the ZIP file password were I used binwalk. It was interesting to go in depth on getting information based on a picture. Transcibing a code into regular text(from BASE64) was familiar and I thought it was a fun concept. Afterwards I used Jack the ripper which was my first time.
# Glossary
<b>FTP </b><br>
-File Transfer Protocol
FTP (File Transfer Protocol) is a standard network protocol used for the transfer of files from one host to another over a TCP-based network, such as the Internet. FTP works by opening two connections that link the computers trying to communicate with each other.
<br>
<br>
<b>Binwalk</b><br>
-Binwalk is a simple linux tool for analysing binary files for embeded files and executable code. It is mostly used to extract the content of firmware images.
<br>
<br>
<b>Stenography</b><br>
-Transcibing<br>
<br>
<b>Jack the ripper</b><br>
-A tool to find weak passwords of users in a server.
<br>
<br>
#  Walkthrough
## How many open ports?
- Enumarate/port scan
- nmap -sS -sV -a [IP ADDRESS] <br>
- <b>3</b>
## How you redirect yourself to a secret page?
- Go to IP  @web browser
- curl -H "user-agent.ck"<br>
- <b> user-agent </b>
## What is the agent name?
- Read curl result<br>
- <b>Chris</b>
## FTP Password
- Login through FTP(terminal)
- ls command
- dir
- mget @ftp (got all files)
- get back regular terminal,
- cat to_agebtJ.txt<br>
- <b>crystal</b>
## ZIP file password
- binwalk cutie.png
- binwalk -e cutie.png
- cd ~/_cutie.png.extracted
- extracted this zip
- binwalk cutie.png
- binwalk cutie.png -e
- ls
- john the ripper
- @cutie.extracted dir -> john output.txt<br>
- <b>Alien</b>
## Steg password(Which text is  needed to encrypt in  order to get the Steg password?)
- QXJlYTUx needed to be converted from Base64
- zip2john
- john output.txt
- 7ze8702.zip
- pwd alien
- choose yes
- cat agent_R.txt
- steghide info cute-alien.jpg<br>
- <b>QXJlYTUx</b>
## Steg password(What is the result of the encrypted password which has been found in the previous question)
- cat messages.txt<br>
- <b>Area51</b>
## Who is the other agent (in full name)?
- Reading messages.txt<br>
- <b>James</b>
## SSH Password
- Reading messages.txt<br>
- <b>Password=hackerrules</b>
## What is the user flag?
- ssh james@IP
- ls
- cat user_flag <br>
- <b> b03d975e8c92a7c04146cfa7a5a313c7 </b>

