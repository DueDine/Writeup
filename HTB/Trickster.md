![image-20240924131528993](./assets/image-20240924131528993.png)

Again 2 ports only.

![image-20240924131648167](./assets/image-20240924131648167.png)

The contact have a form, and the shop points to another site. Shop first.

![image-20240924131916035](./assets/image-20240924131916035.png)

Cannot find the version. Never mind, check exploit first.

![image-20240924132302889](./assets/image-20240924132302889.png)

Not so useful. Maybe we need to find more.

![image-20240924132616799](./assets/image-20240924132616799.png)

Well, we can find a git repo behind the shop. Just dump it and check it locally.

![image-20240924133317548](./assets/image-20240924133317548.png)

Hmm. Quite strange folder name. And no more git record.

![image-20240924133357819](./assets/image-20240924133357819.png)

But it's valid. Popular creds do not work. Now we know it's 8.1.5. Proceed to exp. Then we can find [it](https://github.com/aelmokhtar/CVE-2024-34716).

At the time I play this box, the above exp have been updated by others. Much easier than the OG one.

![image-20240924135725910](./assets/image-20240924135725910.png)

Now we in.

![image-20240924135916382](./assets/image-20240924135916382.png)

At the config file, we can find the database creds.

![image-20240924135947404](./assets/image-20240924135947404.png)

Sadly none of them matched, so we need to inside the database.

![image-20240924140455436](./assets/image-20240924140455436.png)

![image-20240924140525932](./assets/image-20240924140525932.png)

Two user's hash available on employee/customer table.

By the name, we should check on james first.

![image-20240924140724448](./assets/image-20240924140724448.png)

![image-20240924140808429](./assets/image-20240924140808429.png)

![image-20240924140950212](./assets/image-20240924140950212.png)

A container running. Looks like we need to escape soon.

![image-20240924141143497](./assets/image-20240924141143497.png)

Really docker.

![image-20240924141739087](./assets/image-20240924141739087.png)

Do some sweep and we find another port.

![image-20240924141832526](./assets/image-20240924141832526.png)

A website. Then we need to proxy it. We can login using james creds again.

![image-20240924142112522](./assets/image-20240924142112522.png)

It match [this](https://www.exploit-db.com/exploits/52027). But the script requires internet connection so we have to do our own.

![image-20240924144002743](./assets/image-20240924144002743.png)

![image-20240924144853495](./assets/image-20240924144853495.png)

Two backup zip. No unzip on the machine, we have to take it locally.

![image-20240924145823553](./assets/image-20240924145823553.png)

In one of the brotli file. Switch to adam and we have sudo now.

![image-20240924145943709](./assets/image-20240924145943709.png)

![image-20240924150557628](./assets/image-20240924150557628.png)

We have 2.6.1, so it match with [this](https://www.exploit-db.com/exploits/51983).

![image-20240924152044160](./assets/image-20240924152044160.png)

![image-20240924152145389](./assets/image-20240924152145389.png)

Done.







