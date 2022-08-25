# **Week 5** 

## **Task 1:** OSINT pair work

try to find information about your pair online both manually and using OSINT tool framework (SpiderFoot), report information you find and analyze it (do you believe information is about the correct person or someone else with the same name/ uses the same nickname online etc.)
things to look for: possible usernames, social media accounts, interests(accounts in forums about music,sports,gaming etc.), educational background…

spiderfoot open source edition can be installed from github: https://github.com/smicallef/spiderfoot?ref=d
and is also pre installed in kali linux

---

## **Task 2:** Security Questions

Security questions are still often used to confirm your identity in online services

Work to this **Account recovery chatbot** and try to reset the password of a long lost account called **PewDie** that may have once belonged to the internet personality **Felix Kjellberg**

//chatbot in not currently hosted//

---

## **Task 3:** EXIF Metadata

Pictures can contain a lot of additional metadata as EXIF (Exchangeable Image File Format) Data

Download **[image2](https://github.com/ouspg/PrivacyAndSocialEngineering/blob/main/Week5_Topic/images/image2.jpg?raw=true)** and extract the following information from it
- GPS coordinates
- Device manufacturer and the model the image has been taken with
- Date and time when the image has been originally taken

Then strip the image of the above mentioned information and return the image. You can do this for example by using **Imagemagick**. The image should not contain the above mentioned information **in any form**.

For reference here is **[image1](https://github.com/ouspg/PrivacyAndSocialEngineering/blob/main/Week5_Topic/images/image1.jpg?raw=true)** that is an example of a picture where the EXIF data has been stripped
