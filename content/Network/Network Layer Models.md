---
publish: true
title: Network Layer Models
created: 2026-11-15T07:33:07.582Z
modified: 2026-11-15T09:07:21.334Z
tags:
  - Network
  - OSI
  - TCP/IP
---

<div style="height: 30px;"></div>

# OSI 7 Layer Model

Open Systems Interconnection Reference Model

> 국제표준화기구인 `ISO`에서 1984년에 발표한 네트워크 통신 구조를 7개의 계층으로 구분한 표준 참조 모델

## L1 - Physical Layer ( PDU : bit )

> 전기적, 광학적, 무선 신호를 이용해 0과 1로 구성된 `Bit` 데이터를 물리적 전송 매체를 통해 송수신

#### 네트워크 장비

Hub, Repeater, Modem, Media Converter

## L2 - Data Link Layer ( PDU : Frame )

> `MAC Address` 등을 이용해 동일한 Network Link에 연결된 장치 간 데이터를 `Frame` 단위로 전송하며, Frame 구성 및 오류 검출 수행

#### 네트워크 장비

L2 Switch, Bridge, NIC, Wireless AP

## L3 - Network Layer ( PDU : Packet )

> `IP Address` 등의 논리적 주소를 이용해 서로 다른 Network에 있는 장치 간 데이터를 `Packet` 단위로 전달하며, 목적지까지의 경로 결정 및 라우팅 수행

#### 네트워크 장비

Router, L3 Switch, L3 Firewall

## L4 - Transport Layer ( PDU : Segment,Datagram )

> `Port Number`를 통해 Source와 Destination의 Application Process를 구분하고 종단 간 데이터 전송을 수행하며, TCP와 같은 프로토콜에서는 신뢰성 및 흐름 제어 제공

#### 네트워크 장비

L4 Switch, L4 Load Balancer, Stateful Firewall

## L5 - Session Layer ( PDU : Data )

> 통신하는 Application 간 `Session`을 설정, 유지, 종료하고 데이터 교환을 위한 대화 및 동기화 관리

#### 네트워크 장비

Session Gateway, Session Border Controller(SBC)

## L6 - Presentation Layer ( PDU : Data )

> 송신자와 수신자가 데이터를 동일하게 해석할 수 있도록 데이터 형식 변환, 암호화 복호화 및 압축 압축 해제 수행

#### 네트워크 장비

SSL/TLS Offloader, Encryption Gateway

## L7 - Application Layer ( PDU : Data )

> Application이 Network Service를 이용할 수 있도록 Interface와 통신 Protocol을 제공하고 응용 서비스에 필요한 데이터 교환 수행

#### 네트워크 장비

L7 Switch, WAF, Proxy Server, L7 Load Balancer

---

# TCP/IP 4 Layer Model

Transmission Control Protocol / Internet Protocol Model

미국 국방부 산하 `DARPA`의 인터넷 통신 프로토콜 연구에서 유래한 네트워크 참조 모델로, 1989년 `IETF`의 `RFC 1122`에서 인터넷 프로토콜 구조를 4개의 계층으로 설명

## L1 - Link / Network Access Layer ( PDU : Frame, Bit )

> 물리적 Network에 연결된 장치 간 데이터를 `Frame` 단위로 전송하며, `MAC Address` 등을 이용한 장치 식별, Frame 구성 및 오류 검출과 물리적 신호를 통한 Bit 데이터 송수신 수행

#### 네트워크 장비

Hub, Repeater, L2 Switch, Bridge, NIC, Wireless AP

## L2 - Internet Layer ( PDU : Packet )

> `IP Address`를 이용해 서로 다른 Network에 있는 장치 간 데이터를 `Packet` 단위로 전달하며, 목적지까지의 경로 결정 및 라우팅 수행

#### 네트워크 장비

Router, L3 Switch, L3 Firewall

## L3 - Transport Layer ( PDU : Segment, Datagram )

> `Port Number`를 통해 Source와 Destination의 Application Process를 구분하고 종단 간 데이터 전송을 수행하며, TCP와 같은 프로토콜에서는 신뢰성 및 흐름 제어 제공

#### 네트워크 장비

L4 Switch, L4 Load Balancer, Stateful Firewall

## L4 - Application Layer ( PDU : Data )

Application이 Network Service를 이용할 수 있도록 통신 Protocol을 제공하며, 데이터 형식 변환, 암호화 및 Session 관리 등의 기능을 포함하여 응용 서비스에 필요한 데이터 교환 수행

#### 네트워크 장비

Proxy Server, WAF, L7 Switch, L7 Load Balancer, SSL/TLS Offloader
