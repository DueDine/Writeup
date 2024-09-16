![image-20231019135450525](./assets/image-20231019135450525.png)

![image-20231019135639871](./assets/image-20231019135639871.png)

It is a WordPress. Looks very vulnerable.

However, I would like to scan all ports again.

![image-20231019140054625](./assets/image-20231019140054625.png)

Nevermind. So just focus on the web.

![image-20231019140707979](./assets/image-20231019140707979.png)

Looks like a old version. Wonder whether some exploit exist.

However, it seems a secure version. So the last resort I think is brute force.

![image-20231019141449022](./assets/image-20231019141449022.png)

Well. Not much time to find the correct one.

I think then we can edit the theme or else to a webshell. Just try it.

![image-20231019141756654](./assets/image-20231019141756654.png)

Yes. The old way.

![image-20231019141953207](./assets/image-20231019141953207.png)

We can see a user folder. But unfortunately, we need more permission.

Maybe we can checkout the web folder, hopeful some install credential would be left there.

![image-20231019142205135](./assets/image-20231019142205135.png)

So secure. It use a dedicated WordPress user.

![image-20231019142250091](./assets/image-20231019142250091.png)

Something listen to the 8080 port? But we do not find it on the initial Nmap scan. Looks like we need a tunnel inside.

(After refer to other WP. The tunnel thought is right. But actually there is a txt left in the /opt folder which contains the credentials of the user.)

![image-20231019142725347](./assets/image-20231019142725347.png)

![image-20231019142758206](./assets/image-20231019142758206.png)

So the 8080 port likely to be Jenkins.

![image-20231019143045845](./assets/image-20231019143045845.png)

Now we can visit the Jenkins. But default credential and the user credential do not work.

Do we need to brute again?

Well. According to Google and the forum, hydra will produce false positive if using attack machine. So I will just skip this.

![image-20231019145901563](./assets/image-20231019145901563.png)

Looks like Java. Nevermind, just search for reverse shell online.

![image-20231019150126672](./assets/image-20231019150126672.png)

![image-20231019150302522](./assets/image-20231019150302522.png)

/opt again.

![image-20231019150333318](./assets/image-20231019150333318.png)

Root credenti



