Nmap first

![image-20230922171046710](./assets/image-20230922171046710.png)



Look the website first. Default pages. So bust it.



![image-20230922171242536](./assets/image-20230922171242536.png)



![image-20230922171327133](./assets/image-20230922171327133.png)



Seems like a management panel. Bust again.



![image-20230922171645700](./assets/image-20230922171645700.png)

as is the admin panel attachment is uploads folder. If we can find somewhere to upload payload.



The Exploit-DB have several exploits for this. We can use [this](https://www.exploit-db.com/exploits/40718) to get the sql backup. As we know, this kinds of application normally have some startup pages where you would input your database user/pass etc.



![image-20230922172743678](./assets/image-20230922172743678.png)

Those seems like the username and the hash of password.



![image-20230922172846878](./assets/image-20230922172846878.png)

Well. Now we get the access to panel. According to [another]() exploit, we can upload something. So it is not hard to reverse shell.



![image-20230922174042311](./assets/image-20230922174042311.png)

Get the user flag.



![image-20230922174556024](./assets/image-20230922174556024.png)

Hmm. We can sudo the perl.



![image-20230922174716412](./assets/image-20230922174716412.png)

The script is editable. So it is done.



