![image-20231031034258731](./assets/image-20231031034258731.png)

22 and 80.

![image-20231031034708254](./assets/image-20231031034708254.png)

No anything valuable. We need password to login.

![image-20231031034739840](./assets/image-20231031034739840.png)

The source reveals the website is made by bootstrap. Hope we can google something out.

![image-20231031035514114](./assets/image-20231031035514114.png)

By later Enum, we can find this site. Looks like cookie.

![image-20231031035537360](./assets/image-20231031035537360.png)

We are able to login now.

![image-20231031035743786](./assets/image-20231031035743786.png)

Looks like we can submit something. Hope the command is run on the target server.

![image-20231031040610960](./assets/image-20231031040610960.png)

If leave the username blank intentionally, we will notice that the returned address is the usage of the ssh command, which means the command is executed on the target machine.

![image-20231031042908824](./assets/image-20231031042908824.png)

Once we have the shell, we can see a very large .jar file.

![image-20231031042713774](./assets/image-20231031042713774.png)

By examining it, we can get the database password. However by our initial recon, it cannot be accessed from outside.

![image-20231031043323541](./assets/image-20231031043323541.png)

We can get the hash of admin. Hope it is also for the ssh.

![image-20231031043714096](./assets/image-20231031043714096.png)

![image-20231031043723679](./assets/image-20231031043723679.png)

Done.

