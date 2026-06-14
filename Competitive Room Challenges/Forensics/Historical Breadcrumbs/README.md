Description

Osprey Capital Management is a Stamford-based boutique hedge fund. Chief compliance officer Camila Orantes suspects that portfolio manager Piper Landau leaked end-of-day positions to an external channel on 2026-07-18. Camila engaged forensic analyst Augustin Vogel at Resilient Peak Forensics, who imaged Piper's workstation and extracted her user profile.

Solution

1. Extracted zip file to find different folders some showing the user PowerShell, Chrome browser used and their bookmarks, cookies, etc data.
2. Some files were sql database. Upload the different databases and went through the tables. In the History database, url table I saw a url that looked different from the others.

   
<img width="757" height="443" alt="image" src="https://github.com/user-attachments/assets/0527a4a1-87be-48e0-b19f-1b9ae2108cd2" />

<img width="941" height="146" alt="image" src="https://github.com/user-attachments/assets/0522973d-9d24-4def-b9eb-1632b2dec03a" />

4.  The tagged look like an encoded text so I put that in CyberChef in which it was encoded in Base64 that revelaed the flag


<img width="1227" height="647" alt="image" src="https://github.com/user-attachments/assets/eb0b7a17-be22-41e9-8928-29d45c4d43bd" />

Flag


SVIUSCG{osprey_chrome_history_leak_url}

