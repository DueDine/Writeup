![image-20241016004640407](./assets/image-20241016004640407.png)

Standard Web and SSH.

![image-20241016004908331](./assets/image-20241016004908331.png)

A apk file? I do not familiar with android file, so I will proceed to dig more now.

However with no luck, we need to do something to the apk.

![image-20241016005601993](./assets/image-20241016005601993.png)

Luckily, we can decompile it easily. Time for finding.

![image-20241016005715528](./assets/image-20241016005715528.png)

Under the res folder, we can find two subdomains. 

![image-20241016005934835](./assets/image-20241016005934835.png)

The swagger one provide the API document, while the v1 looks like the endpoint.

The website can send request on behalf of us.

![image-20241016010351401](./assets/image-20241016010351401.png)

![image-20241016010426443](./assets/image-20241016010426443.png)

It give us a token, but do not have the admin privilege. We need to find it elsewhere. Maybe still in the apk.

![image-20241016010835734](./assets/image-20241016010835734.png)

![image-20241016010913162](./assets/image-20241016010913162.png)

![image-20241016010947946](./assets/image-20241016010947946.png)

Now we have the privilege. Hope we can exploit LFI on logs.

 ![image-20241016011214255](./assets/image-20241016011214255.png)

![image-20241016011237170](./assets/image-20241016011237170.png)

It works. Then we grab its SSH key and login.

![image-20241016011954479](./assets/image-20241016011954479.png)

We can find a backup of PuTTY, which I think contains SSH credentials. However it was encrypted someway.

Then I find [it](https://github.com/VoidSec/SolarPuttyDecrypt).

![image-20241016012647111](./assets/image-20241016012647111.png)

Looks like it's password-protected. But there's no other information on the machine. So probably we need to brute force.

![image-20241016014147358](./assets/image-20241016014147358.png)

Since using the WSL, I can directly interact with the exe. And it did solve the password.

![image-20241016014246451](./assets/image-20241016014246451.png)

![image-20241016014315526](./assets/image-20241016014315526.png)









