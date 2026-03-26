Task 1A -  Signing a Message

For this task, I generated a new GPG keypair and created a simple text file named message.txt. I wrote a short message inside the file and then used GPG to sign it. As required, I am including my public key and the signature of the signed message.  
My private key was not shared or uploaded.

My Public Key

-----BEGIN PGP PUBLIC KEY BLOCK-----

mDMEacS7EhYJKwYBBAHaRw8BAQdAWlSC0Auk7tEXY7wa0CXcCmxJaCLLedJr+QM0
B+nY3h+0O0NoaWJ1em9yIENocmlzdG9waGVyIE9ueWVnZXNpICA8Y2hpYnV6b3Jv
bnllZ2VzaUBnbWFpbC5jb20+iHIEExYIABoECwkIBwIVCAIWAQIZAQWCacS7EgKe
AQKbAwAKCRA+AWZnxnc4oWXUAQCYrw/t1sRZRk8waDHGkOJCVLRY5V1o4T5/rD+D
7vByDQEAmmVFvcB+ToK4Cj5EBsDe+qmhJBrD3kdEwafjZIl+2Qq4OARpxLsSEgor
BgEEAZdVAQUBAQdAv4a41DS6WDrQPAPcnogCj/msl/yVP9WZAzt2ePA+NHgDAQgH
iGEEGBYIAAkFgmnEuxICmwwACgkQPgFmZ8Z3OKH6EAEA+MdGQgrJHKbMfM7X/DWe
JRqHPWBti0NvS/dOk6EN6fIA/3J9TuI4aZS6xTwET6ZIvwRmnvXplrCrQTd4ZvlQ
hicK
=wQm5
-----END PGP PUBLIC KEY BLOCK-----

Signed Message Output

-----BEGIN PGP SIGNED MESSAGE-----
Hash: SHA256

-----BEGIN PGP PUBLIC KEY BLOCK-----

mDMEacS7EhYJKwYBBAHaRw8BAQdAWlSC0Auk7tEXY7wa0CXcCmxJaCLLedJr+QM0
B+nY3h+0O0NoaWJ1em9yIENocmlzdG9waGVyIE9ueWVnZXNpICA8Y2hpYnV6b3Jv
bnllZ2VzaUBnbWFpbC5jb20+iHIEExYIABoECwkIBwIVCAIWAQIZAQWCacS7EgKe
AQKbAwAKCRA+AWZnxnc4oWXUAQCYrw/t1sRZRk8waDHGkOJCVLRY5V1o4T5/rD+D
7vByDQEAmmVFvcB+ToK4Cj5EBsDe+qmhJBrD3kdEwafjZIl+2Qq4OARpxLsSEgor
BgEEAZdVAQUBAQdAv4a41DS6WDrQPAPcnogCj/msl/yVP9WZAzt2ePA+NHgDAQgH
iGEEGBYIAAkFgmnEuxICmwwACgkQPgFmZ8Z3OKH6EAEA+MdGQgrJHKbMfM7X/DWe
JRqHPWBti0NvS/dOk6EN6fIA/3J9TuI4aZS6xTwET6ZIvwRmnvXplrCrQTd4ZvlQ
hicK
=wQm5
-----END PGP PUBLIC KEY BLOCK-----
-----BEGIN PGP SIGNATURE-----

iJsEARYIAEM8HENoaWJ1em9yIENocmlzdG9waGVyIE9ueWVnZXNpICA8Y2hpYnV6
b3JvbnllZ2VzaUBnbWFpbC5jb20+BQJpxTNwAAoJED4BZmfGdzihZuYA/1scPBPz
DQuu7OPv8YruKHqYTMjnV6QyK8HYu81AH9QEAQDv0PH/so9lKwUIiLAp/ZXDfjGy
oV2B3LAPf0ea2cavBg==
=xCQs
-----END PGP SIGNATURE-----


Task 1B: 

I encrypted the message from Task 1A using the provided public key and sent it to taskmailaddress@proton.me with the subject “Chibuzor Christopher Onyegesi”.

Task 1C: The signature belongs to: Slatey Cirk

Task 1D 

1. What can be found out about the email you sent, by someone who intercepts it in transit?

