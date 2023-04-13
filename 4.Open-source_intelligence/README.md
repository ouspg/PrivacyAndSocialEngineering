# **Week 4: Open-source Intelligence** 

What information is publicly available about you?
The amount can surprise you.

The exercises this week through some popular methods and sources. The information is also used in task three. 
## **Task 1:** Have I been Pwned

One of the most typical and critical situations for a person could be the case when their login credentials have been leaked online publicly as a part of a cyber incident or another matter.

[Have I been Pwned](https://haveibeenpwned.com/) is a site that tracks occurrances of emails and phone numbers in various data leak dumps. 

Search for ***joe@gmail.com*** and answer the following questions:

In how many **data breaches** and **pastes** can this email be found?

What are the **compromised data types** in the following services? (each separately)

- **Bell**
- **Drizly**
- **Robinhood**
    
While you are at it you might want to check if **your own email addresses** have been assosiated with any dataleaks, and promptly change your password in these services

---

## **Task 2:** Hardcoded Passwords

There have been a few cases of compromised systems due to hardcoded passwords and API keys accidentally ending up in production code. [Google offers some advice how to handle such information more securely](https://cloud.google.com/docs/authentication/api-keys)

Use Hex-Rays decompiler via [Dogbolt](https://dogbolt.org/) to check out if you can find a **plaintext hardcoded password** from the provided compiled C code file called **secretKey**. 

As a second task there is a secret **Activation Key** for you to figure out, which has validation arguments that can be seen with the some closer inspection of the decompiler.

As a third and last task there is a **Super secret password** that is hardcoded, but has been encrypted with a mystery hash.


In case if the site is under maintenance, there is a HexRaysOutput file, which has the full output of the decompilation process. Use an editor that can understands C++ to inspect the file with proper highlighting.

You can run the C program to validate your findings in your terminal by navigating to the same folder where the file resides and using the command **./secretKey**

After completing the task, you have five items to return. Return a valid **password** and **one valid activation key** along with the **instructions** on how to create rest of the activation keys, since there are multiple valid ones. Also return the **plaintext version of the super secret password** and **the name of the hash function** it was encrypted with.

---


## **Task 3:** OSINT exploitation

**NOTE**: To do this task, you need to be connected to the University of Oulu VPN or have to be connected to the EDUROAM network on campus:
Instructions for connecting:
https://ict.oulu.fi/16863/


You have applied for a job at Pelle Security, the new clown-themed cybersecurity startup.
As a last round interview assignment, you are tasked with performing OSINT on the company.

Start the task by finding possible social media accounts used for marketing by the company.

Your end goal is to infiltrate the company's server. The server is located at 86.50.170.187

Feel free to use tools such as:

Installation instructions are for the course arch virtual machine.

- [Sherlock](https://github.com/sherlock-project/sherlock)

    ``` sudo pacman -Sy sherlock```
- [Breachdirectory](https://breachdirectory.org/)
- [ReconFTW](https://github.com/six2dez/reconftw#osint)

    ```
    git clone https://github.com/six2dez/reconftw.git 
    cd reconftw/
    ./install.sh
    ```
- [Hashcat](https://hashcat.net/hashcat/)

    ```sudo pacman -Sy hashcat```
- [John the ripper](https://github.com/openwall/john)

    ```sudo pacman -Sy john```
- [Spiderfoot](https://github.com/smicallef/spiderfoot)

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

## **Task 4:** Blockchain

We will take a brief look at online tools available for inspecting the bitcoin blockchain

Just as a quick recap: **Blockchain** is a ledger containing information of all transactions made with the cryptocurrency. Incoming transactions are added as **blocks** into the blockchain when a valid **hash** is found for a certain block. These hashes are brute forces aka **mined** mainly using the prosessing power of Graphics Processing Units (GPU).

Early Bitcoin developer Laszlo Hanyecz was alledgedly one of the first to invent GPU mining. However, what he is remembered for is the first documented purchase of goods using bitcoin, where he traded **10,000** bitcoin for **2 Pizzas**.

You can find conflicting information from the internet about the pizza parlor where the pizzas were bought from. Aside from that, by inspecting the blockchain we can find exact information about the transaction.

Use the [Blockchain explorer](https://www.blockchain.com/explorer) to inspect the block **57043** and provide the following information.

Transaction
- Date and Time of the transaction
- Hash of the transaction
- Address of sender
- Address of receiver
- Transaction fee amount in bitcoin

Receiver Address
- Who was the owner of this address? Use [OXT.me](https://oxt.me/) and Google to figure out the real name of the user
- The owner instantly divided and forwarded the 10,000 to **how many** other addresses
- Addresses that received the 10,000 bitcoin and the corresponding sums to each address

Block
- Hash of the block 57043
- Amount of transactions in the block
- Block reward amount

Miner
- Address of the miner for block 57043
- Has this address spent the block reward they received?


**FYI**: **Maltego** is a great tool for blockchain tracing. It let's you to create a tree like structure out of inbound and outbound transactions from different addresses. It also requires registration.
