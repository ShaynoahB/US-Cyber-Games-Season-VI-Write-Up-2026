# Description

Help us ensure that our 3d assets are safe!


# What I Found

1. Opened the website and found a platform related to 3D assets.

   <img width="1800" height="923" alt="image" src="https://github.com/user-attachments/assets/13256454-c921-4eea-a533-b9fc523985fc" />

2. Clicking the For Devs button revealed an announcement containing information about the application's development environment.

   <img width="548" height="258" alt="image" src="https://github.com/user-attachments/assets/835d8191-209e-46e4-b1fd-36d5e7574de0" />

3. Using Burp Suite, I intercepted requests and modified the HTTP method from GET to POST. The response exposed an archived path:

   <img width="897" height="753" alt="image" src="https://github.com/user-attachments/assets/87ba3814-c750-4649-b654-2a9d47cfe0fb" />

4. Navigating to the exposed path resulted in the download of a file named file_backup.sys.


<img width="737" height="697" alt="image" src="https://github.com/user-attachments/assets/2611f492-59d5-41f4-924e-1acf1e2d0c03" />


5. This is where i got stucked :( Opening the file in a text editor revealed certificate-like data encoded in Base64. After decoding the data, I identified references to OpenSCAD, a script-based 3D modeling application.

<img width="1105" height="556" alt="image" src="https://github.com/user-attachments/assets/e90c8522-ae92-427b-9fba-dc0ba6f7f064" />
