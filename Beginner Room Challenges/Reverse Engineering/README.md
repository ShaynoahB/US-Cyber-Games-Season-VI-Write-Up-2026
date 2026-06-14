Description

A retired cutter's maintenance utility will not bring an emergency beacon back online until the correct override phrase is entered. Recover the phrase from the binary and submit it as the flag.

Solution


1.EXFTOOL th file to confirm its an ELF


2. Changed the permmission of the file so I can run it

   
4. Ran the file

   
6. Open the file in Ghidra

   
8. In the main function (i renamed the fucntion from what ghidra created to help me keep track), I see the process output when we ran the exectuable in temrinal but now we can see that user input isnt being compared

   
<img width="1218" height="612" alt="image" src="https://github.com/user-attachments/assets/bc927eea-a87a-4091-ba6e-1b52501acad3" />

10. First we see that user input (aso what i renamed) it ran through the FUN_00401184 function first.

    
6. The function just removes a \n (santizing function)

   
   <img width="382" height="215" alt="image" src="https://github.com/user-attachments/assets/1557e40b-113f-434c-9a1e-c3fd0b2e71ec" />

8. Then the varible is put in FUN_004011d2 which a integer is suppose to return.

   
10. This function is very important. It shows us the condition. First it checks if the parameter passed is 23 long

<img width="527" height="353" alt="image" src="https://github.com/user-attachments/assets/a6d99dc0-f2c0-47ab-bfd7-c2fe9cdb920e" />

10. Then it first does a mathematical operation on user input in function FUN_00401166. Upon further look, it looks like XOR operation is being udes

   <img width="401" height="135" alt="image" src="https://github.com/user-attachments/assets/6804e396-d7d3-4f40-a87b-280d680ad3dd" />

12. Then compares each character in the string to something name 'DAT_00402130'. If its true, that means we have the write flag the number 1 will return which "override" the program.

<img width="332" height="421" alt="image" src="https://github.com/user-attachments/assets/adb24beb-68c4-4eb8-86b0-bf07e23f1815" />

11. Asked for AI help to get a python script to speed up the decoding the bytes and to reverse to get the flag
    <img width="590" height="367" alt="image" src="https://github.com/user-attachments/assets/446c7932-d933-4b65-bc4c-c3e656db9463" />
12. Output of the script:

    <img width="282" height="48" alt="image" src="https://github.com/user-attachments/assets/49511ed5-364b-4038-ad9c-a453f7655a11" />


Flag

SVIBGR{b3ac0n_0v3rr1d3}
