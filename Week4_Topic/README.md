# **Week 4** 

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

perehtymis linkit Tails, Tor, GPA, OnionShare --

*This task **requires a usb stick** and operates through Tor so we recommend the **TOR TASK HERE** before continuing to this one*

In this task we are taking a look at staying private and anonymous while conducting private business and sharing files.

Tails(The Amnesiac Incognito Live System) is a Linux operating system distribution focused heavily on protecting the user from surveillance and censorship. The portable operating system runs from a live usb installation and routes everything you do online through Tor. Being an amnesiac live system the system is forgets everything everytime you unplug your usb stick, that means always starting with an untracked system.

The recommended way to install Tails is through their [official installation instructions](https://tails.boum.org/install/index.en.html), **note that your usb stick will be wiped clean.** Other installation means are **EXTREMELY HEAVILY DISCOURAGED** as they do not guarantee proper operations and may result in identity leakage or traces on computers. 

After installing **DO NOT UPDATE THE SYSTEM WITH APT**, this might break the operating system or the packages, Tails releases a upgrades every six weeks.

Now that the warnings are done, go ahead and follow their [installation instructions](https://tails.boum.org/install/index.en.html) to install Tails on a usb stick. 

At this point we recommend having this task open on another computer or your phone as you will be booting into Tails shortly.


**TODO**


What to return for this task:

Upload an encrypted image file containing a screenshot of tails with your name and student ID visible to the provided OnionShare address, accompanied by a message containing your public key to decrypt it on the OnionShare address. 

//Then answer the questions below\\ __Is this needed?__

1. What happens when you pull out your Tails usb stick?

2. Why do these kinds of operations and services exist?
