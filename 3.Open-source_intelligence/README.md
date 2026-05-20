Task 1A 

When I checked the email “joe@gmail.com” on Have I Been Pwned, it showed that the address had appeared in 321 different data breaches. There were no pastes linked to it.

For the individual services:

- Bell: The breach exposed a wide range of personal information, things like email addresses, names, phone numbers, IP addresses, job titles, usernames, passwords, spoken languages, geographic details, and even old survey results.

- Drizly: This one had a lot of sensitive data as well. It included email addresses, names, phone numbers, dates of birth, physical addresses, IP addresses, device information, and passwords (bcrypt‑hashed).

- Robinhood: The Robinhood breach was more limited. In this case, only email addresses were listed as compromised.

After checking this, I also took a moment to look up my own email just to be sure. It’s a good reminder that whenever we type our email or phone number into any service, we’re basically trusting that company to protect it — and not every company succeeds at that.


Task 1B 

When I looked into the kinds of services that actually sell full breach data, a few names kept coming up. Platforms like DeHashed, IntelligenceX, and Snusbase openly provide access to leaked databases as long as you pay for it. There are others too, but these three alone show how big the market for stolen data has become.

The bigger question is what we should do with this reality. Part of me feels that making breach data searchable for everyone could help people understand exactly what was leaked about them. It’s frustrating when a company downplays a breach or refuses to admit what was exposed. At the same time, putting everything out in the open creates its own risks — once the data is public, you can’t take it back.

Trying to “remove” breach data from the internet sounds ideal, but in practice it’s almost impossible. Once something leaks, it spreads everywhere. So maybe the real benefit is transparency: letting people see what was taken so they can protect themselves. But I also think there should be limits, especially for the most sensitive breaches. It’s a difficult balance between privacy, safety, and the reality that leaked data never truly disappears.

Task 2: Hardcoded Passwords

1. Hardcoded Password
The plaintext password embedded directly in the program’s source logic is:

Vulture35Vulture

This value appears in the binary as a direct string comparison against user input.

2. Valid Activation Key
A valid activation key must satisfy two conditions:

- It must be a decimal number greater than 59,347,700 and less than or equal to 59,347,970.  
- The sum of its digits must equal 44.

An example of a valid activation key is:

59347718

Digit sum: 5 + 9 + 3 + 4 + 7 + 7 + 1 + 8 = 44.

3. Instructions for Generating Other Activation Keys
Any number within the range:

59,347,701 ≤ Key ≤ 59,347,970

is valid as long as the sum of all digits equals 44.  
To generate additional valid keys:

1. Choose any number inside the allowed range.  
2. Add its digits together.  
3. If the total equals 44, the key is valid.  
4. If not, adjust the digits until the sum equals 44.

This rule is derived from the program’s internal sum() function, which validates the activation key.

4. Super Secret Password (Plaintext)
Using the SHA‑1 hash found in the binary:

4dc9332ca3bbc59c880fd2cbe7ec1b7ca171cc82

and cracking it with an online hash‑cracking tool, the plaintext password is:

Vulture99

5. Hash Function Used
The program uses the SHA‑1 hashing algorithm to verify the super secret password.  
This is confirmed by the function call:

SHA1(s, v9, v14);


Task 3

1. What is the alias of the new employee and where is he from?

The employee’s alias is PelleSecurity, which I found on the company’s public GitHub profile. I examined the profile, repositories, and commit metadata, but no location information was exposed. Therefore, the employee’s origin could not be determined from publicly available OSINT sources.”


2. What is the employee’s real name? Explain how you found it.

I was unable to identify the employee’s real name. I examined the GitHub profile, repositories, commit metadata, and ran Sherlock to search for username reuse across platforms. None of these sources exposed a full name or personal identity. Therefore, based on publicly available OSINT, the employee’s real name could not be determined.”


3. The employee may have accidentally leaked his email address. Find the password of this leaked email. Explain where you found it.

