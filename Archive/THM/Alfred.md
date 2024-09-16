![image-20231019092000529](./assets/image-20231019092000529.png)

Looks like 2 web server. The 80 port one is useless.

And we can login into Jenkins using admin:admin. Great. I know it is a CI/CD platform. So must be somewhere it can execute command on target machine.

![image-20231019092256886](./assets/image-20231019092256886.png)

Yeah. It is great. Then just trigger the build and we have the shell.

![image-20231019092955315](./assets/image-20231019092955315.png)

Powershell command is really long.

So why not upgrade to use meterpreter.

Check the user's privilege, we can see the user can impersonate other user. So just impersonate to the SYSTEM. Migrate to a system process and everything is done.

![image-20231019094355738](./assets/image-20231019094355738.png)



