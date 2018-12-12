reStructuredText 사용법
=======================

reStructuredText (reST) 의 개념, 문법에 대한 간단한 소개이며 사용자가 생산적인 문서 작업을 하기에 부족함 없는 정보를 제공한다.
reST는 간편한 마크업 언어로 고안되었으므로 마크다운 문법과 유사하다.

.. seealso::

  `reStructuredText User Documentation <http://docutils.sourceforge.net/rst.html>`_ 는 신뢰할 수 있으며
   이 문서의 "ref" 링크들은 reST 레퍼런스 내부의 개별 구조로 연결되며 영문으로 되어 있다.


일반 서식 (General Format)
---------------------------
   
 .. sourcecode:: bash

   소스 파일의 여러 줄에 걸쳐있는
   단락은 빌드 된 html 파일에는
   한 줄에 표시된다.

   원본 파일은 두 개의 줄 바꿈(enter 2회)을 사용하여
   단락 나누기를 한다.


소스 파일의 여러 줄에 걸쳐있는
단락은 빌드 된 html 파일에는
한 줄에 표시된다.

원본 파일은 두 개의 줄 바꿈(enter 2회)을 사용하여
단락 나누기를 한다.

 .. sourcecode:: bash	

    a *italic* b **bold** c ``literal`` d
   
   
a *italic* b **bold** c ``literal`` d

 .. sourcecode:: bash
	
   a :emphasis:`중요` b :strong:`강하게` c :literal:`정확히`
   d :subscript:`아래첨자` e :superscript:`위첨자` 
   f :title-reference:`표제참조` g

	
a :emphasis:`중요` b :strong:`강하게` c :literal:`정확히`
d :subscript:`아래첨자` e :superscript:`위첨자` 
f :title-reference:`표제참조` g



.. sourcecode:: bash

  .. Translators:  In this code example, do not translate such and such.   
  
   
.. Translators:  In this code example, do not translate such and such.


Escaping with Backslashes
^^^^^^^^^^^^^^^^^^^^^^^^^

.. sourcecode:: bash

   reST에서는 \*, \`, \\와 같이 특별한 의미를 가진 마크업 문자 그 자체를 얻기 위해서
   backslash(``\``)를 사용한다.
   '\\'를 얻고 싶으면 escaped backslash(``\`` \\)를 사용한다.


reST에서는 \*, \`, \\와 같이 특별한 의미를 가진 마크업 문자 그 자체를 얻기 위해서 
backslash(``\``)를 사용한다.
'\\'를 얻고 싶으면 escaped backslash(``\`` \\)를 사용한다.

   
문단 (Paragraphs)
---------------------------

reST 문서에서 가장 기본적인 블럭은 문단(`ref <paragraphs>`)이며 
문단은 간단히 말해 하나 이상의 공백행으로 구별되는 텍스트 뭉치 이다.
파이썬에서와 마찬가지로 reST 에서 들여쓰기는 중요한 요소이다.
따라서 한 단락에 속하는 모든 라인은 동일한 계층에서 들여쓰기가 좌로 정렬되어 있어야 한다.


 
섹션 (Sections)
----------------------

섹션 헤더(ref)는 섹션 제목 아래에 줄을 그으면 생성된다. (경우에 따라 위에도 긋는다.) 최소한 섹션 제목이 되는 텍스트 만큼 길게 그어야 한다.<br>
한글인 경우에는 2배로(한글 갯수만큼 더) 그어야 한다.

* h1: # 윗줄과 함께, 부(parts)에 사용됨.
* h2: * 윗줄과 함께, 장(chapters)에 사용됨.
* h3: =, 섹션에 사용됨.
* h4: -, 하위 섹션에 사용됨.
* h5: ^, 하위 섹션 아래의 하위 섹션에 사용됨.  
* h6: ", 문단에 사용됨


.. sourcecode:: bash

    
    Heading 3
    ==========
    	
    섹션에 사용 한다.
    
    The second level heading in a topic. Use for high-level 
    concepts, tasks, or reference information.
  

   헤더 4
   -------
   
   세 번째 레벨 제목이다. 
   개념 정보를 이해할 수있는 덩어리로 분해하는 데 사용한다.
  
   The 3rd level heading in a topic. 
   Use for breaking down conceptual information into understandable chunks.

   
  
`작성 결과`  

Heading 3
==========

섹션에 사용 한다.


헤더 4
--------

다섯 번째 레벨 제목이다. 
개념 정보를 이해할 수있는 덩어리로 분해하는 데 사용한다.
  
