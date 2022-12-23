# Configuring-DNS-Forwarder-in-Windows-Server-2019.
Configuring DNS Forwarder in Windows Server 2019.

<h1 align="center">👨‍💻 Configuring DNS Forwarder in Windows Server 2019.:</h1>

DNS forwarders are a useful feature that allows a DNS server to forward DNS queries for external domains to other DNS servers. This can be useful for a number of reasons, such as reducing the load on the DNS server or improving the speed of name resolution for external domains. In this post, I’ll walk you through the process of configuring forwarders in DNS.


Open the “DNS Manager” console on your DNS server.
![Screenshot 2022-12-22 133856](https://user-images.githubusercontent.com/86381942/209290542-371f247f-126a-410d-a500-f158e88d5d37.png)


In the console tree, right-click on the DNS server and select “Properties”.
![2](https://user-images.githubusercontent.com/86381942/209290568-ee002229-0094-4552-b26a-66e9650b9e69.png)


In the “DNS Server Properties” window, click on the “Forwarders” tab.
![3](https://user-images.githubusercontent.com/86381942/209290577-967f6509-a827-4aef-a12c-ec2b46f6a3e6.png)


To add a new forwarder, click the “Edit” button.


In the “Edit Forwarders” window, enter the IP address of the DNS server you want to forward queries to in the “IP address” field. You can also specify multiple DNS servers by separating them with a semicolon.
![4](https://user-images.githubusercontent.com/86381942/209290607-0e79a583-26a7-497e-9023-6f156eea7739.png)


On this DNS Forwarder, I use OpenDNS Public IP.

208.67.222.222 — 208.67.220.220

Click “APPLY” and “OK” to save your changes.
![5](https://user-images.githubusercontent.com/86381942/209290634-944b7227-b4da-4a37-9c7c-99b56c9ad897.png)


In the console tree, right-click on the DNS server and select “All Task”>” Re-start”.
![6](https://user-images.githubusercontent.com/86381942/209290652-87d2db48-fc48-46ef-9c3c-c23dd15deb26.png)


That’s it! You should now have forwarders configured on your DNS server. Remember to test your configuration to ensure that it is working as expected.

If you want to disable forwarders, you can uncheck the “Use root hints if no forwarders are available” box. This will prevent the DNS server from using root hints to resolve queries for external domains.
