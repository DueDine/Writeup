![image-20231009073349804](./assets/image-20231009073349804.png)

Only 2 ports open. Bust the web first.

![image-20231009073504999](./assets/image-20231009073504999.png)

Hmm. /etc seems like the linux folder.

![image-20231009073627561](./assets/image-20231009073627561.png)

At least a share. The passwd contains the salt. So I think we can use hashcat.

![image-20231009074054973](./assets/image-20231009074054973.png)

Get the password. Then try to find somewhere we can use.

![image-20231009074345433](./assets/image-20231009074345433.png)

From this, seems like the password is used to encrypt the archive.

We can download a zip from the website. But it is unencrypted.

![image-20231009074532500](./assets/image-20231009074532500.png)

The key here is quite interesting though.

![image-20231009074746592](./assets/image-20231009074746592.png)

Seems like the backup is inside the zip.

![image-20231009075151186](./assets/image-20231009075151186.png)

Exactly.

![image-20231009075337271](./assets/image-20231009075337271.png)

Guess it may be the ssh password.

![image-20231009075440014](./assets/image-20231009075440014.png)

Then time for elevated.

![image-20231009075624710](./assets/image-20231009075624710.png)

We can sudo the file we own. Simple reverse shell.

![image-20231009075930104](./assets/image-20231009075930104.png)

