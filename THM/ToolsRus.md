![image-20231016201518290](./assets/image-20231016201518290.png)

2 Not frequently seen ports.

![image-20231016201705962](./assets/image-20231016201705962.png)

![image-20231016201710237](./assets/image-20231016201710237.png)

![image-20231016201733643](./assets/image-20231016201733643.png)

Seems like a vulnerable.

![image-20231016202408658](./assets/image-20231016202408658.png)

![image-20231016202443852](./assets/image-20231016202443852.png)

Maybe the 1234 port we find earlier.

The 1234 port is a Tomcat page. And we use the same http credential for the manager panel.

By using the metasploit, CVE-2009-3458 (Very old exploit). Everything is done. We get the root shell.