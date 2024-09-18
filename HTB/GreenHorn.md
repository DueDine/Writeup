![image-20240918160335879](./assets/image-20240918160335879.png)

Normal 22,80 with a strange 3000 port.

![image-20240918161817321](./assets/image-20240918161817321.png)

The website kindly provides its version. And we find [this](https://github.com/Rai2en/CVE-2023-50564_Pluck-v4.7.18_PoC).

![image-20240918162857096](./assets/image-20240918162857096.png)

For the 3000 port, it is the source code of the website. Should not hard to find relative credentials.

![image-20240918163348078](./assets/image-20240918163348078.png)

We can find the SHA512 password. Maybe we can try to crack it.

![image-20240918163510450](./assets/image-20240918163510450.png)

Okay. Now we can use the RCE above.

![image-20240918164010649](./assets/image-20240918164010649.png)

Notice the junior user is also in git. Maybe we can reuse the password here.

It works. Then we just grab his ssh key.

![image-20240918164158344](./assets/image-20240918164158344.png)

![image-20240918164404933](./assets/image-20240918164404933.png)

While we get user, there is another interesting PDF file.

![image-20240918170053248](./assets/image-20240918170053248.png)

The junior have not sudo at the moment. So we need to reveal the password of green. I believe it's for the root.

![image-20240918171025456](./assets/image-20240918171025456.png)

Using the famous depix, then we get.

![image-20240918171156427](./assets/image-20240918171156427.png)

![image-20240918171258108](./assets/image-20240918171258108.png)



