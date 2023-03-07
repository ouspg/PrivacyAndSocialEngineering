# **Week 2: Messaging and mobile privacy**

The nature of privacy has changed over the past decades.
Digital transformation has made it possible to eavesdrop on conversations in new and advanced ways.

Exercises this week goes some basics of the digital confidential discussion and what kind of information you can leave even if the message content is encrypted.

Also, will go through privacy problems, measurements and features on Android-based mobile systems.
Many of these findings reflect iOS-based systems as well.

## Grading

You must do tasks **in order**.
You are expected to use more time on later tasks to get an equal amount of points.

Task #|Points|Description|
-----|:---:|-----------|
[Task 1](#task-1-gdpr-data-request) | 1 | Private messaging
[Task 2](#task-2-cookie-raid) | 2 | Metadata and messaging
[Task 3](#task-3-browser-fingerprinting) | 1 | Application Permissions and Trackers 

## **Task 1:** Private and authentic messaging (PGP)

"PGP" Encryption is short for Pretty Good Privacy, an encryption program originally published by Phil Zimmermann & Associates in 1991 [^1].
Later on derivatives OpenPGP[^2] and GPG[^3] were introduced, which stand for Open-Source PGP and GnuPG/Gnu Privacy Guard respectively.
OpenPGP became standardized by the IETF [^4] and GPG was specifically designed to be compatible with OpenPGP and allows the decryption of OpenPGP encryption.
These encryptions allow users to quite easily have, for example, encrypted email conversations.

"*Arguing that you don't care about the right to privacy because you have nothing to hide is no different from saying you don't care about free speech because you have nothing to say.*" – **Edward Snowden**

Using any(**LEGAL**) means necessary try to stay **as private** and **as anonymous as possible** and exchange public keys to start an encrypted email conversation with your randomly selected classmate. Your goal is to have the conversation **as unlinkable** to yourself **as possible** even for statewide actors. Being completely untraceable is quite impossible, the important part here is to learn and show how invisible you can become and what it takes.

* Document your actions precisely, and name software or services used to the best of your ability. 
* Describe the experience and how difficult you found this to be.

The task will be graded based on the methods used and actions taken to accomplish the conversation and by the level of anonymity achieved.

## **Task 2:** Metadata and messaging

Sometimes the data you send contains more information than you are aware of.
Especially in the context of messaging, the message content might be less interesting than *to whom, where and when you are sending it*.

Depending on the nature of the messaging platform, a centralised platform owner is often able to gather on top of message content:

  * Social graphs [^5]
  * Availability status (last seen and online)
  * Read receipts
  * The intensity of messaging and timestamps
  * Global unique identifier (phone number)
  * Location
  * Device

### **Task 2A)** Compare messaging platforms

Compare different messaging platforms; check online for official and research sources *what kind of information* WhatsApp, Signal, Telegram and Messenger collect about users.
You can also compare additional services if you want to.
To compare specifically mobile application privacy, Apple's Privacy Labels [^8] might be useful:

  * WhatsApp [in App Store](https://apps.apple.com/us/app/whatsapp-messenger/id310633997)
  * Signal [in App Store](https://apps.apple.com/us/app/signal-private-messenger/id874139669)
  * Telegram [in App Store](https://apps.apple.com/us/app/telegram-messenger/id686449807)
  * Meta's Messenger [in App store](https://apps.apple.com/us/app/messenger/id454638411)

Scroll down to *App Privacy* section and click *See Details*.
You can also use Google's Play Store's *Data Safety Labels*, or even compare the labels of these two.

> **Note**
> However, these labels should be taken **with a grain of salt**; both of them are mostly based on the "honour" system; app publisher tells about them and nobody is officially verifying them.
A recent study from Mozilla claims Google's labels are misleading [^9], and also other research [^11][^12] indicates the same about Apple's labels. 


Consider also encryption options from the "defaults" perspective.
In what scenarios is end-to-end-encrypted (E2EE) enabled by default? How about E2EE of the metadata?

By default, for example, WhatsApp backups messages as unencrypted, and recommends backing up the data.
On iOS devices, chats are also included in iCloud Backups as unencrypted by default [^7].
What does it mean if law enforcement wants to access your private conversations?
Has end-to-end encryption on messaging helped in that case?
What is the impact of defaults on the general public, which use the service advertised as a "private, secure messenger"?

Also, consider the following example scenario to highlight the metadata:

> User A only messages User B from an iPhone 14 Pro Max, once a week, every Thursday. Location stays; the same Helsinki City location of “The Nice Cafe,” around 13:00 PM CET

> User B messages User A from a Windows Machine,  Acer Nitro computer, connected to “Best Wi-Fi” with IP address 123.45.67.89 every Thursday at 13:10 PM CET and later around 13:30 PM CET from a Nokia G21 running Android 12 near a Elisa cell tower within a 2-mile radius of the Helsinki City location of “The Nice Cafe.”

Without knowing the message content, can you deduce information from User A and User B?


**Write an essay of one A4 page (400 to 500 words) based on the previous sources and examples, considering also the importance of E2E encrypted metadata.**

Note also the use of the same phone number across different services. 
For example, WhatsApp shares phone numbers and other information with Meta Company outside of the European Union [^6].
What does this mean in the context of social graphs and the accuracy of possible behaviour modelling?

**Write one paragraph of your thoughts.**

Additionally, what privacy risks "last seen" or showing "online status" can include? Imagine a situation, where someone who has the same contact list as you have, automates to process of checking the online status of every contact for every second and finally stores this information for a longer period.

**Write one paragraph of your thoughts.**

### **Task 2 B)** Image metadata

Messaging is not limited to text anymore, and photos and videos might be the most common data you also share.
These can also include more data than you are aware of.

Images can contain a lot of additional metadata as EXIF (Exchangeable Image File Format) data.
Some services (especially image related) strip it off for your own safety, but that is always not the case.


Download [**image2**](images/image2.jpg?raw=true) and extract the following information from it
- GPS coordinates
- Device manufacturer and the model the image has been taken with
- Date and time when the image has been originally taken

You can either use the EXIF tool of [CyberChef](https://gchq.github.io/CyberChef/#recipe=Extract_EXIF()) or install [Perl based tool on Arch Linux, for example](https://archlinux.org/packages/extra/any/perl-image-exiftool/).

Then strip the image of the above-mentioned information and return the image. You can do this for example by using [CyberChef's Remove EXIF](https://gchq.github.io/CyberChef/#recipe=Remove_EXIF()) or  [**Imagemagick**](https://imagemagick.org/index.php).
The image should not contain the above-mentioned information **in any form**.

For reference, here is [**image1**](images/image1.jpg?raw=true) as an example of a picture where the EXIF data has been stripped.

Many other file formats also include metadata, but we don't handle them in this exercise.

---

## **Task 3:** Application Permissions and Trackers

[Exodus](https://reports.exodus-privacy.eu.org/en/)

Applications may have permissions and trackers for data the application does not require to function. Such data may be used for example to profile and hook you, for research, and for monetary gain by selling to third parties, which may or may not handle it safely. 

These permissions might also be exploited by an insider attacker or an outside attacker for compromising your privacy and safety. Such are for example the permission to record audio and full network access.

[Exodus](https://reports.exodus-privacy.eu.org/en/) is a privacy auditing platform for Android applications. You can use Exodus to check Android applications for trackers, permissions and signing fingerprints. 

Choose 2 applications yourself to analyze with the help of Exodus, and find a third application that has obvious unnecessary dangerous permissions, such as a flashlight application accessing your contacts. 

Name your application and answer the following questions for each application.

1. How many trackers and permissions each application has?
2. How many 'dangerous' and/or 'special' permissions does each have? (Red exclamation mark)
3. Did the applications have permissions to access such data they would use or sell for monetary gain? Which permissions and trackers are these?
4. Describe two atttack vectors enabled by these permissions for each application, had an attacker gained access into the application and/or their database.

Facebook Pixel, Authentication?
Google Analytics and friends? (TikTok SDK and Pixel)

[^1]: https://www.philzimmermann.com/EN/essays/WhyIWrotePGP.html
[^2]: https://www.openpgp.org/
[^3]: https://gnupg.org/
[^4]: https://www.ietf.org/
[^5]: [Social graph](https://en.wikipedia.org/wiki/Social_graph)
[^6]: [What information does WhatsApp share with the Meta Companies?](https://faq.whatsapp.com/1303762270462331)
[^7]: [About end-to-end encrypted backup - Device-level backups on iPhone](https://faq.whatsapp.com/490592613091019)
[^8]: [App privacy details on the App Store](https://developer.apple.com/app-store/app-privacy-details/)
[^9]: [See No Evil: Loopholes in Google’s Data Safety Labels Keep Companies in the Clear and Consumers in the Dark](https://foundation.mozilla.org/en/campaigns/googles-data-safety-labels/)
[^10]: [I checked Apple’s new privacy ‘nutrition labels.’ Many were false.](https://www.washingtonpost.com/technology/2021/01/29/apple-privacy-nutrition-label/)
[^11]: [Lalaine: Measuring and Characterizing Non-Compliance of Apple Privacy Labels at Scale](https://arxiv.org/abs/2206.06274)
[^12]: [Goodbye Tracking? Impact of iOS App Tracking Transparency and Privacy Labels](https://dl.acm.org/doi/10.1145/3531146.3533116)