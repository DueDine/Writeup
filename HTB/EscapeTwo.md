![image-20250123015531015](./assets/image-20250123015531015.png)

Have user permission to start.

![image-20250123015655132](./assets/image-20250123015655132.png)

Start with SMB.

![image-20250123015706606](./assets/image-20250123015706606.png)

The first one is interesting. Try to look for some files.

![image-20250123015809819](./assets/image-20250123015809819.png)

Two Excel.

![image-20250123020106405](./assets/image-20250123020106405.png)

Some password inside.

![image-20250123021614382](./assets/image-20250123021614382.png)

And we can login as SA. Time for xp_cmdshell.

![image-20250123022621346](./assets/image-20250123022621346.png)

Inside the SQLServer config, we find another pair of creds.

![image-20250123023027688](./assets/image-20250123023027688.png)

Best chance that ryan and sql_svc share same password. Get the user now.



Escalation requires ADCS, which I don't know much.