# Configuring-DNS-Forwarder-in-Windows-Server-2019.
Configuring DNS Forwarder in Windows Server 2019.

<h1 align="center">👨‍💻 Configuring DNS Forwarder in Windows Server 2019.:</h1>

DNS forwarders are a useful feature that allows a DNS server to forward DNS queries for external domains to other DNS servers. This can be useful for a number of reasons, such as reducing the load on the DNS server or improving the speed of name resolution for external domains. In this post, I’ll walk you through the process of configuring forwarders in DNS.


<h3 align="center">👨‍💻 Open the “DNS Manager” console on your DNS server.:</h3>


![Screenshot 2022-12-22 133856](https://user-images.githubusercontent.com/86381942/209291359-eb3c6236-7bac-4cba-8ed5-629432474bab.png)

<h3 align="center"> In the console tree, right-click on the DNS server and select “Properties”.</h3>

![2](https://user-images.githubusercontent.com/86381942/209291375-4a0f5898-2f0e-43bc-bab6-99bf4d91d12f.png)


<h3 align="center"> In the “DNS Server Properties” window, click on the “Forwarders” tab.</h3>

![3](https://user-images.githubusercontent.com/86381942/209291404-05029fa7-7ade-4781-b9ac-ef3fe0432510.png)


<h3 align="center">To add a new forwarder, click the “Edit” button.</h3>


<h3 align="center">In the “Edit Forwarders” window, enter the IP address of the DNS server you want to forward queries to in the “IP address” field. You can also specify multiple DNS servers by separating them with a semicolon.</h3>

![4](https://user-images.githubusercontent.com/86381942/209291416-af491e91-a574-479a-9a8f-631b2e217941.png)


<h3 align="center">On this DNS Forwarder, I use OpenDNS Public IP.</h3>

208.67.222.222 — 208.67.220.220

<h3 align="center">Click “APPLY” and “OK” to save your changes.</h3>
![5](https://user-images.githubusercontent.com/86381942/209291431-3893d11e-b3b8-4cb5-a3c3-189bbac785a6.png)



<h3 align="center">In the console tree, right-click on the DNS server and select “All Task”>” Re-start”.</h3>

![6](https://user-images.githubusercontent.com/86381942/209291441-1208516c-b44d-43e2-a7c9-4f89870f24ec.png)


<h3 align="center">That’s it! You should now have forwarders configured on your DNS server. Remember to test your configuration to ensure that it is working as expected.</h3>

<h3 align="center">If you want to disable forwarders, you can uncheck the “Use root hints if no forwarders are available” box. This will prevent the DNS server from using root hints to resolve queries for external domains.</h3>
