# Description

Osprey Capital Management is a Stamford-based boutique hedge fund. Chief compliance officer Camila Orantes suspects that portfolio manager Piper Landau leaked end-of-day positions to an external channel on 2026-07-18. Camila engaged forensic analyst Augustin Vogel at Resilient Peak Forensics, who imaged Piper's workstation and extracted her user profile.

# Solution

1. Extracted the provided archive and reviewed its contents. The files appeared to contain artifacts from a user's system, including PowerShell history, Chrome browser data, bookmarks, cookies, and browsing history.
   
2. Several of the recovered files were SQLite databases. I examined the databases and reviewed their tables to identify potentially relevant artifacts. While analyzing the Chrome History database, I inspected the    'urls' table and noticed a URL entry that appeared unusual compared to the rest of the browsing activity.
   
   <img width="757" height="443" alt="image" src="https://github.com/user-attachments/assets/0527a4a1-87be-48e0-b19f-1b9ae2108cd2" />

   <img width="941" height="146" alt="image" src="https://github.com/user-attachments/assets/0522973d-9d24-4def-b9eb-1632b2dec03a" />

3.  The tagged look like an encoded text so I put that in CyberChef in which it was encoded in Base64 that revelaed the flag

   <img width="1227" height="647" alt="image" src="https://github.com/user-attachments/assets/eb0b7a17-be22-41e9-8928-29d45c4d43bd" />

# Flag

SVIUSCG{osprey_chrome_history_leak_url}

