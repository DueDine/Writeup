![image-20231102035940927](./assets/image-20231102035940927.png)

53 and 1883 are useless. 1337 is web. FTP allow anonymous login but contains nothing.

![image-20231102040049369](./assets/image-20231102040049369.png)

Two admin? Looks interesting.

![image-20231102040139149](./assets/image-20231102040139149.png)

Well. Looks like only one of them are useful. The info says about sqlmap. So try it.

![image-20231102040755585](./assets/image-20231102040755585.png)

The link and their corresponding password.

![image-20231102040832459](./assets/image-20231102040832459.png)

Also user/pass creds.

![image-20231102040900934](./assets/image-20231102040900934.png)

Hmm. Nothing. Try the link above.

![image-20231102041158395](./assets/image-20231102041158395.png)

The hash is *easytohack* indeed.

![image-20231102041456696](./assets/image-20231102041456696.png)

For the other website, we need to know the name of the user.

![image-20231102041526179](./assets/image-20231102041526179.png)

In the source file, it tells us to add a parameter likely.

![image-20231102041659768](./assets/image-20231102041659768.png)

Well done. So probably we can view the /etc/passwd.

![image-20231102041822238](./assets/image-20231102041822238.png)

Okay.

![image-20231102041909873](./assets/image-20231102041909873.png)

Seems like we can upload the webshell. However, if we take a look at the source.

![image-20231102041949151](./assets/image-20231102041949151.png)

The filter is likely working. So we need to bypass it.

![image-20231102042716419](./assets/image-20231102042716419.png)

Simply bypass it. 

![image-20231102042940103](./assets/image-20231102042940103.png)

Time for reverse shell.

![image-20231102043257485](./assets/image-20231102043257485.png)

Everyone can read the ssh creds.

![image-20231102043540312](./assets/image-20231102043540312.png)

The nano have SUID. So done.



