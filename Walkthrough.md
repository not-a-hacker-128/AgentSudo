#  Walkthrough
## How many open ports?
- Enumarate/port scan
- nmap -sS -sV -a [IP ADDRESS] <br>
- <b>Answer:3</b>
## How you redirect yourself to a secret page?
- Go to IP  @web browser
- curl -H "user-agent.ck"<br>
- <b>Answer:user-agent </b>
## What is the agent name?
- Read curl result<br>
- <b>AnswerChris</b>
## FTP Password
- Login through FTP(terminal)
- ls command
- dir
- mget @ftp (got all files)
- get back regular terminal,
- cat to_agebtJ.txt<br>
- <b>Answercrystal</b>
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
- <b>Answer:Alien</b>
## Steg password(Which text is  needed to encrypt in  order to get the Steg password?)
- QXJlYTUx needed to be converted from Base64
- zip2john
- john output.txt
- 7ze8702.zip
- pwd alien
- choose yes
- cat agent_R.txt
- steghide info cute-alien.jpg<br>
- <b>Answer:QXJlYTUx</b>
## Steg password(What is the result of the encrypted password which has been found in the previous question)
- cat messages.txt<br>
- <b>Answer:Area51</b>
## Who is the other agent (in full name)?
- Reading messages.txt<br>
- <b>AnswerJames</b>
## SSH Password
- Reading messages.txt<br>
- <b>Answer:Password is hackerrules</b>
## What is the user flag?
- ssh james@IP
- ls
- cat user_flag <br>
- <b> Answer: b03d975e8c92a7c04146cfa7a5a313c7 </b>

