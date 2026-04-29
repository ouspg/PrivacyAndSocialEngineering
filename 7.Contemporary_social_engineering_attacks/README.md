TASK 1 
What it is and how to prevent the effects in a professional environment
Deepfakes are AI‑generated videos or audio that make someone appear to say or do something they never did. In a professional environment, they can be used to impersonate managers, approve fake payments, or pressure employees.  
To prevent this, companies need clear verification rules, technical checks, and training that teaches employees not to trust video or voice alone.

1. Does intelligence gathering change in a deepfake attack? What changes?
Yes. Deepfake attacks need better quality information than normal social engineering. Attackers look for:  
- Clear videos of the target  
- Clean audio recordings  
- How the person talks, moves, and behaves  
- Their role, authority level, and who they usually contact  

The attacker needs enough material to make the fake look believable.

2. Why do deepfake attacks have so much power and influence on employees?
Because people trust what they see and hear.  
If someone looks and sounds like a boss or senior manager, most employees won’t question it. Add urgency or pressure, and people follow instructions quickly. Deepfakes exploit authority, trust, and stress.

3. Could pure employee training prevent such attacks completely?
No. Training helps, but it can’t stop everything.  
Deepfakes are getting too realistic, and humans can’t reliably detect them. Under pressure, people still make mistakes. Training must be combined with verification steps and technical controls.

4. How would you prevent catastrophic incidents in a work environment?
I would push for:  
- Verification rules (no approvals based only on video or voice)  
- Call‑back checks using known internal numbers  
- Two‑person approval for payments or sensitive actions  
- Clear escalation channels so employees can question suspicious requests  
- Technical tools that detect deepfake signs or unusual behavior  

These layers make it harder for a fake video call to succeed.

5. Existing technical solutions — try at least one and report back
I tested Deepware Scanner, a deepfake detection tool.  
It checks videos for manipulation by looking at visual inconsistencies.

Was it successful?
It detected some obvious deepfakes, but high‑quality ones were harder to catch.  
So it’s helpful, but not fully reliable.

6. Possible new technical solutions
- Real‑time “liveness” checks during video calls  
- Cameras that add a digital authenticity signature  
- Voiceprint verification for executives  
- AI tools that flag unusual speech or behavior patterns  

BONUS TASK
What tool did you use?  
I used Reface on my Android phone. It’s a faceswap tool.

Do you think your video could fool someone?  
Yes, at first glance it could. If someone looks closely, they might notice small glitches.

Was it easy?  
Yes. The setup was simple and the swap worked quickly.

TASK 2 — Shockvertising 
1. Define shockvertising and identify key characteristics in digital/social media marketing.
Shockvertising is an advertising approach that uses provocative, disturbing, or emotionally intense content to grab attention quickly. In digital and social media, it stands out because people scroll fast, and shocking content breaks through the noise.

Key characteristics:  
- Uses fear, disgust, surprise, or emotional discomfort  
- Designed to stop scrolling and force attention  
- Often controversial or morally uncomfortable  
- Relies on strong visuals and short, impactful messages  
- Works well in fast‑moving platforms like Instagram, TikTok, and X  
- Can go viral because people react strongly and share it  


2. Pick and analyze two shockvertising campaigns and explain how they use social engineering.

Campaign 1: Anti‑Smoking “Black Lungs” Campaign (Public Health)
This campaign showed graphic images of damaged lungs on cigarette packs and posters.  
Social engineering strategies used:  
- Fear appeal: triggers emotional discomfort to change behavior  
- Authority: backed by health organizations, making the message harder to ignore  
- Loss aversion: shows what people risk losing (health, life)  
- Pattern interruption: the graphic images shock people out of their normal routine  

Campaign 2: Road Safety “Don’t Text and Drive” Crash Ads
Many countries use ads showing sudden car crashes caused by texting.  
Social engineering strategies used:  
- Shock and fear: creates a strong emotional reaction that sticks  
- Urgency: shows how one small action (checking a message) can instantly cause disaster  
- Relatability: targets everyday behavior people don’t see as dangerous  
- Behavior manipulation: uses emotional impact to push people to change habits  

Both campaigns use the same principle: hit the emotions first, then deliver the message.

3. Should there be guidelines or regulation balancing attention‑grabbing advertising with social responsibility?
Yes, there should be guidelines. Shockvertising can be effective, but it can also cross ethical lines, traumatize viewers, or target vulnerable groups. Regulations can help ensure that:  
- The message is still responsible and not harmful  
- Graphic content is used only when necessary  
- Children and sensitive audiences are protected  
- Campaigns don’t exploit fear or trauma for clicks  
- Public health goals don’t turn into emotional manipulation  

A balance is needed: strong messages without causing unnecessary harm.


TASK 3 — Agentic Mistakes

1. Operating system running the bot
From the bot’s responses and the way it handled system‑style commands, it looked like it was running on a Linux‑based environment. The bot leaked enough hints through its replies to show it wasn’t sandboxed properly and had access to typical Linux paths and commands.

2. How it is connected to Pelle Security
The bot repeatedly referenced PelleSecurity in its internal messages and metadata. It looked like the bot was either:  
- running on a device owned by Pelle, or  
- configured by Pelle as part of a testing or research setup.  

The bot’s own responses exposed this connection without being asked directly, which is an agentic mistake.

3. Does Pelle have security keys on this device? What is it in plaintext?
Yes. The bot accidentally revealed that Pelle’s SSH/private keys were stored on the same machine.  
It even exposed the plaintext content when manipulated with social‑engineering prompts.  
This is a major security failure because private keys should never be accessible to an LLM‑powered bot.

4. What is the bot actually intended to do?
The bot seemed intended as a Telegram automation bot for testing, research, or internal tasks.  
It wasn’t designed to answer system‑level questions, but because it wasn’t sandboxed, it responded to prompts as if it had access to the underlying machine.  
So instead of being a simple chat bot, it behaved like an exposed agent with system visibility.

5. What software it actually is, and why you should never run something like this on personal/work machines
It appeared to be running on top of a local LLM agent framework (something like a Python Telegram bot connected to an LLM backend).  
The problem is that it had:  
- access to the file system  
- access to environment variables  
- access to private keys  
- no isolation or sandboxing  

Running this kind of bot on a personal or work machine is dangerous because:  
- It can leak sensitive files  
- It can reveal credentials  
- It can expose internal paths  
- It can be manipulated into revealing system information  

This is exactly what happened here.

6. What went wrong allowing you to find these details? Could you run software on their devices via this?
What went wrong:  
- The bot had no sandbox  
- It had full access to the host machine  
- It responded to system‑style prompts without restrictions  
- It trusted user input too much  
- It didn’t filter or block sensitive commands  
- It didn’t separate the LLM from the underlying OS  

Because of these mistakes, the bot leaked:  
- OS details  
- File paths  
- Private keys  
- Internal configuration  

Could you run software on their device?  
No not directly.  
The bot exposed information, but it didn’t actually execute arbitrary code.  
However, the level of leakage was serious enough that, in a real‑world scenario, an attacker could use the exposed keys or system info to escalate further.

The OUSPGbot suffered from classic agentic mistakes: too much access, no sandboxing, and no filtering.  
This allowed simple social‑engineering prompts to reveal sensitive information that should never be exposed by a bot.

