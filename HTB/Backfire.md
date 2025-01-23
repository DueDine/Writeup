Though label as Medium, should be Hard at least.

![image-20250123133930553](./assets/image-20250123133930553.png)

![image-20250123134012490](./assets/image-20250123134012490.png)

The 8000 port have directory listing.

![image-20250123134119450](./assets/image-20250123134119450.png)

Looks like we have to deal with Havoc, and try to communicate with the backend WS. Since no SSL, should be easier to craft one.

![image-20250123134346527](./assets/image-20250123134346527.png)

Time for finding CVEs.

Checking one of the author's GitHub, there's a [SSRF](https://github.com/chebuya/Havoc-C2-SSRF-poc/blob/main/exploit.py). It works, but we need to get it visit the WS locally.

And another one [here](https://github.com/IncludeSecurity/c2-vulnerabilities/tree/main/havoc_auth_rce), which talk about hardcoded passwords. Hmm, we have some above.

So the problem is how to combine those two together.

![image-20250123141714385](./assets/image-20250123141714385.png)

The shell is very fragile, so write the public key to it.



![image-20250123141949954](./assets/image-20250123141949954.png)

Another framework? Maybe another unexposed port.

![image-20250123151242959](./assets/image-20250123151242959.png)

By [default](https://github.com/DragoQCC/HardHatC2/blob/master/TeamServer/appsettings.json), Hardhat's JWT key is hardcoded. So we can craft a token for us to login.

![image-20250123151730442](./assets/image-20250123151730442.png)

Inside the Hardhat, we can execute command on the machine.

![image-20250123152711181](./assets/image-20250123152711181.png)

Not root, but still better.

![image-20250123153143838](./assets/image-20250123153143838.png)

sudo on iptables. With [this](https://www.shielder.com/blog/2024/09/a-journey-from-sudo-iptables-to-local-privilege-escalation/), again write the public key to root user.



