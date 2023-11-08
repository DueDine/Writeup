![image-20231001005133463](./assets/image-20231001005133463.png)

Got several ports opened. Bust first.

![image-20231001005239780](./assets/image-20231001005239780.png)

Empty.



It is running SMB. Check whether some files on the share.

![image-20231001005630567](./assets/image-20231001005630567.png)

A strange share name revealed. Hope it require no password.

![image-20231001005904304](./assets/image-20231001005904304.png)

![image-20231001010033467](./assets/image-20231001010033467.png)

We got two user-password pair. Try RDP then.



Alright. I look the official writeup. The creator placed these two credentials intentional.

We **should** do a full port scan first.

![image-20231001011515691](./assets/image-20231001011515691.png)

There is another IIS in high port. Bust it.

And actually we can find we could visit the smb from website. So it is nice if we can upload to the smb.

![image-20231001013050593](./assets/image-20231001013050593.png)

We can. So get the shell.

![image-20231001013754428](./assets/image-20231001013754428.png)

Although just a low privilege account.

After searching the Internet, we can use PrinterSpoof to get the SYSTEM since we have impersonate priv.



Actually the target is also eternal-blue able. Then it is much easier.





 