> **Note:** 이 문서는 Sphinx와 같이 마크다운을 사용하는 문법 입니다.

## 마크다운 문법 (Markdown Syntax) 

Markdown은 Plain text로 작성된 파일(.md)를 HTML로 변경해 보여 주는 매우 쉽고 문서를 간결하게 정히할 수 있는 문법 입니다.


### 헤더 Headings 

제목을 만들려면 `#` 다음에 제목을 작성 합니다. 사용하는 숫자 기호의 수는 제목 수준과 일치해야합니다
HTML의 `<h1>`부터 `<h6>`까지 제목을 표현할 수 있습니다.

* h1: #       부(parts)에 사용됨.
* h2: ##      장(chapters)에 사용됨.
* h3: ###,    페이지 섹션에 사용함.
* h4: ####,   하위 섹션에 사용됨.
* h5: #####,  하위 섹션 아래의 하위 섹션에 사용됨.  
* h6: ######, 문단에 


  
  ``` bash
  
  ### 테스트 제목 3
  
  세 번째 레벨 제목입니다. 
  페이지 섹션에 사용합니다.
    

  ###### 테스트 제목 5

   하위 섹션 아래의 하위 섹션 제목입니다. 
  
  ```

  `작성 결과`
  ### 테스트 제목 3
  
  세 번째 레벨 제목입니다. 
  페이지 섹션에 사용합니다.
    

  ###### 테스트 제목 5

   하위 섹션 아래의 하위 섹션 제목입니다. 
    
________________________________________________________________________

### 기본 서식 (General Format)

   
단락을 만들려면 빈 줄을 사용하여 하나 이상의 텍스트 줄을 분리하십시오. 공백이나 탭으로 단락을 들여서는 안됩니다.   
   
``` bash

   소스 파일의 여러 줄에 걸쳐있는
   단락은 빌드 된 html 파일에는
   한 줄에 표시됩니다.

   원본 파일은 두 개의 줄 바꿈(enter 2회)을 사용하여
   단락 나누기를 합니다.
   
```

소스 파일의 여러 줄에 걸쳐있는
단락은 빌드 된 html 파일에는
한 줄에 표시됩니다.

원본 파일은 두 개의 줄 바꿈(enter 2회)을 사용하여
단락 나누기를 합니다.

________________________________________________________________________

#### 강조 (Emphasis) 


  각각 `<em>`, `<strong>`, `<del>` 태그로 변환됩니다. 
  밑줄을 입력하고 싶다면 `<u>` 태그를 사용하세요.
   
  
  ``` html
  .. note:: ** 강조 작성 구문**

  - 이텔릭체는 *별표(asterisks)* 또는 _언더바(underscore)_를 사용하세요.  
  - 두껍게는 **별표(asterisks)** 또는 __언더바(underscore)__를 사용하세요.  
  - **_이텔릭체_와 두껍게**를 같이 사용할 수 있습니다.  
  - <strike>취소선</strike>은 <s>stike</s> 또는 <del>del</del>를 사용하세요.  
  - <u>밑줄</u>은 `<u></u>`를 사용하세요.

  ```
  
  ``작성 결과`` 

  - 이텔릭체는 *별표(asterisks)* 또는 _언더바(underscore)_를 사용하세요.  
  - 두껍게는 **별표(asterisks)** 또는 __언더바(underscore)__를 사용하세요.  
  - **_이텔릭체_와 두껍게**를 같이 사용할 수 있습니다.  
  - <strike>취소선</strike>은 <s>stike</s> 또는 <del>del</del>를 사용하세요.  
  - <u>밑줄</u>은 `<u></u>`를 사용하세요.
________________________________________________________________________
  

#### 줄바꿈 (Line Breaks)


  문장의 줄바꿈은 거의 작성된 문서에 형식을 따라 갑니다.(즉, “enter”로 줄바꿈 구분함)
  적용이 안될 경우 아래를 참조 합니다.
  
  ``` bash
  동해물과 백두산이 마르고 닳도록 
  하느님이 보우하사 우리나라 만세  
  
  무궁화 삼천리 화려 강산<br>
  대한 사람 대한으로 길이 보전하세

  ```

