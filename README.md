# Task_2_Pclub
Reverse engineering a binary file.

First I did objdump on the rev file and read the output. After that I saw that in main, many function are being called. 
I ran that code on ghidra and decompiled it. 
In main there was a checkPassword fucntion which when returned 1 will give me Access granted!
In checkPassword there were many functions like process, prepare, format and checkRes. 
We have to return 1 in checkRes to give 1 in checkPassword and give the answer. 
