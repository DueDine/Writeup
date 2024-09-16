![image-20231016091309222](./assets/image-20231016091309222.png)

Have a SMB, allow anonymous login.

![image-20231016091444682](./assets/image-20231016091444682.png)

Get 2 pics.

![image-20231016091456840](./assets/image-20231016091456840.png)

Either no steg or require password.

![image-20231016091553189](./assets/image-20231016091553189.png)

The FTP allow anonymous login same.

Attention that we have edit permission to the script. Maybe we can upload the reverse shell to wait for cron job.

![image-20231016092320267](./assets/image-20231016092320267.png)

It works.

![image-20231016092418734](./assets/image-20231016092418734.png)

The pic folder is the SMB folder.

![image-20231016093231025](./assets/image-20231016093231025.png)

The user is member of sudo group, but we do not have the password.

![image-20231016093356702](./assets/image-20231016093356702.png)

No cap exist.

![image-20231016093428944](./assets/image-20231016093428944.png)

Lots of file have SUID. 

![image-20231016093551431](./assets/image-20231016093551431.png)

Well. The env looks like exploitable.

![image-20231016093724413](./assets/image-20231016093724413.png)

Works.

