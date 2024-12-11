![image-20241208135318915](./assets/image-20241208135318915.png)



Check the web server first.

![image-20241208135458696](./assets/image-20241208135458696.png)

Looks like we can upload files. Hope it do not check and give us where the file located.



![image-20241208135618967](./assets/image-20241208135618967.png)

We can even share it. Hmm, suspicious. The link_share parameter possibly give us the filename.



![image-20241208140531420](./assets/image-20241208140531420.png)

We can find another subdomain. But it requires basic auth.



![image-20241208141103714](./assets/image-20241208141103714.png)

Maybe we can send payload to admin via this form. 



![image-20241208141819153](./assets/image-20241208141819153.png)

The messages.php is interesting. I suddenly realized we can let the admins send the messages page to us via XSS.



![image-20241208142507504](./assets/image-20241208142507504.png)

![image-20241208142609138](./assets/image-20241208142609138.png)

Looks like it accepts file parameter to load local file. LFI may work here. Currently we need the .htpasswd for another site.



![image-20241208142946389](./assets/image-20241208142946389.png)

Time for cracking hash.![image-20241208143418004](./assets/image-20241208143418004.png)



![image-20241208143531573](./assets/image-20241208143531573.png)

The page is purely static. So maybe the creds work for SSH.



![image-20241208143744160](./assets/image-20241208143744160.png)



Find nothing valuable on the machine except the website monitor.

![image-20241208144256785](./assets/image-20241208144256785.png)

![image-20241208144339708](./assets/image-20241208144339708.png)



But it seems running on root, so we place our shell in it.

![image-20241208145025709](./assets/image-20241208145025709.png)

![image-20241208145154600](./assets/image-20241208145154600.png)

S