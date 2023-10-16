![image-20231016165418658](./assets/image-20231016165418658.png)

FTP allow anonymous login.

![image-20231016165510071](./assets/image-20231016165510071.png)

![image-20231016165528889](./assets/image-20231016165528889.png)

Seems like to tell us that some command will be filtered.

![image-20231016165815724](./assets/image-20231016165815724.png)

Oh. /secret.

![image-20231016165841568](./assets/image-20231016165841568.png)

Alright. A web shell.

Indeed some command are blocked. Although ls is blocked, we can use find. But all command I can think of to view the content of file are blocked.

(Later I found that we can use backslash \ to avoid the detection)

![image-20231016170809131](./assets/image-20231016170809131.png)

They did block many vulnerable command though. But now we can bypass using \\.

![image-20231016171410951](./assets/image-20231016171410951.png)

Now we get the shell access.

![image-20231016171436087](./assets/image-20231016171436087.png)

The user can sudo a script.

![image-20231016171621482](./assets/image-20231016171621482.png)

Seems like the `$msg` will be executed.

![image-20231016171746706](./assets/image-20231016171746706.png)

![image-20231016171908422](./assets/image-20231016171908422.png)

Then I found nothing vulnerable to escalation.

But the www folder have another folder called files looks like another website. Most probably in higher ports which do not reveal in early scan.

![image-20231016172721482](./assets/image-20231016172721482.png)

The code is very easily SQL injectable.

![image-20231016172758937](./assets/image-20231016172758937.png)

While another file give a hint.

![image-20231016173005276](./assets/image-20231016173005276.png)

Looks like a normal pic.

![image-20231016173052881](./assets/image-20231016173052881.png)

Well. The steg do not require password. But the zip ask. So time for john.

![image-20231016173218936](./assets/image-20231016173218936.png)

![image-20231016173258360](./assets/image-20231016173258360.png)

The file tells about the user/pass. Two == at the end means base64.

![image-20231016173457797](./assets/image-20231016173457797.png)

Alright. Now switch to another user again.

![image-20231016173733596](./assets/image-20231016173733596.png)

The user is in docker group means complete control for all containers.

![image-20231016174015867](./assets/image-20231016174015867.png)

![image-20231016174030509](./assets/image-20231016174030509.png)



This should be rated medium though.
