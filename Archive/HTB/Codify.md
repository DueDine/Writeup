![image-20231106095124507](./assets/image-20231106095124507.png)

![image-20231106095055017](./assets/image-20231106095055017.png)

We have a Node.js framework. Looks like we can execute some code.

![image-20231106095313390](./assets/image-20231106095313390.png)

Normal.

![image-20231106095339249](./assets/image-20231106095339249.png)

The main page tells it is a sandbox environment with some restrictions.

![image-20231106095409663](./assets/image-20231106095409663.png)

No child_process.

![image-20231106095424841](./assets/image-20231106095424841.png)

It use vm2 as its sandbox. And point to the Ver 3.9.16

![image-20231106095550397](./assets/image-20231106095550397.png)

Oh. The project have been deprecate since critical security issues.

We can easily find the PoC to get a reverse shell.

![image-20231106095919343](./assets/image-20231106095919343.png)

Then we land as a web user I think. Try to find something to be a normal user.

![image-20231106100021747](./assets/image-20231106100021747.png)

Looks like the shadow hash. Crack it.

![image-20231106100510673](./assets/image-20231106100510673.png)

Well. Sponge Bob!

![image-20231106100654618](./assets/image-20231106100654618.png)

Get the user flag. And find out we can execute some script as root. Unfortunately, we cannot edit it.

![image-20231106100921410](./assets/image-20231106100921410.png)

Looks like we need to know the db password. We also cannot visit the backup file.

Later I find the only way is to brute force. And kindly the password only contains lower case and number.

![image-20231106101530444](./assets/image-20231106101530444.png)

Since it is easy mode, I believe it to be the root password. And indeed it is.





