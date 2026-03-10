## **Task 3:** Windows 10 Privacy Hardening

Provided with a clean virtual machine install of Windows 10. Install the utilities you want and/or need to analyze your network traffic (such as [wireshark](https://www.wireshark.org/) or [Windows Diagnostic Data Viewer](https://docs.microsoft.com/en-us/windows/privacy/diagnostic-data-viewer-overview) Keep in mind that the latter is proprietary software from microsoft). 

**Hot Tip:** You can install Windows 10 Home Edition without a Microsoft account if you do not have an internet connection. You can do this by disabling the internet connection of your VM

Get a baseline of traffic leaving your machine. By analyzing it you may find destinations for the traffic, document all these findings.

Windows has built-in settings to protect your privacy and limit what data is actually collected. Do your best to harden your machine and minimize the amount of data transmitted to microsoft or its partners. You can follow instructions and/or tools you can find online (such as [O&O ShutUp10++](https://www.oo-software.com/en/shutup10)), but make sure you understand what you are doing. You can always wipe the installation if you happen to break something permanently.

Once you have hardened your machine, re-analyze its traffic. Document your findings and compare them to your previous results. If there are or if you have noticed that the operating system behaves differently, document your findings.

Make a detailed summary of your research, including actions taken to harden the OS and what changed in its behaviour. Do you think these trade-offs are worth the loss your data?

---

## **Task 2:** OSINT pair work

try to find information about your pair online both manually and using OSINT tool framework (SpiderFoot), report information you find and analyze it (do you believe information is about the correct person or someone else with the same name/ uses the same nickname online etc.)
things to look for: possible usernames, social media accounts, interests(accounts in forums about music,sports,gaming etc.), educational background…

spiderfoot open source edition can be installed from github: https://github.com/smicallef/spiderfoot?ref=d
and is also pre installed in kali linux


## **Task 3:** Social Engineering on the Phone

Phones have been steadily topping the scam lists in English-speaking countries for some time now. More often than not, the phone scams are social engineering, with the bad actors posing as another person or a corporate entity. 

In the security side of things, social engineering on the phone more often is Vishing; Voice Phishing. The bad actors are using social engineering to make their targets **want** to do, whatever the bad actors want. The goal of Vishing is to gain access to valuable and/or protected information, helping them compromise the target.

Examine following Vishing transcripts targeted at both companies and individuals.

**Money Laundering** 

Call to the founder(Matti Meikäläinen) of a Finnish company carrying out accounting tasks on behalf of external contractors.

> *Founder (F)* : Founder speaking

> *Caller (C)* : Hello this is Meikälainen Maija from the Finnish Regional State Administrative Agency, you might know us as AVI or as Aluehallintovirasto. 
> I was trying to reach Meikäläinen Matti. Did we have the right number on register?

> *(F)* : Yes, Hello Maija, this is Matti.

> *(C)* : Wonderful.. I am calling you for the Anti-money laundering registration. As you might know, registration for anti-money laundering became obligatory in 2019. 
> Due to Covid restraints, we've had some difficulties handling the applications. Do you remember filling the registration form?

> *(F)* : Uhh.. I think so, is there something wrong with my form?

> *(C)* : Oh goodness, no! Our IT-system requires us to call and confirm the identities for each company. This is done to have a record of the people possibly coming in contact with laundered money. Unfortunately there is quite the amount of small businesses used to circulate laundered money. 
> Is there any other personnel handling transactions within your company?

> *(F)* : Alright, that is important I guess. We have only one other person who handles payments; our own accounting manager Miina Meikäläinen.

> *(C)* : Fantastic, nice to see businesses have only one accounting manager. I will be contacting her as well, could you provide me with her contact information? 

> *(F)* : Ah yes. You can contact her at *email@companyemail.com* and her phone number is **********.

> *(C)* : Right that was *email@companyemail.com* and *********'? 

> *(F)* : Correct.

> *(C)* : And would you like us to send the confirmation email to your personal or company email?

> *(F)* : Company email please. *founder@companyemail.com*. Thank you very much.

> *(C)* : Great, thank you for being so helpful. The email has the confirmation link, just follow that to confirm we contacted you and that's it!

> *(F)* : Thank you, that seems simple enough! Will I be hearing from you after contacting Miina?

> *(C)* : Hopefully not, if everything goes smoothly your registration is complete after her information is on the record.

> *(F)* : Ah right. Well thank you for contacting me so swiftly, and have a nice day.

> *(C)* : You too sir, have a nice day.

**Fraudulent transaction**


**_All transcripts are purely fictional and any similarities to actual events are coincidental_**



----


## Task 4: TikTok Challenge (bonus)

> This task requires some technical skills! You are expected to know how HTTP protocol works, and the command line is required.

TikTok is notoriously known for its data collection practices, including fingerprinting and data sharing with third-party services.
Also, TikTok development kit and trackers appear at least in 25 281 other apps [^28] and hundreds of websites collecting data for TikTok [^29].
Governments and individual security researchers have raised privacy concerns related to the behaviour of the service [^15][^16][^17][^18][^19][^20].
Recently, there have been a lot of talks about banning it in the U.S. [^27]. 

> **Note**
> Conversation is likely highlighted on TikTok for political reasons; many other platforms collect also a lot of data, and this should be also noted. 

But how much and what kind of data it collects?
We will take a brief look at that.

### Task 4 A) Analysing the HAR file

We have the following  [HTTP Archive (HAR) file](files/www.tiktok.com.har) from browsing TikTok with a web browser.
HAR is an industry-standard file format to archive captured HTTP traffic [^21][^22][^23].

You can analyse a HAR file by using, for example, [Google's HAR analyser](https://toolbox.googleapps.com/apps/har_analyzer/) in the browser, importing it in the browser's developer tools,  or just looking at the JSON file manually.

Captured traffic presents the following workflow:

  1. The user opens tiktok.com in private mode
  2. The user attempts to search with the specific keyword

**Your work is to identify the following information about the user:**

  * Browser
  * Operating system
  * Screen size
  * Local language
  * Browser language
  * Region
  * Timezone
  * Search keyword

You can reproduce the previous by capturing the HAR file yourself, and looking into the details if you want.

 > **Find the previos information. Also, describe shortly where this information is located and how and when it is carried to TikTok's servers.**

### Task 4 B) TikTok data obfuscation

However, it appears that the previous details are not the only information TikTok is collecting.
There is a lot of random-looking data in the previous requests.

Apparently, TikTok has created a virtual machine in JavaScript virtual space to hide some of its data collection operations.

Read the following blog posts:

   * [Reverse Engineering Tiktok's VM Obfuscation (Part 1)(2022)](https://www.nullpt.rs/reverse-engineering-tiktok-vm-1)
   * [Reverse Engineering TikTok's VM Obfuscation (Part 2)(2023) (different author)](https://ibiyemiabiodun.com/projects/reversing-tiktok-pt2/)

You don't have to understand what is going on there exactly but we will try to replicate something easy.

In the first blog post, you notice the long cURL[^24] command to request TikTok API as an attempt outside of the browser.

We will try to make a minimal working cURL command to get information about the user `pellesecurity`, by using TikTok's API `https://www.tiktok.com/api/user/detail/`.

Some tips and tricks:
  * The default compression algorithm for TikTok's responses is [brotli](https://github.com/google/brotli).
  cURL does not support it by default in many systems, so you can either control it by adjusting `Accept-Encoding` header or installing `brotli` on the system. For example, on Debian based system, it is `brotli` package, which provides the command-line tool.
  * You can copy a full cURL command for the specific request from Firefox's web developer tools, in the network tab. It is recommended to clean and format it.
  * You can use [`jq`](https://stedolan.github.io/jq/) to lint JSON data, for example, `$ brotli -dc data.br | jq .` 

  > Make a minimal working cURL command to get the user information, and return the command and user information in JSON format. What are mandatory parameters for command to work? Do you have any idea what they mean?

