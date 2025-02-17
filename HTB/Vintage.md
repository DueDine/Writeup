The given credentials cannot used to SMB or RPC. Use LDAP.

![image-20250217130909753](./assets/image-20250217130909753.png)

A computer other than DC. Maybe we can log into.

According to Bloodhound, FS01 can read password of MSA. Also member of Pre Windows 2000, which means password maybe the name itself.

![image-20250217132336166](./assets/image-20250217132336166.png)

MSA have Generic Write of another group, which Generic All to other SVC account.

![image-20250217132529558](./assets/image-20250217132529558.png)

![image-20250217133413336](./assets/image-20250217133413336.png)

Of the three SVC accounts, only the SQL disabled and password changed.

![image-20250217134142818](./assets/image-20250217134142818.png)

![image-20250217134542431](./assets/image-20250217134542431.png)

Can be cracked by PREAUTH.

![image-20250217135005386](./assets/image-20250217135005386.png)

Also password for another user. Log into WinRM.

![image-20250217140257936](./assets/image-20250217140257936.png)

Seems like we need to get access to Neri's Admin, a member of delegate admin.

![image-20250217140421065](./assets/image-20250217140421065.png)

![image-20250217141243472](./assets/image-20250217141243472.png)

![image-20250217142133140](./assets/image-20250217142133140.png)

We can also retrieve the MasterKey at Protect folder.

Then we need to exploit S4U2. Use C.Neri to set SPN, Adm to promote to delegate.

![image-20250217150938778](./assets/image-20250217150938778.png)

`Administrator:500:aad3b435b51404eeaad3b435b51404ee:468c7497513f8243b59980f2240a10de:::`

