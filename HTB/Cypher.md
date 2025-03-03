![image-20250303133922522](./assets/image-20250303133922522.png)

Only login not signup.

![image-20250303134825645](./assets/image-20250303134825645.png)

But it have a API endpoint. Though no docs.

![image-20250303134444180](./assets/image-20250303134444180.png)

We can find a JAR at another path. Decompile it.

![image-20250303134739511](./assets/image-20250303134739511.png)

One of the code contains command execution. Looks like point for injection.

The only possible point of inject is login page.

![image-20250303135824615](./assets/image-20250303135824615.png)

We assume both the user/pass will be pass for query.

![image-20250303140542122](./assets/image-20250303140542122.png)

![image-20250303140636288](./assets/image-20250303140636288.png)

The password can be used to login as graphasm.

![image-20250303140827908](./assets/image-20250303140827908.png)

BBOT is a scanner. I would hope it can do command execution or at least read arbitrary files.

The `-cy` switch allows to select a file contains YARA rules. And we can use debug mode to print the content out for us.