``결과``

  동해물과 백두산이 마르고 닳도록 
  하느님이 보우하사 우리나라 만세  <!--띄어쓰기 2번-->
  무궁화 삼천리 화려 강산<br>
  대한 사람 대한으로 길이 보전하세

________________________________________________________________________
  
#### 백 슬래시로 이스케이프 처리하기 (Escaping with  Backslashes)

``` bash

   reST에서는 \*, \`, \\와 같이 특별한 의미를 가진 마크업 문자 그 자체를 얻기 위해서
   backslash(``\``)를 사용합니다.
   '\\'를 얻고 싶으면 escaped backslash(``\`` \\)를 사용합니다.

```

마크다운에서는 \*, \`, \\와 같이 특별한 의미를 가진 마크업 문자 그 자체를 얻기 위해서 
backslash(``\``)를 사용합니다.
'\\'를 얻고 싶으면 escaped backslash(``\`` \\)를 사용합니다.
 
________________________________________________________________________
 
### 수평 규칙 (Horizontal Rule)

**3자 이상 ...**

``` none

하이픈 Hyphens

---

별표 Asterisks 

***

밑줄 Underscores  
___


```

`처리 결과` 

하이픈 Hyphens

---

별표 Asterisks 

***

밑줄 Underscores  
___

  
### 코드 블록 (Code blocks)


**코드블록을 문서 중간에 넣으려면 띄어 쓰기로 코드 블록을 삽입 할 수 있습니다**

``` none
1.  파일 열기
2.  21 행에서 다음 코드 블록을 찾으십시오.

        <html>
          <head>
            <title>Test</title>
          </head>

3.  웹 사이트 이름과 일치하도록 제목을 업데이트하십시오.

```

`작성결과`

1.  파일 열기
2.  21 행에서 다음 코드 블록을 찾으십시오.

        <html>
          <head>
            <title>Test</title>
          </head>

3.  웹 사이트 이름과 일치하도록 제목을 업데이트하십시오.


**Syntax highlighting**

  ``` none

    ```css
    	#button {
    		border: none;
    	}
    ``` 

  ```

`작성결과`
```css
	#button {
		border: none;
	}
``` 

**또 다른 방법**

  ``` none

	~~~~
	This is a 
	piece of code 
	in a block
	~~~~

  ```
 
`작성결과`

~~~~
This is a 
piece of code 
in a block
~~~~

________________________________________________________________________________________________


#### 인라인 코드 (Inline code)

``` html
라인 안에 코드를 삽입 하여 보여 줍니다.
`<addr>`요소를 대신 사용하십시오.

```

`처리 결과` 

라인 안에 코드를 삽입 하여 보여 줍니다.
`<addr>`요소를 대신 사용하십시오.

________________________________________________________________________________________________

#### 들여 쓰기 된 코드 (Indented code)

시작행 에서 2자 이상 들여 쓰기를 합니다.

``` html
    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code

```

`처리 결과` 

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code

	

________________________________________________________________________________________________

#### 인용구 (Blockquotes)

인용구는 '>'로 시작되어 중복 사용이 가능 하며   html 'Blockquote'로 대치 됩니다. 
 
``` none

> **<i class="fa fa-exclamation-triangle" aria-hidden="true"></i> 주의:** 이 구문은 마크다운 인용구 문법 입니다.

> *<i class="fa fa-info-circle" aria-hidden="true"></i> 정보:* 이 구문은 마크다운 인용구 문법 입니다.

> **<i class="fa fa-question-circle"></i> 질문:** 
> 질문 답변입니다. 

```

``작성 결과`` 

> **<i class="fa fa-exclamation-triangle" aria-hidden="true"></i> 주의:** 이 구문은 마크다운 인용구 문법 입니다.

> *<i class="fa fa-info-circle" aria-hidden="true"></i> 정보:* 이 구문은 마크다운 인용구 문법 입니다.

