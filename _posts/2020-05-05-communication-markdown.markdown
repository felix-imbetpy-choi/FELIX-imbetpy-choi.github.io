---
layout: post
title:  "[Markdown] 마크다운 한방에 정복하기-IMBETPY"
subtitle:   "The Way to become a data scientist step by step"
categories: communication
tags: what is Markdown ? notion jekyll blog skill dictionary
comments: true
---
## 개요
> `Markdown` 의 개념과 사용법을 정리 하였습니다.

 목차  
    - [마크다운이란](#마크다운이란)   
    - [마크다운의 장점과 한계](#마크다운의-장점과-한계)  
    - [작성법 - 1. 제목(header)](##1.-제목(header))  
    - [작성법 - 2. 목록(List)](##2.-목록(List))  
    - [작성법 - 3. 인용문(Quote)](##3.-인용문(Quote))  
    - [작성법 - 4. 폰트스타일 & 줄바꿈](##4.-폰트스타일--줄바꿈)  
    - [작성법 - 5. 코드블럭(Code Blocks)](##5.-코드블럭(Code-Blocks))  
    - [작성법 - 6. 링크(Link)](##6.-링크(Link)) 
    - [작성법 - 7. 이미지(Image)](##7.-이미지(Image))   
    - [작성법 - 8. 테이블(Table)](##8.-테이블(Table))   
    - [작성법 - 9. 이모지(Emoji)](##9.-이모지(Emoji))   


---

![이미지](https://steemitimages.com/DQmZoxt18AetawkUVcZX24CZbde9rgQ9gnX1xWFUXTqYAS5/I-love-Markdown.jpg )

# 마크다운이란
> `마크다운(markdown)` 은 읽기 쉽고, 쓰기 쉬운 텍스트 포맷을 사용하여 문서의 양식을 편집하는 문법이다. 이를 통해 작성된 문서는 쉽게 HTML 등 다른 문서 형태로 변환이 가능하다. 
가장 대표적으로 github 에서 작성되는 Readme.md 가 마크다운으로 작성되며, md 가 마크다운의 확장자 이다.

<br/>
<br/>

---


# 마크다운의 장점과 한계
+ ## 장점👍
    1. 문법이 간결하고, 특별한 도구 없이 작성이 가능하다.
    2. 텍스트 파일 형태로 관리가 쉽다. (버전관리 또한 가능)
    3. 여러 플랫폼과 프로그램에서 사용이 가능하다. 
        - 워드프레스(WordPress) 
        - 텀블러(Tumblr) 
        - 레딧(Reddit) 
        - 깃허브(GitHub) 
        - 스택오버플로우(Stack Overflow) 
        - 주피터노트북(Jupyter notebook) 
        - velog 

+ ## 한계👎
    1. 문법이 간결기 때문에, 범위에서 벗어나는 기능은 HTML 을 사용해야 한다.
    2. 표준이 없다. 여러 확장문법이 등장하면서 플랫폼에 따라 작동하지 않는 문법이 있다.
    3. 멀티미디어 삽입이 불편하다. 


<br/>
<br/>

---


# 📌 마크다운 작성법 

## 1. 제목(header)

`h1` 부터 `h6` 까지 표현할 수 있으며, `#` 의 개수에 따라 제목의 크기(계층)을 지정합니다.  

✏️ 마크다운 CODE
```
# h1
## h2
### h3
#### h4
##### h5
###### h6
```

💻 결과값 Console
# h1
## h2
### h3
#### h4
##### h5
###### h6


<br/>
<br/>

---


## 2. 목록(List)

### 2-1. 글머리 목록(Bulleted list)
`순서가 없는 목록` 을 나열할 때 사용하며, `-`, `*`, `+` 로 작성합니다.  
Tab 이나 스페이스바를 이용하여 들여쓰기가 가능합니다.


✏️ 마크다운 CODE
```
+ 1계층
    - 2계층
      * 3계층
        + 4계층
```

💻 결과값 Console
+ 1계층
    - 2계층
      * 3계층
        + 4계층

### 2-2. 번호 목록(Numbered list)
`숫자 목록` 을 나열할 때 사용하며, `숫자`와 `.` 로 작성합니다.  

✏️ 마크다운 CODE
```
1. 첫번째
2. 두번째
3. 세번째
```

💻 결과값 Console
1. 첫번째  
2. 두번째   
3. 세번째   


<br/>
<br/>

---


## 3. 인용문(Quote)

`인용문` 이나 `요약` , `강조` 등을 표현할 때 사용하며,  `>` 로 작성합니다.

✏️ 마크다운 CODE
```
> Who is wise? He that learns from every One. Who is powerful? He that governs his Passions. Who is rich? He that is content. Who is that? Nobody.  
-Benjamin Franklin


> 중첩 1계층
>> 중첩 2계층
>>> 중첩 3계층
```

💻 결과값 Console
> Who is wise? He that learns from every One. Who is powerful? He that governs his Passions. Who is rich? He that is content. Who is that? Nobody.   
-Benjamin Franklin


> 중첩 1계층
>> 중첩 2계층
>>> 중첩 3계층

<br/>
<br/>

---


## 4. 폰트스타일 & 줄바꿈

`줄바꿈` 은 문장 마지막에 (spacebar)(spacebar) 2번, (Enter) 를 적용해야 줄이 변경된다.  
여러줄을 바꾸려면 HTML 태그 `<br/>` 을 사용한다.

✏️ 마크다운 CODE
```
__볼드__   
**볼드**   
_기울임체_  
*기울임체*  
~~취소선~~  
<u>밑줄</u>    
__볼드구역 *이탤릭구역* 볼드구역__  
`인라인코드`

개행
미완료

개행(spacebar)(spacebar)   
완료

개행<br/>
완료
```

💻 결과값 Console  

__볼드__   
**볼드**   
_기울임체_  
*기울임체*  
~~취소선~~  
<u>밑줄</u>    
__볼드구역 *이탤릭구역* 볼드구역__  
`인라인코드`

개행
미완료  

개행(spacebar)(spacebar)   
완료

개행<br/>
완료


<br/>
<br/>

---


## 5. 코드블럭(Code Blocks)
코드를 삽입할 때 사용하며, `백틱(｀)` 을 3개 사용하여 작성한다.  
백틱(`) 뒤에 개발언어를 나타내주면 언어에 맞는 하이라이트가 드러난다.

✏️ 마크다운 CODE
```
```　
백택3개 이상(```)을 위,아래에 작성하면 코드블럭이 만들어진다.
```　
```

```
```java
public static void main(String[] args) {

		int sum1 = 1;
		int sum2 = 2;
		
		int res = sum1 + sum2;
		
		System.out.println(res);
	}
```　
```

💻 결과값 Console  

```
백택3개 이상(```)을 위,아래에 작성하면 코드블럭이 만들어진다.
```

```java
public static void main(String[] args) {

		int sum1 = 1;
		int sum2 = 2;
		
		int res = sum1 + sum2;
		
		System.out.println(res);
	}
```


<br/>
<br/>

---


## 6. 링크(Link)
클릭 시 다른 페이지로 이동하며, 3가지 다른 유형이 존재합니다.

✏️ 마크다운 CODE
```
(유형1)  
`링크제목 지정` : 
[네이버](https://felix-imbetpy-choi.github.io/ "설명어")  

(유형2) 
`링크URL 노출` : <https://felix-imbetpy-choi.github.io/> 

(유형3) 
`동일파일 링크(목차)` : [목차](##개요) 
```

> __`<유형3> 문단 링크 방법`__  
> 1. 링크 할 제목(header)을 복사,붙여넣기
> 2. `특수문자`제거  
> 3. 스페이스를 갯수만큼 `-`로 변경  
> 4. 대문자->`소문자`로 변경   
> ex) "#목차?  !장점" -> "#목차--장점"  



💻 결과값 Console  


(유형1)  
`링크제목 지정` : 
[네이버](https://felix-imbetpy-choi.github.io "설명어")  

(유형2)   
`링크URL 노출` : <https://felix-imbetpy-choi.github.io> 

(유형3)   
`동일파일 링크(목차)` : [목차](##개요)  


<br/>
<br/>

---


## 7. 이미지(Image)
마크다운을 사용하여 `이미지를 삽입`할 땐 사이즈 조절이 불가능하다.    
때문에 `사이즈 조절`이 필요할 땐 `HTML` 을 사용한다.  
또한 이미지에 링크를 적용할 수 있다.  

✏️ 마크다운 CODE
```
(유형1) 이미지 삽입
![이미지](https://topclass.chosun.com/news_img/1807/1807_008.jpg "냐옹이")
  
(유형2) 이미지 사이즈 조절
<img src="https://topclass.chosun.com/news_img/1807/1807_008.jpg" width="300" height="200"> 

(유형3) 이미지 링크
[![이미지](https://topclass.chosun.com/news_img/1807/1807_008.jpg)](https://felix-imbetpy-choi.github.io/)  
```

💻 결과값 Console  

(유형1) 이미지 삽입  
![이미지](https://topclass.chosun.com/news_img/1807/1807_008.jpg "냐옹이")
  
(유형2) 이미지 사이즈 조절  
<img src="https://topclass.chosun.com/news_img/1807/1807_008.jpg" width="300" height="200"> 

(유형3) 이미지 링크  
[![이미지](https://topclass.chosun.com/news_img/1807/1807_008.jpg)](https://felix-imbetpy-choi.github.io/)  


<br/>
<br/>

---


## 8. 테이블(Table)
`표형식` 을 삽입할 때 사용하며, `|` , `:` , `-` 를 통해서 작성한다.  
테이블 헤더를 작성하고, 아래줄에는 구분선(`-`) 과 정렬(`:`) 을 표시한다.  
`:` 를 왼쪽, 양쪽, 오른쪽에 표기하여 왼쪽, 가운데, 오른쪽 정렬을 구현한다.

✏️ 마크다운 CODE
```
| 트레이닝 날짜 | 트레이닝 종류 | 트레이닝 강도 |
|:----------|:----------:|----------:|
| 2020.05.05 | **푸쉬업**, 벤치프레스 | 20*5set, 15*6set |
| 2020.05.07 | _풀업_, 바벨로우, 랫풀다운 | 9*5set, 20*5set, 15*5set,|
| 2020.05.09 | 달리기, 복근운동 | ~~40min~~, 20*5set, |
```

💻 결과값 Console  

| 트레이닝 날짜 | 트레이닝 종류 | 트레이닝 강도 |
|:----------|:----------:|----------:|
| 2020.05.05 | **푸쉬업**, 벤치프레스 | 20*5set, 15*6set |
| 2020.05.07 | _풀업_, 바벨로우, 랫풀다운 | 9*5set, 20*5set, 15*5set,|
| 2020.05.09 | 달리기, 복근운동 | ~~40min~~, 20*5set, |


<br/>
<br/>

---


## 9. 이모지(Emoji)

글과 양식만을 이용해 작성하면 너무 딱딱해 보이기 쉽습니다.  
`윈도우`나 `맥` 에서도 기본적으로 사용할 수 있는 `이모지`를 알아보고,  
`이모지` 를 제공하는 사이트를 소개합니다.  

- 트위터 및 텍스트 이모지 사이트  
https://kr.piliapp.com/twitter-symbols

+ 단축키
    - window10 : `윈도우키` + `마침표(.)`
    - mac : `Command` + `Control` + `스페이스바`

<br/>
<br/>

---



