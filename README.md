# Task_2_Pclub
Reverse engineering a binary file.

First I did objdump on the rev file and read the output. After that I saw that in main, many function are being called. 
I ran that code on ghidra and decompiled it. 


### main:
functions like FUN_001150 which seemed like a print function, as when I ran _*./rev*_, it printed the whole message

WELCOME!  
Made By: Shivam Mishra  
Setting up the challenge  
Please enter the password:  
There was a checkPassword fucntion which when returned 1 will give me Access granted! otherwise ERROR:Invalid Password!  
Also in main there was an array declared with 30 characters.   



### checkPassword
In checkPassword there are 30 variables declared which just again made it sure that 30 characters are there in teh password.   
In checkPassword there were many functions like process, prepare, format and checkRes. 
We have s to give 1 in checkPassword and give the answer. 


### process
In process there were two arrays local_88 and one array which we gave, each element in local_88 is getting increased by 1 and each element in array is getting decreased by 1. 

### prepare
There is switch case:  
It printed &DAT_0001202c if it is "c"  
Printed there at default  
Printed comrade if it is "f"  
Printed harder if it is "t"  
Printed you're if it is "{"  
Printed almost if it is "}"    


### checkRes
It has to return 1 for us to give the correct password. There was a piVar2 which was &DAT_000120c0 which stores **cc0h**, there is one piVar3 which is duplicate of piVar2, 
converting **cc0h** to decimal it gives us **3264**, now converting it into binary it will give me **110011000000**, trimmign the last 5 zeroes will give me **1100110** which in decimal is **!02** in ASCII is **f** which is the forst character.  

