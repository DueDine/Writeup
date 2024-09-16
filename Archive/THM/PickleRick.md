![image-20231016162609264](./assets/image-20231016162609264.png)

![image-20231016163224449](./assets/image-20231016163224449.png)

![image-20231016162644745](./assets/image-20231016162644745.png)

Some background. 

![image-20231016163251412](./assets/image-20231016163251412.png)

Not a normal robots file.

![image-20231016163341525](./assets/image-20231016163341525.png)

Well. So the above robots maybe the password.

![image-20231016163516231](./assets/image-20231016163516231.png)

So a easy webshell. But browse other contents now.

![image-20231016163655927](./assets/image-20231016163655927.png)

Others are directed to the same deny file. And notice that a strange string at the bottom.

![image-20231016163815126](./assets/image-20231016163815126.png)

The first ingredient is in the first file.

Our next step is iterate the file system hopes to find more clue.

![image-20231016164232042](./assets/image-20231016164232042.png)

We find the second but it is a executable file.

![image-20231016164358407](./assets/image-20231016164358407.png)

cat is disabled. Would like to try head/less.

Alright the less is useable.

![image-20231016164545899](./assets/image-20231016164545899.png)

What the hell. The user can sudo as root. Then everything is done.

