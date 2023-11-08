Port scan first.

![image-20231018103250623](./assets/image-20231018103250623.png)

![image-20231018103310917](./assets/image-20231018103310917.png)

A game server.

![image-20231018103402573](./assets/image-20231018103402573.png)

Secret and Uploads. Good.

![image-20231018103438093](./assets/image-20231018103438093.png)

A ssh key.

![image-20231018103515855](./assets/image-20231018103515855.png)

Looks like it is password protected.

![image-20231018103621909](./assets/image-20231018103621909.png)

The dict seems like to use to brute the key.

![image-20231018103843088](./assets/image-20231018103843088.png)

Get the key now. But we need a username.

![image-20231018104052350](./assets/image-20231018104052350.png)

Must be john I think.

![image-20231018104136142](./assets/image-20231018104136142.png)

Yes.

john is user of lxc group. So exploit it.

![image-20231018110354811](./assets/image-20231018110354811.png)

