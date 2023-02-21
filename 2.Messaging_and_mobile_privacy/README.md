# **Week 2: Messaging and mobile privacy**

## **Task 1:** Private messaging (PGP)

"PGP" Encryption is short for Pretty Good Privacy, an encryption program originally published by Phil Zimmermann & Associates in 1991. Later on derivatives [OpenPGP](https://www.openpgp.org/) and [GPG](https://gnupg.org/) were introduced, which stand for Open-Source PGP and GnuPG/Gnu Privacy Guard respectively. OpenPGP became standardized by the [IETF](https://www.ietf.org/) and GPG was specifically designed to be compatible with OpenPGP and allows the decryption of OpenPGP encryption. These encryptions allows users to quite easily have for example encrypted email conversations.

"*Arguing that you don't care about the right to privacy because you have nothing to hide is no different from saying you don't care about free speech because you have nothing to say.*" – **Edward Snowden**

Using any(**LEGAL**) means necessary try to stay **as private** and **as anonymous as possible** and exchange public keys to start an encrypted email conversation with your randomly selected classmate. Your goal is to have the conversation **as unlinkable** to yourself **as possible** even for statewide actors. Being completely untraceable is quite impossible, the important part here is to learn and show how invisible you can become and what it takes.

* Document your acions precisely, and name software or services used to the best of your ability. 
* Describe the experience and how difficult you found this to be.

Task will be graded based on the methods used and actions taken to accomplish the conversation and by the level of anonymity achieved.

## **Task 2:** Metadata (EXIF)

Sometimes the data you send contains more information than you are aware of.

Pictures can contain a lot of additional metadata as EXIF (Exchangeable Image File Format) Data

Download **[image2](images/image2.jpg?raw=true)** and extract the following information from it
- GPS coordinates
- Device manufacturer and the model the image has been taken with
- Date and time when the image has been originally taken

Then strip the image of the above mentioned information and return the image. You can do this for example by using **[Imagemagick](https://imagemagick.org/index.php)**. The image should not contain the above mentioned information **in any form**.

For reference here is **[image1](images/image1.jpg?raw=true)** that is an example of a picture where the EXIF data has been stripped

https://29a.ch/photo-forensics/

---

## **Task 3:** Application Permissions

[Exodus](https://reports.exodus-privacy.eu.org/en/)

Applications may have permissions and trackers for data the appliation does not require to function. Such data may be used for example to profile and hook you, for research, and for monetary gain by selling to third parties, which may or may not handle it safely. 

These permissions might also be exploited by an insider attacker or an outside attacker for compromising your privacy and safety. Such are for example the permission to record audio and full network access.

[Exodus](https://reports.exodus-privacy.eu.org/en/) is a privacy auditing platform for Android application. You can use Exodus to check Android applications for trackers, permissions and signing fingerprints. 

Choose 2 applications yourself to analyze with the help of Exodus, and find a third application that has obvious unnecessary dangerous permissions, such as a flaslight application accessing your contacts. 

Name your application and answer the following questions for each application.

1. How many trackers and permissions each application has?
2. How many 'dangerous' and/or 'special' permissions does each have? (Red exclamation mark)
3. Did the applications have permissions to access such data they would use or sell for monetary gain? Which permissions and trackers are these?
4. Describe two atttack vectors enabled by these permissions for each application, had an attacker gained access into the application and/or their database.
