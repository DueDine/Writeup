![image-20250216135838288](./assets/image-20250216135838288.png)

![image-20250216140207977](./assets/image-20250216140207977.png)

Looks like a website for booking trips.

![image-20250216140306079](./assets/image-20250216140306079.png)

`/download` endpoint require a parameter.

![image-20250216140446807](./assets/image-20250216140446807.png)

Maybe LFI here.

![image-20250216140613379](./assets/image-20250216140613379.png)

User flag is easy to obtain. Then time for digging creds for SSH.

![image-20250216141159756](./assets/image-20250216141159756.png)

Also a `dev` subdomain.

![image-20250216141245679](./assets/image-20250216141245679.png)

![image-20250216141312435](./assets/image-20250216141312435.png)

![image-20250216141726226](./assets/image-20250216141726226.png)

![image-20250216142152921](./assets/image-20250216142152921.png)

We can crack one password from the DB and into SSH.

![image-20250216142743600](./assets/image-20250216142743600.png)

A script in the `/opt` use magick. Maybe we can find some exploit.

![image-20250216143504536](./assets/image-20250216143504536.png)

Then [here](https://github.com/ImageMagick/ImageMagick/security/advisories/GHSA-8rxc-922v-phg8).



