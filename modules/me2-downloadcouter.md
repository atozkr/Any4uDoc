## me2 DownloadsCounter

me2 다운로드카운터는 파일 다운로드 통계를 수집하고 표시하는 Orchard CMS 모듈입니다.
다운로드 카운터는 미디어(file)를 다운로드 할 경우 카운터를 증가 시켜줍니다. 최대 100개의 다운로드 정보를 또한 제공 합니다.  

파일 다운로드 통계를 수집하고 표시합니다.
사용자에 따라 보여주기및 다운로드 권한을 할당 하고 실행 시켜 줍니다.

`:(시작줄),(끝줄)s/찾는패턴/바꿀문자/옵션` 


!!! note
    If the gallery feature has been disabled, there will be no **Gallery** tab visible in the **Themes** or **Modules** dashboard screens.
    To enable the gallery, click **Modules** in the dashboard, find the gallery feature, and then click **Enable** on the feature. 

.. note:: 이것은 note 경고이다.
   이것은 첫문단의 두번째 줄이다.
  
![Enabling Module](../Media/images/modules/orchard.Widgets/modules.png)
> **<i class="fa fa-info-circle"></i> 사용하기:** 모듈릏 사용 하려면 <u>활성화</u> 링크를 클릭하거나 체크한후 실행작업 콤보에서 활성화를 선택하고 ![Enabling Module](../Media/images/buttons/btn-execute.png)버튼을 클릭 합니다.

  
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT 
  

### 활성화 하기

설치하려면 관리자(admin)로 로그인하고 대시보드에서 모듈(Modules)를 선택합니다.
me2 DownloadsCounter 모듈을 찾아 활성화 시킵니다.
파일 미리보기 기능을 사용하려면 쇼파일 사용을 참조 하세요.

![다운로드카운터 활성화](../Media/images/modules/me2.DownloadsCounter/modules.png "다운로드카운터 모듈을 활성화")


다운로드카운터  모듈을 활성화 하려면 활성화를 클릭하거나 체크후  실행작업 콤보에서 활성화를 선택하고 실행 버튼을 클릭 합니다.

다운로드카운터를 사용하려면 내장된 ShowFilePart에서 첨부형 (Attachable) 체크해 주거나 해당 콘텐츠에서 me2.downloadcounter 지원 <u>파일필드(모듈: me2.FileField 설치 필요)</u>를 추가해야 합니다.


![showfile edit](../Media/images/modules/me2.DownloadsCounter/02-downloadcounter-showfile.png "쇼파일 편집")

![showfile edit](../Media/images/modules/me2.DownloadsCounter/03-downloadcounter-showfile-edit.png "쇼파일 편집 저장")

숫자로 지정할 수도 있고(1,10)

문서 전체를 지정할 수도 있다.(.,$)

지금 줄 부터 어디까지 지정할 수도 있다.(.,+10)

`.` 는 문서 시작

`$` 는 문서 마지막

### 옵션

- g: global 
    한 라인에서 패턴이 여러개 존재하면 다 바꾼다.

- i: ignore case
    대소문자 구별을 하지 않는다.

- c: comfirm
    확인하면서 하나씩 바꾼다.






