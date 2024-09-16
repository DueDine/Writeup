Full port scan shows 3 ports open.

![image-20240914212757709](./assets/image-20240914212757709.png)

FTP do not accept anonymous login.

On the website, it points to another service called sqlpad.

![image-20240914212935607](./assets/image-20240914212935607.png)

Looks like very suspicious to vulnerability.

![image-20240914213432235](./assets/image-20240914213432235.png)

It kindly provides its version. And indeed we find it for CVE-2022-0944.

We can get root on a strange hostname, most probably docker.

![image-20240914221849631](./assets/image-20240914221849631.png)

![image-20240914221909978](./assets/image-20240914221909978.png)

Two user exist. But nothing in their folder.

![image-20240914221940004](./assets/image-20240914221940004.png)

![image-20240914221956481](./assets/image-20240914221956481.png)

Only hash for user michael. Maybe we can john it.

![image-20240914222505243](./assets/image-20240914222505243.png)

Wow. Insane Clown >

With the credential, we can ssh into the machine and get user flag.

The user do not have any sudo rights nor suid.

![image-20240914222947840](./assets/image-20240914222947840.png)

Find Chrome on the opt folder. It is not normal.

![image-20240914223159491](./assets/image-20240914223159491.png)

Hmm. Looks like the 8080 do not open for external. We also have several high ports.

![image-20240914223326203](./assets/image-20240914223326203.png)

Curl the 8080 port, it is froxlor. One of the service of website. But we lack the credential.

![image-20240914223409082](./assets/image-20240914223409082.png)

![image-20240914224028554](./assets/image-20240914224028554.png)

Check the currently running process, john is running chrome with debugging port. We only have 3 high ports, so just brute force it.

By attaching to the debugger, we can login the system. It is using version 2.1.8, no vulnerability to exploit.

![image-20240914225559600](./assets/image-20240914225559600.png)

This section looks quite promising, it will exec command on restart.

![image-20240914225759689](./assets/image-20240914225759689.png)

Just let us read the root flag directly.











