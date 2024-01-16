![image-20240116150415436](./assets/image-20240116150415436.png)

Looks like a DC.

Start with SMB. 

![image-20240116143633990](./assets/image-20240116143633990.png)

We can list it anonymously. But looks like nothing valuable.

However we can try to brute the rid.

![image-20240116144127481](./assets/image-20240116144127481.png)

We can several user. Try to crack it with normal password.

![image-20240116144324324](./assets/image-20240116144324324.png)

We get two users now. Since the SMB do not have valuable info, we should try other service that can login with above creds.

![image-20240116144522609](./assets/image-20240116144522609.png)

The operator can log into SQL. Try to find more creds.

Alright. I can find no more info in the db.

![image-20240116145541422](./assets/image-20240116145541422.png)

Although no xp_cmdshell, we can list folder. Remember we have 80 port open.

![image-20240116145841268](./assets/image-20240116145841268.png)

A backup zip. That's enough.

![image-20240116150013269](./assets/image-20240116150013269.png)

Another creds.

 ![image-20240116151909309](./assets/image-20240116151909309.png)

Get the user flag. 

The raven user have few permission. Even the public folder.

![image-20240116152020410](./assets/image-20240116152020410.png)

While the first privilege looks very abnormal. However it doesn't work.

After search the Net, the exploit is about AD Certificate. How do they know?

Refer to [this](https://book.hacktricks.xyz/windows-hardening/active-directory-methodology/ad-certificates/domain-escalation#vulnerable-certificate-authority-access-control-esc7)