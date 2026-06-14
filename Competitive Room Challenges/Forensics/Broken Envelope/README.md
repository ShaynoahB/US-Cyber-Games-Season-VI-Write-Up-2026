Description

Blue Mountain Geotechnical is a Denver-based soils and rock-mechanics consultancy. A cryptolocker affiliate passed through the firm's file shares and partly corrupted several project archives before IT lead Bela Srivastava pulled the plug. Project engineer Adalyn Proteau needs the site dispatch read before Monday's client meeting.

Solution

1.  Of course, I tried to extract the zip file the regural way, but it is in fact corrupted

   <img width="695" height="560" alt="image" src="https://github.com/user-attachments/assets/07486878-ec6e-47f0-bc1f-fa6645c76037" />

3.  Repaired the corrupted file using 'zip -FF bluemountain_project_archive.zip --out UncorruptedBlueMountain.zip' which

   <img width="607" height="223" alt="image" src="https://github.com/user-attachments/assets/7f0b4c72-1a8a-43f4-b2c5-dbfc1f37906b" />

5.  opened the new zip file
   <img width="332" height="87" alt="image" src="https://github.com/user-attachments/assets/27c659a2-f666-439e-8c77-bab3c2b7de30" />

7.  read the text files. IN the Project-DIspatched  file, there is a string encoded in Base64

   <img width="466" height="163" alt="image" src="https://github.com/user-attachments/assets/a24ee4b3-b81d-494c-88e7-8f2e93bf6425" />

9.  Put that in CyberChef to reveal the flag

<img width="1095" height="610" alt="image" src="https://github.com/user-attachments/assets/8ec14804-82ea-49b3-a949-798366079283" />


Flag

SVIUSCG{bluemountain_zip_eocd_rebuild}
