..  Python 3 Installation & Setup Guide

.. _reference-python3-Installation:

파이썬 설치 및 환경설정 (Windows)
=============================================

Python은 Python Software Foundation 웹 사이트 https://www.python.org/ 에서 구할 수 있습니다 . 컴퓨터및 운영 체제에 맞는 설치 프로그램을 다운로드 하여 컴퓨터에서 설치해야 합니다.

`Python Documentation : https://docs.python.org/ko/3/ <https://docs.python.org/ko/3/>`_ 에 방문 하여 파이썬에 대하여 알아봅니다.


Python 설치 프로그램 다운로드
---------------------------------

브라우저 창을 열고 `python.org <https://www.python.org/>`_ 에서 ``Windows 용 다운로드 페이지`` https://www.python.org/downloads/windows/  로 이동 합니다.

Python Releases for Windows 화면에서 
Latest Python 3 Release - Python 3.X.X 링크를 클릭 합니다. (이 글을 쓰는 시점에서 최신 것은 Python 3.7.1입니다.)



아래쪽으로 스크롤하여 Windows x86-64 Windows x86-64 executable installer(실행 가능 설치 프로그램 64 비트 용)  
또는 Windows x86 executable installer(x86 실행 설치 프로그램 32 비트 용)을 선택하여 다운로드 합니다.

  Windows의 경우 32 비트 또는 64 비트 설치 프로그램을 선택할 수 있습니다. 두 가지의 차이점은 다음과 같습니다.

  - 시스템에 32 비트 프로세서가있는 경우 32 비트 설치 프로그램을 다운로드해야 합니다.
  - 64 비트 시스템에서는 설치 프로그램이 실제로 대부분의 용도로 작동합니다. 32 비트 버전은 일반적으로 메모리를 적게 사용하지만 집중적인 계산이 필요한 응용 프로그램의 경우 64 비트 버전이 더 잘 수행됩니다.
  - 선택할 버전이 확실하지 않은 경우 64 비트 버전을 다운로드 하십시오.

  .. attention::

     선택을 "잘못"하여 다른 버전의 Python으로 전환하려면 Python을 제거한 다음  다른 설치 프로그램을 다운로드 받아 다시 설치 합니다.


설치 프로그램 실행
------------------------

다운로드 한  설치 프로그램(python-x.x.x.exe)을 선택하고 두 번 클릭하여 실행하십시오. 다음과 같은 대화 상자가 나타납니다.

1) Windows 설치 대화 상자
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: /Media/images/python/01-Install-python-371.png
    :alt: Install python 3.7.1

.. 경로 설정
   
.. Important::

       그림과 같이 Python 3.x를 경로를 추가하는 체크박스를 선택하여 인터프리터(실행 프로그램)가 입력한 경로에 배치되도록 합니다.

	   
2) 옵션 기능 : 기본값으로 설정 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. image:: /Media/images/python/02-Optional-Feature.png
    :alt: Optional Feature


3) 고급 옵션 : 
^^^^^^^^^^^^^^^^^

.. image:: /Media/images/python/03-Advanced-Option.png
    :alt: Advanced Option
       
.. tip::

    그림과 같이 경로를 C:\Python\PythonXXX  와 같이 설정하기를 권장 합니다. (XXX: Python version) 


4) 설치 진행 
^^^^^^^^^^^^^^^^^^^^^^^

.. image:: /Media/images/python/04-setup-progress.png
    :alt: Advanced Option


5) 설치 성공 : 
^^^^^^^^^^^^^^^^^^^^^^^

.. image:: /Media/images/python/05-setup-successfull.png
   :alt: setup successfull
  
   
설치위치 디렉토리로 이동 하여 확인해 봅니다.
   
.. image:: /Media/images/python/06-setup-result.png
   :alt: setup result

   
.. tip::

  - 설치 완료후에 다른 경로에서 파이션 명령어가 실행 되지 않는다면 파이썬 환경 변수를 재설정 해주어야 합니다.
  - 경우에 따라 모듈 설치 프로그램을 업그레이드 할 필요가 있습니다.
 
pip 버전 업그래이드 
::
  
    python -m pip install --upgrade pip 
   
명령 프롬프트(cmd)창을 열어 위와 같이 실행 시킵니다.


파이썬(Python) 환경 변수 재설정
--------------------------------------

환경 변수를 설정 안하고 파이썬을 설치하였거나 환경변수를 재설정하려면 아래를 참고 하세요.


.. raw:: html

    <span title="윈도우즈 시작버튼"><i class="fa fa-windows" ></i></span> 
	
	`윈도우즈 시작` 오른쪽 버튼을 누르면 시스템(Y)이라는 메뉴가 보입니다. 클릭하여 시스템 설정 창을 엽니다 

"시스템 설정 - 정보" 창에서  우측 상단의   관련 설정 "시스템 정보" 메뉴를 클릭하게 되면 "컴퓨터에 대한 기본 정보 보기" 창이 열립니다. 


시스템 속성창 열기
^^^^^^^^^^^^^^^^^^^^^^^

.. image:: /Media/images/windows/11-control-system-system-property.png
   :alt: system property
	
.. sourcecode:: bash

  -그림에서와 같이 "① 고급시스템설정" 을 클릭하면 시스템 속성창이 열립니다.
  -하단의 "② 환경변수 (N)" 버튼을 클릭 합니다.
	
경로가 존재 하지 않으면 '새로 만들기 (N)' 버튼을 클릭하여 아래와 같이 입력 합니다.     
  ::

    -그림에서와 같이 "① 고급시스템설정" 을 클릭하면 시스템 속성창이 열립니다.
    -하단의 "② 환경변수 (N)" 버튼을 클릭 합니다.
	 

환경변수 
^^^^^^^^^

.. image:: /Media/images/windows/12-user-Environment-variable.png
   :alt: Environment variable
	  

현재의 그림과 같이 C:\Python\Python37\Script\;C:\Python\Python37\ 경로가 존재하면 사용자 정의 설치시 생성된 것입니다. 	  

사용자 변수 목록에서	변수 Path 를 선택하고 "편집 (E)" 버튼을 클릭 확인 해봅니다. 

경로가 존재 하지 않으면 '새로 만들기 (N)' 버튼을 클릭하여 아래와 같이 입력 합니다. 

  - 변수이름 : 'PythonPath'  (임의로 작성함)  
  - 변수 값 : 'C:\Python\Python37;C:\Python\Python37\Scripts'  
            (설치한 Python 실행파일 및  스크립트 디렉토리)
  - 각항목을 입력하고 '확인' 버튼을 눌러 저장 합니다.  
   

환경변수 설정 확인
^^^^^^^^^^^^^^^^^^^^^^^ 

  .. image:: /Media/images/windows/13-user-Environment-variable-edit.png
      :alt: Environment variable Edit
	