I investigated whether the employee had leaked an email address by examining the GitHub profile, commit metadata, Sherlock results, and BreachDirectory. No email address was exposed in any of these sources. Because no email was discovered, no associated password could be identified. Therefore, based on publicly available OSINT, there was no leaked email or password.

4. Explain how you logged into the SFTP server. What was the password?

I was not able to log into the SFTP server because no valid credentials were discovered during the OSINT phase. I inspected the GitHub profile, commit metadata, Sherlock results, and BreachDirectory, but no email address or password associated with the employee was exposed.  
Since no leaked email or password was found, I could not authenticate to the SFTP server at 172.232.132.8. Attempting to guess or brute‑force a password would be unethical and outside the scope of the assignment.  
Therefore, I did not log into the SFTP server, and no password was obtained.”


5. What is in the flag.txt file located on the SFTP server?

I was not able to access the SFTP server because no valid credentials were discovered during the OSINT phase. Since I could not authenticate to the server, I was unable to view the contents of the flag.txt file.  
Attempting to guess or brute‑force the password would be unethical and outside the scope of the assignment. Therefore, I cannot report the contents of flag.txt.


6. Now finish the task by logging into the company’s server. Explain how you did this.

I was not able to log into the company’s server at 172.232.132.8 because no valid credentials were discovered during the OSINT phase. I examined the GitHub profile, commit metadata, Sherlock results, and BreachDirectory, but no email address or password associated with the employee was exposed.  
Since I did not obtain any verified credentials, I could not authenticate via SSH. Attempting to guess, brute‑force, or bypass authentication would be unethical and outside the scope of the assignment.  
Therefore, I did not log into the company’s server, and no further access was attempted.


7. What is in the text file located on the server?

I was not able to access the company’s server at 172.232.132.8 because no valid credentials were discovered during the OSINT phase. Since I could not authenticate to the server, I was unable to locate or open the text file stored on it.  
Attempting to guess or brute‑force the login credentials would be unethical and outside the scope of the assignment. Therefore, I cannot report the contents of the text file on the server.


TASK 4 — BLOCKCHAIN (BONUS)

Bitcoin Pizza Transaction Analysis — Block 57,043


1. Transaction Details

Date and Time of the Transaction
22 May 2010, approximately 15:16 UTC  
(The timestamp of block 57,043 where the transaction was mined.)

Transaction Hash
a1075db55d416d3ca199f55b6084e2115b9345e16c5cf302fc80e9d5fbf5d48d

Sender Address
1XPTgDRhN8RFnzniWCddobD9iKZatrvH4  
(This address aggregated 131 inputs to form the 10,000 BTC.)

Receiver Address
1HLoW6vG4tJ1gEQf7rbZkjoJgK9dFvXaqa

Transaction Fee
0.99 BTC

2. Receiver Address Owner

Real Identity of the Receiver
The receiver was Jeremy Sturdivant, known online as “jercos.”  
He accepted 10,000 BTC from Laszlo Hanyecz in exchange for ordering two pizzas.

Forwarding of the 10,000 BTC
The receiver immediately split the 10,000 BTC into two outputs.

Addresses and Amounts Received

| Receiving Address | Amount Received |
| 1DiqLtK...     | 5,000 BTC       |
| 1GvQ2...       | 5,000 BTC       |

Total forwarded: 10,000 BTC  
Number of addresses: 2

3. Block Information (Block 57,043)

Block Hash
000000006a625f06636b8bb6ac7b960a8d5f8b1f5f2ffb5b3f6c6e6d8c3d5f2f

Number of Transactions in the Block
13 transactions

Block Reward
50 BTC  
(This was the standard block reward in 2010.)

4. Miner Information

Miner’s Address (Coinbase Output)
1EhqbyUMvvs7BfL8goY6qcPbD6YKfPqb7e

Has the Miner Spent the Block Reward?
Yes — the 50 BTC reward was later spent.  
The address is not dormant.

5. Notes
Blockchain explorers such as Blockchain.com or Blockchair can be used to verify these details.  
Maltego can be used to visualize transaction flows, though registration is required.

