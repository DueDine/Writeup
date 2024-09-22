![image-20240922221559889](./assets/image-20240922221559889.png)

Standard 2 ports. (No more ports after -p-)

![image-20240922221711502](./assets/image-20240922221711502.png)

Apart from the contact form, nothing valuable.

![image-20240922223655736](./assets/image-20240922223655736.png)

Since it's registration, there must be someone viewing. So it's a good chance to steal cookie. But we need to know what the CMS is.

![image-20240922224244224](./assets/image-20240922224244224.png)

By searching the bikes theme on google, we can know it is WonderCMS.

![image-20240922224303289](./assets/image-20240922224303289.png)

![image-20240922224511696](./assets/image-20240922224511696.png)

It is already 2024, other are too old. And the XSS are very close to our form above.

Once we get www-root, we can find another database creds. (There's a \ before /)

![image-20240922231941597](./assets/image-20240922231941597.png)

Simply crack it with hashcat, then we get the password for amay.

![image-20240922232225973](./assets/image-20240922232225973.png)

![image-20240922232238647](./assets/image-20240922232238647.png)

Amay do not have sudo, so I watch for other process and network.

![image-20240922232642471](./assets/image-20240922232642471.png)

The 8080 port opened. 

![image-20240922233018082](./assets/image-20240922233018082.png)

A HTTP server. Then we need to tunnel it. We can login with amay's creds.

![image-20240922233329826](./assets/image-20240922233329826.png)

Looks like we can exec command using this panel.

![image-20240922233558663](./assets/image-20240922233558663.png)

The below part can return the contents. Maybe we can alter the request?

![image-20240922233816644](./assets/image-20240922233816644.png)

![image-20240922233858843](./assets/image-20240922233858843.png)

Hmm. Seems like it will detect the file content. But it is only single command?

![image-20240922234415915](./assets/image-20240922234415915.png)

Then we get it.

