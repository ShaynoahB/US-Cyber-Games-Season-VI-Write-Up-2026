Description

Mr Jiggles my pet cat ran away and when I put up flyers this was the photo I used. I feel it really captures his catty essence. Regardless, I think it would have been helpful if I had been able to extract data about him and maybe learn more about his whereabouts. (He came home 2 weeks ago don’t worry)

Solution

1. Used exiftool to analyze image metadata and discovered a Base64 encoded string in the comment field in the metadata.
<img width="642" height="511" alt="image" src="https://github.com/user-attachments/assets/5d8f197a-dbbe-409d-b5fd-9ee9e8a47517" />
2. Decoded the string in CyberChef
<img width="1038" height="635" alt="image" src="https://github.com/user-attachments/assets/7e66d8e2-243e-4d15-bd01-1b4d04637353" />

Flag

SVIBRG{Y0u_F0unD_Mr_J1GgL3$!}
