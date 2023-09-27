Nmap first

![image-20230922145346732](./assets/image-20230922145346732.png)

Only 22 and 80 live.



Bust it.



![image-20230922145642854](./assets/image-20230922145642854.png)

Maybe check admin.





![image-20230922150137684](./assets/image-20230922150137684.png)

Seems like we can john the ssh key.



![image-20230922150419564](./assets/image-20230922150419564.png)

Processed with the ssh key.



![image-20230922150550325](./assets/image-20230922150550325.png)

Get the user.txt



![image-20230922150757711](./assets/image-20230922150757711.png)

Seems like the password is stored on overpass and not strong encryption.



![image-20230922150833841](./assets/image-20230922150833841.png)

Hidden files though. Looks like some hash or. Just decrypt it.

(Well. Later I found this is no use for root. But for the bonus subscription. And it requires to read the source of the overpass. I do not know Golang.)



The txt also mentions automated script. So crontab is next to visit.



![image-20230922151254335](./assets/image-20230922151254335.png)

The root updates source code every minute from online resource. So if we can control the dns, we can make it a reverse shell.



![image-20230922151415012](./assets/image-20230922151415012.png)

Everyone can rw the hosts file.



Then it is easy. Start a web server to serve a script. Then get the shell.

