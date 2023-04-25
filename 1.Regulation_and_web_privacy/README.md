# **Week 1: Regulation and privacy on the web** 

The GDPR regulation [^8][^11] entered into force on May 2016 and applies since May 2018.
Since then, data collection of the companies has been restricted and consumer rights have been expanded [^7].
The usage, processing, and storage of personally identifiable information (PII) (information about an identifiable, living person) was limited for companies operating in European Union.

Exercises this week go through some practical examples of why the regulation exists and what it means in practice.
The focus is on browser-based internet use.

## Required tools and environments

  * Browser with developer tools, Firefox Developer Edition (recommended)
  * Linux for the final task (`cURL`, `jq`, GNU Core Utilities...)

## Grading

Points from the exercises count towards better grades than the passable grade 1, which is obtained by doing weekly quizzes.

You must do tasks **in order**.

You are expected to use more time on later tasks to get an equal amount of points than in previous tasks.

The bonus task is not counted toward the course's maximum possible points; it is extra and can compensate for other work.

Task #|Points|Description|
-----|:---:|-----------|
[Task 1](#task-1-gdpr-data-request) | 1 | GDPR Data Request
[Task 2](#task-2-cookie-raid) | 1 | Cookie Raid
[Task 3](#task-3-browser-fingerprinting) | 1 | Browser Fingerprinting
[Task 4](#task-4-tiktok-challenge-bonus) | 2 | TikTok Challenge (bonus)


## **Task 1:** GDPR Data Request

But now, companies are obligated to provide the information they have collected about you, and this will be your first task.

Create a GDPR-compliant data access request from a company of your choice. We recommend you choose a company you know holds data on you.
The response may take some time, according to GDPR [^6][^7] this **shouldn't** take more than a month from them receiving the request, however, it might take longer than this depending on the company and your request.
Therefore it is better to do it as soon as possible after starting the course.

Read at least [GDPR Article 15](https://gdpr-info.eu/art-15-gdpr/) before crafting your request.

You may use prewritten templates, however, you should make sure the template used requests all of your data.

You can return to this assignment once you have received your information, but you should make the request as soon as possible.

After receiving the answer to your data request answer the following questions. Keep your answers concise, focused and **at most** 200 words.

1. Which company did you choose to request your data from and how long did it take to submit that information?
2. In what format did you receive your data and how many pages/bytes of it were there?
3. What kind of information was there that you had not directly given yourself? 
4. Did you understand the meaning of the information?
5. Do you think that the company collected the least amount of data required to provide the service you needed? 
6. Were you surprised about something, what? 

> Please, aswer to these questions to complete this assigment.

---

## **Task 2:** Cookie Raid


If you have been using the internet before and after the GDPR regulation, you might have noticed that banners have drastically increased.
European ePrivacy Directive (Cookie Law) was already effective in 2002 [^1], but GDPR changed the overall impact.

Cookie banners are a known phenomenon, and they have been used mainly for one purpose; **to **ask for consent to identify** you**.

Cookies will allow the website to store domain-specific information in the browser, for example to: 

  * Keep you authenticated [^10] to the website (**session management**)
  * Site settings and targeted advertising (**personalisation**)
  * How do you behave? (**tracking**)
    * All over the internet (third-party cookies)

Essentially, cookies are the more or less persistent way to store user and website-specific data.


> If the website would use only session management-related technical cookies required for the site need to be functional, they would not need a consent. [^1][^2][^3][^4][^5]

When asking for consent, there is often included also a bit confusing term: legitimate interest, which means, for example following:

> Your company/organisation has a legitimate interest when the processing takes place within a client relationship, when it processes personal data for direct marketing purposes, to prevent fraud or to ensure the network and information security of your IT systems. [^9]

To read more about security-related properties of cookies, see the book Computer Security and the Internet and the Chapter *Web and Browser Security* [^10]. 

### Looking at the [Old School Runescape Landing Page](https://oldschool.runescape.com/)

Let's look at the information about cookies on the Old School Runescape landing page. When you enter the page, you should be prompted to give your consent to the use of cookies. If this is not the case, you may have visited the site before or you may have already given your consent to bulk cookie tracking on another site that uses Cookiebot as its cookie manager. You can see the prompt again if you open the page in a new safe search page, such as Incognito in Chrome or Private Search in Safari and Firefox. Use the *Details* tab **to answer the following questions**:

* How many necessary cookies are there? 
* What happens if you try to disable necessary cookies? 
* List at least 7 different expiry times from the necessary cookies 
* List 3 different cookie types from necessary cookies 
* In Statistics, what are the expiry time and cookie type of **JXWEBUID** 
* In Statistics and Marketing, what other Apps or Companies are listed, other than Jagex 

You can inspect cookies in depth by using the browser's developer tools.
For example, with Firefox, you can open `Web Developer Tools` panel, and from there the storage tab.
Cookies are presented as key-value pairs.

---

## **Task 3:** Browser Fingerprinting

Cookies are an efficient way to identify the specific user from a single device, especially if they have authenticated against the service.
What if the user has not always logged in to the website or has prevented all the cookies?

A more general way to identify the specific user across the different services is *fingerprinting*.
With fingerprinting, a website might also acquire data to link multiple different accounts of the user into a single one or include all unauthenticated traffic to authenticated accounts.
Fingerprinting attempts to use all available information from the user to generate unique and identifying characteristics. 

A notorious case about general fingerprinting is Google's "No CAPTCHA reCAPTCHA", while the purpose might have been good [^12][^13][^14].

In this assignment, you can test your browsers and the traces they leave.

### Task 3 A) [EFF Cover Your Tracks](https://coveryourtracks.eff.org/)

Run the test made by EFF. After running the test you will see a score for ‘Bits of identifying information’. Below each score, you will see how many users on X amount of devices are running the same setup. The rarer your setup is the more uniquely identifiable you are. Return two categories and results where you had the highest and lowest amount of identifying bits of information.

**(Ignore the AD BLOCKER USED section, as it appears to not work correctly, giving a -0.0 score)**

Why does identifiability matter? 

What pros and cons can you think of to being unique vs common?

---

### Task 3 B) [AmIUnique](https://amiunique.org/)

View your browser fingerprint with Am I Unique. **Canvas elements** are created by taking features from your device and browser. These features are used to generate a picture that represents your browsing setup. Return the similarity percentages of your Canvas and, if your browser supports it, WebGL Data Attributes.
The information that WebGL can provide about your machine, is yet another efficient way to fingerprint across the web [^25][^26]. 

What are your Screen width and Screen height similarity percentage? You may or may not have a common screen resolution in use. However, people use User Interfaces and Taskbars of different sizes. Now check out the similarity percentage for Screen available width and Screen available height. Can you explain your result?

Return similarity percentage and explanations of results for:
- Canvas + WebGL Data
- Screen width, Screen height
- Screen available width, Screen available height


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


[^1]: [ePrivacy Directive](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=CELEX:32002L0058)

[^2]: [Cookies, the GDPR, and the ePrivacy Directive](https://gdpr.eu/cookies/)

[^3]: [Cookie Banner](https://cookieinformation.com/cookie-banner/)

[^4]: [Cookie Consent Exemptions: Strictly Necessary Cookies](https://www.cookieyes.com/blog/cookie-consent-exemption-for-strictly-necessary-cookies/)

[^5]: [Consent guidelines by The European Data Protection Board](https://edpb.europa.eu/sites/edpb/files/files/file1/edpb_guidelines_202005_consent_en.pdf)

[^6]: [GDPR - Right of Access](https://gdpr-info.eu/issues/right-of-access/)

[^7]: [Guidelines 01/2022 on data subject rights - Right of access](https://edpb.europa.eu/our-work-tools/documents/public-consultations/2022/guidelines-012022-data-subject-rights-right_en)

[^8]: [REGULATION (EU) 2016/679 OF THE EUROPEAN PARLIAMENT AND OF THE COUNCIL](https://eur-lex.europa.eu/eli/reg/2016/679/oj)

[^9]: [What does ‘grounds of legitimate interest’ mean?](https://commission.europa.eu/law/law-topic/data-protection/reform/rules-business-and-organisations/legal-grounds-processing-data/grounds-processing/what-does-grounds-legitimate-interest-mean_en)

[^10]: [Computer Security and the Internet | Web and Browser Security](https://link.springer.com/chapter/10.1007/978-3-030-83411-1_9)

[^11]: [Data protection under GDPR](https://europa.eu/youreurope/business/dealing-with-customers/data-protection/data-protection-gdpr//index_en.htm)

[^12]: [Reverse-engineering the new “captchaless” ReCaptcha system...](https://github.com/neuroradiology/InsideReCaptcha)

[^13]: [Are you a robot? Introducing “No CAPTCHA reCAPTCHA”](https://security.googleblog.com/2014/12/are-you-robot-introducing-no-captcha.html)

[^14]: [I’m not a human: Breaking the Google reCAPTCHA](https://www.blackhat.com/docs/asia-16/materials/asia-16-Sivakorn-Im-Not-a-Human-Breaking-the-Google-reCAPTCHA-wp.pdf)

[^15]: [EU confirms multiple ongoing investigations into TikTok data practices](https://www.engadget.com/tiktok-data-investigation-data-practices-161535147.html)

[^16]: [TikTok is "unacceptable security risk" and should be removed from app stores, says FCC](https://www.malwarebytes.com/blog/news/2022/07/tiktok-is-unacceptable-security-risk-and-should-be-removed-from-app-stores-says-fcc)

[^17]: [EXCLUSIVE: TikTok Spied On Forbes Journalists](https://www.forbes.com/sites/emilybaker-white/2022/12/22/tiktok-tracks-forbes-journalists-bytedance/?sh=49a7f8d67da5)

[^18]: [TikTok to end clipboard snooping following iOS 14 revelations](https://www.imore.com/tiktok-end-clipboard-snooping-following-ios-14-revelations)

[^19]: [Privacy Analysis of Tiktok’s App and Website](https://rufposten.de/blog/2019/12/05/privacy-analysis-of-tiktoks-app-and-website/)

[^20]: [TikTok Quietly Updated Privacy Policy to Collect Faceprints and Voiceprints](https://www.pandasecurity.com/en/mediacenter/security/tiktok-privacy-faceprints/)

[^21]: [HAR (file format)](https://en.wikipedia.org/wiki/HAR_(file_format))

[^22]: [HTTP Archive format](https://docs.gitlab.com/ee/user/application_security/api_fuzzing/create_har_files.html)

[^23]: [HTTP Archive (HAR) format - Historical Draft August 14, 2012](https://w3c.github.io/web-performance/specs/HAR/Overview.html)

[^24]: [curl:// command line tool and library for transferring data with URLs (since 1998)](https://curl.se/)

[^25]: [Researchers use GPU fingerprinting to track users online](https://www.bleepingcomputer.com/news/security/researchers-use-gpu-fingerprinting-to-track-users-online/)

[^26]: [DRAWNAPART: A Device Identification Technique based on Remote GPU Fingerprinting](https://arxiv.org/abs/2201.09956)

[^27]: [Banning TikTok](https://www.schneier.com/blog/archives/2023/02/banning-tiktok.html)

[^28]: [We Found 28,000 Apps Sending TikTok Data. Banning the App Won't Help.](https://gizmodo.com/tiktok-ban-joe-biden-28000-apps-sdk-data-china-1850174019)

[^29]: [How TikTok Tracks You Across the Web, Even If You Don’t Use the App](https://www.consumerreports.org/electronics-computers/privacy/tiktok-tracks-you-across-the-web-even-if-you-dont-use-app-a4383537813/)
