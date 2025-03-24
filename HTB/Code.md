![image-20250324134552791](./assets/image-20250324134552791.png)

Interesting 5000 port.

![image-20250324134633291](./assets/image-20250324134633291.png)

Online IDE. Maybe we can use it to execute command on that machine?

![image-20250324134755922](./assets/image-20250324134755922.png)

Some blacklist thing I think.

![image-20250324134953195](./assets/image-20250324134953195.png)

After some digging, the db is SQLAlchemy object. And we can extract pairs of creds in it.

![image-20250324140726033](./assets/image-20250324140726033.png)

![image-20250324140954796](./assets/image-20250324140954796.png)

Then we can SSH into the system.

![image-20250324141107233](./assets/image-20250324141107233.png)

![image-20250324141200060](./assets/image-20250324141200060.png)

Looks like we can edit the task.json to backup things we need.

![image-20250324141614202](./assets/image-20250324141614202.png)

Since martin can sudo as root, basically we can backup root's file as well. But the script has built-in detection. 

However can be evade by append another directory then ../. The script will replace it but we can do that twice.

![image-20250324142850849](./assets/image-20250324142850849.png)