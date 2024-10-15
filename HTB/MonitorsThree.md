![image-20240925000821081](./assets/image-20240925000821081.png)

Strange 8084 port. But it's filtered.

![image-20240925001942279](./assets/image-20240925001942279.png)

The web have a login panel. Tried several popular creds but do not work.

By doing vhost search, we can find cacti.

![image-20240925005027088](./assets/image-20240925005027088.png)

Yet again it prompted for creds. But since it have provide its version, look for exp first. We can find [this](https://github.com/thisisveryfunny/CVE-2024-25641-RCE-Automated-Exploit-Cacti-1.2.26?tab=readme-ov-file), but it's a authenticated RCE.

We have to back to the reset password pages.

![image-20240925010145751](./assets/image-20240925010145751.png)

It will reflect whether user are valid. I think it would a little bit chance we can SQL injection it.





![image-20240925015154124](./assets/image-20240925015154124.png)

After obtaining the shell, we can get the database.

![image-20240925015506250](./assets/image-20240925015506250.png)

marcus is one of the user on the machine. Hope we can crack it.

Skip at present.
