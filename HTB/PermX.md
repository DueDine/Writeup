Scan shows only 2 ports open. Consider it's a easy box, will do full port scan later.

![image-20240917113410506](./assets/image-20240917113410506.png)

![image-20240917142338389](./assets/image-20240917142338389.png)

Looks like very normal. Do a detail search then.

After fuzz, we can find another subdomain at lms. Require credential to login. Try several default but do not work. 

![image-20240917143423039](./assets/image-20240917143423039.png)

![image-20240917143814703](./assets/image-20240917143814703.png)

Consider the footnote's copyright is 2024, it should be a recent version.

And luckily we can find [this](https://github.com/m3m0o/chamilo-lms-unauthenticated-big-upload-rce-poc).

![image-20240917144243744](./assets/image-20240917144243744.png)

Then we have a basic shell.

![image-20240917144910971](./assets/image-20240917144910971.png)

![image-20240917144937808](./assets/image-20240917144937808.png)

We can find a config file in the parent folder, which includes database password. Since it is a easy one, maybe we can try it on another user.

![image-20240917145034336](./assets/image-20240917145034336.png)

![image-20240917145143885](./assets/image-20240917145143885.png)

It works.

![image-20240917145159213](./assets/image-20240917145159213.png)

The user have sudo on a shell file.

![image-20240917145229961](./assets/image-20240917145229961.png)

Unfortunately, we cannot edit it directly.

![image-20240917145404412](./assets/image-20240917145404412.png)

Looks like this script is use to change the permission of a file, but has some restriction to the location.

I started to wonder whether file link will work.

![image-20240917150427436](./assets/image-20240917150427436.png)

It works.





