---
layout: post
title:  "[Markdown] 마크다운 한방에 정복하기-IMBETPY"
subtitle:   "The Way to become a data scientist step by step"
categories: communication
tags: what is Markdown ? notion jekyll blog skill dictionary
comments: true
header-img: https://i0.wp.com/jnwhome.iptime.org/wordpress/wp-content/uploads/1/cfile25.uf.236D8D36568A660C1D2202.png?resize=672%2C372 
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
-----


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
-----


## 5. 코드블럭(Code Blocks)
코드를 삽입할 때 사용하며, 백틱(｀)을 세 개 사용하여 작성한다.  
백틱(`) 뒤에 개발언어를 나타내주면 하이라이트가 드러난다.

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
-----

## 6. 링크(Link)
클릭 시 다른페이지로 이동하며, 3가지 다른 유형이 존재합니다.

✏️ 마크다운 CODE
```
<유형1>  
`링크제목 지정` : 
[네이버](https://felix-imbetpy-choi.github.io/ "설명어")  

<유형2>  
`링크URL 노출` : <https://felix-imbetpy-choi.github.io/> 

<유형3>  
`동일파일 링크(목차)` : [목차](##개요)  
```
> __`<유형3> 문단 링크 방법`__  
> 1. 링크 할 제목(header)을 복사,붙여넣기
> 2. `특수문자`제거  
> 3. 스페이스를 갯수만큼 `-`로 변경  
> 4. 대문자->`소문자`로 변경   
> ex) "#목차?  !장점" -> "#목차--장점"  


💻 결과값 Console  

<유형1>  
`링크제목 지정` : 
[네이버](https://felix-imbetpy-choi.github.io/ "설명어")  

<유형2>  
`링크URL 노출` : <https://felix-imbetpy-choi.github.io/> 

<유형3>  
`동일파일 링크(목차)` : [목차](##개요) 


<br/>
<br/>
-----
## 7. 이미지(Image)
마크다운을 사용하여 이미지를 삽입할 땐 사이즈 조절이 불가능하다.    
때문에 사이즈 조절이 필요할 땐 HTML 을 사용한다.  
또한 이미지에 링크를 적용할 수 있다.  

✏️ 마크다운 CODE
```
<유형1> 이미지 삽입
![이미지](https://topclass.chosun.com/news_img/1807/1807_008.jpg "인공지능")
  
<유형2> 이미지 사이즈 조절
<img src="https://topclass.chosun.com/news_img/1807/1807_008.jpg" width="300" height="200"> 

<유형3> 이미지 링크
[![이미지](https://topclass.chosun.com/news_img/1807/1807_008.jpg)](https://felix-imbetpy-choi.github.io/)  
```
> __`<유형3> 문단 링크 방법`__  
> 1. 링크 할 제목(header)을 복사,붙여넣기
> 2. `특수문자`제거  
> 3. 스페이스를 갯수만큼 `-`로 변경  
> 4. 대문자->`소문자`로 변경   
> ex) "#목차?  !장점" -> "#목차--장점"  


💻 결과값 Console  

<유형1>  
`링크제목 지정` : 
[네이버](https://felix-imbetpy-choi.github.io/ "설명어")  

<유형2>  
`링크URL 노출` : <https://felix-imbetpy-choi.github.io/> 

<유형3>  
`동일파일 링크(목차)` : [목차](##개요) 


<br/>
<br/>
-----

- [ ] 운동 하기
- [x] 강의 듣기


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
*  __[4단계] `UML 다이어그램` : 순서도, 흐름도 등을 표현할 때 유용하다.__  
필요시 아래 링크를 참조하기 바란다.
  
> * [Flow charts](http://flowchart.js.org/)
> * [Sequence diagrams](https://bramp.github.io/js-sequence-diagrams/)
  
  
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
