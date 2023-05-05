# **Week 3: Operating system privacy** 

Operating systems and their representative devices very often "phone home"[^21], collect telemetry or another kind of data for their respective owners and/or manufacturers. 
In 2021, Windows OS talked to 291 hosts and 2,764 IPs on the internet [^0].

This data can be misused and also could be vulnerable for example to leaks and intercepting. 
In some cases, these devices do not require this data transportation which may leave a remote attack surface for attackers.
For example, Internet of Things (IoT) devices may, and have been used in [botnets.](https://www.cloudflare.com/learning/ddos/glossary/mirai-botnet/)

Exercises this week focus on problems with operating systems and the way they can affect your privacy. We also take a look at how to avoid these issues in the last task, in a bit extreme way.

## Required tools and environments

  - The final task requires a USB stick to boot from and a PC you can boot from said USB stick
  - The final task uses Linux, but it is not required beforehand

## Grading

Points from the exercises count towards better grades than the passable grade 1, which is obtained by doing quizzes.

You must do tasks **in order**.

You are expected to use more time on later tasks to get an equal amount of points than in previous tasks.

Task #|Points|Description|
-----|:---:|----------|
[Task 1](#task-1-telemetry-and-other-data-collection) | 1 | Telemetry and other data collection
[Task 2](#task-2-vpn8-comparison) | 1 | VPN comparison
[Task 3](#task-3-leaving-no-traces-with-tails-gpg-tor-and-onionshare) | 2 | Tails, GPG, Tor, Onionshare

## **Task 1:** Telemetry and other data collection

In the first task, we take a look into some common data collection scenarios and evaluate whether there are data collection and risks present.

### **Task 1A)** IoT Home Assistants

A quite frenzied discussion has been going on around the privacy, security, and safety of IoT devices [^22][^23][^24].

Take a quick look at these few, trailing articles about IoT devices.
Use your browser's private mode if they seem to be behind a paywall.

- **Ring Always Home Cam** [Wired](https://web.archive.org/web/20230215011008/https://www.wired.com/story/ring-always-home-cam-september-2021/), 
- **Roomba** [Wired](https://www.wired.com/story/amazon-irobot-roomba-acquisition-data-privacy/)
- **Alexa/Echo** [The Verge](https://www.theverge.com/2022/4/28/23047026/amazon-alexa-voice-data-targeted-ads-research-report)
- **Ring Doorbell cameras** [Wired](https://www.wired.com/story/ring-hacks-exemplify-iot-security-crisis/), [Politico](https://www.politico.com/news/2023/03/07/privacy-loophole-ring-doorbell-00084979)
- **Astro** [Wired](https://www.wired.com/story/amazon-astro/), [Slashgear](https://www.slashgear.com/911997/the-amazon-astro-poses-a-huge-privacy-threat/)

What **security risks** and **privacy implications** there are from bringing this kinds of devices to your home?


**Answer the following questions:**

- For each device separately describe two situations where the privacy and/or security of the user can be compromised
- Find and list 5 CVEs[^1] for IOT devices such as those above. Give a short explanation of the CVEs. (You can choose the devices and CVEs yourself and the CVEs can be patchable)
- In the U.S., there is a so-called [third-party doctorine](https://en.wikipedia.org/wiki/Third-party_doctrine), which essentially gives the government access to all of your data without warrants, if you have given consent for a service provider to collect your data. Does this apply in Finland? If not, is it prevented by the Finnish legislation or European Union regulation?

A great place to search for the CVEs is [Mitre](https://cve.mitre.org/index.html). Their CVE list search is an amazing tool. [Tips for the search](https://cve.mitre.org/find/search_tips.html)

> You are expected to produce essay-like answer, approximately half A4 (200-250 words).

---

### **Task 1B)** Regular operating systems

Most operating systems and manufacturers collect and send telemetry and other information about your device[^2]. This information may include data such as location, time, usage times and reasons for use. 


Search online to find out what data your phone or computer manufacturer and operating system are sending forward.
If you are unable to find sources for your devices, you can use some well-studied ones instead.

> Include at least two **peer-reviewed** research sources

> Analyze your findings, write a summary and list your sources. (Keep this at around half a page / 200-250 words)

**List at least the following at the beginning:**

- The phone/computer and the OS version
- Manufacturer and their country of origin
- Did you learn anything new about your phone/computer?

---

## **Task 2:** VPN[^3] comparison

Go to [Techlore VPN comparison](https://techlore.tech/vpn) and choose three VPNs from the list and click compare.
Provide short answers to what **the following listings mean**, keeping VPNs' privacy and security in mind and how different VPNs fare in each category. (you can change your choices to get differing results in each category):
* OpenVPN[^4] and Wireguard[^5]
* System/app killswitch[^6]
* Infrastructure and client audit[^7]
* Logging policy[^8]
* Jurisdiction [^9]
* 14 Eyes[^10]
* Warrant canary/transparency report[^11]
* Anonymous Payment and Signup
* Misleading security marketing
* Open-source client
* Multihop[^12]
* Port Forwarding[^13]

In addition to explaining the listings, find out why Wireguard protocol is often considered "superior" to OpenVPN from a performance and security point of view, but this might not be the case with privacy.

### What to return

> Explain the listings and compare three VPNs.

> Reason on a technical level, why privacy might, or might not be an issue, with Wireguard. 

> Which three VPN service providers do you think are the most important to avoid and why?

---

## **Task 3:** Leaving no traces with, Tails, GPG, Tor and OnionShare

[Tails](https://tails.boum.org/), [GPG](https://www.gnupg.org/software/index.html)/[GPA](https://www.gnupg.org/related_software/gpa/index.html), [Tor](https://www.torproject.org/), [OnionShare](https://onionshare.org/) 


*This task **requires a USB stick** and operates through the Tor network.*

It is recommended to use a USB stick, but if you really can't, you can boot Tails with the virtual machine.

In this task, we are taking a look at staying private and anonymous while conducting private business and sharing files.

<details>
<summary>What is Tails</summary>
<br>

Tails(The Amnesiac Incognito Live System)[^14] is a Linux operating system distribution focused heavily on protecting the user from surveillance and censorship as well as keeping the user private. 
The portable operating system runs from the live USB installation and routes everything you do online through Tor.
Being an amnesiac live system the system forgets everything every time you unplug your USB stick, which means always starting with an untracked system. 

**NOTE** Privacy and security gains are assuming that your Tails download was not compromised, and your BIOS, firmware and hardware are not compromised [More on this](https://tails.boum.org/doc/about/warnings/index.en.html).

The recommended way to install Tails is through their [official installation instructions](https://tails.boum.org/install/index.en.html), **note that your USB stick will be wiped clean.** Other installation means are **HEAVILY DISCOURAGED** as they do not guarantee proper operations and may result in identity leakage or traces on computers. 

After installing **DO NOT UPDATE THE SYSTEM WITH APT[^19][^20]**, this might break the operating system or the packages, Tails releases upgrades every six weeks.

</details>

<details>
<summary>What is GPG/GPA?</summary>
<br>

GPG[^15][^16] is a complete and free implementation of the OpenPGP standard. GPG has an extensive list of features and libraries, it can for example be used to manage your keys, sign and encrypt your data and create TLS server certificates.  GPA is GUI-application for GPG.

Here in this task, we are using it to encrypt an image file; a screenshot of your Tails instance with your name and Student ID.

[More on this](https://www.gnupg.org/faq/gnupg-faq.html)

</details>

<details>
<summary>What is Tor?</summary>
<br>

You should by now be a bit familiar at least with Tor[^17] and aware of its capabilities and limitations. Tor(The Onion Router) is free and open-source and designed for enabling anonymous communications. Here you can find a little bit about [perfect anonymity](https://support.torproject.org/faq/#faq_staying-anonymous), in short, it's generally impossible. 

Tor network consists of thousands of relays worldwide concealing users' location and usage. 
Tor attempts to protect the privacy of its users and enable the ability to communicate freely and confidentially.

For more precise information on how Tor networks and browsers operate, refer into their own [site](https://www.torproject.org/), their documentation is vast and of high quality

</details>

<details>
<summary>What is OnionShare?</summary>
<br>

Onionshare[^18] is a privacy-focused open-source tool for chatting, hosting websites and sending and receiving files anonymously using Tor. 
Tails comes with Onionshare installed and features at least the GUI application. 

We are using Onionshare here to send an encrypted image with a message to the provided [.onion address](https://en.wikipedia.org/wiki/.onion).

</details>

---

Now that the introductions and warnings are done, go ahead and follow Tails' [installation instructions](https://tails.boum.org/install/index.en.html) to install Tails on a USB stick. These are fairly straightforward and should go without trouble.

At this point, we recommend having this task and the instructions open on another computer or your phone as you will be booting into Tails shortly. 

Go ahead and follow the instructions to boot into the Tails instance on the computer of your choosing.

Most computers handle this without any implications, and the most common problem is with internet connections. In case of problems we hope you try troubleshooting a little before contacting us, for example, you could try using an ethernet cable to fix internet connection issues.

---

**Once inside Tails**

- Take a screenshot showing your name and student id on any text editor.

- Encrypt the screenshot with GPG/GPA [**by using the provided public key**](for_tails_encryption.pub).

- Follow the [provided](https://github.com/ouspg/PrivacyAndSocialEngineering/blob/main/3.Operating_system_privacy/onionshare.md) .onion address to the Onionshare file-sharing site. It should ask for a password, it is also provided. The site should say "Task # return box". 

### Task 3 A) What to return on the ~~website~~ **GitHub**

Upload an encrypted image file containing a screenshot of the Tails desktop with your name and student ID visible to the ~~provided OnionShare address~~ **Github repository**, accompanied by a message containing your name or another identifier. (Identifier can be mentioned in the return repository) 

### Task 3 B) Onionshare website

Set up a static website with just your name on it with Onionshare.
You can do this in another system than Tails.

However, you should do it as **a reproducible service**.
1. Take a look for [`onionshare-cli`](https://docs.onionshare.org/2.3.1/en/advanced.html#command-line-interface).
2. Create `index.html` and modify it as you like, but include your name or another identifier which you should mention.
3. Use containers to deploy the service (Docker[^25], Podman [^26] et. al). See the Dockers' guide [^25] if you are new to containers.
`ENTRYPOINT` and `CMD` instructions should be used to launch the site with your configurations.
4. Take a screenshot of your website from the Onion address. Identifier and address should be visible.
5. Return the screenshot and Dockerfile[^27] or Containerfile [^28], which was used to create the service. These should be returned to your own repository.


### Task 3 C) Then answer the questions below:

1. What happens when you pull out your Tails USB stick, did you try this?

2. Why do these kinds of operations and services exist? Answer at around between 100 and 200 words.

---

[^0]: [Windows OS, Services & Apps: Network Connection Target Hosts](https://helgeklein.com/blog/windows-os-services-apps-network-connection-target-hosts/)
[^1]: [Mitre](https://cve.mitre.org/index.html)
[^2]: [Extensive scale of phone data sharing revealed](https://www.ed.ac.uk/news/2021/extensive-scale-of-phone-data-sharing-revealed)
[^3]: [VPN](https://en.wikipedia.org/wiki/Virtual_private_network)
[^4]: [OpenVPN](https://fi.wikipedia.org/wiki/OpenVPN)
[^5]: [Wireguard](https://fi.wikipedia.org/wiki/WireGuard)
[^6]: [Killswitches](https://www.techtarget.com/whatis/definition/kill-switch)
[^7]: [VPN audits: what do they mean and why are they important?](https://www.techradar.com/features/vpn-audits-what-do-they-mean-and-why-are-they-important)
[^8]: [What Information do VPN’s Really Log?](https://www.vpnuniversity.com/learn/what-do-vpn-really-log)
[^9]: [Why VPN jurisdiction matters](https://medium.com/@gershwin.aaron/one-of-the-essential-features-of-a-high-quality-vpn-service-is-a-no-logs-policy-d570a02622dd)
[^10]: [14 Eyes](https://en.wikipedia.org/wiki/UKUSA_Agreement#9_Eyes,_14_Eyes,_and_other_%22third_parties%22)
[^11]: [What is a warrant canary?](https://www.cloudflare.com/learning/privacy/what-is-warrant-canary/)
[^12]: [Multihop](https://www.comparitech.com/blog/vpn-privacy/multi-hop-vpn/)
[^13]: [VPN port forwarding](https://surfshark.com/blog/vpn-port-forwarding)
[^14]: [TAILS](https://tails.boum.org/)
[^15]: [GPG](ttps://www.gnupg.org/software/index.html)
[^16]: [GPA](https://www.gnupg.org/related_software/gpa/index.html)
[^17]: [Tor Project](https://www.torproject.org/)
[^18]: [Onionshare](https://onionshare.org/)
[^19]: [APT](https://ubuntu.com/server/docs/package-management)
[^20]: [Do not update via APT](https://tails.boum.org/support/faq/index.en.html#index10h2)
[^21]: [Phoning home](https://en.wikipedia.org/wiki/Phoning_home)
[^22]: [IoT Privacy and Security: Challenges and Solutions ](https://www.mdpi.com/2076-3417/10/12/4102)
[^23]: [IoT Security, Privacy, Safety and Ethics](https://link.springer.com/chapter/10.1007/978-3-030-18732-3_8)
[^24]: [IoT Privacy and Security Challenges for Smart Home Environments](https://www.mdpi.com/2078-2489/7/3/44)
[^25]: [Docker overview](https://docs.docker.com/get-started/)
[^26]: [Podman](https://podman.io/)
[^27]: [Dockerfile reference](https://docs.docker.com/engine/reference/builder/)
[^28]: [Containerfile](https://github.com/containers/common/blob/main/docs/Containerfile.5.md)
