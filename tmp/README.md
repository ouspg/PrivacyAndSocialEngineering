## **Task 3:** Windows 10 Privacy Hardening

Provided with a clean virtual machine install of Windows 10. Install the utilities you want and/or need to analyze your network traffic (such as [wireshark](https://www.wireshark.org/) or [Windows Diagnostic Data Viewer](https://docs.microsoft.com/en-us/windows/privacy/diagnostic-data-viewer-overview) Keep in mind that the latter is proprietary software from microsoft). 

**Hot Tip:** You can install Windows 10 Home Edition without a Microsoft account if you do not have an internet connection. You can do this by disabling the internet connection of your VM

Get a baseline of traffic leaving your machine. By analyzing it you may find destinations for the traffic, document all these findings.

Windows has built-in settings to protect your privacy and limit what data is actually collected. Do your best to harden your machine and minimize the amount of data transmitted to microsoft or its partners. You can follow instructions and/or tools you can find online (such as [O&O ShutUp10++](https://www.oo-software.com/en/shutup10)), but make sure you understand what you are doing. You can always wipe the installation if you happen to break something permanently.

Once you have hardened your machine, re-analyze its traffic. Document your findings and compare them to your previous results. If there are or if you have noticed that the operating system behaves differently, document your findings.

Make a detailed summary of your research, including actions taken to harden the OS and what changed in its behaviour. Do you think these trade-offs are worth the loss your data?

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

## **Task 3:** Blockchain

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
- The owner instantly divided and forwarded the 10,000 to **how many** other addresses
- Addresses that received the 10,000 bitcoin and the corresponding sums to each address

Block
- Hash of the block 57043
- Amount of transactions in the block
- Block reward amount

Miner
- Address of the miner for block 57043
- Has this address spent the block reward they received?


**FYI**: **Maltego** is a great tool for blockchain tracing. It let's you to create a tree like structure out of inbound and outbound transactions from different addresses. It also requires registration.
