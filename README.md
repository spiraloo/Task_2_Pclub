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

