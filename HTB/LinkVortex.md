![image-20241209055319887](./assets/image-20241209055319887.png)

Check the web. ![image-20241209055641128](./assets/image-20241209055641128.png)Hmm. Maybe some CVE would work. But we need to know the version first.

![image-20241209055828760](./assets/image-20241209055828760.png)

![image-20241209055920609](./assets/image-20241209055920609.png)

![image-20241209060144991](./assets/image-20241209060144991.png)

![image-20241209060201955](./assets/image-20241209060201955.png)

So we know it's Ghost 5.58. Then we can find [this](https://github.com/0xyassine/CVE-2023-40028). Now we need to find the admin creds.

![image-20241209062149419](./assets/image-20241209062149419.png)

It's really hard to find it.

![image-20241209062226589](./assets/image-20241209062226589.png)

Guess the username would be either admin or admin@domain

![image-20241209062412523](./assets/image-20241209062412523.png)

But we still need to find another interesting file.

![image-20241209062457340](./assets/image-20241209062457340.png)

Via the Docker file, there's a production config.

![image-20241209062535840](./assets/image-20241209062535840.png)

Time for SSH.

![image-20241209062653252](./assets/image-20241209062653252.png)

env_keep. Then of course we exploit it.

![image-20241209062934475](./assets/image-20241209062934475.png)

![image-20241209063039141](./assets/image-20241209063039141.png)

It has a filter for root, but seems like we can bypass it using two links. i.e. Chained Link.

![image-20241209063714238](./assets/image-20241209063714238.png)







