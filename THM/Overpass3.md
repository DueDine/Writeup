![image-20231016135814712](./assets/image-20231016135814712.png)

FTP open. But no anonymous login.

![image-20231016135933534](./assets/image-20231016135933534.png)

Looks normal.

![image-20231016140057958](./assets/image-20231016140057958.png)

Oh backups.

![image-20231016140129744](./assets/image-20231016140129744.png)

Looks like we need to brute the key.

![image-20231016140305117](./assets/image-20231016140305117.png)

No password protected. Great!

![image-20231016141355453](./assets/image-20231016141355453.png)

So we can extract some credentials.

Although I hope it would be for SSH, but it is for FTP. Since the SSH do not allow password auth.

![image-20231016141850318](./assets/image-20231016141850318.png)

Noticed that we have write permission. So time for webshell.

![image-20231016142111890](./assets/image-20231016142111890.png)

![image-20231016142634289](./assets/image-20231016142634289.png)

![image-20231016142737682](./assets/image-20231016142737682.png)

We can try to switch to parabox using the same password.

![image-20231016142922034](./assets/image-20231016142922034.png)

We can. And we find some binarys with cap. Sadly none of them works.





By searching the web, I get to know that the machine's NFS configure is bad.

![image-20231016143458272](./assets/image-20231016143458272.png)

The no_root_squash allows any other machine's root user acts like root.

But we do know from the previous nmap scan that few ports were opened. So we have to tunnel the NFS traffic using SSH etc.

![image-20231016144951157](./assets/image-20231016144951157.png)

And get jame's SSH key.

![image-20231016145321954](./assets/image-20231016145321954.png)

Using our attacking machine to add setuid to the bash binary.



