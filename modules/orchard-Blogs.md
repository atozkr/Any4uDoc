# 블로그 -Blog

오차드(Orchard)는 웹 사이트에 블로그를 쉽게 추가 할 수있는 블로그 엔진을 제공합니다.  사이트에 새 블로그를 생성하고 블로그에 게시물을 추가하는 방법에 대해 알아 봅니다.


**종속 모듈** Dependencies: 
- Shapes : 오차드에서 Shape(모양)모듈은 HTML이 작성하는 UI(사용자 인터페이스)의 기본 단위입니다.
- Common : common part(공통 부분)는 콘텐츠 항목의 소유자(owner), 생성, 수정 및 게시 날짜를 담고 있습니다. 
- Feeds : 피드 핵심(Feeds core) 모듈은 모듈이 RSS, Atom 또는 다른 유형의 피드를 노출하는 데 사용할 수있는 인프라를 제공합니다.
- Navigation : 탐색메뉴(Navigation) 모듈은 URL을 가리킬 수있는 사용자 정의 항목과 특정 컨텐트 항목을 가리키는 컨텐트 메뉴 항목이 함께 제공됩니다.
- Orchard.Widgets
- Orchard.Resources
- Orchard.PublishLater
- Orchard.Autoroute


## 블로그 모듈 기능 - Blog Module Features

Orchard Blogs 모듈은 기본적인 블로깅 기능을 구현합니다.

* Orchard.Blogs.RemotePublishing: 전용 MetaWeblogAPI-compatible 게시를 사용하여 블로그를  쉽게 원격으로 게시할 수 있습니다.

> 이름: Remote Blog Publishing
> 의존: XmlRpc, Orchard.Autoroute, Orchard.ContentPicker

* Orchard.Blogs.LocalizationExtensions: 완전히 통합 된 다국어 지원으로 오차드 블로그 모듈 확장

> 이름 : Blog multi-language support
> 의존 : Orchard.Localization
 		
![Enabling Module](../Media/images/modules/orchard.blogs/modules.png)
> **<i class="fa fa-info-circle"></i> 사용하기:** 모듈릏 사용 하려면 <u>활성화</u> 링크를 클릭하거나 체크한후 실행작업 콤보에서 활성화를 선택하고 ![Enabling Module](../Media/images/buttons/btn-execute.png)버튼을 클릭 합니다.



## 블로그 추가  - Add the Blog

관리자(admin)로 로그인한 후 대시보드(Dashboard)에서 `블로그(Blog)` 하위 메뉴를 확장하십시오(처음인 경우엔 `블로그(Blog)` 메뉴를 클릭). 그런 다음 새 블로그를 클릭하십시오. 


![Add the Blog](../Media/images/modules/Orchard.blogs/01-addblog.png)

> 새 블로그 화면에서 블로그의 제목, 설명 및 메뉴 텍스트를 추가하고 게시하기 버튼을 누르면 블로그 관리 페이지가 표시 됩니다.
 

## 블로그 관리  - Managing The Blog
 
블로그를 추가하여 입력하고 게시하게 되면 블로그 관리 화면이 나타 납니다.

![Managing The Blog](../Media/images/modules/Orchard.Blogs/02-managingtheblog.png) 

> <span class="info"><i class="fa fa-exclamation-circle" ></i> 참고</span> : <br />동일 사이트에 여러개의  블로그를 추가 할 수 있습니다.
 
 
### 블로그 속성 (Blog Properties)

블로그 속성을 수정하거나 삭제 합니다. 

![Blog Properties](../Media/images/modules/Orchard.blogs/03-blogproperties.png)

> 블로그 이름(제목), 블로그개요(설명), 메뉴명 등을 수정하고 게시 할 수 있습니다.


## 블로그 게시물 추가  - Add a post to the Blog

`새 포스트`를 클릭 하여 새 블로그 게시글 항목을 만듭니다. 새 포스트 화면이 표시되면 게시물의 제목과 게시물의 내용(본문)을 입력합니다


![Add a post](../Media/images/modules/Orchard.blogs/04-blogsAddaPost.png) 
> 태그 필드에 쉼표(comma)로 구분된 태그를 입력 합니다.
댓글를 달게 하려면  Check Show comments , Allow new comments and Allow threaded comments. Click Save to save it as a draft.


### 샘플 블로그 관리  (Managing The Sample Blog)

![Add a post](../Media/images/modules/Orchard.blogs/05-manage-sampleblog.png)
> 게시를 클릭하게 되면 화면에 '<span class="info">Blog Post이(가) 게시되었습니다. The Blog Post has been published.</span>' 메세지를 표시 합니다.
.

 
 
### 블로그 모듈  지원 (Blog Module Support)

문제가 있으면 알려 주시기 바랍니다.
다음 주소에 메일 링리스트가 있습니다. project@google-groups.com

* 개발자 (Author)

	Author: The Orchard Team
	Website: http://orchardproject.net
	Version: 1.10.2
	OrchardVersion: 1.9
	Category: Content
	

* 기부 (Contribute)



* 설치 (Installation)

	<i class="fa fa-link"></i> [ 모듈 기능 활성화 방법](../inx2-modules.html#module-features)을 알아 보십시오.

* 라이센스 (License)

  <del>이 프로젝트는 BSD 라이센스에 따라 라이센스가 부여됩니다.</del>

![Responsive Theme](../Media/images/_blank.png)


