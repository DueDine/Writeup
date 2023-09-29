Nmap first

![image-20230928183425218](./assets/image-20230928183425218.png)

![image-20230928183431910](./assets/image-20230928183431910.png)

Anonymous FTP allowed. So we download files first.



![image-20230928183524840](./assets/image-20230928183524840.png)

The pic is not a real pic. Extract the zlib will get some mysql thing. Ignore it first.





![image-20230928184138313](./assets/image-20230928184138313.png)

Seems like we can download some files.

![image-20230928184219544](./assets/image-20230928184219544.png)

Well. It is the ftp folder.



According to nmap, we can write to the ftp. So we should try it.



Using [this](https://github.com/artyuum/simple-php-web-shell/blob/master/index.php), we get a web shell.

![image-20230928184654719](./assets/image-20230928184654719.png)



It is time for reverse shell.



![image-20230928185145639](./assets/image-20230928185145639.png)

We can answer the first question. But we do not have permission to the home folder.



![image-20230928190136987](./assets/image-20230928190136987.png)

We can find a package so we just copy it to ftp that we can download on website.

By analyzing the packet, we can get the password for lennie.



![image-20230928190241475](./assets/image-20230928190241475.png)

Get the user flag. There is a folder called scripts.



![image-20230928191209624](./assets/image-20230928191209624.png)

We can edit the print.sh. So it is done.



![image-20230928191231697](./assets/image-20230928191231697.png)

