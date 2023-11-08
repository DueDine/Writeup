![image-20231020185345233](./assets/image-20231020185345233.png)

FTP allow anonymous login. And we can nc to the 9999 port.

The FTP provide a exe. Obviously buffer overflow.



![image-20231020205410727](./assets/image-20231020205410727.png)

EIP at 2012.

![image-20231020205848827](./assets/image-20231020205848827.png)

Only \x00 is bad char.

![image-20231020205947252](./assets/image-20231020205947252.png)

9 Jmp to choose.

![image-20231020210535660](./assets/image-20231020210535660.png)

Exploit and get SYSTEM.