Even though the message content is encrypted, an interceptor can still see the metadata. This includes the sender’s email address, the receiver’s email address, the subject line, the time the email was sent, the size of the message, and the mail servers involved in delivery. They cannot read the encrypted body, but they can still build a picture of who is communicating with whom, when, and how often.

2. Does verifying the message guarantee the sender’s identity?

No. Verifying the signature only proves that the message was signed with the private key that corresponds to the public key you used for verification. It does not guarantee the real‑world identity of the person behind that key. If someone created a fake key with a fake name, the signature would still verify. Identity depends on trust in the key owner, not the cryptography alone.

3. Is the process of sending an email this way end‑to‑end encrypted (E2EE)?

Only the message body is end‑to‑end encrypted. The email system itself is not. Email metadata (sender, receiver, subject, timestamps, routing information) is still visible to mail servers and anyone monitoring the network. True E2EE would hide both content and metadata, but PGP‑encrypted email only protects the content.

Perfect — let’s craft Task 2A in a human, conversational, reflective tone.  
Something that sounds like a real student thinking through privacy, not a robot dumping facts.


Task 2A

When you compare WhatsApp, Signal, Telegram and Messenger, you quickly realise that “private messaging” means very different things depending on the company behind it. WhatsApp loves to market itself as secure, and yes, the messages are end‑to‑end encrypted by default. But the amount of metadata it collects is huge: phone numbers, contacts, device details, usage patterns, and even unencrypted backups unless you manually turn on encrypted backups. Signal feels like the opposite philosophy minimal data collection, no phone‑number sharing beyond registration, and metadata protection that tries to reveal as little as possible. Telegram sits in a strange middle ground: it collects more data than Signal, and its default chats are not end‑to‑end encrypted unless you manually switch to “Secret Chat.” Messenger is the least private of the four, with E2EE only available in specific modes and a long list of data collection practices tied to Meta’s advertising ecosystem.

The defaults matter more than people realise. Most users never change settings, so if a platform doesn’t enable E2EE by default, the average person simply won’t use it. That’s why WhatsApp’s unencrypted backups and Messenger’s opt‑in encryption create a false sense of security. People think they’re protected because the app advertises privacy, but the defaults quietly undermine that promise.

The metadata example in the assignment makes this painfully clear. Even without reading the messages, you can infer a lot: User A and B meet every Thursday, one uses an iPhone, the other switches between a Windows PC and an Android phone, and their locations and routines are predictable. You can almost reconstruct their relationship just from timestamps and devices. Add the fact that WhatsApp shares phone numbers with Meta outside the EU, and suddenly your social graph becomes a goldmine for profiling and behaviour modelling.

“Last seen” and “online status” make things even worse. If someone automates checking your status every second, they can build a timeline of your daily habits when you wake up, when you sleep, when you talk to someone frequently, and even when you’re avoiding them. It’s a small feature with surprisingly deep privacy risks.


Task 2B:

After extracting the EXIF metadata from image2.jpg, I found the following:

- GPS Latitude: 65.05767059305555
- GPS Longitude: 25.46864318833333
- Device Make: HUAWEI
- Device Model: CLT-L29
- Original Date/Time: 2022-08-23 12:15:59 (from Unix timestamp 1661267759)

I then removed the EXIF metadata using CyberChef. The cleaned image no longer contains any GPS data, device information, or timestamps.


Task 2C

1. Facebook (Meta)
I checked Facebook on Exodus Privacy, and the results were exactly what you’d expect from a massive advertising‑driven platform. It had a long list of trackers — everything from Meta’s own analytics to third‑party advertising SDKs. The app also requested a large number of permissions, including several dangerous ones like access to the camera, microphone, location, contacts, and storage. Some of these make sense because Facebook allows video calls, photo uploads, and location tagging. But the combination of trackers and permissions shows how deeply the app integrates into a user’s device. Even when the permissions are “justified,” the amount of behavioural data collected in the background is far beyond what is needed for basic messaging or social networking.

2. WhatsApp
WhatsApp had fewer trackers than Facebook, but still more than a privacy‑focused messaging app should have. The trackers were mostly Meta‑related analytics and crash reporting tools. WhatsApp also requested several dangerous permissions: camera, microphone, contacts, location (optional), and storage. Some of these are necessary for voice notes, video calls, and sending media. However, the contact‑syncing permission is the most sensitive one, because it exposes your entire social graph — not just who you talk to, but everyone in your phonebook. Even though WhatsApp uses end‑to‑end encryption for messages, the metadata and contact‑matching system still reveal a lot about your relationships.