The 3rd level heading in a topic. 
Use for breaking down conceptual information into understandable chunks.

 
  
.. important::
   각 헤더는  네비게이션 메뉴(메뉴명)로 이용 된다.
..




리스트와 유사 인용 블럭 (list and bullets)
------------------------------------------------------

리스트 마크업(ref)도 지원한다. : 적절히 들여쓰고 문단 앞에 별표를 두면 된다.  
번호 리스트도 동일한 방법으로 할 수 있다. # 기호를 사용하면 자동으로 번호가 부여된다

.. sourcecode:: bash

   * 글머리 기호 리스트이다.
   * 두개의 항목이 있으며, 두번째 항목은
     두개의 라인을 사용한다.

   1. 번호 리스트이다.
   2. 여기서도 두개의 항목을 사용했다.

   #. 번호 리스트이다.
   #. 여기서도 두개의 항목을 사용했다.


Then in your ``conf.py``:

* 글머리 기호 리스트이다.
* 두개의 항목이 있으며, 두번째 항목은
  두개의 라인을 사용한다.

1. 번호 리스트이다.
2. 여기서도 두개의 항목을 사용했다.

#. 번호 리스트이다.
#. 여기서도 두개의 항목을 사용했다.



		  
코드블럭 (Codeblock)
-------------------------

- 코드 블록에서 텍스트를 설정하려면 이전 단락을 ::(2 콜론)으로 끝내고 한 줄을 원하는 코드 블록 앞에 넣어 주고 표시 하려는 코드 블록이 첫 번째 콜론(:)위치에서 들여쓰기가 되어 있어야 한다.

	.. sourcecode:: none

		예를 들어, 이것은 예시 단락이다.
		::

		  <p> 이것은 다음에 작성된 코드 블록이다. </ p>
		 
		 
	``작성 결과``
		 
	예를 들어, 이것은 예시 단락이다.
	::

	  <p> 이것은 다음에 작성된 코드 블록이다. </ p>
 


 

- 다른 언어로 표시해야하는 문서의 경우 강조 표시를 직접 지정하는 코드 블록 지시문이 있다.

	rst HTML YAML bash


	* none : 강조 표시 없음
	* python : `highlight_language <http://www.sphinx-doc.org/en/1.5/config.html#confval-highlight_language>`_ 가 설정되지 않은 경우 기본값
	* guess : Pygments가 내용을 기반으로 렉서를 추측하도록하고, 잘 알려진 언어에서 작동한다
	* rest
	* bash

	``bash`` 작성 예시

	.. sourcecode:: bash

	   .. code-block:: bash

		ls
		pwd
		touch a.txt
		
		
	``작성 결괴``
		  
	.. code-block:: bash

		ls
		pwd
		touch a.txt
		
	   


    ``지시문을 이용하여 라인번호 달기``

     .. sourcecode:: bash
 
        .. code-block:: html
           :linenos:

           <html>
            <head>Hello!</head>
            <body>Hello, world!</body>
           </html>

	``작성 결괴``

    .. code-block:: html
       :linenos:

        <html>
          <head>Hello!</head>
          <body>Hello, world!</body>
        </html>
		
		
경고(Admonitions)
------------------

You can use Markdown and reStructuredText in the same Sphinx project.
We support this natively on Read the Docs, and you can do it locally:

attention, caution, danger, error, hint, important, note, tip, warning

.. sourcecode:: rst

   .. note::

      note 지시어 이용
   ..


``지시어`` 바꾸어 준 **결과**:

.. note::

    note 지시어 이용
..

.. attention::

    attention 지시어 이용
..

.. caution::

    caution 지시어 이용
..

.. danger::

    danger 지시어 이용
..


.. error::
    error 지시어 이용
..

.. hint::
    hint 지시어 이용
..
	
.. important::
   important 지시어 이용
..

.. tip::
   tip 지시어 이용
..


.. warning:: 
		 지시어 warning 이용
		 하여 보여준 결과이다
..


.. error


.. reStructuredText-reference.rst 파일에서 호출 샘플용
	
.. _my-Internal-links:


하이퍼 링크 (Hyperlinks)
-------------------------------

**외부 링크**

링크 텍스트가 웹 주소라면 특별한 마크업을 사용하지 않아도 된다. 파서가 텍스트로부터 링크와 메일주소를 찾아낸다.

 
.. sourcecode:: rst

   스핑크스 http://www.sphinx-doc.org/  로 접속 한다.

   `스핑크스(Sphinx) <http://www.sphinx-doc.org/en/master/>`_ 에 접속 한다.

``작성 결과``

