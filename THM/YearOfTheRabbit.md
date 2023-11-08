![image-20231015222106478](./assets/image-20231015222106478.png)

Have a FTP, but looks like no anonymous login.

![image-20231015222239115](./assets/image-20231015222239115.png)

Default page. Bust needed.

![image-20231015222337868](./assets/image-20231015222337868.png)

![image-20231015222403093](./assets/image-20231015222403093.png)

Rickrolled... And a strange css file.

![image-20231015222434743](./assets/image-20231015222434743.png)

![image-20231015222514098](./assets/image-20231015222514098.png)

![image-20231015222539984](./assets/image-20231015222539984.png)

Thanks for the ad.

![image-20231015222830360](./assets/image-20231015222830360.png)

By capturing the traffic, seems like there is another hidden folder.

![image-20231015222928852](./assets/image-20231015222928852.png)

A very famous pic in CV field. But here, maybe some steg.

![image-20231015223117029](./assets/image-20231015223117029.png)

![image-20231015223243883](./assets/image-20231015223243883.png)

It is time for hydra.

![image-20231015223405721](./assets/image-20231015223405721.png)

![image-20231015223445561](./assets/image-20231015223445561.png)

Some very strange combination. 

![image-20231015223640943](./assets/image-20231015223640943.png)

It is a programming language.

![image-20231015223751872](./assets/image-20231015223751872.png)

Alright. Looks like we get the ssh credentials.

![image-20231015223919804](./assets/image-20231015223919804.png)

![image-20231015224024645](./assets/image-20231015224024645.png)

Lack the permission to read the user flag. Maybe the info given when connected to ssh are somekind useful.

![image-20231015224516647](./assets/image-20231015224516647.png)

Oh. Get the secret folder.

![image-20231015224552441](./assets/image-20231015224552441.png)

Looks like the current password is given.

![image-20231015224643197](./assets/image-20231015224643197.png)

![image-20231015224726642](./assets/image-20231015224726642.png)

Somehow interesting. The user is the owner for user flag, so we can edit it. But cannot sudo as root.

By referencing other writeup, there is a vulnerability CVE-2019-14287.

![image-20231015225312380](./assets/image-20231015225312380.png)
