# Social-Engineering-attack
This is a typical workflow used in security audits and penetration testing to assess an organization's vulnerability to social engineering.
The provided images illustrate a demonstration of a **Credential Harvester Attack** using the **Social-Engineer Toolkit (SET)**, a penetration testing framework.

Here is an explanation of the contents:

### 1. Social-Engineer Toolkit (SET) Interface
The first image shows the main menu of the Social-Engineer Toolkit (SET), created by David Kennedy (ReLiK) of TrustedSec.
* **Purpose:** SET is a platform designed for social engineering testing and is used by ethical hackers (penetration testers) to simulate attacks.
* **Menu Options:** The main menu lists various attack vectors, including:
    1)  Spear-Phishing Attack Vectors
    2)  **Website Attack Vectors** (Selected for the demonstration)
    3)  Infectious Media Generator
    4)  Create a Payload and Listener
    5)  Mass Mailer Attack
    6)  Arduino-Based Attack Vector
    7)  Wireless Access Point Attack Vector
    8)  QR Code Generator Attack Vector
    9)  Powershell Attack Vectors
    10) Third Party Modules

### 2. Website Attack Vectors Menu
The second image shows the sub-menu for Website Attack Vectors after selecting option '2'.
* **Methods:** It describes several web-based attack methods aimed at compromising a victim, such as the Java Applet Attack, Metasploit Browser Exploit, **Credential Harvester** (selected in the next step), Tabnabbing, Web Jacking Attack, Multi-Attack, and HTA Attack Method.

### 3. Credential Harvester Setup
The third and fourth images detail the setup for the Credential Harvester Attack, which is initiated by selecting '3' from the Website Attack Vectors menu, and then '2) Site Cloner' from the Webattack menu.

* **Attack Method:** The **Credential Harvester** attack is designed to clone a legitimate website that has username and password fields and then harvest the credentials entered by the victim.
* **Site Cloning:** The user selects 'Site Cloner' and then inputs the target website URL to clone, in this case, `https://github.com/login`.
* **IP Address:** The user specifies an IP address (`192.168.113.128`) for the POST back in the Harvester/Tabnabbing attack, which is where the stolen credentials will be sent.
* **Networking Note:** There is an **IMPORTANT** note explaining the use of external IP addresses and the necessity of port forwarding if the attack is being run from a private network and accessed externally, emphasizing that this is a fundamental networking concept, not a SET issue.
* **Cloning Process:** The toolkit begins the process of cloning the GitHub login page.

### 4. Attack Execution and Credential Capture
The fourth image also shows the successful execution and logging of the attack.

* **Server Running:** The image confirms that the Social-Engineer Toolkit Credential Harvester Attack is running on port 80.
* **Logging and Capture:** It shows the POST data captured when a user (possibly the attacker for testing or the victim) submits a form on the cloned page. It specifically logs a **POSSIBLE USERNAME FIELD FOUND: login=shreya** and a **POSSIBLE PASSWORD FIELD FOUND: password=hegde**.

### 5. Cloned Website and Email Lure
The fifth, sixth, and seventh images show the victim-side of the attack.

* **Cloned Page:** The fifth image displays the cloned GitHub Sign in page, which appears identical to the real one to the victim.
* **Phishing Email:** The sixth image shows the attacker composing an email that contains a link to the real GitHub login page (`https://github.com/login`) but has the link text masked by the attacker's server address (`http://192.168.113.128/`). This is a common phishing technique to lure a victim.
* **Victim's Inbox:** The seventh image shows the email as received by the victim (Shreya Hegde), where the displayed link is the legitimate GitHub URL, but clicking it would lead to the attacker's cloned site if the masking was successful.

---

**In summary, the images document the process of setting up and executing a highly effective phishing attack using the Social-Engineer Toolkit to clone a legitimate login page (GitHub) and harvest a user's credentials.** This is a typical workflow used in security audits and penetration testing to assess an organization's vulnerability to social engineering.