> **<i class="fa fa-question-circle"></i> 질문:** 
> 질문 답변입니다. 


인용하고 싶다면 라인 앞에 > 문자를 사용하십시오 :  

``` none

> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.
> * Quoted 1
> * Quoted 2
> * List 1
> * List 2


```  

  
``작성 결과`` 

> Blockquotes can also be nested...
>> ...by using additional greater-than signs right next to each other...
> > > ...or with spaces between arrows.
> * Quoted 1
> * Quoted 2
> * List 1
> * List 2

________________________________________________________________________  


### 목록 (List)
  
  

**번호 매기기 목록**

``` none
1. 첫번째 아이템
2. 두번째 아이템
#. 세번째 아이템
```

`작성결과`

1. 첫번째 아이템
2. 두번째 아이템
#. 세번째 아이템


**블렛 목록**

스타가있는 행을 시작하십시오.

``` none
* 첫번째 아이템
* 스타가있는 행을 시작합니다
* 또는 대시로도 잘 작동합니다
```

`작성결과`

* 첫번째 아이템
* 스타가있는 행을 시작합니다
* 또는 대시로도 잘 작동합니다


**블렛 목록**

``` none

+ `+`,`-` 또는`*`를 사용하여 행을 시작하여 목록을 만들게 됩니다.
+ 하위 목록은 2 칸을 들여서 만들어집니다:
    - 마커 문자 변경으로 새로운 목록 시작:
       * 하위 점이 있다면 대시 또는 별 앞에 두 칸을 놓으십시오.
       + 이어서 테스트
       - 대시는 잘 작동합니다.
+ 매우 쉽습니다!

- Dashes work just as well
- And if you have sub points, put two spaces before the dash or star:
    - 하위
    - 하위 아이템
- 대시는 잘 작동합니다.
- 그리고 하위 점이 있다면 대시 또는 별 앞에 두 칸을 놓으십시오.
```

`작성결과`

+ `+`,`-` 또는`*`를 사용하여 행을 시작하여 목록을 만들게 됩니다.
+ 하위 목록은 2 칸을 들여서 만들어집니다:
    - 마커 문자 변경으로 새로운 목록 시작:
       * 하위 점이 있다면 대시 또는 별 앞에 두 칸을 놓으십시오.
       + 이어서 테스트
       - 대시는 잘 작동합니다.
+ 매우 쉽습니다!



- Dashes work just as well
- And if you have sub points, put two spaces before the dash or star:
    - 하위
    - 하위 아이템
- 대시는 잘 작동합니다.
- 그리고 하위 점이 있다면 대시 또는 별 앞에 두 칸을 놓으십시오.

________________________________________________________________________________________________

### 인라인 HTML (Inline HTML)

마크다운에서 원시 HTML을 사용할 수도 있으며 대부분 잘 작동합니다. *하지만 PDF가 아닌 웹 사이트에만 표시됩니다.*

``` none
<dl>
  <dt>아이템 1 제목</dt>
  <dd>아이템 1 내용 입니다.</dd>

  <dt>아이템 2 제목</dt>
  <dd>아이템 2 내용 입니다.</dd>
</dl>

```

`작성결과`

<dl>
  <dt>아이템 1 제목</dt>
  <dd>아이템 1 내용 입니다.</dd>

  <dt>아이템 2 제목</dt>
  <dd>아이템 2 내용 입니다.</dd>
</dl>

________________________________________________________________________________________________

### 이미지 (Images)

``` none
이미지를 연결 하려면 다음과 같이하십시오.
[Imgur](https://i.imgur.com/4EjEpQX.png)

이미지를 임베드하려면 다음과 같이하십시오.
![Imgur](https://i.imgur.com/Esghlhd.png)

내부용 이미지를 연결하려면 다음과 같이하십시오.
Format: [Alt Text](Media/images/figure-reference.png)

내부용 이미지를 임베드하려면 다음과 같이하십시오.
Format: ![Alt Text](Media/images/figure-reference.png)

```

`작성결과`

