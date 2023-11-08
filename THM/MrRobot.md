![image-20231017090854230](./assets/image-20231017090854230.png)

For the first time encounter https. However, they looks identical.

The main page is cool. But did not give any helpful information as I thought.

![image-20231017093126879](./assets/image-20231017093126879.png)

Oh. Famous WordPress.

![image-20231017092745473](./assets/image-20231017092745473.png)

There is 2 links in the robots. One I believe to be one of the flag.

![image-20231017092832448](./assets/image-20231017092832448.png)

The other file contains one string per line, must be some kind of dictionary. Now we lack the username.

![image-20231017093012068](./assets/image-20231017093012068.png)

Normally, it would say 'Wrong username or password' etc. But it is clearly to say invalid username now. So we can brute it. 

![image-20231017093259898](./assets/image-20231017093259898.png)

But it is a themed box. Would it be the main character's name? 

![image-20231017093346979](./assets/image-20231017093346979.png)

Yes. It is. So just brute for password. 

The process is extremely slow for no reason. So I just search for password in other writeup.

![image-20231017094648755](./assets/image-20231017094648755.png)

Login now. Seems like we can do anything for the WP.

So let us change the default 404 page to a webshell.

![image-20231017094931705](./assets/image-20231017094931705.png)

![image-20231017095246360](./assets/image-20231017095246360.png)

Looks like a SSH credential.

![image-20231017095323373](./assets/image-20231017095323373.png)

![image-20231017095747642](./assets/image-20231017095747642.png)

Now time for elevation.

![image-20231017100202472](./assets/image-20231017100202472.png)

nmap here. Interesting.

![image-20231017100338462](./assets/image-20231017100338462.png)



