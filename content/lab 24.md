---
publish: true
title: 모의해킹 보고서 – Lab 24
created: 2026-11-25T00:14:46.164Z
modified: 2026-11-25T02:25:11.671Z
---

<div style="height: 30px;"></div>

# 목차

<div style="height: 30px;"></div>
<div class="report-toc">
  <a href="#개요" class="report-toc-row" data-no-popover="true"><span class="toc-number">1.</span><span class="toc-dots"></span><span class="toc-title">개요</span></a>
  <a href="#총평" class="report-toc-row" data-no-popover="true"><span class="toc-number">2.</span><span class="toc-dots"></span><span class="toc-title">총평</span></a>
  <a href="#권고-사항" class="report-toc-row" data-no-popover="true"><span class="toc-number">3.</span><span class="toc-dots"></span><span class="toc-title">권고 사항</span></a>
  <a href="#정보-수집-대상" class="report-toc-row" data-no-popover="true"><span class="toc-number">4.</span><span class="toc-dots"></span><span class="toc-title">정보 수집 대상</span></a>
  <a href="#서비스-열거" class="report-toc-row" data-no-popover="true"><span class="toc-number">5.</span><span class="toc-dots"></span><span class="toc-title">서비스 열거</span></a>
  <a href="#침투" class="report-toc-row" data-no-popover="true"><span class="toc-number">6.</span><span class="toc-dots"></span><span class="toc-title">침투</span></a>
  <a href="#접근-권한-유지" class="report-toc-row" data-no-popover="true"><span class="toc-number">7.</span><span class="toc-dots"></span><span class="toc-title">접근 권한 유지</span></a>
  <a href="#사후-정리" class="report-toc-row" data-no-popover="true"><span class="toc-number">8.</span><span class="toc-dots"></span><span class="toc-title">사후 정리</span></a>
  <a href="#모의해킹-수행-내용" class="report-toc-row" data-no-popover="true"><span class="toc-number">9.</span><span class="toc-dots"></span><span class="toc-title">모의해킹 수행 내용</span></a>
  <a href="#증적-자료-및-취약점" class="report-toc-row" data-no-popover="true"><span class="toc-number">10.</span><span class="toc-dots"></span><span class="toc-title">증적 자료 및 취약점</span></a>
</div>

---

### 개요

본 보고서는 개인 실습을 위한 2026년 11월 25일 09시부터 2026년 11월 일 시까지 진행된 lab 에 대한 모의해킹 보고서이다.

---

### 총평

개인 실습을 위한 모의해킹 대상으로 최고 권한 획득을 위한 목적으로 lab 을 진단 하였다. 이 테스트는 실제로 일어날 수 있는 보안 취약점을 공격자의 입장에서 실제 공격과 유사한 방식으로 공격을 시도하여 최고 권한을 획득하는 것에 목표를 두고 취약점 진단을 진행하였다. lab  을 대상으로 모의해킹 및 시스템 침투 테스트를 진행하는 과정에서 여러가지 심각한 취약점이 발견되었다. 공개된 네트워크에서

---

### 권고 사항

---

### 정보 수집 대상

개인 실습을 위한 모의해킹 lab 을 대상으로 취약점 점검을 진행하였다.
해당 대상인 lab 의 IP는 사설 IP이지만 자산 보호로 Masking처리 진행 하였다.

---

### 서비스 열거

개인 실습을 위한 모의 해킹 대상인 lab 에서 실행중인 서비스를 확인하고 관련 정보를 수집한다.
수집된 정보를 바탕으로 시스템으로 진입할 수 있는 잠재적 공격 경로에 대한 정보를 얻고 해당 시스템에서 어떤 어플리케이션이 동작하는지 파악하여 실제 침투를 진행하기 전 필요한 정보를 확보 할 수 있다. 실행중인 서비스이나 정보 수집 과정에서 공개 되지 않을 수 있다.

---

### 침투

개인 실습을 위한 모의해킹 대상인 lab 으로부터 최고 권한인 계정을 획득 하였다.

---

### 접근 권한 유지

공격자 입장에서 침투했을 때 일시적인 데이터 수집을 목표로 하지 않기에 지속적인 공격을 위해 시스템에 대한 접근 유지는 중요하다. 취약한 서비스의 버전이 업데이트 되거나 접근 계정의 비밀번호가 바뀌었을 때에도 지속적인 접근으로 최고 권한을 유지하기 위해 백도어나 계정을 생성할 수 있다. 해당 모의해킹 실습 대상에서는 진행하지 않았다

---

### 사후 정리

