![image-20231030222300382](./assets/image-20231030222300382.png)





![image-20231030222456247](./assets/image-20231030222456247.png)

According to info, we do not need to brute. So password must be left somewhere.

![image-20231030222534016](./assets/image-20231030222534016.png)

Looks like default info on the web.

![image-20231030222706212](./assets/image-20231030222706212.png)

All blocked.

![image-20231030223341354](./assets/image-20231030223341354.png)

Well. Subdomains. Now we get the credentials for the CMS.

![image-20231030223602470](./assets/image-20231030223602470.png)

Looks like we can upload the shell.

![image-20231030223842060](./assets/image-20231030223842060.png)

Yeah.

![image-20231030223922567](./assets/image-20231030223922567.png)

At least the database creds. Let us try whether we can use it for shell. No.

![image-20231030224327523](./assets/image-20231030224327523.png)

Switch to user.

![image-20231030224411448](./assets/image-20231030224411448.png)

Backup? Sounds like cronjob.

![image-20231030224503180](./assets/image-20231030224503180.png)

Run as root. So it is clear now. We can use somekind called wildcard attack to the tar.





