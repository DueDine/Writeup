![image-20250124155808052](./assets/image-20250124155808052.png)

Only 22 / 80 Open.

Bust the website for both dir / vhost, get nothing valuable.

![image-20250124160721160](./assets/image-20250124160721160.png)

Well, it's SNMP.

![image-20250124160843426](./assets/image-20250124160843426.png)

![image-20250124160947857](./assets/image-20250124160947857.png)

It did exist on the server. But we need to find entry point.

![image-20250124161107134](./assets/image-20250124161107134.png)

![image-20250124161149937](./assets/image-20250124161149937.png)

![image-20250124161136653](./assets/image-20250124161136653.png)

Using default creds, we can login at the /operator one.

![image-20250124162956204](./assets/image-20250124162956204.png)

Only 1 user with their hash. Looks like MD5, easily crackable.

![image-20250124163603423](./assets/image-20250124163603423.png)

We can have a mosh server running at root, then just connect to it.