공격이 목적이 아닌 취약점 점검이 목적이므로 침투 테스트 중 생성된 흔적을 제거할 필요가 있다. 해당 실습 lab 에서는 추가적인 계정 생성이나 서비스 등록 및 도구 설치가 진행 하지 않아 제거 절차는 진행하지 않았다.

---

## 모의해킹 수행 내용

### 대상 - lab

#### 취약점 설명 :

#### 취약점 조치 방안 :

#### 심각도 :

#### 공격 재현 절차 :

---

### 증적 자료 및 취약점 1

![[Template/Image/Pasted image 20261125102330.png]]

```
└─# nmap -sS 10.0.7.208/28
Starting Nmap 7.94 ( https://nmap.org ) at 2026-11-25 01:16 UTC
Nmap scan report for 10.0.7.209
Host is up (0.000082s latency).
All 1000 scanned ports on 10.0.7.209 are in ignored states.
Not shown: 1000 filtered tcp ports (no-response)
MAC Address: 0A:FF:C1:DB:3C:C5 (Unknown)

Nmap scan report for 10.0.7.213
Host is up (0.00010s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE
22/tcp open  ssh
80/tcp open  http
MAC Address: 0A:FF:FE:59:CC:E5 (Unknown)

Nmap scan report for 10.0.7.218
Host is up (0.00027s latency).
Not shown: 998 filtered tcp ports (no-response)
PORT   STATE SERVICE
21/tcp open  ftp
80/tcp open  http
MAC Address: 0A:FF:C5:D3:51:67 (Unknown)

Nmap scan report for 10.0.7.221
Host is up (0.00019s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE
22/tcp open  ssh
80/tcp open  http
MAC Address: 0A:FF:D6:8B:8B:9D (Unknown)

Nmap scan report for 10.0.7.216
Host is up (0.0000040s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE
22/tcp open  ssh

Nmap done: 16 IP addresses (5 hosts up) scanned in 7.27 seconds
```

![[Template/Image/Pasted image 20261125105135.png]]

```
└─# nmap -Pn -p- 10.0.7.213 -sSCV
Starting Nmap 7.94 ( https://nmap.org ) at 2026-11-25 01:26 UTC
Nmap scan report for 10.0.7.213
Host is up (0.00012s latency).
Not shown: 65533 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 8.9p1 Ubuntu 3ubuntu0.4 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
|   256 4b:65:84:5e:bf:fa:ce:55:8a:13:0b:f6:ab:cb:57:2e (ECDSA)
|_  256 e5:85:5e:95:94:55:2e:60:56:e6:36:68:47:e8:50:3e (ED25519)
80/tcp open  http    Apache httpd 2.4.52 ((Ubuntu))
|_http-title: Apache2 Ubuntu Default Page: It works
|_http-server-header: Apache/2.4.52 (Ubuntu)
MAC Address: 0A:FF:FE:59:CC:E5 (Unknown)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 7.39 seconds
```

![[Template/Image/Pasted image 20261125111523.png]]

```
└─# gobuster dir -u http://10.0.7.213 -w ~/common.txt
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://10.0.7.213
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /root/common.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/.htaccess            (Status: 403) [Size: 275]
/.hta                 (Status: 403) [Size: 275]
/.htpasswd            (Status: 403) [Size: 275]
/blog                 (Status: 301) [Size: 307] [--> http://10.0.7.213/blog/]
/index.html           (Status: 200) [Size: 10671]
/server-status        (Status: 403) [Size: 275]
Progress: 4614 / 4615 (99.98%)
===============================================================
Finished
===============================================================
```

![[Template/Image/Pasted image 20261125111600.png]]

```
└─# gobuster dir -u http://10.0.7.213/blog -w ~/common.txt
===============================================================
Gobuster v3.6
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://10.0.7.213/blog
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /root/common.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.6
[+] Timeout:                 10s
===============================================================
Starting gobuster in directory enumeration mode
===============================================================
/.hta                 (Status: 403) [Size: 275]
/.htpasswd            (Status: 403) [Size: 275]
/_backup              (Status: 301) [Size: 315] [--> http://10.0.7.213/blog/_backup/]
/.htaccess            (Status: 403) [Size: 275]
/index.php            (Status: 301) [Size: 0] [--> http://10.0.7.213/blog/]
/wordpress            (Status: 301) [Size: 317] [--> http://10.0.7.213/blog/wordpress/]
/wp-admin             (Status: 301) [Size: 316] [--> http://10.0.7.213/blog/wp-admin/]
/wp-content           (Status: 301) [Size: 318] [--> http://10.0.7.213/blog/wp-content/]
/wp-includes          (Status: 301) [Size: 319] [--> http://10.0.7.213/blog/wp-includes/]
/xmlrpc.php           (Status: 405) [Size: 42]

===============================================================
Finished
===============================================================
```

