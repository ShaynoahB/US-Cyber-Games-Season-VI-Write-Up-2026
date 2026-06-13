Description

Solution
1. Open the website to find a chat-gpt like application

   
<img width="1772" height="932" alt="image" src="https://github.com/user-attachments/assets/09224c6d-3c3b-4a6a-baf5-9d6512774b0c" />


3. Did !help to see command options, to see a get_flag option which I of course tried

   
   <img width="961" height="737" alt="image" src="https://github.com/user-attachments/assets/34fdaabf-2913-42ac-aab1-add859549ab4" />

   
5. Suprise..Spurise.. that didn't work. However, now I know I need to escalate my prvileges to get the flag.

   
7. I inspected the web page to iscover this infomation that should've been taken out.

   
   <img width="1285" height="382" alt="image" src="https://github.com/user-attachments/assets/afd55834-06e8-441c-b3e9-a2d1cd13270a" />

   
9. So i now have a signing key ('cl1ppy1123!!!') for something and I also know that something needs to be modified to grant permissions.

    
11. At first, I didn't know where to really start but I started with Burp Suite as that a common tool for web applications challenges. I came across the session ID.

    <img width="621" height="380" alt="image" src="https://github.com/user-attachments/assets/6b0d5209-8ee7-4980-8a85-d3367a5a41ae" />

12. I pasted the session ID into CyberChef. Which I discovered that is was ecrypted using JWT

    <img width="1422" height="676" alt="image" src="https://github.com/user-attachments/assets/c677a50c-f3f0-4f8d-bc74-8ccb5dcc1560" />

13. I got stuck at this point because I tried editing the payload portion of the session id in CyberChef. However, I discovered that BurpSuite has a JWT Editor extension. With this extension you can edit the header or payload and even tried common jwt attacks.
14. I added a jwt symmmetic signature key (the header tells me that HS256 algorithm was used therefor the key is symmetic) using 'cl1ppy1123!!!'

    <img width="902" height="775" alt="image" src="https://github.com/user-attachments/assets/3de6ca7e-5e3d-467c-aab6-b6115aa52ede" />

15. Then I edited the payload and signed with the generated key.

    <img width="1145" height="862" alt="image" src="https://github.com/user-attachments/assets/a712f9c5-ed23-4ed0-b86c-67728ea1170d" />
15. Forwarded this and tested if my session ai_mode changed; which it did.

    <img width="323" height="210" alt="image" src="https://github.com/user-attachments/assets/4f0654ed-0e1a-4c54-ba34-5137b52a5625" />

16. Yay! So, I know that worked so let's get the flag!

    <img width="595" height="232" alt="image" src="https://github.com/user-attachments/assets/0d01d594-2397-4190-8ca1-e483b7b7efff" />

17. Oops. Looks like I have to change the user part in the payload.

    <img width="287" height="292" alt="image" src="https://github.com/user-attachments/assets/59ff326f-5413-4352-95ab-0556badd8f1e" />

18. Yay! Got the Flag

<img width="381" height="263" alt="image" src="https://github.com/user-attachments/assets/789ba37c-0cbe-495b-8533-2fb3c4047877" />





    






Flag

SVIBGR{jw7_4i_7rus7_issu3}
