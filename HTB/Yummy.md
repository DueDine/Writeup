![image-20241006232708712](./assets/image-20241006232708712.png)

Only those two.

We can easily create a new account on the website and make some reservation.

![image-20241006234406470](./assets/image-20241006234406470.png)

When we try to export the ICS. Looks like it is a LFI.

![image-20241006235235575](./assets/image-20241006235235575.png)

So our next step is to browse for some useful files.

![image-20241006235450022](./assets/image-20241006235450022.png)

From the crontab, we can find three scripts.

![image-20241006235617775](./assets/image-20241006235617775.png)

First we know where the backup zip.

![image-20241006235737533](./assets/image-20241006235737533.png)

Then the db creds. The last script do not give information.

We can start to check the code of the website.

![image-20241007000636225](./assets/image-20241007000636225.png)

There's a admin dashboard. And according to the html, it can directly interact with SQL. But we require another account to login.

![image-20241007000735437](./assets/image-20241007000735437.png)

The source code also provides their way to create key pair. Maybe we need to break the JWT?

The prime q seems a little bit smaller, which means the n can be factorize.

![image-20241007003458621](./assets/image-20241007003458621.png)

So by obtain both of them, we can craft the admin jwt on our own. 

![image-20241007003325317](./assets/image-20241007003325317.png)

Finally we in.

![image-20241007003652035](./assets/image-20241007003652035.png)

![image-20241007003733716](./assets/image-20241007003733716.png)

It's vulnerable to injection.

Once get a shell, there's a .hg not included in the backup zip which contains the user creds.

![image-20241007005309343](./assets/image-20241007005309343.png)

![image-20241007005440232](./assets/image-20241007005440232.png)

The user can run as dev while using hg. Refer to [this](https://wiki.mercurial-scm.org/Hook), such program always have some kind of hooks.

![image-20241007010110965](./assets/image-20241007010110965.png)

![image-20241007010129576](./assets/image-20241007010129576.png)

We know that rsync can change owner at sync. So why not let it make a root-owned SUID enabled shell for us.

![image-20241007011020456](./assets/image-20241007011020456.png)







