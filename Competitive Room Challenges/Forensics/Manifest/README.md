# Description

Lakeshore Threat Lab confirmed an attacker pivoted from FIN-WS-07 to NAS-MARITIME-01, the Wabash Marine NAS that hosts the internal Lakefront Fleet Manager web app on port 8088. Imani Boateng captured a short east-west slice of that pivot. Her capture is attached.

# Solution
1. Opened the pcap in Wireshark and examined the packcets
   
   <img width="1256" height="747" alt="image" src="https://github.com/user-attachments/assets/0b693269-e9e7-4f25-9dea-09ad650c746f" />

2. Notice some HTTP communciation so I 'Follow HTTP Stream' on the some of the packets. I see the person pivot to server backup . I also see that files were sent
   
   <img width="1242" height="870" alt="image" src="https://github.com/user-attachments/assets/b5b88b03-d23b-486e-9afe-3c7a8b1b2c1e" />

   
3. I Export the HTTP objects to further investigate the files.
   
 <img width="742" height="537" alt="image" src="https://github.com/user-attachments/assets/1be79501-dc31-4329-b592-3866d889798c" />

 
4. In the dispatcher file, it mentions speaking with the "master"
   
   <img width="632" height="441" alt="image" src="https://github.com/user-attachments/assets/6b51b8ac-1278-4199-8b0e-889068c94e0b" />

5.  So, in the csv file that list all the crew members, I looked for the "master" in which there was a text that was encoded in Base64. I put the string into CyberChef to decode the flag
 
   <img width="1305" height="660" alt="image" src="https://github.com/user-attachments/assets/3755cf77-fc10-4825-b150-128621aa6d6a" />

# Flag

SVIUSCG{wabash_finws_pivot_nas_maritime_01}