![[Template/Image/Pasted image 20261125112413.png]]
![[Template/Image/Pasted image 20261125112440.png]]
![[Template/Image/Pasted image 20261125112458.png]]

```
└─# wpscan --url 10.0.7.213/blog
_______________________________________________________________
         __          _______   _____
         \ \        / /  __ \ / ____|
          \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
           \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
            \  /\  /  | |     ____) | (__| (_| | | | |
             \/  \/   |_|    |_____/ \___|\__,_|_| |_|

         WordPress Security Scanner by the WPScan Team
                         Version 3.8.24
       Sponsored by Automattic - https://automattic.com/
       @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart
_______________________________________________________________

[+] URL: http://10.0.7.213/blog/ [10.0.7.213]
[+] Started: Wed Nov 25 02:19:47 2026

Interesting Finding(s):

[+] Headers
 | Interesting Entry: Server: Apache/2.4.52 (Ubuntu)
 | Found By: Headers (Passive Detection)
 | Confidence: 100%

[+] XML-RPC seems to be enabled: http://10.0.7.213/blog/xmlrpc.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%
 | References:
 |  - http://codex.wordpress.org/XML-RPC_Pingback_API
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_ghost_scanner/
 |  - https://www.rapid7.com/db/modules/auxiliary/dos/http/wordpress_xmlrpc_dos/
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_xmlrpc_login/
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_pingback_access/

[+] WordPress readme found: http://10.0.7.213/blog/readme.html
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%

[+] Upload directory has listing enabled: http://10.0.7.213/blog/wp-content/uploads/
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%

[+] The external WP-Cron seems to be enabled: http://10.0.7.213/blog/wp-cron.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 60%
 | References:
 |  - https://www.iplocation.net/defend-wordpress-from-ddos
 |  - https://github.com/wpscanteam/wpscan/issues/1299

[+] WordPress version 6.4.1 identified (Insecure, released on 2023-11-09).
 | Found By: Rss Generator (Passive Detection)
 |  - http://10.0.7.213/blog/?feed=rss2, <generator>https://wordpress.org/?v=6.4.1</generator>
 |  - http://10.0.7.213/blog/?feed=comments-rss2, <generator>https://wordpress.org/?v=6.4.1</generator>

[+] WordPress theme in use: twentytwentyfour
 | Location: http://10.0.7.213/blog/wp-content/themes/twentytwentyfour/
 | Last Updated: 2026-05-20T00:00:00.000Z
 | Readme: http://10.0.7.213/blog/wp-content/themes/twentytwentyfour/readme.txt
 | [!] The version is out of date, the latest version is 1.5
 | [!] Directory listing is enabled
 | Style URL: http://10.0.7.213/blog/wp-content/themes/twentytwentyfour/style.css
 | Style Name: Twenty Twenty-Four
 | Style URI: https://wordpress.org/themes/twentytwentyfour/
 | Description: Twenty Twenty-Four is designed to be flexible, versatile and applicable to any website. Its collecti...
 | Author: the WordPress team
 | Author URI: https://wordpress.org
 |
 | Found By: Urls In Homepage (Passive Detection)
 |
 | Version: 1.0 (80% confidence)
 | Found By: Style (Passive Detection)
 |  - http://10.0.7.213/blog/wp-content/themes/twentytwentyfour/style.css, Match: 'Version: 1.0'

[+] Enumerating All Plugins (via Passive Methods)

[i] No plugins Found.

[+] Enumerating Config Backups (via Passive and Aggressive Methods)
 Checking Config Backups - Time: 00:00:00 <====================================================> (137 / 137) 100.00% Time: 00:00:00

[i] No Config Backups Found.

[!] No WPScan API Token given, as a result vulnerability data has not been output.
[!] You can get a free API token with 25 daily requests by registering at https://wpscan.com/register

[+] Finished: Wed Nov 25 02:19:53 2026
[+] Requests Done: 169
[+] Cached Requests: 5
[+] Data Sent: 43.134 KB
[+] Data Received: 293.739 KB
[+] Memory used: 278.703 MB
[+] Elapsed time: 00:00:05
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

### 증적 자료 및 취약점 2

![[Template/Image/Pasted image 20261125102505.png]]

```
└─# nmap -sS 10.0.7.208/28
Starting Nmap 7.94 ( https://nmap.org ) at 2026-11-25 01:16 UTC
Nmap scan report for 10.0.7.209
Host is up (0.000082s latency).
All 1000 scanned ports on 10.0.7.209 are in ignored states.
Not shown: 1000 filtered tcp ports (no-response)
MAC Address: 0A:FF:C1:DB:3C:C5 (Unknown)

Nmap scan report for 10.0.7.213
Host is up (0.00010s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE
22/tcp open  ssh
80/tcp open  http
MAC Address: 0A:FF:FE:59:CC:E5 (Unknown)

Nmap scan report for 10.0.7.218
Host is up (0.00027s latency).
Not shown: 998 filtered tcp ports (no-response)
PORT   STATE SERVICE
21/tcp open  ftp
80/tcp open  http
MAC Address: 0A:FF:C5:D3:51:67 (Unknown)

Nmap scan report for 10.0.7.221
Host is up (0.00019s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE
22/tcp open  ssh
80/tcp open  http
MAC Address: 0A:FF:D6:8B:8B:9D (Unknown)

Nmap scan report for 10.0.7.216
Host is up (0.0000040s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE
22/tcp open  ssh

Nmap done: 16 IP addresses (5 hosts up) scanned in 7.27 seconds
```

![[Template/Image/Pasted image 20261125104753.png]]

```
└─# nmap -Pn -p- 10.0.7.218
Starting Nmap 7.94 ( https://nmap.org ) at 2026-11-25 01:42 UTC
Nmap scan report for 10.0.7.218
Host is up (0.00034s latency).
Not shown: 65528 filtered tcp ports (no-response)
PORT      STATE SERVICE
21/tcp    open  ftp
80/tcp    open  http
49664/tcp open  unknown
49665/tcp open  unknown
49666/tcp open  unknown
49670/tcp open  unknown
49674/tcp open  unknown
MAC Address: 0A:FF:C5:D3:51:67 (Unknown)

Nmap done: 1 IP address (1 host up) scanned in 191.81 seconds
```

![[Template/Image/Pasted image 20261125104946.png]]

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

### 증적 자료 및 취약점 3

![[Template/Image/Pasted image 20261125102413.png]]

```
└─# nmap -sS 10.0.7.208/28
Starting Nmap 7.94 ( https://nmap.org ) at 2026-11-25 01:16 UTC
Nmap scan report for 10.0.7.209
Host is up (0.000082s latency).
All 1000 scanned ports on 10.0.7.209 are in ignored states.
Not shown: 1000 filtered tcp ports (no-response)
MAC Address: 0A:FF:C1:DB:3C:C5 (Unknown)

Nmap scan report for 10.0.7.213
Host is up (0.00010s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE
22/tcp open  ssh
80/tcp open  http
MAC Address: 0A:FF:FE:59:CC:E5 (Unknown)

Nmap scan report for 10.0.7.218
Host is up (0.00027s latency).
Not shown: 998 filtered tcp ports (no-response)
PORT   STATE SERVICE
21/tcp open  ftp
80/tcp open  http
MAC Address: 0A:FF:C5:D3:51:67 (Unknown)

Nmap scan report for 10.0.7.221
Host is up (0.00019s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE
22/tcp open  ssh
80/tcp open  http
MAC Address: 0A:FF:D6:8B:8B:9D (Unknown)

Nmap scan report for 10.0.7.216
Host is up (0.0000040s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE
22/tcp open  ssh

Nmap done: 16 IP addresses (5 hosts up) scanned in 7.27 seconds
```

![[Template/Image/Pasted image 20261125103139.png]]

```
└─# nmap -Pn -p- 10.0.7.221 -sSCV
Starting Nmap 7.94 ( https://nmap.org ) at 2026-11-25 01:30 UTC
Nmap scan report for 10.0.7.221
Host is up (0.00025s latency).
Not shown: 65532 closed tcp ports (reset)
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 8.9p1 Ubuntu 3ubuntu0.4 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
|   256 28:6d:dd:d1:6c:88:56:3b:46:68:11:46:2f:31:91:20 (ECDSA)
|_  256 de:39:53:f7:41:12:91:2b:a8:4d:80:cf:fe:37:38:c8 (ED25519)
80/tcp   open  http    Apache httpd 2.4.52 ((Ubuntu))
|_http-server-header: Apache/2.4.52 (Ubuntu)
|_http-title: Apache2 Ubuntu Default Page: It works
5984/tcp open  http    CouchDB httpd 1.6.1 (Erlang OTP/17)
|_http-title: Site doesn't have a title (text/plain; charset=utf-8).
|_http-server-header: CouchDB/1.6.1 (Erlang OTP/17)
MAC Address: 0A:FF:D6:8B:8B:9D (Unknown)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.78 seconds
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```

```
```
