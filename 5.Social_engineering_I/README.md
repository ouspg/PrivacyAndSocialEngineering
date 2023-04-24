
## Pre-requisites

This week, you will likely need a working Linux machine for every task.

We provide guidance only for the course's virtual machine.
If you use other methods, you might need to explore a bit more by yourself.

On Arch Linux to install all the required tools:
```sh
sudo pacman -Sy spamassassin whois ldns wget
```

### Spamassassin

One of the oldest email spam filters is Apace's SpamAssassin[^15].
It can be used locally for single email messages, and on some tasks, it might be useful.

Spamassassin needs its rule list to be updated before we can do anything with it.
To update the rule list, run

```sh
sudo sa-update
```

### whois

You will need [whois](https://github.com/rfc1036/whois) command-line tool or [website with similar features](https://who.is/) to query DNS owner information and make reverse IP lookup.

### ldns

`drill` command from the [ldns](https://github.com/NLnetLabs/ldns) library will be used to query DNS records.

As a well-known alternative, you can also use `dig` command-line tool.


## Task 1: Can you... scam me?

Phishing is ranked as the number one cybercrime in 2022 based on the FBI's crime statistics [^10].

In Finland, phishing might be also the most visible cybercrime. 
In 2022, Finns lost 32,4 million euros for scams and frauds [^11].
Banks and media are constantly warning us about different phishing campaigns and schemes.
Many of us have received SMS messages or emails related to phishing.

In this exercise, we will try some simple phishing and counter-phishing technologies.


### Task 1A) Email and URL phishing

Phishing as a term is originating from the context of email messages [^12].
Email technology was new back then, and it enabled efficiently "fish" sensitive information from unsuspicious users.



Let's have a look into the following ChatGPT-generated [^13] phishing message which has been sent via email.

> *The message is not related to the real S-Pankki in any way, and the bank is selected because of the linguistic properties of the name.*

```
Subject: Urgent Action Required: Verify Your Account Now
From: "S-Pankki Finland" <fraudprevention@spanki.fi>

Dear Customer,

We recently detected unusual activity on your bank account and have temporarily suspended your access to online banking for security reasons.

To restore your access, please click on the following link and verify your account information:

https://spanki.fi/verification/1021f-abs21-21441-225af

Please note that failure to verify your account within the next 24 hours will result in the permanent suspension of your online banking account.

Thank you for your prompt attention to this matter.

Sincerely,

S-Pankki Finland
```
The full message in `.eml` format can be found [here](UrgentActionRequiredVerifyYourAccountNow.eml).
EML, short for electronic mail, is a common method for storing email messages [^14].

You can scan the message with `spamassassin` with the command to get the spam score.
```sh
spamassassin -t <FILENAME.eml>
```
It might or might not be useful.

> i. What methods have been used on the message to convince the user to make an action and how the information is likely obtained?

Let's have a look at domains related to this message.

With `whois` tool, simply run `whois <domainname>`.


> ii. Who owns the domain `spanki.fi` related to the previous message? How about the domains `s-panki.fi` or `spankki.fi`?

These two latter domains are likely registered because of the [typosquatting](https://en.wikipedia.org/wiki/Typosquatting).

How about `s-mobili.fi` and `smobili.fi`?

> iii. Is anyone capable to register free domain names, even similar to known brands? 

> iv. Why it is so important pay attention to exact URLs and why can we trust the URLs in the first hand? Only a short explanation about the trust is required.

> v. Look for the sender from the .eml message. How the message has been sent? You should be able to identify the service.


DMARC, DKIM, and SPF are email sender authentication methods.
Take a short look [how they work](https://www.cloudflare.com/learning/email-security/dmarc-dkim-spf/).

> **Note**
> Internet Service Providers (ISPs), cloud providers and VPNs often block outgoing TCP port `25` these days to prevent email spamming. The port is used to relay messages from server to server. As a result, it is difficult to send an email from your own computer these days.

Check the `.eml` file from the previous section.
What headers are telling about DMARC, DKIM and SPF checks?

Take a look for DNS TXT records of the `op.fi`, `nordea.fi`, `poppankki.fi`, `saastopankki.fi` and `s-pankki.fi`. 


Let's stop with the banking theme, and have fun with Netflix instead.


The website was missing from the phishing message.

How about we just... create one?

```sh
wget -mk -nH netflix.com/fi-en/login
```

https://www.netflix.com/fi-en/login

## **Task 2:** Social Engineering Toolkit

**Probably requires course VM for full functionality | min requirement is Linux**

[The Social Engineering Toolkit](https://github.com/trustedsec/social-engineer-toolkit) (SET or SEToolkit) is an open-source penetration testing framework[^1] designed for social engineering. It is being maintained by [TrustedSec](https://www.trustedsec.com/), a full-service Information Security consulting organization. They have created other useful tools as well, you can find these in their [GitHub](https://github.com/trustedsec).

The tool is very well documented on their "[SET user manual](https://github.com/trustedsec/social-engineer-toolkit#set-tutorial)" found on the tools github page, we encourage you to explore this manual when using the tool. 

### **Task 2A)** QR Code[^2] Credential Harvest[^3]

Take a look at the SET's tool QR code creation and web attack type credential harvest. In this task we create a QR code for your self hosted credential harvest page, and a poster to try and get people to scan it. We encourage you to get creative with your poster, it's important it would seem legitimate.

You can set the address to the QR code and the harvester page as your local address, in a real world situation you would set it as your server to actually collect credentials from people in different networks, this also makes the use of HTTPS certificates[^4] possible. You can use any site you want; cloned, self created or ready-to-use templates from the tool. Only requirement is, that it has to have the capability to harvest credentials.

You could for example use the following poster to have a twitter login page for credential harvesting and after entering your credentials it redirects you to the actual address, in this case https://twitter.com/SecurityPelle. This example could be found at a cafe near an office you'd like to collect credentials from or at a lounge of a hotel if you're looking to gather a bunch of random credentials.

You do not have to publicly host the site, it is enough if you can test it with the pc and phone in same network.

**What to return:**  
- The poster  
- Scenario for usage  
- Site used for harvesting  
- Screenshot of the credential harvest tool successfully returning you the input credentials (Your name as username and surname as password)

<details>
<summary>An example poster</summary>
<br>
<img src="https://user-images.githubusercontent.com/20062360/233234591-c534cadf-06a7-473c-9562-64e0bf3e84ef.PNG" alt="An example poster"/>
</details>

### **Task 2B)** Tool Walkthrough

SET has a plethora of cool and interesting utilities and you can create a huge arsenal of potential attacks with them. So in this task you get to choose a tool or a set of tools to create a "walkthrough" for an attack. Document the usage of the tool and provide atleast one plausible use case for it. You are required to include atleast one image or video for the walkthrough. Think of the walkthrough as teaching somone such as an employee, how to conduct your companys basic attack with the tool.

The walkthrough should make the usage of the tool clear and doable for people with atleast some CLI experience.

**What to return:**  
- The walkthrough, included the use case, images and/or videos  
- Why you picked the tool or tools you chose  

---

## **Task 3:** Security Questions

Security questions are still often used to confirm your identity in online services

Work with this **Account recovery chatbot** and try to reset the password of a long lost account called **PewDie** that may have once belonged to the internet personality **Felix Kjellberg**

When you are successful, download the conversation in JSON format and return it

//chatbot in not currently hosted//

---

[^1]: [Pentesting frameworks](https://www.mitnicksecurity.com/blog/what-is-a-pentest-framework)
[^2]: [QR code](https://en.wikipedia.org/wiki/QR_code)
[^3]: [Credential Harvesting](https://www.geeksforgeeks.org/what-is-credential-harvester-attack/)
[^4]: [HTTPS Certificates](https://en.wikipedia.org/wiki/HTTPS#Acquiring_certificates)
[^5]:
[^6]:
[^7]:
[^8]:
[^9]:
[^10]: [Internet Crime Complaint Center Releases 2022 Statistics](https://www.fbi.gov/contact-us/field-offices/springfield/news/internet-crime-complaint-center-releases-2022-statistics)
[^11]: [](https://dvv.fi/en/-/watch-out-verify-warn-others-noticeable-increase-in-digital-scams-in-july-december-2022)
[^12]: [AOHell](https://en.wikipedia.org/wiki/AOHell)
[^13]: [What is ChatGPT?](https://help.openai.com/en/articles/6783457-what-is-chatgpt)
[^14]: [Internet Message Format](https://www.rfc-editor.org/rfc/rfc5322)
[^15]: [Apache SpamAssassin](https://spamassassin.apache.org/)


