![image-20231029153035470](./assets/image-20231029153035470.png)

Get a SMB. Let us look for something.

![image-20231029153250715](./assets/image-20231029153250715.png)

We have a share. 

![image-20231029153702153](./assets/image-20231029153702153.png)

Looks like the username.

![image-20231029153520874](./assets/image-20231029153520874.png)

Well. A rabbit hole. Let us focus on the web.

![image-20231029153828104](./assets/image-20231029153828104.png)

WordPress. So wpscan now.

![image-20231029154344418](./assets/image-20231029154344418.png)

At least we can the version.

![image-20231029154507413](./assets/image-20231029154507413.png)

Looks like we can get a shell if we have the author permission. Maybe we need to brute the password?

![image-20231029154754635](./assets/image-20231029154754635.png)

We have two username now. So hydra.

![image-20231029155712724](./assets/image-20231029155712724.png)

Well. Metasploit now.

![image-20231029160035151](./assets/image-20231029160035151.png)

Now try to elevate.

![image-20231029160559047](./assets/image-20231029160559047.png)

checker? Looks like user-created binary.

![image-20231029160722819](./assets/image-20231029160722819.png)

Root-owned.

![image-20231029161118054](./assets/image-20231029161118054.png)

![image-20231029161139570](./assets/image-20231029161139570.png)

It retrieve a env. If satisfy the condition, it will execute the bash.

![image-20231029161259201](./assets/image-20231029161259201.png)

Okay.
