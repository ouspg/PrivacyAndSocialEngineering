# **Week 3** 

## **Task 1:** Hardcoded Passwords

There have been a few cases of compromised systems due to hardcoded passwords and API keys accidentally ending up in production code. [Google offers some advice how to handle such information more securely](https://cloud.google.com/docs/authentication/api-keys)

Use Hex-Rays decompiler via [Dogbolt](https://dogbolt.org/) to check out if you can find a single hardcoded password from the provided compiled C code. There is also a secret 'Activation Key' for you to figure out, which has validation arguments that can be seen with the some closer inspection of the decompiler

You can run the C program in your terminal by navigating to the same folder where the file resides and and using the command **./secretKey**

Return a valid **password** and a **valid activation key** along with the **instructions** on how to create a activation key, since there are multiple correct activation keys
