.. reStructuredText.rst 파일에서 호출 샘플용

.. _my-figure:

.. figure:: /Media/images/figure-reference.png

   Figure caption
   
   
.. _my-reference-label:

상호 레퍼런스 문법
=======================

상호 레퍼런스는 여러 의미 해석 텍스트 기능에 의해 생성된다. 
기본적으로, role 의 형식을 가지며 target 이라는 이름을 가지는 항목에 링크가 생성된다. 이 때, 링크 텍스트는 target 과 동일하게 표시해 준다.

.. 코멘트

.. sourcecode:: bash

   :ref:`my-figure` figure로 이동 한다
   
   :ref:`my-reference-label`
   
다른파일에서 위의 문법으로 불러서 볼 수 있다. 

:ref:`my-Internal-links` 페이지를 열어 내부 링크 항목을 확인해 보자.
 
