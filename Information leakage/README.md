# Ruijie NBR3000D-E gateway has information leakage vulnerability

## Overview
Manufacturer's address：[(https://113.93.51.149:4430/main.htm)]
## Vulnerability impact
Ruijie NBR3000D-E gateway
## Vulnerability location
/tool/shell/postgresql.conf
## Vulnerability details
Ruijie Network is a professional network manufacturer with a full range of network equipment product lines and solutions, including switches, routers, software, security firewalls, wireless products, storage, and more. There is an information leakage vulnerability in the Ruijie NBR3000D-E gateway, which allows attackers to obtain server privileges and cause the server to crash 
## Vulnerability verify
[(https://113.93.51.149:4430/main.htm)]
<br />1.Code analysis
<br />The configuration file postgresql.exe has not been authenticated, resulting in direct access to the configuration file by the frontend.
<br />![alt text](image.png)
<br />And the following code includes the authentication file mvc/controller/core.controller.php, as shown in the following figure:The function point containing authentication files requires login
<br />![alt text](image-1.png)
<br />![alt text](image-2.png)
<br />2.Vulnerability reproduction
<br />https://113.93.51.149:4430/main.htm
<br />The login interface is shown in the figure
<br />admin/lwd1012
<br />![alt text](image-3.png)
<br />Accessing without logging in
<br />https://113.93.51.149:4430/tool/shell/postgresql.conf，You can view the PostgreSQL configuration file
<br />![alt text](image-4.png)
<br />![alt text](image-5.png)