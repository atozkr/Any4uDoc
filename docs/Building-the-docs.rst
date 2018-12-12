.. 외부 파일에서 호출 

.. _reference-building-the-docs:

문서 제작 Building the docs
===================================

`스핑크스(Sphinx)  <http://www.sphinx-doc.org/en/master/>`_ 는 정리된 문서 페이지(html)로 만들어 주는 도구(package) 입니다.

스핑크스 도구를 이용하려면 
 `파이썬(Python) <https://www.python.org/>`_ 이 설치 되어 있어야 합니다.

.. 상호 참조 : /attach/zz-python-install

:ref:`reference-python3-Installation` 방법을 알아 봅니다. 

 
다운로드하여  설치하기 - github.com/atozkr/any4udocs
----------------------------------------------------------------
   
`https://github.com/atozkr/any4udocs <https://github.com/atozkr/atoz>`_ **에서 소스를 다운로드 합니다.**
   
   
압축을 풀면 "~/docs" 폴더가 있읍니다. ``conf.py`` 파일은 스핑크스 구성 설정 파일입니다.
  모듈 설치에 따라 수정 하여 사용 합니다.

압축해제한 후 Any4uDocs 디렉토리는 기본 구조는 아래처럼 되어 있으며 수시로 변경될 수 있습니다. 

  .. code-block:: none

    ├── docs
        ├── _build
        ├── _static
        ├── _templates
        ├── appl
        │      ├── handyweb.md
        │      └── ...	   
        ├── attach
        │      ├── doc-markdown.md
        │      ├── doc-reStructuredText.rst	   
        │      └── ...
        │ 
        ├── Media
        │      ├── images
        │      └── videos
        │
        ├── modules
        │      ├── me2-downloadcouter.md
        │      └── ...
        │		
        ├── themes
        │      ├── response-theme
        │      └── ...
        │		
        ├── conf.py
        ├── index.rst
        ├── ........
        ├── "make.bat"
        └── "makefile"   
	   
	   
 
**명령 프롬프트(cmd)창을 열고 ~/docs 디레토리로 이동 합니다.**
   
#. Sphinx를 설치 합니다.

   `스핑크스(Sphinx)  <http://www.sphinx-doc.org/en/master/>`_  는 Python Documentation Generator 입니다.

   .. code-block:: python
  
      pip install -U Sphinx
	 
   명령 프롬프트(cmd) 창에서 붙여넣기하여 실행 시킵니다.
   
   .. attention::
   
     설치가 안될 경우에는 python 설치가 안되어 있거나 python 경로를 지정 안한 상태 입니다.
     
     :ref:`reference-python3-Installation` 방법을 알아 보고 진행 해야 합니다. 
  
  
   **업그레이드 고려**
   
   .. tip::
   
     You should consider upgrading via the 'python -m pip install --upgrade pip' command.
 
     **다음과 같이 설치 프로그램 업그레이드**
     ::   
  
       python -m pip install --upgrade pip
	    

#. Sphinx에서 마크다운을 사용하려면 `recommonmark <http://www.sphinx-doc.org/en/master/usage/markdown.html>`_ 라는 패키지를 사용해야 합니다.
	
   .. code-block:: python
	 
        pip install recommonmark

   명령 프롬프트(cmd) 창에서 실행 시킵니다.

   .. tip::
   
     마크다운을 사용하지 않으려면 ``conf.py`` 파일을 수정 해야 합니다.
	 
     .. code-block:: rst
	 
       from recommonmark.parser import CommonMarkParser
	 
	 
       source_parsers = {
    
       '.md': 'recommonmark.parser.CommonMarkParser',
       }
       source_suffix = ['.rst', '.md']
	
     위 박스내용을 찾아 내어 제거하고

     .. code-block:: rst	
	 
	    source_suffix = ['.rst']
     
     수정 합니다.	 
	
   
	
#. 이 밖에도 아래의 모듈을 설치 해줍니다. 

   - sphinx-markdown-tables 설치
   
   .. code-block:: python
	 
      pip install sphinx-markdown-tables
 
   - sphinx_sitemap 설치
   
   .. code-block:: python
	 
      pip install sphinx_sitemap
 	
	
#. 테마 바꾸기
  
   서드파트 테마 설치
   ::

      pip install sphinx_rtd_theme
	
	
   명령 프롬프트(cmd) 창에서 실행 시킵니다.
    설치후 ``conf.py`` 파일을 텍스트 에디터로 열어
	
   .. code-block:: none
	 
      html_theme = sphinx_rtd_theme
	
   와 같이 수정하여 줍니다.

	
	
