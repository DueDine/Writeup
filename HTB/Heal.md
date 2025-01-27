Port 22 and 80.

![image-20250127122515101](./assets/image-20250127122515101.png)

Both login and register do not work at site. 

![image-20250127123049830](./assets/image-20250127123049830.png)

So there's a API endpoint.

![image-20250127123126479](./assets/image-20250127123126479.png)

We can get the version of the backend.

After add api to the host, we can login into the main site.

![image-20250127125933826](./assets/image-20250127125933826.png)

We can get another subdomain.

![image-20250127130115555](./assets/image-20250127130115555.png)

![image-20250127130135672](./assets/image-20250127130135672.png)

Try some default creds but do not work.

![image-20250127130303829](./assets/image-20250127130303829.png)

The filename parameter looks promising for a LFI.

![image-20250127130657914](./assets/image-20250127130657914.png)

![image-20250127131153302](./assets/image-20250127131153302.png)

![image-20250127131250483](./assets/image-20250127131250483.png)

![image-20250127131740436](./assets/image-20250127131740436.png)

![image-20250127131851021](./assets/image-20250127131851021.png)

This pair of creds allow us to login the survey site.

We can find a RCE exploit on [GitHub](https://github.com/N4s1rl1/Limesurvey-6.6.4-RCE.git).

![image-20250127132539666](./assets/image-20250127132539666.png)

Get shell as www-root.

![image-20250127132847422](./assets/image-20250127132847422.png)

Retrieve the db password from config.php. Then SSH into the machine as Ron.

![image-20250127133509486](./assets/image-20250127133509486.png)

The server have Consul running at port 8500.

We can find another RCE [here](https://www.exploit-db.com/exploits/51117).

