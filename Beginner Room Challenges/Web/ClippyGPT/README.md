# Description

# Solution
1. Opened the web application and discovered a chatbot-style interface.

   
<img width="1772" height="932" alt="image" src="https://github.com/user-attachments/assets/09224c6d-3c3b-4a6a-baf5-9d6512774b0c" />


2. Ran the !help command to enumerate the available commands and identified a get_flag option. Attempting to use it resulted in an authorization failure, indicating that additional privileges were required.

   
   <img width="961" height="737" alt="image" src="https://github.com/user-attachments/assets/34fdaabf-2913-42ac-aab1-add859549ab4" />

   
3. Inspected the page source and discovered a note to the developers including a signing key: 'cl1ppy1123!!!' and instructions to change 'ai_mode' to debug.

   
   <img width="1285" height="382" alt="image" src="https://github.com/user-attachments/assets/afd55834-06e8-441c-b3e9-a2d1cd13270a" />

   
4. The exposed information suggested that user permissions were controlled through a signed token.

    
5. Using Burp Suite, I intercepted requests and identified a session token.

    <img width="621" height="380" alt="image" src="https://github.com/user-attachments/assets/6b0d5209-8ee7-4980-8a85-d3367a5a41ae" />

6. Decoding the token revealed that it was a JSON Web Token (JWT) signed using the HS256 algorithm.

    <img width="1422" height="676" alt="image" src="https://github.com/user-attachments/assets/c677a50c-f3f0-4f8d-bc74-8ccb5dcc1560" />

7. I got stuck at this point because I tried editing the payload portion of the session id in CyberChef. However, I discovered that BurpSuite has a JWT Editor extension. With this extension you can edit the header or payload and even tried common jwt attacks.
8. Since the JWT header specified the HS256 algorithm, the exposed signing key could be used as the symmetric secret for generating a valid signature.

    <img width="902" height="775" alt="image" src="https://github.com/user-attachments/assets/3de6ca7e-5e3d-467c-aab6-b6115aa52ede" />

9. After importing the key into JWT Editor, I modified the payload to elevate my permissions and re-signed the token.

    <img width="1145" height="862" alt="image" src="https://github.com/user-attachments/assets/a712f9c5-ed23-4ed0-b86c-67728ea1170d" />
    
10. Sending the modified JWT confirmed that the privilege changes had taken effect.

    <img width="323" height="210" alt="image" src="https://github.com/user-attachments/assets/4f0654ed-0e1a-4c54-ba34-5137b52a5625" />

11. Yay! So, I know that worked so let's get the flag!

    <img width="595" height="232" alt="image" src="https://github.com/user-attachments/assets/0d01d594-2397-4190-8ca1-e483b7b7efff" />

12. Oops. Looks like I have to change the user part in the payload.

    <img width="287" height="292" alt="image" src="https://github.com/user-attachments/assets/59ff326f-5413-4352-95ab-0556badd8f1e" />

13. Yay! Got the Flag

<img width="381" height="263" alt="image" src="https://github.com/user-attachments/assets/789ba37c-0cbe-495b-8533-2fb3c4047877" />


# Flag

SVIBGR{jw7_4i_7rus7_issu3}
