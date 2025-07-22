1. Windows Defender ("Windows Security" app) is Turned on
    This is Windows' on AntiVirus


2. Real-Time Protection is Turned on (Windows Security -> Virus & threat protection -> Virus & threat protection settings "Manage Settings")


3. Latest updates installed (non-windows apps too) | Why:
    First of all, **outdated software very often contains vulnerabilities**, which can lead to an unwanted actors gaining remote access, executing arbitrary code, escalating privileges, stealing sensitive data from your device. *Vulnerabilities could or do exist in Operating System (Windows itself), Software, 3rd-party apps, etc.* Even worse, there are some tools to find devices with outdated version of OS, Software that are exposed to the internet. SO it is crucial to always have the latest updates on all the apps, OS, etc on your device!
    ention PrivEsc, Exploits, How hackers can discover can discover vulnerable devices using search engines


4. Using strong password | Why: 
    **This is another crucial setting, this includes not only your own, administrator accounts but every account existing on the device**. 1 - Easy passwords could be cracked, guessed, etc, leading to unwanted actors getting access to user accounts and estabilishing remote sessions on the device, stealing sensitive data and/or other unwanted & malicious actions; 2 - Even unprivileged accounts MUST have strong passwords, as it could lead to privilege escalation via different ways, e.g unprivileged user still has access to some or all locally stored credentials, software/OS is outdated and is vulnerable to privilege escalation, has 0-day vulnerabilities (newly discovered and not fixed yet) leading to privilege escalation, etc.
    ==I highly recommend not using next things as passwords, even encoded==:
    seasons, months, names, years, dates, usernames, obvious things, easy combinations


5. Regularly updates for OS, software, 3rd-party apps, etc | Why:
    Again, this was mentioned previously, you should often update. Outdates OS versions, software, etc are very often vulnerable to numerous different vulnerabilities. 
    **==IMPORTANT NOTE==**: On Windows there's a thing called "Microsoft Recall" which I HIGHLY RECOMMEND to turn off, also I heard that it could turn on after updates, so turn it off after updates if it does! Here's how to disable it:
    - Open PowerShell as Administrator
    - Type this (check status): Dism /Online /Get-Featureinfo /Featurename:Recall
    - Then type this (disable if exists): Dism /Online /Disable-Feature /Featurename:Recall


6. UAC turned on | Why: 
    UAC (User Account Control) SHOULD be at level 3 (or 4 if you want!). This is important, dont change it to "Never Notify" or level 2, no lower than level 3! 


7. You do not connect to random WI-FIs  | Why:
    Connecting to random WI-FIs could expose your device to various WI-FI attacks, such as **Man-In-The-Middle** (Attackers can position themselves between your device and the internet, intercepting and potentially modifying all traffic including credentials, sensitive data, and communications.), **Evil-Twin** (Malicious actors create fake hotspots mimicking legitimate networks (like "Starbucks_WiFi" or "Airport_Free") to capture login credentials and monitor all network activity.), and more. SO it is crucial to never connect to random WI-FIs


8. Closed ports that you dont use/need | Why: 
   This creates a Lateral Movement opportunities for unwanted actors, again as mentioned earlier, there are some tools that could be used to search for open ports on devices on the internet. You can download & use nmap to scan your own device for open ports: 
   **IMPORTANT NOTE:** ONLY RUN SCANS ON THE TARGETS YOU ARE AUTHORIZED TO OR ON YOUR OWN DEVICES!: `nmap -sV -sC localhost` 
   After identifying the open ports, close them if you do not need them
   

9. Not storing sensitive data in plain-text or easily accessible ways:
    It is dangerous and totally not-recommended to store your and others' sensitive data, and credentials, on your device, especially in plaintext could be easily accessed if someone gets access to your device (this includes physical access too!), or is already on your device, remember that they could get access to your device through social engineering too, then your device could become easy target as the sensitive info and credentials are already there


10. PowerShell history
    PowerShell usually stores its command history, so if anyone or you have entered credentials or some other sensitive info in PowerShell, PowerShell commands, it could be found. So I highly advise you to either clear out PowerShell history sometimes or totally disable PowerShell history
