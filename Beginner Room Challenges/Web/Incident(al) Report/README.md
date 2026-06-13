Description

Mid-Atlantic Cyber Systems publishes a public status page for customers. A recent internal review suggests something sensitive may have been left too close to the public incident feed.

Solution


1. Open the website to see a service status page

   
3. Inspected the page source to see that its talking to an API to display the different components of the page

   <img width="521" height="445" alt="image" src="https://github.com/user-attachments/assets/69bed27c-104a-4cb4-bb3c-79e5415cad7f" />

4. I intercepted the traffic in BurpSuite and noticed "/api/incidents?public=1" and the "?public=1" caught my eye so I looked that up and found out that 1 = privatr and 0 = public

<img width="482" height="150" alt="image" src="https://github.com/user-attachments/assets/3004b7a2-daca-4fc5-b1e5-def9a37b29b0" />

5. Changed it to 0 in which a hidden incident report appears with the flag in it.
   <img width="427" height="227" alt="image" src="https://github.com/user-attachments/assets/1a8e372d-0248-4f1f-a940-869c81ce4e19" />

   <img width="870" height="410" alt="image" src="https://github.com/user-attachments/assets/17167f68-1ec1-4b0a-a8b6-ddc5244d802c" />



Flag

SVIBGR{pr073c7_y0ur_s747us_p4g3s}
