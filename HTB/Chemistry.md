![image-20241020112812628](./assets/image-20241020112812628.png)

Only SSH in top 1000. Have to do a full scan.

Also another web port at 5000.

![image-20241020115612829](./assets/image-20241020115612829.png)

Seems like we can upload CIF. Try some default password first.

No luck. So just register a new one and login. 

Then I find [this](https://github.com/advisories/GHSA-vgv8-5cpj-qj2f). Exploit to make a rev shell.

![image-20241020120819434](./assets/image-20241020120819434.png)

![image-20241020121405927](./assets/image-20241020121405927.png)

![image-20241020121421555](./assets/image-20241020121421555.png)

Given by the length, it should be MD5. We do not need to crack it ourself.

![image-20241020121521408](./assets/image-20241020121521408.png)



Now we can SSH into the machine. No sudo, no SUID.

But I found another website. Through no permission to the folder, maybe we can still visit it.

![image-20241020121750129](./assets/image-20241020121750129.png)

![image-20241020121859154](./assets/image-20241020121859154.png)

![image-20241020122145524](./assets/image-20241020122145524.png)

A static site. Thus we need to find exploit on the framework.

![image-20241020122242759](./assets/image-20241020122242759.png)

Python 3.9 is a little bit old, hope we can find something.

[Here](https://github.com/z3rObyte/CVE-2024-23334-PoC). It's about path traversal. We can read root flag directly.

![image-20241020122642692](./assets/image-20241020122642692.png)



