# Description

Mid-Atlantic Cyber Systems publishes a public status page for customers. A recent internal review suggests something sensitive may have been left too close to the public incident feed.

# Solution


1. Opened the website and observed a service status dashboard displaying operational components and incident information.

<img width="1206" height="928" alt="image" src="https://github.com/user-attachments/assets/82bcc07e-2d9e-4503-adda-feceafb638a6" />

   
2. Inspected the page source and discovered that the dashboard was retrieving its data from backend API endpoints.

   <img width="521" height="445" alt="image" src="https://github.com/user-attachments/assets/69bed27c-104a-4cb4-bb3c-79e5415cad7f" />

3. Intercepted the application's traffic using Burp Suite and identified a request to the endpoint: "/api/incidents?public=1". The "?public=1" query parameter stood out so I researched that and found out that 1 = private and 0 = public

<img width="482" height="150" alt="image" src="https://github.com/user-attachments/assets/3004b7a2-daca-4fc5-b1e5-def9a37b29b0" />

4. Modified the request by changing the parameter value from 1 to 0 and resent the request through Burp Suite. 
   <img width="427" height="227" alt="image" src="https://github.com/user-attachments/assets/1a8e372d-0248-4f1f-a940-869c81ce4e19" />

5. The server returned an additional incident report that was not displayed in the normal user interface. Reviewing the contents of the hidden incident report revealed the flag.
   
   <img width="870" height="410" alt="image" src="https://github.com/user-attachments/assets/17167f68-1ec1-4b0a-a8b6-ddc5244d802c" />


# Flag

SVIBGR{pr073c7_y0ur_s747us_p4g3s}
