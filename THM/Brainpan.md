9999 and 10000 port open. We can nc to the 9999. And the 10000 is a web server, under /bin. We can download .exe.

Time for overflow.

![image-20231020030506732](./assets/image-20231020030506732.png)

![image-20231020030807995](./assets/image-20231020030807995.png)

EIP at 515.

![image-20231020031120365](./assets/image-20231020031120365.png)

Looks like only '\x00' is bad char.

![image-20231020031259665](./assets/image-20231020031259665.png)

Only 1 ret.

![image-20231020031605074](./assets/image-20231020031605074.png)

Get she

