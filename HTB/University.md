![image-20241030135410876](./assets/image-20241030135410876.png)

Normal Windows DC with web open.

![image-20241030140856853](./assets/image-20241030140856853.png)

We can login with cert. It's not usual, so it must be the entry point.

![image-20241030141015879](./assets/image-20241030141015879.png)

We can register two types of account. The professor one require additional confirmation.

(The password policy is too strict for such environment)

![image-20241030141441984](./assets/image-20241030141441984.png)

So we can request cert once signed in.

![image-20241030145019170](./assets/image-20241030145019170.png)

The upper-right side have a button for export profile, which generates a PDF.

![image-20241030145100708](./assets/image-20241030145100708.png)

Maybe we can whether command injection available for this producer.

Then I find [this](https://github.com/c53elyas/CVE-2023-33733).

![image-20241030150442690](./assets/image-20241030150442690.png)

Get the shell as WAO.

![image-20241030150731594](./assets/image-20241030150731594.png)

Seems like the password for WAO user. 

I would like to check the db file for another creds.

![image-20241030151440141](./assets/image-20241030151440141.png)

![image-20241030151552466](./assets/image-20241030151552466.png)

Looks like the nya is next target. But we only have PBKDF2 hash. It's considered secure, so there should be another way to elevate.

![image-20241030152719831](./assets/image-20241030152719831.png)

There's a script which tells the existence of other VMs. But I do not have access to another script.



Later I was told the WAO user actually have powerful privileges.

![image-20241030154756363](./assets/image-20241030154756363.png)

We can direct to SYSTEM using potato. Well, it's much more unintended.



For future use:

![image-20241030154905419](./assets/image-20241030154905419.png)

`Administrator:500:aad3b435b51404eeaad3b435b51404ee:e63413bab01a0b8820983496c0be3a9a:::`