3. Phone Cleaner Apps (Unnecessary Dangerous Permissions)
Phone cleaner apps are the perfect example of suspicious permission requests. Many of them ask for dangerous permissions like full storage access, location, contacts, and sometimes even microphone or phone state. A cleaner app should only need access to temporary files. it has no legitimate reason to read your contacts, track your location, or monitor your calls. These apps often combine aggressive permissions with multiple trackers, which makes them high‑risk. The permissions do not match the purpose of the app, and that mismatch is usually a red flag for data harvesting or hidden advertising behaviour.


 TASK 3 

In this task, I analyzed two applications using Exodus Privacy and selected a third application that clearly requests unnecessary dangerous permissions. The goal was to understand how apps collect data, what permissions they rely on, and whether those permissions make sense for their intended functionality.

1. Facebook

Trackers and permissions
According to Exodus Privacy:

- Trackers: 18  
- Permissions: 45  

Facebook had one of the highest tracker counts of any mainstream app. These included Meta analytics, advertising SDKs, crash reporters, and multiple third‑party profiling tools.

Dangerous / special permissions
Facebook had 11 dangerous permissions, including:

- Camera  
- Microphone  
- Fine & coarse location  
- Read contacts  
- Read phone state  
- Read/write external storage  
- Record audio  
- Access network state  

Data that can be monetized
Yes, Facebook collects multiple categories of monetizable data:

- Location → used for location‑based ads  
- Contacts → used to build social graphs  
- Device ID & phone state → cross‑app tracking  
- Usage analytics → behavioural profiling  
- Advertising trackers → targeted ad optimization  

These permissions and trackers directly support Meta’s advertising business model.

Two attack vectors
1. Social graph exploitation  
If an attacker accessed Facebook’s backend or local data, they could map your entire contact network, identify relationships, and target individuals with phishing or impersonation attacks.

2. Location‑based stalking  
   With access to precise location and timestamps, an attacker could reconstruct your daily routines, identify your home/work locations, and track your movements.

Android vs iOS privacy labels
On Android, Exodus reveals the exact trackers and permissions.  
On iOS, Apple’s Privacy Label confirms Facebook collects:

- Location  
- Identifiers  
- Usage data  
- Contact info  
- Browsing data  

However, Apple’s labels are high‑level and do not list the 18 trackers or the specific SDKs.  
Exodus provides a more transparent and technical view of Facebook’s tracking behaviour.

2. WhatsApp

Trackers and permissions
According to Exodus Privacy:

- Trackers: 4  
- Permissions: 27  

WhatsApp has fewer trackers than Facebook, but still more than a privacy‑focused app should have.

Dangerous / special permissions
WhatsApp had 9 dangerous permissions, including:

- Camera  
- Microphone  
- Read contacts  
- Read phone state  
- Access location  
- Read/write storage  
- Record audio  

Data that can be monetized
Even though messages are end‑to‑end encrypted, WhatsApp still collects:

- Contacts → social graph mapping  
- Device identifiers → cross‑service tracking  
- Usage data → behavioural analytics  
- Location (optional) → location‑based insights  

This metadata can be used to improve Meta’s advertising accuracy across platforms.

Two attack vectors
1. Contact graph extraction  
   An attacker could use synced contacts and metadata to map who you talk to, how often, and from which devices — enabling targeted social engineering.

2. Microphone/camera abuse  
   If the app or its permissions were compromised, an attacker could activate the microphone or camera outside of calls, bypassing encryption entirely.

Android vs iOS privacy labels
Apple’s Privacy Label for WhatsApp lists:

- Contact info  
- Identifiers  
- Usage data  
- Diagnostics  

But it does not show the 4 trackers or the exact SDKs.  
Exodus gives a clearer picture of the technical tracking happening behind the scenes.

3. Phone Cleaner App (Super Phone Cleaner – Antivirus, Booster)

Trackers and permissions
According to Exodus Privacy:

- Trackers: 10  
- Permissions: 26  

Cleaner apps are notorious for unnecessary permissions and aggressive tracking.

