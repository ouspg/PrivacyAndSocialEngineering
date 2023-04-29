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