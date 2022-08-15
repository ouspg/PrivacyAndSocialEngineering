# **Week 3** 

## **Task 1:** PGP Keys

"PGP" Encryption is short for Pretty Good Privacy, an encryption program originally published by Phil Zimmermann & Associates in 1991. Later on derivatives [OpenPGP](https://www.openpgp.org/) and [GPG](https://gnupg.org/) were introduced, which stand for Open-Source PGP and GnuPG/Gnu Privacy Guard respectively. OpenPGP became standardized by the [IETF](https://www.ietf.org/) and GPG was specifically designed to be compatible with OpenPGP and allows the decryption of OpenPGP encryption. These encryptions allows users to quite easily have for example encrypted email conversations.

"*Arguing that you don't care about the right to privacy because you have nothing to hide is no different from saying you don't care about free speech because you have nothing to say.*" – **Edward Snowden**

Using any(**LEGAL**) means necessary try to stay **as private** and **as anonymous as possible** and exchange public keys to start an encrypted email conversation with your randomly selected classmate. Your goal is to have the conversation **as unlinkable** to yourself **as possible** even for statewide actors. Being completely untraceable is quite impossible, the important part here is to learn and show how invisible you can become and what it takes.

* Document your acions precisely, and name software or services used to the best of your ability. 
* Describe the experience and how difficult you found this to be.

Task will be graded based on the methods used and actions taken to accomplish the conversation and by the level of anonymity achieved.

---

## **Task 2:** Hardcoded Passwords

There have been a few cases of compromised systems due to hardcoded passwords and API keys accidentally ending up in production code. [Google offers some advice how to handle such information more securely](https://cloud.google.com/docs/authentication/api-keys)

Use Hex-Rays decompiler via [Dogbolt](https://dogbolt.org/) to check out if you can find a single hardcoded password from the provided compiled C code file called **secretKey**. There is also a secret 'Activation Key' for you to figure out, which has validation arguments that can be seen with the some closer inspection of the decompiler

In case if the site is under maintenance, there is a HexRaysSecretKey file, which has the full output of the decompilation process. Use an editor that can understands C++ to inspect the file with proper highlighting.

You can run the C program to validate your findings in your terminal by navigating to the same folder where the file resides and using the command **./secretKey**

Return a valid **password** and a **valid activation key** along with the **instructions** on how to create an activation key, since there are multiple correct activation keys
