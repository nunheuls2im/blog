---
publish: true
title: 모의해킹 보고서 – Lab 22
created: 2026-11-20T00:02:44.797Z
modified: 2026-11-20T00:09:38.415Z
tags:
  - pentest
  - linux
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

본 보고서는 개인 실습을 위한 2026년 11월 20일 09시부터 2026년 11월 일 시까지 진행된 lab 22 에 대한 모의해킹 보고서이다.

---

### 총평

개인 실습을 위한 모의해킹 대상으로 최고 권한 획득을 위한 목적으로 lab 22 을 진단 하였다. 이 테스트는 실제로 일어날 수 있는 보안 취약점을 공격자의 입장에서 실제 공격과 유사한 방식으로 공격을 시도하여 최고 권한을 획득하는 것에 목표를 두고 취약점 진단을 진행하였다. lab 22  을 대상으로 모의해킹 및 시스템 침투 테스트를 진행하는 과정에서 여러가지 심각한 취약점이 발견되었다. 공개된 네트워크에서

---

### 권고 사항

---

### 정보 수집 대상

개인 실습을 위한 모의해킹 lab 22 을 대상으로 취약점 점검을 진행하였다.
해당 대상인 lab 22 의 IP는 사설 IP이지만 자산 보호로 Masking처리 진행 하였다.

---

### 서비스 열거

개인 실습을 위한 모의 해킹 대상인 lab 22 에서 실행중인 서비스를 확인하고 관련 정보를 수집한다.
수집된 정보를 바탕으로 시스템으로 진입할 수 있는 잠재적 공격 경로에 대한 정보를 얻고 해당 시스템에서 어떤 어플리케이션이 동작하는지 파악하여 실제 침투를 진행하기 전 필요한 정보를 확보 할 수 있다. 실행중인 서비스이나 정보 수집 과정에서 공개 되지 않을 수 있다.

---

### 침투

개인 실습을 위한 모의해킹 대상인 lab 22 으로부터 최고 권한인 계정을 획득 하였다.

---

### 접근 권한 유지

공격자 입장에서 침투했을 때 일시적인 데이터 수집을 목표로 하지 않기에 지속적인 공격을 위해 시스템에 대한 접근 유지는 중요하다. 취약한 서비스의 버전이 업데이트 되거나 접근 계정의 비밀번호가 바뀌었을 때에도 지속적인 접근으로 최고 권한을 유지하기 위해 백도어나 계정을 생성할 수 있다. 해당 모의해킹 실습 대상에서는 진행하지 않았다

---

### 사후 정리

공격이 목적이 아닌 취약점 점검이 목적이므로 침투 테스트 중 생성된 흔적을 제거할 필요가 있다. 해당 실습 lab 22 에서는 추가적인 계정 생성이나 서비스 등록 및 도구 설치가 진행 하지 않아 제거 절차는 진행하지 않았다.

---

## 모의해킹 수행 내용

### 대상 - lab 22

#### 취약점 설명 :

#### 취약점 조치 방안 :

#### 심각도 :

#### 공격 재현 절차 :

---

### 증적 자료 및 취약점

![[Template/Image/Pasted image 20261120090423.png]]

```
└─$ cat /etc/hosts
127.0.0.1	localhost
127.0.1.1	kali
10.129.244.177	lab22

::1     localhost ip6-localhost ip6-loopback
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters
```

![[Template/Image/Pasted image 20261120090618.png]]

```
└─$ nmap -Pn -p- lab22
Starting Nmap 7.99 ( https://nmap.org ) at 2026-11-20 09:04 +0900
Nmap scan report for lab22 (10.129.244.177)
Host is up (0.086s latency).
Not shown: 65532 closed tcp ports (reset)
PORT    STATE SERVICE
22/tcp  open  ssh
139/tcp open  netbios-ssn
445/tcp open  microsoft-ds

Nmap done: 1 IP address (1 host up) scanned in 37.32 seconds

```

![[Template/Image/Pasted image 20261120090713.png]]

```
└─$ nmap -Pn -p 22,139,445 lab22 -sSCV
Starting Nmap 7.99 ( https://nmap.org ) at 2026-11-20 09:05 +0900
Nmap scan report for lab22 (10.129.244.177)
Host is up (0.087s latency).

PORT    STATE SERVICE     VERSION
22/tcp  open  ssh         OpenSSH 9.6p1 Ubuntu 3ubuntu13.16 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
|   256 0c:4b:d2:76:ab:10:06:92:05:dc:f7:55:94:7f:18:df (ECDSA)
|_  256 2d:6d:4a:4c:ee:2e:11:b6:c8:90:e6:83:e9:df:38:b0 (ED25519)
139/tcp open  netbios-ssn Samba smbd 4
445/tcp open  netbios-ssn Samba smbd 4
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Host script results:
|_nbstat: NetBIOS name: ABDUCTED, NetBIOS user: <unknown>, NetBIOS MAC: <unknown> (unknown)
| smb2-time:
|   date: 2026-11-20T00:04:40
|_  start_date: N/A
|_clock-skew: -1m30s
| smb2-security-mode:
|   3.1.1:
|_    Message signing enabled but not required

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 14.10 seconds
```

![[Template/Image/Pasted image 20261120090930.png]]

```
└─$ smbclient -L lab22 -p 139 -N

	Sharename       Type      Comment
	---------       ----      -------
	HP-Reception    Printer   Reception printer
	projects        Disk      Hartley Group Project Files
	transfer        Disk      Staff file transfer
	IPC$            IPC       IPC Service (Hartley Group Document Services)
Reconnecting with SMB1 for workgroup listing.
smbXcli_negprot_smb1_done: No compatible protocol selected by server.
Protocol negotiation to server lab22 (for a protocol between LANMAN1 and NT1) failed: NT_STATUS_INVALID_NETWORK_RESPONSE
Unable to connect with SMB1 -- no workgroup available

┌──(kali㉿133)-[~/Desktop/lab/lab22]
└─$ smbclient -L lab22 -p 445 -N

	Sharename       Type      Comment
	---------       ----      -------
	HP-Reception    Printer   Reception printer
	projects        Disk      Hartley Group Project Files
	transfer        Disk      Staff file transfer
	IPC$            IPC       IPC Service (Hartley Group Document Services)
Reconnecting with SMB1 for workgroup listing.
smbXcli_negprot_smb1_done: No compatible protocol selected by server.
Protocol negotiation to server lab22 (for a protocol between LANMAN1 and NT1) failed: NT_STATUS_INVALID_NETWORK_RESPONSE
Unable to connect with SMB1 -- no workgroup available
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
