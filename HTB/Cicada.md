![image-20240929141817315](./assets/image-20240929141817315.png)

No web port open. Maybe we can try anonymous SMB first.

![image-20240929142848936](./assets/image-20240929142848936.png)

HR and DEV.

![image-20240929143023459](./assets/image-20240929143023459.png)

The HR kindly give us the default password while the DEV refuse.

Now we lack the username. We may try to brute it.

![image-20240929143805003](./assets/image-20240929143805003.png)

Now let us check who do not change their password.

![image-20240929144937034](./assets/image-20240929144937034.png)

And just in case we find it.

![image-20240929145117139](./assets/image-20240929145117139.png)

![image-20240929145143031](./assets/image-20240929145143031.png)

Another creds get. And based on the full port scan, the 5985 port also opens.

![image-20240929145531144](./assets/image-20240929145531144.png)

![image-20240929145554602](./assets/image-20240929145554602.png)

Oh. BackupPrivilege.

![image-20240929150058270](./assets/image-20240929150058270.png)

We can make robocopy work in backup mode to bypass the ACL.



