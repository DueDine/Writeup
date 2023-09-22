![image-20230922141051143](E:\Misc\Writeups\assets\image-20230922141051143.png)

First two questions solved.



Add -sC to Nmap parameter, we could find ftp server allow and only allow anonymous login.



![image-20230922141305548](E:\Misc\Writeups\assets\image-20230922141305548.png)

Read the txt.



![image-20230922141335786](E:\Misc\Writeups\assets\image-20230922141335786.png)

Seems like the mitch user is something interesting.



Let us see the web server.



![image-20230922141551616](E:\Misc\Writeups\assets\image-20230922141551616.png)

Default pages though. 



Gobust it.

![image-20230922141729767](E:\Misc\Writeups\assets\image-20230922141729767.png)

Hmm. Should visit the robot and simple page.



![image-20230922142117407](E:\Misc\Writeups\assets\image-20230922142117407.png)

Well The name already tells. Notice using version 2.2.8



We can exploit [this](https://www.exploit-db.com/exploits/46635). It is a script for python2. Need to install some packages for it.



![image-20230922143550196](E:\Misc\Writeups\assets\image-20230922143550196.png)

So now we get the password for mitch. We can try to ssh it.



![image-20230922143756397](E:\Misc\Writeups\assets\image-20230922143756397.png)

Get the user flag. Then it is time to get root.



![image-20230922143952096](E:\Misc\Writeups\assets\image-20230922143952096.png)

Well We can use vim as sudo. Checkout GTFOBins.



![image-20230922144057916](E:\Misc\Writeups\assets\image-20230922144057916.png)



![image-20230922144210202](E:\Misc\Writeups\assets\image-20230922144210202.png)

Get it.