![image-20231016103509131](./assets/image-20231016103509131.png)

So much port opened. Strange.

![image-20231016103720251](./assets/image-20231016103720251.png)

Those higher ports run sshd.

![image-20231016115643974](./assets/image-20231016115643974.png)

While connecting those higher ports, it will displayed whether its higher or lower.

Using binary search method, we can easily find out the true port.

![image-20231016115727198](./assets/image-20231016115727198.png)

So finally we have a challenge. Some very strange string. It must have some meaning.

![image-20231016115835113](./assets/image-20231016115835113.png)

The first line suggests that the following strange text maybe a poem.

![image-20231016120330622](./assets/image-20231016120330622.png)

Crack it using Vigenere Cipher.

![image-20231016120647088](./assets/image-20231016120647088.png)

This time looks like ssh credential to 22 port.

![image-20231016120935145](./assets/image-20231016120935145.png)

Reversed.

![image-20231016121150837](./assets/image-20231016121150837.png)

We can sudo the reboot. It is useless unless we can control some startup program.

![image-20231016121226962](./assets/image-20231016121226962.png)

Oh. The script is in our folder.

![image-20231016121248226](./assets/image-20231016121248226.png)

We can edit it. So time for shell.

![image-20231016124040323](./assets/image-20231016124040323.png)

Get something like hash.

![image-20231016124210136](./assets/image-20231016124210136.png)

Hmm. Looks like the last one is the possible password.

![image-20231016124243529](./assets/image-20231016124243529.png)

The chef did well.

![image-20231016124409266](./assets/image-20231016124409266.png)

Switch to another user.

![image-20231016124749401](./assets/image-20231016124749401.png)

The alice folder is little bit strange. There is execute permission for everyone.

![image-20231016125127008](./assets/image-20231016125127008.png)

Although cannot list anything, we can host the ssh key to web.

![image-20231016125150040](./assets/image-20231016125150040.png)

We do not have the password so cannot use command to check for sudo.

![image-20231016125403654](./assets/image-20231016125403654.png)

But we indeed have a file in the directory.

![image-20231016125545169](./assets/image-20231016125545169.png)



