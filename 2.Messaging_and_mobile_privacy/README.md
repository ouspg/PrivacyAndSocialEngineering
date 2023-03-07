# **Week 2: Messaging and mobile privacy**

The nature of privacy has changed over the past decades.
Digital transformation has made it possible to eavesdrop on conversations in new and advanced ways.

Exercises this week goes some basics of the digital confidential discussion and what kind of information you can leave even if the message content is encrypted.

Also, will go through privacy problems, measurements and features on Android-based mobile systems.
Many of these findings reflect iOS-based systems as well.

## Grading


Task #|Points|Description|
-----|:---:|-----------|
[Task 1](#task-1-gdpr-data-request) | 1 | Private messaging
[Task 2](#task-2-cookie-raid) | 1 | Metadata
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

## **Task 2:** Metadata 

Sometimes the data you send contains more information than you are aware of.
Especially in the context of messaging, the message content might be less interesting than *to whom, where and when you are sending it*.

Depending on the nature of the platform, centralised platform owner is often able to gather:

  * Social graphs [^5]
  * Availability status (last seen and online)
  * Read receipts
  * Intensivity of messaging and timestamps
  * Global unique identifier (phone number)
  * Location
  * Device

### Task 2A) Compare messaging platforms

Compare different messaging platforms; check for online for official and research sources *what kind of information* WhatsApp, Signal and Telegram collects about users.
You can also include additional services.

Consider also encryption options from the "defaults" perspective.
In what scenearios is end-to-end-encrypted (E2EE) enabled by default?

By default, for example, WhatsApp backups messages as unencrypted, and recommends backing up the data. 
On iOS devices chats are alse included into iCloud Backups as unencrypted by default [^7].
What it means if law enforments want to access your data?
Has end-to-end encryption on messaging helped in that case?


**Write a short comparison of 3-4 paragraphs.**

Note also the use of same phone number accross different services.For example, WhatsApp shares phone numbers and other information with Meta Company outside of European Union [^6].
What this means in the context of social graphs and accuracy of possible behavior modeling?

**Write a one paragraph of your thoughts.**

Additionally, what privacy risks "last seen" or showing "online status" can include? Imagine a situation, where someone who has the same contact list as you have, automates to process of checking online status of every contact for every second and stores this information for a longer period of time.

**Write a one paragraph of your thoughts.**

### **Task 2 B)** Image metadata


Some services(especially image related) strip it off for your own safety, but that is always not the case.

Pictures can contain a lot of additional metadata as EXIF (Exchangeable Image File Format) Data

Download **[image2](images/image2.jpg?raw=true)** and extract the following information from it
- GPS coordinates
- Device manufacturer and the model the image has been taken with
- Date and time when the image has been originally taken

Then strip the image of the above mentioned information and return the image. You can do this for example by using **[Imagemagick](https://imagemagick.org/index.php)**. The image should not contain the above mentioned information **in any form**.

For reference here is **[image1](images/image1.jpg?raw=true)** that is an example of a picture where the EXIF data has been stripped

https://29a.ch/photo-forensics/

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


[^1]: https://www.philzimmermann.com/EN/essays/WhyIWrotePGP.html
[^2]: https://www.openpgp.org/
[^3]: https://gnupg.org/
[^4]: https://www.ietf.org/
[^5]: https://en.wikipedia.org/wiki/Social_graph
[^6]: https://faq.whatsapp.com/1303762270462331
[^7]: https://faq.whatsapp.com/490592613091019