스핑크스 http://www.sphinx-doc.org/  로 접속 한다.
  
`스핑크스(Sphinx)  <http://www.sphinx-doc.org/en/master/>`_ 에 접속 한다.

.. important::
    
   링크 텍스트와 URL이 시작되는 < 사이에 반드시 공백이 있어야 한다.

	
**내부 링크**

내부 링크는 Sphinx가 제공하는 특정 reST 기능으로 사용할 수 있다.   아래는 특정 마크업(임의의 위치의 상호 레퍼런스)을 이용한 예시 이다.
  
.. sourcecode:: rst

   :ref:`my-figure` figure로 이동 한다
   
   :ref:`my-reference-label`
  
  
``작성 결과``:

:ref:`my-figure` figure로 이동 한다
  
:ref:`my-reference-label`

.. important:: 
  
  .. _my-figure: <br>
  .. _my-reference-label: <br>
   로 정의되어 있어야 한다. - 다른 파일(.rst)에 정의되어 있어도 된다)
 

비디오 및 HTML 태그 <br> - YouTube videos (and other raw html in rst files)
---------------------------------------------------------------------------------

**iframe 적용 예시**

.. sourcecode:: bash

	.. raw:: html
		<h4>iframe 샘플 </h4>
		<iframe width="100%" height="350" src="https://www.youtube.com/embed/oJsUvBQyHBs?rel=0" frameborder="0" scrolling="no"  allow="autoplay; encrypted-media" allowfullscreen></iframe>


.. raw:: html

	<iframe width="100%" height="350" src="https://www.youtube.com/embed/oJsUvBQyHBs?rel=0" frameborder="0" scrolling="no"  allow="autoplay; encrypted-media" allowfullscreen></iframe>

**embed 적용 예시**
	
.. sourcecode:: bash

	.. raw:: html
       <h4>embed 샘플 </h4>
	   <embed type="text/html" src="http://anys4u.com" width="100%" height="400" style="max-width: 100%; overflow-x: auto; overflow-y: hidden;" > </embed>


.. raw:: html

    <h4>embed 샘플 </h4> 
	<embed type="text/html" src="http://anys4u.com" width="100%" height="400" style="max-width: 100%; overflow-x: auto; overflow-y: hidden;" > </embed>
	<p><small>기본 html 구문 지원 한다.</small></p>
	
	
이미지 Images
-------------------------

이미지는 "image"지시어 또는 "figure"지시어를 사용할 수 있다. 
이미지를 원격으로 연결하는 것은 일반적으로 처음에는 허용되지만 Sphinx에서는 '비 로컬 이미지'경고가 나타난다.

.. sourcecode:: bash

	.. image:: /Media/images/figure-reference.png
	   :width: 300 px

	.. figure:: /Media/images/figure-reference.png
	   
	   그림 제목 



.. image:: /Media/images/figure-reference.png
   :width: 300 px

.. figure:: /Media/images/figure-reference.png
   
   그림 제목 


파일 다운로드 Downloadable files
---------------------------------------

다운로드 가능한 파일은 디렉토리 구조의 어느 위치에나 있을 수 있다. 일반적으로 파일을 참조하는
 .rst 파일과 동일한 디렉토리에 보관하는 것이 가장 쉽다.

.. sourcecode:: bash

   :download:`figure-reference 다운로드 </Media/images/figure-reference.png>`
   
 
:download:`figure-reference 다운로드 </Media/images/figure-reference.png>`

 
각주 (Footnotes)
-------------------

Lorem ipsum [#f1]_ 
dolor sit amet ... [#f2]_

.. rubric:: 각주

.. [#f1] Text of the first footnote.
.. [#f2] Text of the second footnote.
 
 
.. list-table::
   :widths: 25 25 50

 * - Annotation Problem
   -
   - Annotation problems ask students to respond to questions about a
     specific block of text. The question appears above the text when the
     student hovers the mouse over the highlighted text so that students can
     think about the question as they read.
 * - Example Poll
   - Conditional Module
   - You can create a conditional module to control versions of content that
      groups of students see. For example, students who answer "Yes" to a
      poll question then see a different block of text from the students who
      answer "No" to that question.
 * - Example JavaScript Problem
   - Custom JavaScript
   - Custom JavaScript display and grading problems (also called *custom
     JavaScript problems* or *JS input problems*) allow you to create a
     custom problem or tool that uses JavaScript and then add the problem or
     tool directly into Studio.	 
	 
 
 
https://draft-edx-style-guide.readthedocs.io/en/latest/ExampleRSTFile.html
 