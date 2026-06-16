# Description

Mr Jiggles my pet cat ran away and when I put up flyers this was the photo I used. I feel it really captures his catty essence. Regardless, I think it would have been helpful if I had been able to extract data about him and maybe learn more about his whereabouts. (He came home 2 weeks ago don’t worry)

# Solution

1. The challenge description mentioned learning more about the subject's "whereabouts," which suggested that the solution might involve examining the image metadata. Metadata can contain information such as GPS coordinates, timestamps, camera details, and user-added comments.
   
2. Used ExifTool to analyze the image metadata and identified a Base64-encoded string stored in the Comment field.
   
<img width="642" height="511" alt="image" src="https://github.com/user-attachments/assets/5d8f197a-dbbe-409d-b5fd-9ee9e8a47517" />

3. Copied the encoded string and decoded it using CyberChef, which revealed the flag.
<img width="1038" height="635" alt="image" src="https://github.com/user-attachments/assets/7e66d8e2-243e-4d15-bd01-1b4d04637353" />

# Flag

SVIBRG{Y0u_F0unD_Mr_J1GgL3$!}
