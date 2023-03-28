# **Week 4: Open-source Intelligence** 

## **Task 1:** Have I been Pwned

[Have I been Pwned](https://haveibeenpwned.com/) is a site that tracks occurrances of emails and phone numbers in various data leak dumps. 

Search for ***joe@gmail.com*** and answer the following questions:

In how many **data breaches** and **pastes** can this email be found?

What are the **compromised data types** in the following services? (each separately)

- **Bell**
- **Drizly**
- **Robinhood**
    
While you are at it you might want to check if **your own email addresses** have been assosiated with any dataleaks, and promptly change your password in these services

---

## **Task 2:** OSINT pair work

try to find information about your pair online both manually and using OSINT tool framework (SpiderFoot), report information you find and analyze it (do you believe information is about the correct person or someone else with the same name/ uses the same nickname online etc.)
things to look for: possible usernames, social media accounts, interests(accounts in forums about music,sports,gaming etc.), educational background…

spiderfoot open source edition can be installed from github: https://github.com/smicallef/spiderfoot?ref=d
and is also pre installed in kali linux

# **Week 4: Open-source Intelligence** 

## **Task 1:** Have I been Pwned

[Have I been Pwned](https://haveibeenpwned.com/) is a site that tracks occurrances of emails and phone numbers in various data leak dumps. 

Search for ***joe@gmail.com*** and answer the following questions:

In how many **data breaches** and **pastes** can this email be found?

What are the **compromised data types** in the following services? (each separately)

- **Bell**
- **Drizly**
- **Robinhood**
    
While you are at it you might want to check if **your own email addresses** have been assosiated with any dataleaks, and promptly change your password in these services

---

## **Task 2:** OSINT pair work

try to find information about your pair online both manually and using OSINT tool framework (SpiderFoot), report information you find and analyze it (do you believe information is about the correct person or someone else with the same name/ uses the same nickname online etc.)
things to look for: possible usernames, social media accounts, interests(accounts in forums about music,sports,gaming etc.), educational background…

spiderfoot open source edition can be installed from github: https://github.com/smicallef/spiderfoot?ref=d
and is also pre installed in kali linux

## **Task 3:** OSINT exploitation
You have applied for a job at Pelle Security, the new clown-themed cybersecurity startup.
As a last round interview assignment, you are tasked with performing OSINT on the company.

Start the task by finding possible social media accounts used for marketing by the company.

Your end goal is to infiltrate the company's server. The server is located at 86.50.170.187

Feel free to use tools such as:

- [Sherlock](https://github.com/sherlock-project/sherlock)
- 
    ``` sudo pacman -Sy sherlock```
- [Breachdirectory](https://breachdirectory.org/)
- [ReconFTW](https://github.com/six2dez/reconftw#osint)
-
 ```
 git clone https://github.com/six2dez/reconftw.git 
 cd reconftw/
 ./install.sh
 ```
- [Hashcat](https://hashcat.net/hashcat/)
- 
```sudo pacman -Sy hashcat```
- [John the ripper](https://github.com/openwall/john)
- 
```sudo pacman -Sy john```
- [Spiderfoot](https://github.com/smicallef/spiderfoot)
- 
 ```
 wget https://github.com/smicallef/spiderfoot/archive/v4.0.tar.gz
 tar zxvf v4.0.tar.gz
 cd spiderfoot-4.0
 pip3 install -r requirements.txt
 python3 ./sf.py -l 127.0.0.1:5001
 ```

**PROVIDE SCREENSHOTS FOR ALL PARTS OF THIS TASK!**


### 1. What is the alias of the new employee and where is he from? Explain where you found this information.



### 2. What is the employee's real name? Explain how you found it.



### 3. The employee may have accidentally leaked his email address. Find the password of this leaked email. Explain where you found it:



### 4. Explain how you logged into the SFTP server. What was the password?



### 5. What is in the flag.txt file located on the SFTP server?


### 6. Now finish the task by logging into the company's server. Explain how you did this.


### 7. What is in the text file located on the server?




---





