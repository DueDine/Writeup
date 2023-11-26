Not so hard to find only 22 and 80 open.

![image-20231126142517507](./assets/image-20231126142517507.png)

The main site contains nothing interesting. Though it has a form, it is no use. Bust the vhost can reveal the true dev site.

![image-20231126142652355](./assets/image-20231126142652355.png)

So we have the Joomla now. This CMS do not have default creds so we have to find it manually.

![image-20231126142739760](./assets/image-20231126142739760.png)

First always the version of the CMS. And luckily we can find a ruby script to extract the site creds. Once login, we can make use of template to get the webshell. We need to switch to user before we get the user.txt

So it is database now.

![image-20231126142930330](./assets/image-20231126142930330.png)

We can find the hash. And john can crack it for us.

![image-20231126143031095](./assets/image-20231126143031095.png)

Actually the first time I have seen this in sudo.

![image-20231126143157608](./assets/image-20231126143157608.png)

The version looks vulnerable for CVE-2023-1326.

And yes indeed. So just generate a fake report to get root. 