**아래와 같이 오류가 발생할 경우에는**
   
.. error::
   
  Extension error:
  Could not import extension sphinx_sitemap (exception: No module named 'sphinx_sitemap')
 
  **다음과 같이 해결 할 수 있습니다.**
  ::   
  
    pip install sphinx_sitemap 
	   

모듈관련된 오류는 명령 프롬프트(cmd)창에서 ``pip install`` '모듈명'을 입력하고 실행 합니다.
	
**HTML파일을 생성 하려면 'make.bat' 파일를 실행 합니다.**
	   
.. code-block:: bash
	 
	     make html
		  
		  
~/docs/_build/html 디렉토리에 index.htm 외 작성한 페이지가 생성 됩니다. index.html 파일를 열어 확인 합니다.
	   
___
	   
sphinx 설정을 초기화하여 설치
---------------------------------------

'~/docs/' 디렉토리의 폴더및 파일을 삭제하거나 ``conf.py``, ``index.rst``, ``make.bat``, ``makefile`` 파일을 삭제하고 sphinx를 시작 합니다.

#. 명령 프롬프트(cmd) 창을 열고 설치할 디렉토리(혹은 ~/docs/)로 이동 합니다.

   .. code-block:: python
     
	  sphinx-quickstart
	 

#. ``sphinx-quickstart`` 를 실행하고 아래를 참고하여 입력 합니다.

   ====================================================================================   ================
   Prompt                                                                                 Choice
   ====================================================================================   ================
   > Root path for the documentation [.]:                                                 [Enter]
   > Separate source and build directories (y/n) [n]:                                      n 
   > Name prefix for templates and static dir [_]:                                        [Enter]
   > Project name:                                                                         your project
   > Author name(s):                                                                       your name
   > Project release [1.0]:                                                                1.0
   > Project language [en]:                                                                ko
   > Source file suffix [.rst]:                                                           [Enter]
   > Name of your master document (without suffix) [index]:                               [Enter]
   > Do you want to use the epub builder (y/n) [n]:                                        n
   > autodoc: automatically insert docstrings from modules (y/n) [n]:                      y
   > doctest: automatically test code snippets in doctest blocks (y/n) [n]:                n
   > intersphinx: link between Sphinx documentation of different projects (y/n) [n]:       n
   > todo: write "todo" entries that can be shown or hidden on build (y/n) [n]:            n
   > coverage: checks for documentation coverage (y/n) [n]:                                n
   > imgmath: include math, rendered as PNG or SVG images (y/n) [n]:                       y
   > mathjax: include math, rendered in the browser by MathJax (y/n) [n]:                  n
   > ifconfig: conditional inclusion of content based on config values (y/n) [n]:          n
   > viewcode: include links to the source code of documented Python objects (y/n) :       n
   > githubpages: create .nojekyll file to publish the document on GitHub pages (y/n):     n
   > Create Makefile? (y/n) [y]:                                                           y
   > Create Windows command file? (y/n) [y]:                                               y
   ====================================================================================   ================ 

   ``conf.py``, ``index.rst``,  ``makefile`` 파일 등을 생성 합니다.
  
#. 설치 완료후 필요에 따라 ``conf.py`` 파일을 수정및 추가해야 합니다. 

   * 마크다운을 사용 하려면 아래 내용을 conf.py에 추가및 수정하십시오
  
   .. code-block:: python
       :linenos:

        from recommonmark.parser import CommonMarkParser
	  
        source_parsers = {
          '.md': CommonMarkParser,
        }
        source_suffix = ['.rst', '.md']

   * 사용자 정의 CSS 를 적용 하려면 아래 내용을 conf.py에 추가하십시오
  
   .. code-block:: python
       :linenos:
	 
        def setup(app):
           app.add_stylesheet('css/custom.css')
		   
   저장후  .css 파일을 '_static/css/폴더'에 넣습니다.
	  
	  
#. 생성된 ``index.rst`` 파일을 편집기로 열어 적정한 `toctree <https://veranostech.github.io/docs-korean-sphinx/doc/_build/html/markup/toctree_ko.html>`_ 를 삽입 수정 합니다.
 
   .. code-block:: rst
     :linenos:
 
      Contents:

      .. toctree::
      :maxdepth: 2
      :glob:

     *
 

참고 #

- https://pythonhosted.org/an_example_pypi_project/sphinx.html
- http://docutils.sourceforge.net/docs/user/rst/quickref.html
 
- https://veranostech.github.io/docs-korean-sphinx/doc/_build/html/markdown.html  
- https://www.sphinx-doc.org/en/master/usage/markdown.html
  
