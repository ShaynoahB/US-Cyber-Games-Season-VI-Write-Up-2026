# Description

Every traveler comes home with a bag full of souvenirs — some you put on a shelf, some you tuck quietly inside other things so the airport doesn't ask questions.

This postcard came back from a long trip around the world. Open it carefully. Some travelers leave more behind a picture than you'd think.

This is an Around The World challenge submitted by Women in CyberSecurity Middle East (WiCSME)

# Solution
1. Opened the image and immediately suspected steganography. I used binwalk to scan the file and found four hidden "postcards" text files
   
   <img width="713" height="331" alt="image" src="https://github.com/user-attachments/assets/ed1bcafd-fea0-4409-985f-ff75dbb571f2" />

2. I extracted the embedded files and reviewed each one. The flag was located in postcard4.
   
   <img width="582" height="410" alt="image" src="https://github.com/user-attachments/assets/115059cf-8c54-4337-a94d-c10d43c0ddba" />
   
   <img width="665" height="398" alt="image" src="https://github.com/user-attachments/assets/6e0c8b16-0a6d-4b45-aeb7-bd10e0983c0f" />

# Flag

SVIUSCG{p0stc4rds_h1dd3n_p4st_th3_FFD9_h0r1z0n}
