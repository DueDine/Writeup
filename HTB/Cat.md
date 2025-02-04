![image-20250203202351048](./assets/image-20250203202351048.png)

![image-20250203202543366](./assets/image-20250203202543366.png)

Can register/login, but nothing interesting.

![image-20250203202705707](./assets/image-20250203202705707.png)

Time for git-dumper.

![image-20250203202817051](./assets/image-20250203202817051.png)

Now we have the source code for the site.

![image-20250203202931855](./assets/image-20250203202931855.png)

The admin is axel. Try to looking for password.

![image-20250203203242471](./assets/image-20250203203242471.png)

First query is not prepared, maybe we can inject on the cat_name parameter later.

![image-20250203204403876](./assets/image-20250203204403876.png)

Username are directly retrieved from session, and we do know admin will check the website. Looks like a XSS.

![image-20250203204912475](./assets/image-20250203204912475.png)

![image-20250203205242953](./assets/image-20250203205242953.png)

Use sqlmap to dump the user table. The password looks like MD5 hash.

![image-20250203205748196](./assets/image-20250203205748196.png)

The axel one is uncrackable. But we can login as rosa.

![image-20250203210507518](./assets/image-20250203210507518.png)

Though no sudo, adm group grant us privilege to read logs.

![image-20250203210600959](./assets/image-20250203210600959.png)

Then switch to axel.

![image-20250203210825386](./assets/image-20250203210825386.png)

Port 3000 open.

![image-20250203211039750](./assets/image-20250203211039750.png)

![image-20250203211112406](./assets/image-20250203211112406.png)

![image-20250203211227144](./assets/image-20250203211227144.png)

Seems like we need to send our exploit using email.

![image-20250203211452067](./assets/image-20250203211452067.png)

Though we cannot see any other repo in Gitea. This version have a stored XSS.

![image-20250203212317516](./assets/image-20250203212317516.png)

The README do not give further information.

![image-20250203212724199](./assets/image-20250203212724199.png)

The index.php hard-coded the password which can login as root.





