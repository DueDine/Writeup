22,80,139,445 Port Open.

SMB looks normal.

![image-20231103003203684](./assets/image-20231103003203684.png)

Default page is some kind admin panel. Try some default creds but failed.

![image-20231103003234920](./assets/image-20231103003234920.png)

Bust find a cloud page.

![image-20231103003254705](./assets/image-20231103003254705.png)

File upload. It have extension filter, but we can easily bypass it by like ".php\x00.jpg".

![image-20231103003556317](./assets/image-20231103003556317.png)

It kindly provide the file link.

After getting a shell, we can retrieve the website password from the php file. But it points to a static site.

![image-20231103005001909](./assets/image-20231103005001909.png)

We can find a keepass database in the /opt folder. So download to local machine to crack it.

![image-20231103005106371](./assets/image-20231103005106371.png)

![image-20231103005146672](./assets/image-20231103005146672.png)

Now we can get sysadmin creds.

![image-20231103005406988](./assets/image-20231103005406988.png)

There is a script folder own by root. 

![image-20231103011930417](./assets/image-20231103011930417.png)

It is kind of tricky actually. The require backup file is owned by root so we cannot modify it. But the folder is own by the user. So we can make our own file.

![image-20231103012909323](./assets/image-20231103012909323.png)

Done.