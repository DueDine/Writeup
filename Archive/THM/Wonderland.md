![image-20230930165715399](./assets/image-20230930165715399.png)

Looks like can only rely on HTTP.



![image-20230930165806548](./assets/image-20230930165806548.png)

Hmm. Some interesting directory.



![image-20230930170020203](./assets/image-20230930170020203.png)

Some jpg. Maybe some steg?



![image-20230930171128125](./assets/image-20230930171128125.png)

No password though.

![image-20230930171214319](./assets/image-20230930171214319.png)

Remember there are still two jpg not displayed. So must be other directory not found by buster.



![image-20230930171410575](./assets/image-20230930171410575.png)

Seems like we get the ssh password. Quite long.

![image-20230930171518911](./assets/image-20230930171518911.png)

Alright. Having the root flag in user home although we do not have such permission. The python file is suspicious.

![image-20230930172621559](./assets/image-20230930172621559.png)

Seems like really random though.

![image-20230930172812040](./assets/image-20230930172812040.png)

But we can sudo the rabbit. Although we do not have file permission.

Look into the source code, the file import random library, so we can assume whether we can fake the lib in our home folder. It works.

![image-20230930173411443](./assets/image-20230930173411443.png)



![image-20230930173521890](./assets/image-20230930173521890.png)

Now we have a executable with s permission.

![image-20230930173629045](./assets/image-20230930173629045.png)

Maybe we should change the time? But it require privilege.

Direct view the file. The core dumped is intended.

![image-20230930173840478](./assets/image-20230930173840478.png)

It used /bin/echo for echo but just date for date. So let us change the PATH.

![image-20230930175302430](./assets/image-20230930175302430.png)

Get the hatter.

![image-20230930182415045](./assets/image-20230930182415045.png)

The perl have uid cap.



![image-20230930182342582](./assets/image-20230930182342582.png)



![image-20230930182514686](./assets/image-20230930182514686.png)

Interesting reversed.

