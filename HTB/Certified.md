![image-20250126153345128](./assets/image-20250126153345128.png)

The given creds do not have WinRM access. Have to use nxc for enumeration.

![image-20250126153848692](./assets/image-20250126153848692.png)

Judith can rewrite the owner of management group. The group name itself means some privilege.

 ![image-20250126155055867](./assets/image-20250126155055867.png)

Now we can GenericWrite on management_svc. Kerberoast failed since the user have strong password. So we need to use Shadow Creds.

![image-20250126162640065](./assets/image-20250126162640065.png)

PTH to WinRM.

![image-20250126163239491](./assets/image-20250126163239491.png)

Since GenericAll, we can change the password directly.

Obviously from its username, we need to dig out the CS.

![image-20250126164309328](./assets/image-20250126164309328.png)

We can find a template vulnerable to ESC9.

![image-20250126165311527](./assets/image-20250126165311527.png)

