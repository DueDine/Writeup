The label says tom. Seems like relate to Tomcat.



![image-20230930011334854](./assets/image-20230930011334854.png)

Well. We get Tomcat. And a interesting one called Jserv.



Bust it first to look for some hidden folder.

![image-20230930011500792](./assets/image-20230930011500792.png)

Very normal. So we should hope whether some exploit of tomcat or Jserv exist.



Seems like we get it.

![image-20230930011754256](./assets/image-20230930011754256.png)



Just using the exploit we can see the inf file.

![image-20230930012337651](./assets/image-20230930012337651.png)

Looks like password. And we know the ssh open.



So we get the user flag.

![image-20230930012627607](./assets/image-20230930012627607.png)



And we have a GPG encrypt file and its corresponding key. We need to john it.



![image-20230930013127874](./assets/image-20230930013127874.png)

Get the password for merlin.



![image-20230930013227375](./assets/image-20230930013227375.png)

We can sudo the zip. According to gtfo,



![image-20230930013337474](./assets/image-20230930013337474.png)

Get the root.