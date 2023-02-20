# **Week 1: Regulation and privacy on the web** 

The GDPR regulation [^8][^11] entered into force on May 2016 and applies since May 2018.
Since then, data collection of the companies has been restricted and consumer rights have been expanded [^7].
The usage, processing, and storage of personally identifiable information (PII) (information about an identifiable, living person) was limited for companies operating in European Union.

Exercises this week go through some practical examples of why the regulation exists and what it means in practice.
The focus is on browser-based internet use.

## Required tools and environments

  * Browser with developer tools, Firefox Developer Edition (recommended)

## Grading

Points from the exercises count towards better grades than the passable grade 1, which is obtained by doing weekly quizzes.

Task #|Points|Description|
-----|:---:|-----------|
Task 1 | 1 | GDPR Data Request
Task 2 | 1 | Cookie Raid
Task 3 | 1 | Browser Fingerprinting
Task 4 | 2 | TikTok Challenge (bonus)


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


> If the website would use only session management-related technical cookies required for the site need to be functional, they would not need a consent. [^1] [^2] [^3] [^4] [^5]

When asking for consent, there is often included also a bit confusing term: legitimate interest, which means, for example following:

> Your company/organisation has a legitimate interest when the processing takes place within a client relationship, when it processes personal data for direct marketing purposes, to prevent fraud or to ensure the network and information security of your IT systems. [^9]

To read more about security related properties of the cookies, see the book Computer Security and the Internet and the Chapter *Web and Browser Security* [^10]. 

### Looking at the [Old School Runescape Landing Page](https://oldschool.runescape.com/)

Let's look at the information about cookies on the Old School Runescape landing page. When you enter the page, you should be prompted to give your consent to the use of cookies. If this is not the case, you may have visited the site before or you may have already given your consent to bulk cookie tracking on another site that uses Cookiebot as its cookie manager. You can see the prompt again if you open the page in a new safe search page, such as Incognito in Chrome or Private Search in Safari and Firefox. Use the *Details* tab to answer the following questions:

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

[EFF Cover Your Tracks](https://coveryourtracks.eff.org/)

Run the test made by EFF. After running the test you will see a score for ‘Bits of identifying information’. Below each score you will see how many users on X amount of devices are running the same setup. The rarer your setup is the more uniquely identifiable you are. Return two categories and results where you had the highest and lowest amount of identifying bits of information.

**(Ignore the AD BLOCKER USED section, as it appears to not work correctly, giving a -0.0 score)**

Why does identifiability matter? 

What pros and cons can you think of to being unique vs common?

---

[AmIUnique](https://amiunique.org/)

View your browser fingerprint with Am I Unique. **Canvas elements** are created by taking features from your device and browser. These features are used to generate a picture that represents your browsing setup. Return the similarity percentages of your Canvas and, if your browser supports it, WebGL Data Attributes.

What is your Screen width and Screen height similarity percentage? You may or may not have a common screen resolution in use. However people use User Interfaces and Taskbars of different sizes. Now check out the similarity percentage for Screen available width and Screen available height. Can you explain your result?

Return similarity percentage for:
- Canvas + WebGL Data
- Screen width, Screen height
- Screen available width, Screen available height

---

[^1]: [ePrivacy Directive](https://eur-lex.europa.eu/legal-content/EN/ALL/?uri=CELEX:32002L0058)

[^2]: [Cookies, the GDPR, and the ePrivacy Directive](https://gdpr.eu/cookies/)

[^3]: [Cookie Banner](https://cookieinformation.com/cookie-banner/)

[^4]: [Cookie Consent Exemptions: Strictly Necessary Cookies](https://www.cookieyes.com/blog/cookie-consent-exemption-for-strictly-necessary-cookies/)

[^5]: [Consent guidelines by The European Data Protection Board](https://edpb.europa.eu/sites/edpb/files/files/file1/edpb_guidelines_202005_consent_en.pdf)

[^6]: [GDPR - Right of Access](https://gdpr-info.eu/issues/right-of-access/)

[^7]: [Guidelines 01/2022 on data subject rights - Right of access](https://edpb.europa.eu/our-work-tools/documents/public-consultations/2022/guidelines-012022-data-subject-rights-right_en)

[^8]: [REGULATION (EU) 2016/679 OF THE EUROPEAN PARLIAMENT AND OF THE COUNCIL](https://eur-lex.europa.eu/eli/reg/2016/679/oj)

[^9]: [What does ‘grounds of legitimate interest’ mean?](https://commission.europa.eu/law/law-topic/data-protection/reform/rules-business-and-organisations/legal-grounds-processing-data/grounds-processing/what-does-grounds-legitimate-interest-mean_en)

[^10] [Computer Security and the Internet | Web and Browser Security](https://link.springer.com/chapter/10.1007/978-3-030-83411-1_9)

[^11] [Data protection under GDPR](https://europa.eu/youreurope/business/dealing-with-customers/data-protection/data-protection-gdpr//index_en.htm)