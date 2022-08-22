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

Use Hex-Rays decompiler via [Dogbolt](https://dogbolt.org/) to check out if you can find a **plaintext hardcoded password** from the provided compiled C code file called **secretKey**. 

As a second task there is a secret **Activation Key** for you to figure out, which has validation arguments that can be seen with the some closer inspection of the decompiler.

As a third and last task there is a **Super secret password** that is hardcoded, but has been encrypted with a mystery hash.

In case if the site is under maintenance, there is a HexRaysOutput file, which has the full output of the decompilation process. Use an editor that can understands C++ to inspect the file with proper highlighting.

You can run the C program to validate your findings in your terminal by navigating to the same folder where the file resides and using the command **./secretKey**

After completing the task, you have five items to return. Return a valid **password** and **one valid activation key** along with the **instructions** on how to create rest of the activation keys, since there are multiple valid ones. Also return the **plaintext version of the super secret password** and **the name of the hash function** it was encrypted with.

---

## **Task 3:** Blockhain

We will take a brief look at online tools available for inspecting the bitcoin blockchain

Just as a quick recap: **Blockchain** is a ledger containing information of all transactions made with the cryptocurrency. Incoming transactions are added as **blocks** into the blockchain when a valid **hash** is found for a certain block. These hashes are brute forces aka **mined** mainly using the prosessing power of Graphics Processing Units (GPU).

Early Bitcoin developer Laszlo Hanyecz was alledgedly one of the first to invent GPU mining. However, what he is remembered for is the first documented purchase of goods using bitcoin, where he traded **10,000** bitcoin for **2 Pizzas**.

You can find conflicting information from the internet about the pizza parlor where the pizzas were bought from. Aside from that, by inspecting the blockchain we can find exact information about the transaction.

Use the [Blockchain explorer](https://www.blockchain.com/explorer) to inspect the block **57043** and provide the following information.

Transaction
- Date and Time of the transaction
- Hash of the transaction
- Address of sender
- Address of receiver
- Transaction fee amount in bitcoin

Receiver Address
- Who was the owner of this address? Use [OXT.me](https://oxt.me/) and Google to figure out the real name of the user
- Date and Time when he 'spent' the 10,000 bitcoins they received from the trade
- Transaction hash of the above mentioned transaction
- Addresses that received the 10,000 bitcoins and the corresponding sums to each address

Block
- Hash of the block
- Amount of transactions in the block
- Block reward amount

Miner
- Address of the miner for the block 57043
- Has this address spent the block reward they received?


**FYI**: **Maltego** is a great tool for blockchain tracing. It let's you to create a tree like structure out of inbound and outbound transactions from different addresses. It also requires registration.
