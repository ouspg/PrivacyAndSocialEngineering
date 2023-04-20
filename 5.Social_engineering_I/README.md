## **Task 2:** Social Engineering Toolkit

**Probably requires course VM for full functionality | min requirement is Linux**

[The Social Engineering Toolkit](https://github.com/trustedsec/social-engineer-toolkit) (SET or SEToolkit) is an open-source penetration testing framework[^1] designed for social engineering. It is being maintained by [TrustedSec](https://www.trustedsec.com/), a full-service Information Security consulting organization. They have created other useful tools as well, you can find these in their [GitHub](https://github.com/trustedsec).

The tool is very well documented on their "[SET user manual](https://github.com/trustedsec/social-engineer-toolkit#set-tutorial)" found on the tools github page, we encourage you to explore this manual when using the tool. 

### **Task 2A)** QR Code[^2] Credential Harvest[^3]

Take a look at the SET's tool QR code creation and web attack type credential harvest. In this task we create a QR code for your self hosted credential harvest page, and a poster to try and get people to scan it. We encourage you to get creative with your poster, it's important it would seem legitimate.

You can set the address to the QR code and the harvester page as your local address, in a real world situation you would set it as your server to actually collect credentials from people in different networks, this also makes the use of HTTPS certificates[^4] possible. You can use any site you want; cloned, self created or ready-to-use templates from the tool. Only requirement is, that it has to have the capability to harvest credentials.

You could for example use the following poster to have a twitter login page for credential harvesting and after entering your credentials it redirects you to the actual address, in this case https://twitter.com/SecurityPelle. This example could be found at a cafe near an office you'd like to collect credentials from or at a lounge of a hotel if you're looking to gather a bunch of random credentials.

You do not have to publicly host the site, it is enough if you can test it with the pc and phone in same network.

**What to return:**  
- The poster  
- Scenario for usage  
- Site used for harvesting  
- Screenshot of the credential harvest tool successfully returning you the input credentials (Your name as username and surname as password)

<details>
<summary>An example poster</summary>
<br>
<img src="https://user-images.githubusercontent.com/20062360/233234591-c534cadf-06a7-473c-9562-64e0bf3e84ef.PNG" alt="An example poster"/>
</details>

### **Task 2B)** Tool Walkthrough

SET has a plethora of cool and interesting utilities and you can create a huge arsenal of potential attacks with them. So in this task you get to choose a tool or a set of tools to create a "walkthrough" for an attack. Document the usage of the tool and provide atleast one plausible use case for it. You are required to include atleast one image or video for the walkthrough. Think of the walkthrough as teaching somone such as an employee, how to conduct your companys basic attack with the tool.

The walkthrough should make the usage of the tool clear and doable for people with atleast some CLI experience.

**What to return:**  
- The walkthrough, included the use case, images and/or videos  
- Why you picked the tool or tools you chose  

---

## **Task 3:** Security Questions

Security questions are still often used to confirm your identity in online services

Work with this **Account recovery chatbot** and try to reset the password of a long lost account called **PewDie** that may have once belonged to the internet personality **Felix Kjellberg**

When you are successful, download the conversation in JSON format and return it

//chatbot in not currently hosted//

---

[^1]: [Pentesting frameworks](https://www.mitnicksecurity.com/blog/what-is-a-pentest-framework)
[^2]: [QR code](https://en.wikipedia.org/wiki/QR_code)
[^3]: [Credential Harvesting](https://www.geeksforgeeks.org/what-is-credential-harvester-attack/)
[^4]: [HTTPS Certificates](https://en.wikipedia.org/wiki/HTTPS#Acquiring_certificates)
[^5]:
[^6]:
[^7]:
[^8]:
[^9]:
[^10]:
[^11]:
[^12]:
[^13]:


