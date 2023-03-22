# **Week 3: Operating system privacy** 

Operating systems and devices very often "call back" to their respective owners and/or manufacturers. This data can be used against people and is vulnerable for example to leaks and intercepting. In some cases these devices do not require this data transportation and may leave entry holes for attackers e.g. IOT devices may be used in botnets 

Exercises this week focus on problems with operating systems and the way they can affect your privacy. We also take a look at how to avoid these issues in the last task.

## Required tools and environments

  - Last task requires a USB stick to boot from and a PC you can boot from said USB stick
  - Last task uses Linux, but it is not required before hand

## Grading

Points from the exercises count towards better grades than the passable grade 1, which is obtained by doing quizzes.

You must do tasks **in order**

You are expected to use more time on later tasks to get an equal amount of points than in previous tasks.

The bonus task is not counted toward the courses maximum possible points; it is extra and can compensate for other work.

Task #|Points|Description|
-----|:---:|----------|
[Task 1](#task-1-iot-home-assistants) | 1 | Home IOT
[Task 2](#task-2-telemetry-and-data-collection) | 1 | Telemetry and Data Collection
[Task 3](#task-3-vpn3-comparison) | 1 | VPN Comparison
[Task 4](#task-4-leaving-no-traces-with-tails-gpg-tor-and-onionshare) | 2 | Tails, GPG, TOR, Onionshare

## **Task 1:** IoT Home Assistants

Take a quick look at these few short articles about

- **Ring Always Home Cam** [Wired](https://www.wired.com/story/ring-always-home-cam-september-2021/)
- **Roomba** [Wired](https://www.wired.com/story/amazon-irobot-roomba-acquisition-data-privacy/)
- **Alexa/Echo** [The Verge](https://www.theverge.com/2022/4/28/23047026/amazon-alexa-voice-data-targeted-ads-research-report)
- **Doorbell cameras** [Wired](https://www.wired.com/story/ring-hacks-exemplify-iot-security-crisis/)
- **Astro** [Wired](https://www.wired.com/story/amazon-astro/)

What **security risks** and **privacy implications** there are from bringing these kind of devices to your home?

**Answer the following questions:**

- For each device separately describe two situations where privacy and/or security of the user can be compromised
- Find and list 5 CVEs[^1] for IOT devices such as above. Give a short explanation of the CVEs. (You can choose the devices and CVEs yourself and the CVEs can be patchable)

A great place to search for the CVEs is [Mitre](https://cve.mitre.org/index.html). Their CVE list search is an amazing tool. [Tips for the search](https://cve.mitre.org/find/search_tips.html)

---

## **Task 2:** Telemetry and data collection

Most operating systems and manufacturers collect and send telemetry and other information about your device[^2]. This information may include data such as location, time, usage times and reasons for use. 

Search online to find out what data your phone manufacturer and operating system are sending forward. Analyze your findings, write a summary and list your sources. (Try keep this at around one page / 300 words)

**List atleast the following at the beginning:**

- Your phone and the OS version
- Manufacturer and their country of origin
- Did you learn anything new about your phone **yes/no**

---

## **Task 3:** VPN[^3] comparison

Go to [Techlore VPN comparison](https://techlore.tech/vpn) and choose three vpn:s from the list and click compare.
Provide short answers to what the following listings mean, keeping vpn:s privacy and security in mind and how different vpn:s fare in each category. (you can change your choices to get differing results in each category):
* OpenVPN[^4] and Wireguard[^5]
* System/app killswitch[^6]
* Infracture and client audit[^7]
* Logging policy[^8]
* Jurisdiction [^9]
* 14 Eyes[^10]
* Warrant canary/transparency report[^11]
* Anonymous Payment and Signup
* Misleading security marketing
* Open source client
* Multihop[^12]
* Port Forwarding[^13]

**Which 3 VPN:s do you think are the most important to avoid and why?**

---

## **Task 4** Leaving no traces with, Tails, GPG, Tor and OnionShare

[Tails](https://tails.boum.org/), [GPG](https://www.gnupg.org/software/index.html)/[GPA](https://www.gnupg.org/related_software/gpa/index.html), [Tor](https://www.torproject.org/), [OnionShare](https://onionshare.org/) 


*This task **requires a usb stick** and operates through Tor*

In this task we are taking a look at staying private and anonymous while conducting private business and sharing files.

<details>
<summary>What is Tails</summary>
<br>

Tails(The Amnesiac Incognito Live System)[^14] is a Linux operating system distribution focused heavily on protecting the user from surveillance and censorship as well as keeping the user private. The portable operating system runs from a live usb installation and routes everything you do online through Tor. Being an amnesiac live system the system forgets everything everytime you unplug your usb stick, that means always starting with an untracked system. **NOTE** Privacy and security gains are assuming that your Tails download was not compromised, and your BIOS, firmware and hardware are not compromised [More on this](https://tails.boum.org/doc/about/warnings/index.en.html).

The recommended way to install Tails is through their [official installation instructions](https://tails.boum.org/install/index.en.html), **note that your usb stick will be wiped clean.** Other installation means are **HEAVILY DISCOURAGED** as they do not guarantee proper operations and may result in identity leakage or traces on computers. 

After installing **DO NOT UPDATE THE SYSTEM WITH APT[^19]**, this might break the operating system or the packages, Tails releases upgrades every six weeks.

</details>

<details>
<summary>What is GPG/GPA?</summary>
<br>

GPG[^15][^16] is a complete and free implementation of OpenPGP stadard. GPG has an extensive list of features and libraries, it can for example be used to manage your keys, sign and encrypt your data and create TLS server certificates.  GPA is GUI application for GPG.

Here in this task we are using it to encrypt an image file; a screenshot of your Tails instance with your name and Student ID.

[More on this](https://www.gnupg.org/faq/gnupg-faq.html)

</details>

<details>
<summary>What is TOR?</summary>
<br>

You should by now be a bit familiar atleast with Tor[^17] and aware of it's capabilities and limitations. Tor(The Onion Router) is free and open-source designed for enabling anonymous communications. Here you can find a little bit about [perfect anonymity](https://support.torproject.org/faq/#faq_staying-anonymous), in short, it's generally impossible. 

Tor network consists of thousands of relays worldwide concealing user's location and usage. Tor attempts to protect the privacy of it's users and enable the ability to communicate freely and confidentially.

For more and precise information on how Tor networks and browsers operate, refer their own [site](https://www.torproject.org/), their documentation is vast and of high quality

</details>

<details>
<summary>What is OnionShare?</summary>
<br>

Onionshare[^18] is a privacy focused open-source tool for chatting, hosting websites and sending and receiving files anonymously using Tor. Tails comes with onionshare installed and features at least the GUI application. 

We are using Onionshare here to send an encrypted image with a message to the provided [.onion address](https://en.wikipedia.org/wiki/.onion).

</details>

---

Now that the introductions and warnings are done, go ahead and follow Tails' [installation instructions](https://tails.boum.org/install/index.en.html) to install Tails on a usb stick. These are fairly straight forward and should go without trouble.

At this point we recommend having this task and the instructions open on another computer or your phone as you will be booting into Tails shortly. 

Go ahead and follow the instructions to booting in to the Tails instance on the computer of your choosing.

Most computers handle this without any implications, and the most common problem is with internet connections. In case of problems we hope you try troubleshooting a little before contacting us, for example, you could try using an ethernet cable to fix internet connection issues.

---

**Once inside Tails**

- Take a screenshot showing your name and student id on any text editor.

- Encrypt the screenshot with GPG/GPA.

- Follow the provided .onion address to an onionshare file sharing site. It should ask for a password, it is also provided. The site should say "Task 4 return box". **Here upload the encrypted image and add your name and public key as a message.**

What to return for this task:

Upload an encrypted image file containing a screenshot of tails with your name and student ID visible to the provided OnionShare address, accompanied by a message containing your name and public key to decrypt the image on the OnionShare address. 

**Then answer the questions below:**

1. What happens when you pull out your Tails usb stick, did you try this?

2. Why do these kinds of operations and services exist? Answer in less than 200 words.

<details>
<summary>For a bonus point</summary>
<br>

Set up a static website with just your name on it with Onionshare, keep in mind this should be made visible. Provide the .onion address and possible password with your answers. Your site should be up for time of the in class exercise time, it is at this time we check the sites.

</details>

---

[^1]: [Mitre](https://cve.mitre.org/index.html)
[^2]: [Scale of phone data sharing](https://www.ed.ac.uk/news/2021/extensive-scale-of-phone-data-sharing-revealed)
[^3]: [VPN](https://en.wikipedia.org/wiki/Virtual_private_network)
[^4]: [OpenVPN](https://fi.wikipedia.org/wiki/OpenVPN)
[^5]: [Wireguard](https://fi.wikipedia.org/wiki/WireGuard)
[^6]: [Killswitches](https://www.techtarget.com/whatis/definition/kill-switch)
[^7]: [VPN audits](https://www.techradar.com/features/vpn-audits-what-do-they-mean-and-why-are-they-important)
[^8]: [VPN Logging](https://www.vpnuniversity.com/learn/what-do-vpn-really-log)
[^9]: [Jurisdiction](https://medium.com/@gershwin.aaron/one-of-the-essential-features-of-a-high-quality-vpn-service-is-a-no-logs-policy-d570a02622dd)
[^10]: [14 Eyes](https://en.wikipedia.org/wiki/UKUSA_Agreement#9_Eyes,_14_Eyes,_and_other_%22third_parties%22)
[^11]: [Warrrant canary](https://www.cloudflare.com/learning/privacy/what-is-warrant-canary/)
[^12]: [Multihop](https://www.comparitech.com/blog/vpn-privacy/multi-hop-vpn/)
[^13]: [VPN port forwarding](https://surfshark.com/blog/vpn-port-forwarding)
[^14]: [TAILS](https://tails.boum.org/)
[^15]: [GPG](ttps://www.gnupg.org/software/index.html)
[^16]: [GPA](https://www.gnupg.org/related_software/gpa/index.html)
[^17]: [TOR](https://www.torproject.org/)
[^18]: [Onionshare](https://onionshare.org/)
[^19]: [APT](https://ubuntu.com/server/docs/package-management)