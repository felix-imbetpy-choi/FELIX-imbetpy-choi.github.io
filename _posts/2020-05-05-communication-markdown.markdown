---
layout: post
title:  "[Markdown] 마크다운 한방에 정복하기-IMBETPY"
subtitle:   "The Way to become a data scientist step by step"
categories: communication
tags: what is Markdown ? notion jekyll blog skill dictionary
comments: true
header-img: https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Markdown-mark.svg/1920px-Markdown-mark.svg.png  
---
## 개요
> `Markdown` 의 개념과 사용법을 정리 하였습니다.

 목차  
	- [마크다운이란](#마크다운이란)   
	- [마크다운의 장점과 한계](#마크다운의-장점과-한계)  
	- [작성법 - 1. 제목(header)](##1.-제목(header))  
	- [Markdown 문법2(유용한 부가기능)](#markdown-문법2유용한-부가기능)  
	- [실전연습](#실전연습)  
	- [이미지를 쉽게 업로드 하는 방법](#이미지를-쉽게-업로드-하는-방법)  
	- [소소한 Tip 그리고 고장났을 때](#소소한-tip-그리고-고장났을-때)  


# 마크다운이란
> `마크다운(markdown)` 은 읽기 쉽고, 쓰기 쉬운 텍스트 포맷을 사용하여 문서의 양식을 편집하는 문법이다. 이를 통해 작성된 문서는 쉽게 HTML 등 다른 문서 형태로 변환이 가능하다. 
가장 대표적으로 github 에서 작성되는 Readme.md 가 마크다운으로 작성되며, md 가 마크다운의 확장자 이다.

<br/>
<br/>
-----


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
-----


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
-----


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
-----


## 3. 인용문

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
-----


## 4. 폰트스타일 & 줄바꿈

`줄바꿈` 은 문장 마지막에 (spacebar)(spacebar) 2번, (Enter) 를 적용해야 줄이 변경된다.

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


<br/>
<br/>
-----





 

---
*  __[5단계] `강조` : 문장 내 강조하고 싶은 단어를 눈에 띄게__  
  
```
__볼드(진하게)__  
_이탤릭체(기울여서)_    
~~취소선~~  
<u>밑줄</u>  
__볼드로 진하게 만들다가*이탤릭으로 기울이고*다시 볼드로__(중복 활용도 가능하다.)
```
  
__볼드(진하게)__  
_이탤릭체(기울여서)_    
~~취소선~~  
<u>밑줄</u>  
__볼드로 진하게 만들다가*이탤릭으로 기울이고*다시 볼드로__(중복 활용도 가능하다.)  

---
*  __[6단계] `인용구` : 인용할 경우 또는 분위기 전환시에도 사용(중복 형태 가능)__  
  
```
> 위키백과?
>> 중대장 드립 검색
>>> "오늘 중대장은 너희에게 실망했다"
```
  
> 위키백과?
>> 중대장 드립 검색
>>> "오늘 중대장은 너희에게 실망했다"  
  
---
*  __[7단계] `링크(Link)` : 클릭하면 다른 페이지, 다른 부분으로 이동 가능__  
  
```
유형1(`설명어`를 클릭하면 URL로 이동) : [TheoryDB 블로그](https://theorydb.github.io "마우스를 올려놓으면 말풍선이 나옵니다.")  
유형2(URL 보여주고 `자동연결`) : <https://theorydb.github.io>  
유형3(동일 파일 내 `문단 이동`) : [동일파일 내 문단 이동](#markdown의-반드시-알아야-하는-문법)  
```
  
유형1(`설명어`를 클릭하면 URL로 이동) : [TheoryDB 블로그](https://theorydb.github.io "마우스를 올려놓으면 말풍선이 나옵니다.")  
유형2(URL 보여주고 `자동연결`) : <https://theorydb.github.io>  
유형3(동일 파일 내 `문단 이동`) : [동일파일 내 문단 이동](#markdown의-반드시-알아야-하는-문법)  
>__유형3 문단 매칭방법__ : 제목(header)를 복사 붙여넣기 후,  
> 1) `특수문자`제거  
> 2) 스페이스를 갯수만큼 `-`로 변경  
> 3) 대문자->`소문자`로 변경   
> 예) "#Markdown!  장점" -> "#markdown--장점"
  
유형4(상대 경로로 서버 내 파일이동) 기능은 쓸 일이 거의 없어 제외한다.  
  
---
*  __[8단계] `이미지(Image)` : 이미지 보여주기__  
  
```
유형1(`이미지` 삽입) :  
![이미지](https://theorydb.github.io/assets/img/think/2019-06-25-think-future-ai-1.png "인공지능")
  
유형2(`사이즈를 조절`하고 싶은 경우 HTML 태그로 처리) :   
<img src="https://theorydb.github.io/assets/img/think/2019-06-25-think-future-ai-1.png" width="300" height="200"> 

유형3(이미지 삽입 후, `링크 걸기`)
[![이미지](https://theorydb.github.io/assets/img/think/2019-06-25-think-future-ai-1.png)](https://theorydb.github.io/think/2019/06/25/think-future-ai/)  
```
  
유형1(`이미지` 삽입) :  
![이미지](https://theorydb.github.io/assets/img/think/2019-06-25-think-future-ai-1.png "인공지능")
  
유형2(`사이즈를 조절`하고 싶은 경우 HTML 태그로 처리) :   
<img src="https://theorydb.github.io/assets/img/think/2019-06-25-think-future-ai-1.png" width="300" height="200"> 

유형3(이미지 삽입 후, `링크 걸기`)
[![이미지](https://theorydb.github.io/assets/img/think/2019-06-25-think-future-ai-1.png)](https://theorydb.github.io/think/2019/06/25/think-future-ai/)
  
이상 글을 쓸 때 매번 사용하는 Markdown의 문법을 알아보았다. 

## Markdown 문법2(유용한 부가기능)  
---
이 Chapter에서 배울 것들은 위의 기능보다는 사용 빈도가 낮지만 굉장히 고차원 적인 표현을 가능하게 해주는 매우 유용한 문법들이다. 필요할 때마다 참고하여 익히면 큰 도움이 될 것이다.  

---
*  __[1단계] `표(Table)` : 표 그리기__  
  
```
|                  | 수학                        | 평가              |  
|:--- | ---: | :---: |  
| 철수             | 90            | 참잘했어요. |  
| 영희           | 50            | 분발하세요. |
```
  
|                  | 수학                        | 평가              |  
|:--- | ---: | :---: |  
| 철수             | 90            | 참잘했어요. |  
| 영희           | 50            | 분발하세요. |
  
> * 라인 단위로 생각하면서 구분자(`|`)로 열을 구분해주면 위와 같이 대충 그려도 알아서 예쁘게 완성된다.  
> * 헤더(머리글)를 분리하고 싶은 경우, 위 예제와 같이 2번째 라인에 `---`을 사용하면 된다.
> * 정렬이 필요한 경우, 콜론(`:`) 기호를 구분선(`---`) 왼쪽, 오른쪽, 양쪽에 배치한다.      
   
---
*  __[2단계] `수식` : 수학, 논문분석 등에 사용__  
  
```
$$f(x)= if x < x_{min} : (x/x_{min})^a$$  
$$otherwise : 0$$  
$$P(w)=U(x/2)(7/5)/Z$$  
$$p_{\theta}(x) = \int p_{\theta}(2z)p_{\theta}(y\mid k)dz$$  
$$x = argmax_k((x_t-x_u+x_v)^T*x_m)/(||x_b-x_k+x_l||)$$  
```

$$f(x)= if x < x_{min} : (x/x_{min})^a$$  
$$otherwise : 0$$  
$$P(w)=U(x/2)(7/5)/Z$$  
$$p_{\theta}(x) = \int p_{\theta}(2z)p_{\theta}(y\mid k)dz$$  
$$x = argmax_k((x_t-x_u+x_v)^T*x_m)/(||x_b-x_k+x_l||)$$  
  
> * 필자가 사용하는 지킬 테마는 별도 설정없이 위 예제와 같이 자유롭게 사용할 수 있다.   
> * 수식 표현에 제한이 있는 경우, `MathJax` Javascript를 include하여 사용한다.
> ```
> <script type="text/javascript" 
> src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML">
> </script>
> ```
> * 표현형식은 [Latex](https://en.wikibooks.org/wiki/LaTeX/Mathematics) 표기법과 동일하다.
> * 몇가지 예를 들자면, 수식은 `$$`으로 둘러쌓여야 하고 `(),{}`으로 감싸면 우선순위를 고려한 동일 단위로 인식한다.
  
---
*  __[3단계] `코드 블록(Code Block)` : 소스코드, 외부 인용자료 블록처리 등에 사용__  
  
~~~
```python
py_vector = one_hot_encoding("파이",word2index)
py_vector.dot(torch_vector)
>>> 0.0
```
~~~
  
```python
py_vector = one_hot_encoding("파이",word2index)
py_vector.dot(torch_vector)
>>> 0.0
```  
  
> * `뒤에 python이라고 쓰면 python 언어 스타일에 맞게 구문이 강조된다.   
> * 보통 강조하고 싶은 프로그래밍 언어를 그대로 쓰면 된다.  
>   ex) bash, cpp, dockerfile, markdown, yml, html, http, json, r, ruby, xml, sql ... 등
    
---
*  __[4단계] `UML 다이어그램` : 순서도, 흐름도 등을 표현할 때 유용하다.__  
필요시 아래 링크를 참조하기 바란다.
  
> * [Flow charts](http://flowchart.js.org/)
> * [Sequence diagrams](https://bramp.github.io/js-sequence-diagrams/)
  

## 실전연습  
---
자! 이제 Markdown의 거의 모든 문법을 알아보았다. `백견이 불여일타`이므로 반드시 직접 마크다운 문서를 작성해보자.

1. 연습문제1 : 위의 문법 실습을 그대로 타이핑하는 문서 만들기  
2. 연습문제2 : 이 포스팅과 동일한 문서 만들기  
최대한 정답 없이 위에서 배운 문법을 이용하여 본 포스팅과 동일하게 만들어보자.  
성공한다면 앞으로 그 어떤 마크다운 문서 작성도 두렵지 않을 것이다.   

> __`연습문제2` 정답__   
> 1. [필자의 블로그 Github](https://github.com/theorydb/theorydb.github.io)에 접속  
> 2. 우측의 `Clone or download`(녹색버튼) 클릭  
> 3. `/theorydb.github.io-master/_posts/` 폴더 이동  
> 4. `2019-05-22-envops-blog-how-to-use-md.markdown`를 확인 

## 이미지를 쉽게 업로드 하는 방법
이미지를 웹 어디에 저장하는 것이 편리할까? 더불어 포스트 뿐만 아니라 이미지도 마치 데이터베이스 처럼 평생 관리하고 싶다면? 필자가 추천하고 싶은 방식은 크게 3가지이다.  

* __GitHub의 Issue를 이용하는 방법__
  + 일종의 편법인데 GitHub에서 `Issue를 하나 생성`한다.   
    ![이미지1](https://theorydb.github.io/assets/img/envops/2019-07-22-envops-blog-how-to-use-md-1.jpg)
  + Write 탭에 PC에 있는 이미지를 `Drag & Drop`한다. 최종 저장을 안해도 GitHub에 자동으로 업로드가 된다.
    ![이미지2](https://theorydb.github.io/assets/img/envops/2019-07-22-envops-blog-how-to-use-md-2.jpg)
  + 업로드가 다 되면 위 그림과 같은 경로가 생기므로 `해당 URL을 복사해서 사용`한다. 테스트로 복사한 URL로 접속해보았다.
    ![이미지3](https://theorydb.github.io/assets/img/envops/2019-07-22-envops-blog-how-to-use-md-3.jpg)
  + 이 방식은 즉석 URL을 생성하는데는 최고의 방법이나, 대신 이미지를 체계적으로 관리하기가 어렵다. 대신 중요하지 않은 그림은 이 방식으로 운영하면 편리하다고 하겠다. 
  > __쉬어가며__  
  > 저장할지 취소할지 결정되지 않은 작성중인 글에 종속된 이미지를 저장하는 것은 분명 자원 낭비다. 보통 이런 웹프로그램을 개발할 때는 브라우저의 Cache Storage 같은 영역에 임시로 올려두고 글의 저장 요청이 발생하는 순간 같이 전송시켜 I/O 접근을 최소화한다.  
  >  또, 단순히 저장공간 낭비만의 문제가 아니다. 네트워크 사용량이 증가하기 때문이다. 만약 AWS같은 클라우드 인프라 위에 이런 프로그램을 개발한다면 엄청난 네트워크 사용량을 유발하게 되고 속도, 저장 공간 문제를 떠나 네트워크 사용량에 따른 과금 폭탄을 맞게 될 것이다.   
  > 그런데 GitHub이 그걸 몰라서 이렇게 자원을 낭비하는 프로그램을 개발했을까? 원래도 GitHub은 소스 코드부터 이미지까지 무한에 가깝게 업로드 가능한 저장소이다. 더불어 짧은 생각에 GitHub Pages를 운영하는 사람들이 편리하게 이미지 관리를 할 수 있도록 서비스 개념으로 열어두지 않았을까 싶기도 한다. 한 수 더 바라보면 딥러닝 등에 활용하지 않을까 싶기도 하고..  
  > 아무튼 이렇게 계속 퍼주기만 하는 Git 당신은 도대체... 리스펙트 그 이상이다. 

  
* __GitHub를 이용하는 방법__  
  + 필자가 자주 애용하는 방식이다.
  + 예를 들면 `theorydb.github.io\assets\img\`의 위치에 포스트 계층과 동일하게 폴더를 만들어 `포스트 제목-일련번호`의 형태로 파일을 저장한 후, `https://theorydb.github.io/assets/img/think/2019-06-25-think-future-ai-1.png`와 같은 방식으로 링크를 걸어 활용한다.
  + 물론, 이미지 파일 관리에 있어 노가다가 첨가되고 GitHub에 이미지를 먼저 올리지 않으면 Markdown을 작성하며 실시간으로 확인할 수 없다는 불편한 점이 있다.
  + 하지만 필자가 처음 블로그를 개발했을 때 가장 중요했던 목적 하나는 블로그 서비스가 종료되더라도 포스트와 이미지를 개인 DB화 하여 영구 보존하는 것이었기에 큰 불만이 없는 방식이다. 더불어 숙달되어 큰 불편을 느끼지 않는다.

* __기타__
  + 구글드라이브, 플리커, 드랍박스에 이미지를 체계적으로 관리하고 URL을 생성하여 연결하는 것도 한가지 방법이다.
  + 큰 불편함을 느끼지 않아 더 찾아보지는 않았는데 이 부분을 쉽게 처리해 줄 Plug-in이 존재할 것으로 믿는다.ㅎㅎ  
  
## 이미지 만들기 막막할 때
* __간단한 이미지는 `직접` 만들자__    
  간단한 도식이나 관계도를 정도는 쉽게 만들수 있도록 서비스를 제공하는 사이트를 추천해보겠다.
  + 1. [`오토드로우`](https://www.autodraw.com/)   
    정말 자주 애용하는 등장한지 얼마 안된 따끈따끈한 사이트로 강추한다. 마우스로 대충 그리면 그와 유사한 이미지를 AI가 추천하여 선택할 수 있게 해준다.

  + 2. 간단한 그림을 그릴 수 있게 도와주는 사이트 

* __`무료 이미지` 제공 Site__   
  도저히 개인 실력으로 만들 수 없는 고급 퀄리티 이미지는 아래 무료로 제공하는 사이트를 이용하자.
  + <https://pixabay.com/>
  + <https://morguefile.com/>
  + <http://gratisography.com/>
  + <https://unsplash.com/>
  + <http://littlevisuals.co/> 

## 소소한 Tip 그리고 고장났을 때
---
이 부분은 본 포스트에 댓글로 질문이 달릴 경우 하나씩 추가해 나갈 예정이다. 더불어 언제나 통용되는 한가지 해결책을 남긴다. 

* 기능용도로 사용하는 특수문자(\*,\+,\- 등)를 있는 그대로 표현하고 싶은경우 `\` 기호를 앞에 붙이면 된다.
* 마크다운에서 지원하지 않거나 표현하기 어려운 경우 `HTML 태그로 직접 표현`하는 것도 한가지 방법이다. 
  ```
  예를 들어 테마의 특성 때문에 줄바꿈이 잘 되지 않으면,
  줄바꿈을 원하는 문장뒤에 <BR/> 태그를 원하는 라인 수만큼 넣으면 된다. 
  ```


이것으로 Markdown의 사용법 강좌를 마치려한다. 꽤 오랜 시간을 내어 성의를 들여 작성했기에 자주 레퍼런스로 활용해 주시면 감사하겠다. 부족한 점은 댓글로 남겨주시면 보완하겠다.  
