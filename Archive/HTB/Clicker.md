![image-20240117204812225](./assets/image-20240117204812225.png)

NFS here.

![image-20240117204835086](./assets/image-20240117204835086.png)

A backup folder.

![image-20240117204851207](./assets/image-20240117204851207.png)

All the source code of the website.

Play the game little while. We can save the game.

![image-20240117204958973](./assets/image-20240117204958973.png)

Looks like the msg will be reflected on the site. And indeed.

![image-20240117205111828](./assets/image-20240117205111828.png)

![image-20240117205120469](./assets/image-20240117205120469.png)

Look through the code. Seems like we can update our role through a parameter. But there is a check.

But since it requires a full equal (===). Maybe we can add some useless char.

![image-20240117205630462](./assets/image-20240117205630462.png)

Now we can see the admin panel.

![image-20240117210144909](./assets/image-20240117210144909.png)

Looks like we can export the data.

![image-20240117210215024](./assets/image-20240117210215024.png)

![image-20240117210251717](./assets/image-20240117210251717.png)

Looks like a very good point for webshell.

![image-20240117210913087](./assets/image-20240117210913087.png)

So it works. Time for rev shell.

![image-20240117213146278](./assets/image-20240117213146278.png)

There is a manage tool in the /opt folder. So we play with it.

![image-20240117213216337](./assets/image-20240117213216337.png)

A hidden fifth choice. We can get the private key of the user.

![image-20240117213518410](./assets/image-20240117213518410.png)

Get user. Time for PE.

![image-20240117213600775](./assets/image-20240117213600775.png)

Oh? SETENV here. So it likely to be relevant with env variable.

![image-20240117213856025](./assets/image-20240117213856025.png)

xml_pp is a Perl script. So we can instruct the Perl to execute our code first by env.

![image-20240117214433182](./assets/image-20240117214433182.png)



