# Description

Lakeshore Threat Lab confirmed an attacker pivoted from FIN-WS-07 to NAS-MARITIME-01, the Wabash Marine NAS that hosts the internal Lakefront Fleet Manager web app on port 8088. Imani Boateng captured a short east-west slice of that pivot. Her capture is attached.

# Solution
1. Opened the PCAP in Wireshark and started examining the packets.
   
   <img width="1256" height="747" alt="image" src="https://github.com/user-attachments/assets/0b693269-e9e7-4f25-9dea-09ad650c746f" />

2. I noticed some HTTP traffic, so I used Follow HTTP Stream on several packets. From the HTTP conversations, I could see the user pivoting to the server_backup system and noticed that files were being              transferred.
   
   <img width="1242" height="870" alt="image" src="https://github.com/user-attachments/assets/b5b88b03-d23b-486e-9afe-3c7a8b1b2c1e" />

   
3. I exported the HTTP objects to investigate the transferred files further.
   
   <img width="742" height="537" alt="image" src="https://github.com/user-attachments/assets/1be79501-dc31-4329-b592-3866d889798c" />

4. Looking through the dispatcher file, I found a reference to speaking with the "master".
   
   <img width="632" height="441" alt="image" src="https://github.com/user-attachments/assets/6b51b8ac-1278-4199-8b0e-889068c94e0b" />

5.  I then opened the crew member CSV and filtered the entries to show only users with the master rank. One of the rows contained a Base64-encoded string.
   
    <img width="1305" height="168" alt="image" src="https://github.com/user-attachments/assets/0338becf-e6dd-4e03-8815-64de3bc49c73" />

 6. I copied the string into CyberChef, decoded it from Base64, and recovered the flag.
    
    <img width="1305" height="660" alt="image" src="https://github.com/user-attachments/assets/3755cf77-fc10-4825-b150-128621aa6d6a" />

# Flag

SVIUSCG{wabash_finws_pivot_nas_maritime_01}
