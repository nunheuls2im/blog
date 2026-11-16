---
publish: true
title: Network Packet Structure & Protocol Header
created: 2026-11-16T00:02:20.876Z
modified: 2026-11-16T15:32:25.065Z
tags:
  - Network
  - PDU
  - Header
  - Packet
  - Ethernet
  - IPv4
  - TCP
  - UDP
  - ARP
  - ICMP
  - DNS
  - DHCP
---

Frame = L2의 PDU : Protocol Data Unit

packet = L3의 PDU :

segment : TCP의 PDU  , datagram UDP의 PDU

data : Application의 PDU

---

데이터는 Header들의 연속된 집합

L1
Physical Layer Header
7 Preamble
1 SFD

---

L2
Ethernet Frame header는 총 14bytes

Dst MAC addr 6 bytes
Src MAC addr 6 bytes
Type or Length 2 bytes

Data 46~1500 bytes

Trailer 4 bytes

Frame의 최대 크기는 14 + 1500 + 4  = 1518

---

L3
IP Header의 최소 크기는 20 bytes, 최대 크기는 60bytes
options + padding 40 bytes

최대 packet의 크기는 65535 bytes

version 4 bits + header length 4bits = 1 bytes
TOS: type of service = 1 byte
total length : 2 bytes
Identification 2 bytes
flag 1 byte
fragment Offset 1 byte
TTL 1 byte
Protocol Type 1 byte
Header Checksum 2 bytes
Src IP addr 4 bytes
Dst IP addr 4 bytes
++ Options 40 bytes

Payload : Data 65475 ~ 65515

---

L4
TCP Header 의 최소 크기는 20bytes 최대 크기는 60bytes
Source Port 2bytes
Destination Port 2bytes
Sequence Number 4bytes
Acknowledgement Number 4bytes
Offset 1 byte
최소 값은 5이며 단위로 환산시 4를 곱한다. 5 x 4 = 20 bytes
Reserved 3 bits
AE (Accurate ECN) 1 bit
26년 4월 24일 할당
TCP Flags 1 byte
CMR 1 bit
ECE 1 bit
URG 1 bit
ACK 1 bit
RSH 1 bit
RST 1 bit
SYN 1 bit
FIN 1 bit
Window 2 bytes
Checksum 2 bytes
Urgent Pointer 2 bytes
TCP Options 40 bytes

UDP Header 의 크기는 8 bytes
Source Port 2bytes
Destination Port 2 bytes
Length 2 bytes
Checksum 2bytes

---

DHCP Header 크기는 236 bytes

Operation 1 byte
Hardware type 1byte
Hardware address length 1byte
hops 1 byte
transaction ID 4 bytes
second elapsed 2 bytes
flags 2 bytes
client address 4 bytes
server address 4 bytes
gateway address 4 bytes
client hardware address 16 bytes
server name 64 bytes
file 128 bytes 부트파일 이름과 경로만 알려주는 영역
options + message type

- Disco ver
- Offer
- Request
- Decline
- ACK
- NAK
- Release
- Inform

---

DNS header 는 12bytes

transaction ID 2 bytes
Flag 2 bytes

- QR (Query / Response)  1 bit
  - 0 request
  - 1 reply
- Op code (Operation Code) 4 bits
  - 0 표준 질의
  - 1 역 질의
  - 2 서버의 상태 요구
  - 4 통지
  - 5 갱신
- AA (Authoritative Answer) 1bit
- DNS 응답 메시지에 만 사용됨
  - 1 네임서버 권한이 인정된 서버일 때
- TC (Truncated) 1bit
  - 512 bytes 초과 여부 확인
  - 0 not truncated
  - 1 512 이상이라서 truncated , 이때는 TCP를 통해 질의 재전송
- RD (Recursion Desired) 1 bit
  - 1 클라이언트가 재귀 질의를 원함
- RA (Recursion Available) 1 bit
  - 재귀 질의가 가능한지 나타냄
- Reserved 3bit : 0 0 0
  - Z (zero)
  - AD (Authentic Data)
  - CD (Checking Disabled)
- rCode (response code) 4 bit
  - 0 no error
  - 1 format error
  - 2 server failure
  - 3 도메인네임 존재하지 않음 등
    Question count 2 bytes
    질의 수
    Query Count / Zon Count
    Answer count 2 bytes
    응답 수
    Anser Count / Prerequisite Count
    Name Server count 2 bytes
    Authority Record count / update count
    Additional count 2 bytes
    additional information count

---

ARP header 크기는 28 bytes
Hardware Type : 2 bytes
네트워크 유형을 나타냄
Protocol Type : 2 bytes
ipv4, ipv6, ATM 등 프로토콜 정의
hardware address size / hardware length 1 byte
이더넷의 경우 6
protocol address length 1 byte
ipv4의 경우 4
Opertation code 2 bytes
arp request : 1
arp reply : 2
rarp request 3
rarp reply 4
sender ahrdware address : 6bytes
seder protocol address : 4 bytes
target hardware address : 6 bytes
target protocol address 4 bytes

---

ICMP header 는 8 bytes

Type 1 byte
type 0 Echo Reply
type 3 Destination Unreachable
code 0 network unrechable
code 1 host unrechable
code 2 protocol unrechable
code 3 port unrechable
type 4 Source Quench
type 5 Redirect
type 8 echo request
type 9 Router Advertisement
type 10 Router Solicitation
type 11 Time exceeded
type 12 Parameter Problem
Code 1 byte
Checksum 2 bytes
Rest of Header 4 byte

---
