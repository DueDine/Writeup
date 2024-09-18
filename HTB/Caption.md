![image-20240917022457981](./assets/image-20240917022457981.png)

Scan shows two web ports and one ssh.

![image-20240917022526702](./assets/image-20240917022526702.png)

For the 80 port, we lack the credential to login. Common credential do not work. 

![image-20240917022629510](./assets/image-20240917022629510.png)

For the 8080, looks like we have a git repository. This time, we can login with root/root.

![image-20240917022933610](./assets/image-20240917022933610.png)

It gives us access to two repo. For the second one, maybe we can find hardcoded creds in it.

![image-20240917023507830](./assets/image-20240917023507830.png)

And we found it in previous commit. However, it seems useless at current stage.

![image-20240917023752088](./assets/image-20240917023752088.png)

Check the admin panel, looks like we can use the H2 database at the web.

Search the web, we can find this [post](https://gist.github.com/h4ckninja/22b8e2d2f4c29e94121718a43ba97eed).

![image-20240917024355526](./assets/image-20240917024355526.png)

User get.

![image-20240917024450395](./assets/image-20240917024450395.png)

It use ECDSA instead of RSA.

![image-20240917025947027](./assets/image-20240917025947027.png)

The machine have another user called ruth.

![image-20240917025516137](./assets/image-20240917025516137.png)

The server have 9090 port in use. Very suspicious.

Back to git repo, Apache Thrift actually using the 9090 port. Seems like a point to exploit.

![image-20240917030729055](./assets/image-20240917030729055.png)

From the function, there maybe a point. It will execute the logs variable. We will try to control it.

![image-20240917030904428](./assets/image-20240917030904428.png)

![image-20240917032019137](./assets/image-20240917032019137.png)

Just crafted a log file like above to run another command. Then we use a standard client file to communicate with the 9090 port to make it run.

![image-20240917032147693](./assets/image-20240917032147693.png)

And it works.