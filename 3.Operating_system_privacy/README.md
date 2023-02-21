# **Week 3** 

## **Task 1:** Telemetry and data collection

Most operating systems and manufacturers collect and send telemetry and other information about your device. This information may include data such as location, time, usage times and reasons for use. 

Search online to find out what data your phone manufacturer and operating system are sending forward. Analyze your findings, write a summary and list your sources. (Maximum one A4 page)

---

## **Task 2:** VPN comparison

Go to https://techlore.tech/vpn and choose three vpn:s from the list and click compare.
provide short answers to what following listings mean vpn:s privacy and security in mind and how different vpn:s fare in each category. (you can change your choices to get differing results in each category):
* OpenVPN and Wireguard
* System/app killswitch
* Infracture and client audit
* Logging policy
* Jurisdiction
* 14 Eyes
* Warrant canary/transparency report
* Anon Payment and Signup
* Misleading security marketing
* Open source client
* Multihop
* Port Forwarding

---

## **Task 3:** Windows 10 Privacy Hardening

Provided with a clean virtual machine install of Windows 10. Install the utilities you want and/or need to analyze your network traffic (such as [wireshark](https://www.wireshark.org/) or [Windows Diagnostic Data Viewer](https://docs.microsoft.com/en-us/windows/privacy/diagnostic-data-viewer-overview) Keep in mind that the latter is proprietary software from microsoft). 

**Hot Tip:** You can install Windows 10 Home Edition without a Microsoft account if you do not have an internet connection. You can do this by disabling the internet connection of your VM

Get a baseline of traffic leaving your machine. By analyzing it you may find destinations for the traffic, document all these findings.

Windows has built-in settings to protect your privacy and limit what data is actually collected. Do your best to harden your machine and minimize the amount of data transmitted to microsoft or its partners. You can follow instructions and/or tools you can find online (such as [O&O ShutUp10++](https://www.oo-software.com/en/shutup10)), but make sure you understand what you are doing. You can always wipe the installation if you happen to break something permanently.

Once you have hardened your machine, re-analyze its traffic. Document your findings and compare them to your previous results. If there are or if you have noticed that the operating system behaves differently, document your findings.

Make a detailed summary of your research, including actions taken to harden the OS and what changed in its behaviour. Do you think these trade-offs are worth the loss your data?

---

## **Task 4** Leaving no traces with, Tails, GPG, Tor and OnionShare

[Tails](https://tails.boum.org/), [GPG](https://www.gnupg.org/software/index.html)/[GPA](https://www.gnupg.org/related_software/gpa/index.html), [Tor](https://www.torproject.org/), [OnionShare](https://onionshare.org/) 


*This task **requires a usb stick** and operates through Tor so we recommend the **TOR TASK HERE** before continuing to this one*

In this task we are taking a look at staying private and anonymous while conducting private business and sharing files.

<details>
<summary>What is tails</summary>
<br>

Tails(The Amnesiac Incognito Live System) is a Linux operating system distribution focused heavily on protecting the user from surveillance and censorship as well as keeping the user private. The portable operating system runs from a live usb installation and routes everything you do online through Tor. Being an amnesiac live system the system forgets everything everytime you unplug your usb stick, that means always starting with an untracked system. **NOTE** Privacy and security gains are assuming that your Tails download was not compromised, and your BIOS, firmware and hardware are not compromised [More on this](https://tails.boum.org/doc/about/warnings/index.en.html).

The recommended way to install Tails is through their [official installation instructions](https://tails.boum.org/install/index.en.html), **note that your usb stick will be wiped clean.** Other installation means are **HEAVILY DISCOURAGED** as they do not guarantee proper operations and may result in identity leakage or traces on computers. 

After installing **DO NOT UPDATE THE SYSTEM WITH APT**, this might break the operating system or the packages, Tails releases upgrades every six weeks.

</details>

<details>
<summary>What is GPG/GPA?</summary>
<br>

GPG is a complete and free implementation of OpenPGP stadard. GPG has an extensive list of features and libraries, it can for example be used to manage your keys, sign and encrypt your data and create TLS server certificates. 

Here in this task we are using it to encrypt an image file; a screenshot of your Tails instance with your name and Student ID.

[More on this](https://www.gnupg.org/faq/gnupg-faq.html)

</details>

<details>
<summary>What is TOR?</summary>
<br>

You should by now be familiar with Tor and aware of it's capabilities and limitations. Tor(The Onion Router) is free and open-source designed for enabling anonymous communications. Little about [perfect anonymity](https://support.torproject.org/faq/#faq_staying-anonymous), in short, it's generally impossible. 

Tor network consists of thousands of relays worldwide concealing user's location and usage. Tor attempts to protect the privacy of it's users and enable the ability to communicate freely and confidentially.

For more and precise information on how Tor networks and browsers operate, refer their own [site](https://www.torproject.org/), their documentation is vast and of high quality

</details>

<details>
<summary>What is OnionShare?</summary>
<br>

OnionShare principles and how we are using it in this task

</details>

---

Now that the introductions and warnings are done, go ahead and follow Tails' [installation instructions](https://tails.boum.org/install/index.en.html) to install Tails on a usb stick. 

At this point we recommend having this task open on another computer or your phone as you will be booting into Tails shortly.


**TODO**


What to return for this task:

Upload an encrypted image file containing a screenshot of tails with your name and student ID visible to the provided OnionShare address, accompanied by a message containing your public key to decrypt it on the OnionShare address. 

//Then answer the questions below\\ __Is this needed?__

1. What happens when you pull out your Tails usb stick?

2. Why do these kinds of operations and services exist?


# **Week 3** 

## **Task 1:** IoT Home Assistants

Take a quick look at these few short articles about

- **Ring Always Home Cam** https://www.wired.com/story/ring-always-home-cam-september-2021/
- **Roomba** https://www.wired.com/story/amazon-irobot-roomba-acquisition-data-privacy/
- **Alexa/Echo** https://www.theverge.com/2022/4/28/23047026/amazon-alexa-voice-data-targeted-ads-research-report
- **Doorbell cameras** https://www.wired.com/story/ring-hacks-exemplify-iot-security-crisis/
- **Astro** https://www.wired.com/story/amazon-astro/

What **security risks** and **privacy implications** there are from bringing all these devices to your home?

For each device separately describe
- Two situations where privacy and/or security of the user can be compromised
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

## **Task 3:** Blockchain

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