이미지를 연결 하려면 다음과 같이하십시오.
[Imgur](https://i.imgur.com/4EjEpQX.png)

이미지를 임베드하려면 다음과 같이하십시오.
![Imgur](https://i.imgur.com/Esghlhd.png)

내부용 이미지를 연결하려면 다음과 같이하십시오.
Format: [Alt Text](/Media/images/figure-reference.png)

내부용 이미지를 임베드하려면 다음과 같이하십시오.
Format: ![Alt Text](/Media/images/figure-reference.png)

내부용 이미지에 링크를 걸려면 다음과 같이하십시오.
[![anys4u](/Media/images/figure-reference.png)](http://anys4u.com/)

________________________________________________________________________________________________

### 링크 (Links)

http://github.com 

``` none

  [anys4u](http://anys4u.com)

  [마크다운 샘플](doc-markdown-sample.html)
  
```

`작성결과`

[anys4u](http://anys4u.com)

[마크다운 샘플](doc-markdown-sample.html)




#### iframe 샘플



.. seealso::

   The authoritative `reStructuredText User Documentation
   <http://docutils.sourceforge.net/rst.html>`_.  The "ref" links in this
   document link to the description of the individual constructs in the reST
   reference.


<iframe width="100%" height="350" src="https://www.youtube.com/embed/oJsUvBQyHBs?rel=0" frameborder="0" scrolling="no"  allow="autoplay; encrypted-media" allowfullscreen></iframe>

  

### Plugins

The killer feature of `markdown-it` is very effective support of
[syntax plugins](https://www.npmjs.org/browse/keyword/markdown-it-plugin).


#### [Emojies](https://github.com/markdown-it/markdown-it-emoji)

> Classic markup: :wink: :crush: :cry: :tear: :laughing: :yum:
>
> Shortcuts (emoticons): :-) :-( 8-) ;)

see [how to change output](https://github.com/markdown-it/markdown-it-emoji#change-output) with twemoji.


#### [Subscript](https://github.com/markdown-it/markdown-it-sub) / [Superscript](https://github.com/markdown-it/markdown-it-sup)

- 19^th^
- H~2~O


#### [\<ins>](https://github.com/markdown-it/markdown-it-ins)

++Inserted text++


#### [\<mark>](https://github.com/markdown-it/markdown-it-mark)

==Marked text==


#### [Footnotes](https://github.com/markdown-it/markdown-it-footnote)

Footnote 1 link[^first].

Footnote 2 link[^second].

Inline footnote^[Text of inline footnote] definition.

Duplicated footnote reference[^second].

[^first]: Footnote **can have markup**

    and multiple paragraphs.

[^second]: Footnote text.





#### Extra

**FONT AWESOME** v.4.7.0

| angle | Center-aligned | Right-aligned | Left-aligned | Center-aligned | Right-aligned |
|     :---:    |     :---:      |     :---:     |     :---:    |     :---:      |     :---:     |
| <i class="fa fa-angle-left"></i>  | git status     | git status    | git status   | git status     | <i class="fa fa-external-link" aria-hidden="true"></i>   |
| <i class="fa fa-angle-right"></i>    | git diff       | git diff      | git diff     | git diff       | <i class="fa fa-cog" aria-hidden="true"></i>     |
| <i class="fa fa-angle-up"></i>   | git status     | git status    | git status   | git status     | git status    |
| <i class="fa fa-angle-down"></i>     | git diff       | git diff      | git diff     | git diff       | git diff      |
| git status   | git status     | git status    | git status   | git status     | git status    |
| git diff     | git diff       | git diff      | git diff     | git diff       | git diff      |







GitHub supports many extras in Markdown that help you reference and link to people. If you ever want to direct a comment at someone, you can prefix their name with an @ symbol: Hey @kneath — love your sweater!

But I have to admit, tasks lists are my favorite:

- [x] This is a complete item
- [ ] This is an incomplete item

When you include a task list in the first comment of an Issue, you will see a helpful progress bar in your list of issues. It works in Pull Requests, too!

And, of course emoji! :sparkles: :camel: :boom:


