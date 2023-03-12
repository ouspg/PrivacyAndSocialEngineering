# **Week 2: Messaging and mobile privacy**

The nature of privacy has changed over the past decades.
Digital transformation has made it possible to eavesdrop on conversations in new and advanced ways.

Exercises this week goes some basics of the digital confidential discussion and what kind of information you can leave even if the message content is encrypted.

Also, we will go through privacy problems, measurements and features on iOS and Android-based mobile systems.

## Grading

You must do tasks **in order**.

You are expected to use more time on later tasks to get an equal amount of points than in previous tasks.

The bonus task is not counted toward the course's maximum possible points; it is extra and can compensate for other work.

Task #|Points|Description|
-----|:---:|-----------|
[Task 1](#task-1-private-and-authentic-messaging) | 1 | Private and authentic messaging
[Task 2](#task-2-metadata-and-messaging) | 2 | Metadata and messaging
[Task 3](#task-3-application-permissions-and-trackers) | 1 | Application permissions and trackers 
[Task 4](#task-4-application-sdks-code-signatures-tags-and-pixels-bonus) | 1 | Application SDKs, code signatures, Tags and Pixels (bonus)

## **Task 1:** Private and authentic messaging

In private messaging, no other than the sender and intended receiver should be able to read the message content.
For the receiver to be able to verify that the message is coming from the claimed source, the sender must sign it, and then the receiver can verify it from the *signature*.
You can read more about encryption and digital signatures from Wikipedia if needed [^29][^28].

This task will combine some of the basic concepts of encryption and authentication, by using PGP as an example, which is often used in emails.

"PGP" Encryption is short for Pretty Good Privacy, an encryption program originally published by Phil Zimmermann & Associates in 1991 [^1].
Later on derivatives OpenPGP[^2] and GPG[^3] were introduced, which stand for Open-Source PGP and GnuPG/Gnu Privacy Guard respectively.
OpenPGP became standardized by the IETF [^4] and GPG was specifically designed to be compatible with OpenPGP and allows the decryption of OpenPGP encryption.
These encryptions allow users to quite easily have, for example, encrypted email conversations.

"*Arguing that you don't care about the right to privacy because you have nothing to hide is no different from saying you don't care about free speech because you have nothing to say.*" – **Edward Snowden**

Using any(**LEGAL**) means necessary to try to stay **as private** and **as anonymous as possible** and exchange public keys to start an encrypted email conversation with your randomly selected classmate. Your goal is to have the conversation **as unlinkable** to yourself **as possible** even for statewide actors. Being completely untraceable is quite impossible, the important part here is to learn and show how invisible you can become and what it takes.


* Document your actions precisely, and name software or services used to the best of your ability. 
* You are expected to generate PGP keys, exchange them (public keys only!), encrypt, sign, verify and decrypt the message content
* Describe the experience and how difficult you found this to be.

The task will be graded based on the methods used and actions taken to accomplish the conversation and by the level of anonymity achieved.

<details><summary>Tips and Tricks</summary>

You can generate PGP keys [in the browser as well](https://gchq.github.io/CyberChef/#recipe=Generate_PGP_Key_Pair('ECC-384','','','')) by using CyberChef. For practice only!

> **Warning**
> Cryptographic operations in CyberChef should not be relied upon to provide security in any situation. No guarantee is offered for their correctness. We advise you not to use keys generated from CyberChef in operational contexts.

You can use [CyberChef](https://gchq.github.io/CyberChef/) to encrypt and sign the data as well. 
You can also use it for verifying and decrypting the data.

There is a search in CyberChef. Use `PGP` search word to find the required operations.

</details>

## **Task 2:** Metadata and messaging

Sometimes the data you send contains more information than you are aware of.
Especially in the context of modern messaging, the message content might be less interesting than *to whom, where and when you are sending it*.

Depending on the nature of the messaging platform, a centralised platform owner is often able to gather on top of message content:

  * Social graphs [^5]
  * Availability status (last seen and online)
  * Read receipts
  * The intensity of messaging and timestamps
  * Global unique identifier (phone number)
  * Location
  * Device

### **Task 2A)** Compare messaging platforms

Compare different mobile messaging platforms; check online for official and research sources *what kind of information* WhatsApp, Signal, Telegram and Messenger collect about users.
You can also compare additional services if you want to.
To compare specifically mobile application privacy, Apple's Privacy Labels [^8] might be useful:

  * WhatsApp in [App Store](https://apps.apple.com/us/app/whatsapp-messenger/id310633997) and [Play Store](https://play.google.com/store/apps/details?id=com.whatsapp) 
  * Signal in [App Store](https://apps.apple.com/us/app/signal-private-messenger/id874139669) and [Play Store](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
  * Telegram in [App Store](https://apps.apple.com/us/app/telegram-messenger/id686449807) and [Play Store](https://play.google.com/store/apps/details?id=org.telegram.messenger)
  * Meta's Messenger in [App Store](https://apps.apple.com/us/app/messenger/id454638411) and [Play Store](https://play.google.com/store/apps/details?id=com.facebook.orca)

Scroll down to *App Privacy* section and click *See Details*.
You can also use Google's Play store's *Data Safety Labels* [^13], or even compare the labels of these two.

> **Note**
> However, these labels should be taken **with a grain of salt**; both of them are mostly based on the "honour" system; app publisher tells about them and nobody is officially verifying them.
A recent study from Mozilla claims Google's labels are misleading [^9], and also other research [^11][^12] indicates the same about Apple's labels. 


Consider also encryption options from the "defaults" perspective.
In what scenarios is end-to-end-encrypted (E2EE) enabled by default? How about E2EE of the metadata?

By default, for example, WhatsApp encrypts messages in the delivery phase, but backups messages as unencrypted, and recommends backing up the data.
On iOS devices, chats are also included in iCloud Backups as unencrypted by default [^7].
What does it mean if law enforcement wants to access your private conversations?
Has end-to-end encryption on messaging helped on preventing access in that case?
What is the impact of defaults on the general public, which use the service advertised as a "private, secure messenger", but has no idea of the meaning of defaults?

Also, consider the following example scenario to highlight the metadata:

> User A only messages User B from an iPhone 14 Pro Max, once a week, every Thursday. Location stays; the same Helsinki City location of “The Nice Cafe,” around 13:00 PM CET

> User B messages User A from a Windows machine,  Acer Nitro computer, connected to “Best Wi-Fi” with IP address 123.45.67.89 every Thursday at 13:10 PM CET and later around 13:30 PM CET from a Nokia G21 running Android 12 near a Elisa cell tower within a 3-kilometer radius of the Helsinki City location of “The Nice Cafe.”

Without knowing the message content, can you deduce information from User A and User B?


**Write an essay of one A4 page (400 to 500 words) based on the previous sources and examples, including app comparison and considering also the importance of E2E encrypted metadata.**

Note also the use of the same phone number across different services. 
For example, WhatsApp shares phone numbers and other information with Meta Company outside of the European Union [^6].
What does this mean in the context of social graphs and the accuracy of possible behaviour and knowledge modelling?

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

## **Task 3:** Application permissions and trackers

In the previous task, we observed data collection practices on some common messaging applications.
Apple's Privacy Labels and Google's Data Safety Labels were mentioned as one measurement.

In this task, we expand the scope for general applications and we will make some research by ourselves.

### Identifying permissions and trackers

Applications may have permissions [^14][^15] and trackers for data the application does not require to function. Such data may be used for example to profile and hook you, for research, and for monetary gain by selling to third parties, which may or may not handle it safely. 

These permissions might also be exploited by an insider attacker or an outside attacker for compromising your privacy and safety. Such are for example the permission to record audio and full network access.

[Exodus](https://reports.exodus-privacy.eu.org/en/) is a privacy auditing platform for Android applications. You can use Exodus to check Android applications for trackers, permissions and signing fingerprints. 

You can either use it on the browser or [in command-line.](https://github.com/Exodus-Privacy/exodus-standalone)

**Choose two (2)** applications yourself to analyze with the help of Exodus, **and find a third** application that has obvious unnecessary dangerous permissions, such as a flashlight application accessing your contacts. 

Name your application and answer the following questions for each application.

1. How many trackers and permissions each application has?
2. How many "dangerous" (runtime) and/or "special" permissions does each have? (Red exclamation mark, see these in Google's guide [^14])
3. Did the applications have permission to access such data they could use or sell for monetary gain? Which permissions and trackers are these?
4. Describe two attack vectors enabled by these permissions for each application, had an attacker gained access into the application and/or their database.
5. Compare Android and iOS privacy labels (if it is available on both platforms) to your findings about trackers


## Task 4: Application SDKs, code signatures, Tags and Pixels (bonus)

> What is the motivation behind advertising business and trackers? Let's see how do they work in the mobile world and elsewhere.

Mobile business advertising spending was estimated to be around 330 billion U.S. dollars worldwide in 2022 [^19][^20], from a total of 600 billion spent on digital ads[^21].

Revenue of some of the world's most valuable companies is based on ads:
  * Alphabet, Inc. (Google Ads, YouTube Ads)
  * Meta Platforms, Inc. (Facebook, Instagram, Messenger, WhatsApp, Oculus, etc.)

In 2022, Meta and Alphabet took alone 48,4% of the digital ad revenue [^22]. 

Other companies with audience-based platforms have also high revenue on ads:
  * ByteDance (TikTok)
  * Twitter, Inc. (Twitter)
  * Snap Inc. (Snapchat)
  * Microsoft (LinkedIn, Microsoft Search Network)
  * Amazon.com, Inc (Amazon Ads)

Companies spend a lot of money on advertising, and they like to know whether their money has had any impact, or what kind of impact it has been.
To offer capabilities for estimating the ad efficiency and targeting of the ads, many of these advertising companies have developed many, but similar kinds of technologies.

### Task 4A) Legacy technologies

Some traditional tracking technologies to track users across the web and apps include
  * Third-party cookies (the end is near [^24][^30])
  * Advertising ID by Google [^23] and Identifier for Advertisers (IDFA)[^16] by Apple on mobile phones

In early 2021, Apple made use of the IDFA, currently known as App Tracking Transparency (ATT) [^18] feature, requiring a prompt for users; the user was able to opt-in or out of IDFA.
As a result, about 75% of worldwide users opted out of IDFA[^17], which made it significantly harder to track users between different applications. 
Google followed, and a year later, they introduced similar permission [^23].

This little change has been estimated to bring a significant impact on the advertising business and user privacy.
As a response, for example, ByteDance (TikTok) has started to test more efficient device fingerprinting technologies [^25].

> Look for research articles regarding the impact of this change. Write 2-3 paragraphs based on at least 3 sources.


### Task 4B) The use of the advanced technologies

Currently, there are more sophisticated ways to track users across devices.
They are also developer-friendly and easy to use.

On mobile applications, the normal way for ad platform providers **and their partners** is to develop and offer application SDKs which can be embedded into the other apps.
They often bring post-install tracking capabilities off the self.


So-called **Pixels** or **Tags** are currently trending ways to track the efficiency of ads and people's actions after they see the ads and go to the websites. 
They are little code snippets that you inject into your website or integrate into the mobile application.

See [TikTok's graph](https://ads.tiktok.com/help/article/tiktok-pixel?lang=en#) to understand the basic workflow.

|Platform| Pixel/Tag | Helper |
|-|-|-|
|Google| [Google Tag](https://developers.google.com/tag-platform/devguides)| [Tag Assistant](https://tagassistant.google.com/)/[Legacy extension](https://chrome.google.com/webstore/detail/tag-assistant-legacy-by-g/kejbdjndbnbjgmefkgdddjlbokphdefk?hl=en)
|Meta Platforms| [Meta Pixel](https://developers.facebook.com/docs/meta-pixel/)/[Meta App Event Tracking](https://developers.facebook.com/docs/app-events/) | [Meta Pixel Helper](https://chrome.google.com/webstore/detail/meta-pixel-helper/fdgfkebogiimcoedlicjlajpkdmockpc) |
|Twitter | [Twitter Pixel](https://business.twitter.com/en/help/campaign-measurement-and-analytics/conversion-tracking-for-websites.html) | [Twitter Pixel Helper](https://chrome.google.com/webstore/detail/twitter-pixel-helper/jepminnlebllinfmkhfbkpckogoiefpd) |
| TikTok | [TikTok Pixel](https://ads.tiktok.com/help/article/tiktok-pixel?redirected=2#) | [TikTok Pixel Helper](https://chrome.google.com/webstore/detail/tiktok-pixel-helper/aelgobmabdmlfmiblddjfnjodalhidnn?hl=en) |
| Snapchat | [Snap Pixel](https://businesshelp.snapchat.com/s/article/snap-pixel-about?language=en_US) | [Snap Pixel Helper](https://chrome.google.com/webstore/detail/snap-pixel-helper/hnlbfcoodjpconffdbddfglilhkhpdnf?hl=en) | 
| LinkedIn | [Linkedin Insight Tag](https://business.linkedin.com/marketing-solutions/insight-tag) | [LinkedIn Pixel Helper](https://chrome.google.com/webstore/detail/pixel-helper-for-linkedin/adbhmmjkppnhjjiapocjgjaknpigdoaa)|


Go through some Finnish or other web services with the above helper extensions installed. 




* For example, you can check [here for analytics on sites](https://trends.builtwith.com/analytics) in Finland, or some examples below.

  * motonet.fi
  * masku.com
  * polar.com
  * wolt.com
  * verkkokauppa.com
  * power.fi
  * etuovi.com
  * huutokaupat.com
  * tentree.ca
  * crypto.com
  * investing.com

What kind of tracking pixels you are finding? Note, that you might need to accept all the cookies.

Have you encountered ads when using some of the social platforms? You can check if the advertising entity has analytics integrated.

Use Exodus privacy to detect possible code signatures of the advertising platform SDKs if the website has its own app.
Many of the tracking capabilities are integrated into "partners", software.
Take a look for example the partnership between AppFlyers and TikTok [^26][^27]. 

Do you find similar analytics from their apps? If you don't, but for example, you find AppFlyers integrated, do you have any idea where your data is going and what is even tracked?

Also, consider what is the impact of using advertiser-provided log-in options.
E.g. for using Google login or Facebook login to some service, which has integrated relevant tracking software.

> Write at least 4-5 paragraphs of your thoughts and findings, when looking these trackers.


[^1]: [Why I Wrote PGP](https://www.philzimmermann.com/EN/essays/WhyIWrotePGP.html)
[^2]: [OpenPGP ](https://www.openpgp.org/)
[^3]: [The GNU Privacy Guard](https://gnupg.org/)
[^4]: [IETF](https://www.ietf.org/)
[^5]: [Social graph](https://en.wikipedia.org/wiki/Social_graph)
[^6]: [What information does WhatsApp share with the Meta Companies?](https://faq.whatsapp.com/1303762270462331)
[^7]: [About end-to-end encrypted backup - Device-level backups on iPhone](https://faq.whatsapp.com/490592613091019)
[^8]: [App privacy details on the App Store](https://developer.apple.com/app-store/app-privacy-details/)
[^9]: [See No Evil: Loopholes in Google’s Data Safety Labels Keep Companies in the Clear and Consumers in the Dark](https://foundation.mozilla.org/en/campaigns/googles-data-safety-labels/)
[^10]: [I checked Apple’s new privacy ‘nutrition labels.’ Many were false.](https://www.washingtonpost.com/technology/2021/01/29/apple-privacy-nutrition-label/)
[^11]: [Lalaine: Measuring and Characterizing Non-Compliance of Apple Privacy Labels at Scale](https://arxiv.org/abs/2206.06274)
[^12]: [Goodbye Tracking? Impact of iOS App Tracking Transparency and Privacy Labels](https://dl.acm.org/doi/10.1145/3531146.3533116)
[^13]: [Provide information for Google Play's Data safety section](https://support.google.com/googleplay/android-developer/answer/10787469?hl=en)
[^14]: [Permissions on Android](https://developer.android.com/guide/topics/permissions/overview)
[^15]: [Requesting access to protected resources](https://developer.apple.com/documentation/uikit/protecting_the_user_s_privacy/requesting_access_to_protected_resources)
[^16]: [Identifier for Advertisers](https://en.wikipedia.org/wiki/Identifier_for_Advertisers)
[^17]: [App Tracking Transparency Opt-In Rate - Monthly Updates](https://www.flurry.com/blog/att-opt-in-rate-monthly-updates/)
[^18]: [App Tracking Transparency](https://developer.apple.com/documentation/apptrackingtransparency)
[^19]: [Mobile advertising spending worldwide from 2007 to 2024 ](https://www.statista.com/statistics/303817/mobile-internet-advertising-revenue-worldwide/)
[^20]: [State of Mobile](https://www.data.ai/en/go/state-of-mobile-2023/)
[^21]: [Digital Ad Spend (2021–2026)](https://www.oberlo.com/statistics/digital-ad-spend)
[^22]: [Slow fade for Google and Meta's ad dominance](https://www.axios.com/2022/12/20/google-meta-duopoly-online-advertising)
[^23]: [Advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248?hl=en)
[^24]: [What the Death of Browser Tracking Cookies Means for Marketers: Part 1](https://www.invoca.com/blog/what-the-death-of-browser-tracking-cookies-means-for-marketers-part-1)
[^25]: [CAID (technology)](https://en.wikipedia.org/wiki/CAID_(technology))
[^26]: [TikTok partners with AppsFlyer to boost in-app measurement and performance](https://www.tiktok.com/business/en-US/blog/appsflyer-in-app-measurement-performance)
[^27]: [How to win on iOS 14+ with AppsFlyer and TikTok: The complete guide](https://www.tiktok.com/business/en-US/blog/win-ios14-appsflyer-tiktok-complete-guide)
[^28]: [Digital signature](https://en.wikipedia.org/wiki/Digital_signature)
[^29]: [Encryption](https://en.wikipedia.org/wiki/Encryption)
[^30]: [Tracking Cookies are Dead: What Marketers Can Do About It](https://www.invoca.com/blog/tracking-cookies-are-dead-what-marketers-can-do-about-it)