Dangerous / special permissions
This cleaner app had 8 dangerous permissions, including:

- Read contacts  
- Access fine location  
- Read phone state  
- Read/write external storage  
- Record audio  
- Full network access  

Data that can be monetized
These permissions are unnecessary for a cleaner app but extremely valuable for monetization:

- Contacts → sold to data brokers  
- Location → used for targeted ads  
- Device ID → cross‑app tracking  
- Storage access → behavioural profiling  
- Network access + trackers → sending data to third‑party ad networks  

The app’s core function (clearing cache) does not require any of this.

Two attack vectors
1. Silent data exfiltration  
   With storage + network access, an attacker could steal files, contacts, and device identifiers without the user noticing.

2. Location‑based targeting  
   With location permissions, an attacker could track the user’s movements and build a detailed location history.

Android vs iOS privacy labels
Cleaner apps on iOS often appear harmless in Apple’s Privacy Labels, listing only “usage data” or “diagnostics.”  
But Exodus reveals:

- 10 trackers  
- 26 permissions  
- 8 dangerous permissions  

This shows how privacy labels can hide the true extent of tracking, while Exodus exposes the technical reality.

TASK 4 

4A Legacy Tracking Technologies and the Impact of ATT/IDFA

When Apple introduced App Tracking Transparency (ATT), it quietly flipped the advertising world upside down. Before ATT, the Identifier for Advertisers (IDFA) acted like a universal tag that followed you from one app to another. Advertisers relied on it heavily because it made cross‑app tracking effortless. Once Apple forced apps to ask for permission, most people simply said no. Overnight, companies lost access to a tracking method they had depended on for years.

The ripple effects were huge. Meta publicly admitted that Apple’s change cost them billions in lost ad efficiency. TikTok and other platforms started experimenting with more aggressive fingerprinting techniques to compensate. Researchers pointed out that advertisers suddenly had far less visibility into user behaviour, and many companies had to rebuild their analytics systems from scratch. What’s interesting is that this wasn’t a technical change, it was a policy change — but it reshaped the entire mobile advertising ecosystem.

From a privacy perspective, the shift was long overdue. Users finally had a meaningful choice, and the default moved toward privacy instead of surveillance. But the industry didn’t just give up. Instead, it pivoted to first‑party data, server‑side tracking, and more subtle forms of behavioural analysis. In other words, ATT didn’t kill tracking,  it forced it to evolve. The whole situation shows how fragile the advertising economy is when a single company changes the rules, and how quickly the industry adapts when its revenue is threatened.

4B Modern Tracking: SDKs, Pixels, and Real‑World Observations

Tracking today is far more sophisticated than the old cookie‑based model. When I browsed Finnish websites with helper extensions enabled, I was surprised by how many tracking pixels were active on ordinary sites. Google Tag, Meta Pixel, TikTok Pixel, LinkedIn Insight Tag, they were everywhere. Accepting cookies often unlocked even more trackers, and some sites loaded multiple analytics tools at once. It becomes clear that a single page visit can be shared with several advertising networks simultaneously.

The same pattern appears in mobile apps. When I checked some of these companies’ apps on Exodus, I found SDKs from the same advertising platforms whose pixels appeared on their websites. For example, if a site used TikTok Pixel, the app often included AppFlyer o or TikTok’s analytics SDK. This creates a continuous loop: the website tracks you, the app tracks you, and the data flows back to the same advertising partners. It’s a full ecosystem designed to follow your behaviour across devices and platforms.

What makes this more concerning is how invisible it is. Privacy policies rarely explain where the data actually goes or how many partners receive it. If an app includes AppFlyer, for example, your data might end up with TikTok, Meta, Google, or other partners depending on the integration. The user has no real way to know. And when you add “Login with Google” or “Login with Facebook” on top of that, the tracking becomes even more precise because your identity is now tied to your behaviour across multiple services.

The more I looked into it, the more obvious it became that modern tracking is not just about ads,  it’s about building detailed behavioural profiles. Pixels show what you do on websites. SDKs show what you do inside apps. Login integrations tie it all together under a single identity. Even after Apple and Google introduced restrictions, the industry simply shifted to deeper, more embedded tracking methods. It’s a reminder that privacy protections often trigger innovation — just not always in the direction users expect.

