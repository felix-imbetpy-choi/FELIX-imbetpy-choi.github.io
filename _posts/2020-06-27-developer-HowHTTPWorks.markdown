---
layout: post
title:  "[Internet] HTTP? 개념잡기 통신과정 -IMBETPY"
subtitle:   "About HTTP"
categories: developer
tags: internet what is HTTP ?
comments: true
---
## 개요
> `HTTP` 의 개념과 통신과정, 세부사항, 버전역사 등을 정리 하였습니다.

---


![](https://images.velog.io/images/doomchit_3/post/ff741055-7c6a-4a47-9333-500be49a31fc/http2-http.jpg)


# ⚔ HTTP란?
대량의 정보가 흐르는 곳이라면 언제나 효율적인 교류를 위한 규칙이 존재한다. 
예를들어 주식시장에서 거래를 하고 싶다면  이름, 계좌, 거래일자, 금액 등 정해진 규칙을 지켜 거래를 작성해야 한다.   
규칙을 지켜야 사는사람, 파는사람 모두 효율적인 거래를 성사할 수 있다.  

> `HTTP(Hyper Text Transfer Protocol)` 란 한마디로 **HTML(웹문서를 만들기 위한 언어)** 문서를 주고 받는데 쓰이는 통신프로토콜(통신규약)이며,  **TCP**  와 **UDP** 를 사용하여 통신하며 80번 포트를 사용하는 통신프로토콜(통신규약)이다.


※ **통신프로토콜** : 통신규약이라고도 하며 컴퓨터나 원거리 통신 장비 사이에서 메세지를 주고 받는 양식과 규칙의 체계이다. 이는 신호체계, 인증, 오류감지 기능을 포함할 수 있다. 구성은 물리적측면(매체, 단자, 전송신호, 회선규격) 과 논리적측면(자료 형식 단위, 자료 전송 절차) 로 이루어 진다.

<br/>
<br/>

# 🎈 HTTP 특징
- HTTP 메세지는 **서버와 클라이언트에 의해 해석**된다.
- TCP/IP 를 이용하는 **응용프로토콜(application protocol)** 이다.
- HTTP는 연결상태를 유지하지 않는 **비연결성 프로토콜**입니다. 클라이언트가 이전에 요청한 내용을 기억하고 있지 않는다 라는 것. 
- 비연결성의 단점을 해결하기 위해 **Cookie 와 Session** 이 등장했다.  
- 비연결성 프로토콜이기 때문에 **요청/응답 방식** 으로 동작한다.  
- **도메인 + 자원위치(URL), 도메인 + 자원의 식별자(URI)** 를 통해서 요청을 하고, 서버가 요청에 따른 **HTML 문서응답**을 해줌
- HTML 문서만이 HTTP 통신을 위한 유일한 정보문서는 아니다.   
	- Plain text로 부터 JSON데이터 및 XML과 같은 형태의 정보도 주고 받을 수 있다.
	- 보통은 클라이언트가 어떤 정보를 HTML 형태로 받고 싶은지, JSON 형태로 명시하는 경우가 많다.
- HTTP 가 전체 인터넷 프로토콜에서 위치하는 곳은 **응용계층**이다.
	- 응용 계층 (DNS, FTP, HTTP)
	- 전송 계층 (TCP,UDP,SCTP)
	- 네트워크 계층 (IP,ARP,RARP)
	- 링크 계층 (이더넷, WIFI, 토큰링)



<br/>
<br/>

# 📡 HTTP 통신과정(요청과 응답)

>① 클라이언트(사용자)가 서버에 HTTP Request (요청)을 한다.
② 서버가 사용자의 요청을 받고 HTTP Response (응답)을 한다.

**_각 메세지는 브라우저에서 `F12` -> `Network탭` 에서 확인가능합니다._**

![](https://images.velog.io/images/doomchit_3/post/ddabe01d-65c7-4be4-b5fa-72112f71dc71/http-rere2.png)

## 🛸 1) HTTP Request(요청) 메시지
`요청`은 웹브라우저의 **URL** 을 통해 어느 **웹사이트(도메인)** 의 어느경로에 있는 페이지를 요청할지 나타내는 행위이다. 요청 메세지의 세부사항은 아래와 같다.

```
Request-Line
*(( general-header | request-header | entity-header ) CRLF)
CRLF
[ message-body ]
```

### ① Request-Line 
**Request-Line**, URL정보, 요청방식(Method), HTTP버전정보제공 의 규칙입니다.
아래 그림에서는 Request URL, Request Method 를 나타내고 있습니다.

![](https://images.velog.io/images/doomchit_3/post/fed43472-01f3-4778-b43e-c206a6606860/http-rere4.PNG)


### ② *(( general-header | request-header | entity-header ) CRLF)
**헤더정보** , 헤더에는 요청하는 클라이언트 PC, 브라우저정보, 사용자언어환경, 쿠키 등의 다양한 클라이언트 환경에 대한 정보를 가지고 있다.
때문에 헤더영역에 존재하는 데이터는 보안에 취약하다.

![](https://images.velog.io/images/doomchit_3/post/529a78f6-b86f-43dc-8a54-232ee2ff78c4/http-rere5.PNG)

### ③ CRLF
줄바꿈 명령.

### ④ [ message-body ]
**HHTTP본문영역**, 주로 클라이언크가 입력한 데이터를 저장하는 영역이다.
입력폼에 입력한 각종 데이터가 Method 방식에 따라 서버로 전달할 때 보안이 강화된 방식으로 message-body 에 넣어 전달한다.

<br/>
<br/>

## 🚀 2) HTTP Response(응답)  메시지
`응답`은 HTTP Request 를 통해 요청된 정보에 대해 웹서버가 클라이언트에 보내는 응답형식 및 결과를 나타냅니다.

```
Status-Line
*(( general-header | response-header | entity-header ) CRLF)
CRLF
[ message-body ]
```

### ① Status-Line
**응답 상태정보 표시 라인**, HTTP버전정보 와 세자리 숫자값(200) 과 상태코드 값을 통해 응답결과 및 상태정보를 나타냅니다.

![](https://images.velog.io/images/doomchit_3/post/89dbacfc-2a0b-407d-ab1f-7d8509ae78c2/http-rere6.PNG)

### ② 응답 헤더정보 제공
**헤더정보**, 각종 서버 및 웹사이트 관련 환경정보를 제공한다.

![](https://images.velog.io/images/doomchit_3/post/3f11e3b4-97b0-4e70-af27-84e568c83327/http-rere7.PNG)

### ③ [ message-body ]
**HTTP본문영역**, 주로 서버에서 사용자에게 전달되는 HTML 소스 및 포함된 데이터를 저장하는 영역이다. 

<br/>
<br/>

## 🌔 HTTP Method
`Method` 는 클라이언트가 웹서버에게 사용자의 요청의 목적/종류를 알리는 수단이다.

- GET : 정보 검색 ex) 게시판 리스트 불러오기
- POST : 실행 / 저장 ex) 회원가입 / 로그인
- PUT : 전체 수정 ex) 회원정보 전체 수정
- DELETE : 삭제 ex) 회원정보 삭제
- PATCH : 일부 수정 ex) 회원정보 일부 수정 (Update에 가장 가깝게 쓰이고 있다)
- OPTIONS : 시스템에서 지원하는 메소드 확인

<br/>
<br/>

## 🌕 HTTP Status code

`상태 코드` 는  서버가 클라이언트에게 응답의 상태를 알리는 수단이며, 다섯가지 클래스로 분류된다.

- 1xx: Informational : 요청 정보 처리 중
- 2xx: Success : 요청을 정상적으로 처리함
- 3xx: Redirection : 요청을 완료하기 위해 추가 동작 필요
- 4xx: Client Error : 서버가 요청을 이해하지 못함
- 5xx: Server Error : 서버가 요청 처리 실패함


### ① 1xx: Informational 정보
서버가 요청을 클라이언트에서 성공적으로 수신했으며 서버 끝에서 처리 중이라는 정보를 나타낸다. 
서버의 임시 응답이며 일반적으로 상태 줄과 선택적 헤더 만 포함하며 빈 줄로 끝난다. 
현재는 거의 사용하지 않는다.


### ② 2xx: Success 성공
서버가 요청을 받고 성공적으로 처리되었음을 나타낸다.

### ③ 3xx: Redirection 리디렉션
브라우저는 자동으로 다른 URL로 리디렉션되므로 브라우저 창에는이 코드가 표시되지 않지만, 
이미지 파일처럼 캐싱된 파일을 새로고침 후 확인하면 3xx 코드를 확인할 수 있다.

### ④ 4xx: Client Error 클라이언트 오류
서버가 해결할 수 없는 클라이언트 측 에러 코드다. 
주로 클라이언트(사용자)가 서버에 잘못된 요청을 했을 경우 발생한다.

### ⑤ 5xx: Server Error 서버 오류
서버가 클라이언트의 요청을 처리하지 못했을 때 발생한다. 
서버는 보안 상 통신하지 않는 것이 가장 좋으므로 대부분의 에러 코드를 500 Error로 처리한다.

<br/>
<br/>

## 🌖 HTTP Header 
### ① General header
요청과 응답에 모두 적용되지만, 데이터와는 관련이 없는 헤더
Date나 Connenction(클라이언트와 서버 간의 연결에 대한 옵션) 등

### ② Request header
요청하는 클라이언트의 대한 자세한 정보를 포함하는 헤더
Host, User-Agent, Cookie 등

### ③ Response header
서버 자체에 대한 정보, 응답에 대한 부가적인 정보를 포함하는 헤더
Server, Allow, ETag, Access-Control-Allow-Origin 등

### ④ Entity header
컨텐츠의 길이나 MIME 타입과 같이 엔티티 바디에 대한 자세한 정보를 포함하는 헤더
Content-Type, Content-Length 처럼 엔티티(콘텐츠, 본문, 리소스) 관련 정보 등

<br/>
<br/>

## 🌙 HTTP Content-type
`Content-type` 은 헤더에 포함되는 속성으로 리소스의 미디어 타입을 나타냄

- Application/x-www-form-urlencoded : HTML Form 형태
- Application/json : JSON 형태 값
- multipart/form-data : 파일 첨부
- text/* : 단순 html, css, javascript 파일

Application/x-www-form-urlencoded 과 form-data 모두 폼데이터이지만,
x-www-form-urlencoded 는 대용량 바이너리를 보내는데 비능률적이다.

<br/>
<br/>

# 📆 HTTP 버전의 역사
### 0.9 (1990~)
- 팀 버너스리 를 통해 개발
- 요청은 단일 라인으로 구성되며 가능한 메서드는 GET
- HTML 파일만 전송 가능

### 1.0 (1996~)
- 요청에 HTTP 버전이 전송 HTTP/1.0
- 요청에 대한 성공과 실패을 알 수 있고, 그 결과에 대한 동작이 가능
- 헤더 도입, 메타데이터 전송을 허용
- 헤더 도입으로 다양한 문서 전송이 가능해졌음

### 1.1 (1999~)
- 장기집권하며 대부분의 웹 환경은 1.1을 따르는 중.
- 파이프 라이닝을 추가하여 첫번째 요청이 전송되기 이전에 두번째 요청을 전송 가능
- 캐시 제어 매커니즘 도입
- 이전 버전의 모호함을 명확하게 하고 많은 개선 사항을 도입함
- SPDY (2012~)
- 구글이 주도적으로 진행
- 클라이언트와 서버간의 데이터 교환을 대체한 수단 실증

### 2.0 (2015~)
- SPDY를 통해서 표준으로 지정.
- 텍스트 프로토콜을 이진 프로토콜로 대체
- 병렬 요청 가능
- 중복돤 요청, 불필요한 오버헤드를 제거, 연속된 요청 사이의 매우 유사한 내용으로 존재하는 헤더를 압축
- server push 라는 매커니즘을 통해 필요하게 될 데이터를 채워놓도록 허용
- stream 방식의 멀티 request처리
- TLS기반



# 참고📚
[위키피디아](https://ko.wikipedia.org/wiki/HTTP)  
[토마의 개발노트 - http 특징](https://toma0912.tistory.com/69)  
[seunghyun90](https://seunghyun90.tistory.com/41)  
[jinbroing](https://jinbroing.tistory.com/63) 
[모든상태코드](https://ko.wikipedia.org/wiki/HTTP_%EC%83%81%ED%83%9C_%EC%BD%94%EB%93%9C)  
[나도개발자시리즈1](http://mixedcode.com/Article/Index?aidx=1054)  
  