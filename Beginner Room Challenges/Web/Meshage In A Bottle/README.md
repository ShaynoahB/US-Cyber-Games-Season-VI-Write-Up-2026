Description

Help us ensure that our 3d assets are safe!


Steps

1. Open the site to see

   <img width="1800" height="923" alt="image" src="https://github.com/user-attachments/assets/13256454-c921-4eea-a533-b9fc523985fc" />

2. Pressing the 'For Dev' button to see this annoucement

   <img width="548" height="258" alt="image" src="https://github.com/user-attachments/assets/835d8191-209e-46e4-b1fd-36d5e7574de0" />

3. Open BurpSuite, intercepted the site and changed the header to Post. This revela an archived path called '/assets_production_system_v3/bak/file_backup.sys'. This made me realize I could've just change the URL to v3

   <img width="897" height="753" alt="image" src="https://github.com/user-attachments/assets/87ba3814-c750-4649-b654-2a9d47cfe0fb" />

4. This downloaded a file which I opened in notepad which a certificate data is showed.


<img width="737" height="697" alt="image" src="https://github.com/user-attachments/assets/2611f492-59d5-41f4-924e-1acf1e2d0c03" />


5. This is where i got stucked :( Im assumming I had to used Openssl and maybe upload the file in BurpSuite
