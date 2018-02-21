## Infrastructure > Compute & Network > Windows SFTP Guide

이 문서는 윈도우즈에서 WinSCP를 이용하여 인스턴스에 데이터를 SFTP로 전송하는 방법에 대하여 설명합니다.

## 사용 파일

다음 파일 2개를 사용합니다.
- WinSCP 인스톨러 : SFTP 전송 프로그램입니다.
- .ppk 파일 : 비밀번호 대신 이 파일을 사용합니다.

> [참고]  
> .ppk파일 생성 방법은 Windows SSH Guide > ppk파일 변환 내용을 참고해 주십시오.

## WinSCP 설치

WinSCP 다운로드 페이지에서 [Installation package] 링크를 클릭하여 다운로드 및 설치합니다.

```
http://winscp.net/eng/download.php#download2 접속
[Installation package] 링크 클릭
```
![](http://static.toastoven.net/toastcloud/static/common/img/cms_img/compute/img_01.jpg)

## 서버 등록

WinSCP를 실행하고 로그인 정보를 등록합니다.

```
좌측 메뉴 [새 사이트] 클릭
[호스트 이름]란에 IP 입력
[사용자 이름]란에 아이디 입력
[고급] 버튼 클릭
```

![](http://static.toastoven.net/toastcloud/static/common/img/cms_img/compute/img_02.jpg)
<center>[그림 1] [호스트 이름], [사용자 이름] 입력 및 [고급] 버튼 클릭</center>

개인키(.ppk) 파일을 등록합니다.

```
좌측 탭에서 [인증]을 선택합니다.
[개인키 파일]란에 [...]을 클릭한 후 .ppk 파일을 선택합니다.
[확인] 버튼을 클릭합니다.
```

![[그림 2] 개인키 파일(.ppk) 등록](http://static.toastoven.net/toastcloud/static/common/img/cms_img/compute/img_03.jpg)
<center>[그림 2] 개인키 파일(.ppk) 등록</center>

서버 로그인 정보를 정합니다.

```
[저장] 버튼을 클릭합니다.
```

![](http://static.toastoven.net/toastcloud/static/common/img/cms_img/compute/img_04.jpg)
<center>[그림 3] [저장] 버튼 클릭</center>

## 서버 접속

좌측 리스트에서 서버를 선택하고 접속합니다.

```
리스트에서 서버 선택
[로그인] 버튼 클릭
```

![](http://static.toastoven.net/toastcloud/static/common/img/cms_img/compute/img_05.jpg)
<center>[그림 4] 사이트 선택 및 [로그인] 버튼 클릭</center>

호스트 키를 캐시에 추가합니다.

```
[예] 버튼 클릭
```

![[그림 5]서버에 연결하고 호스트 키를 캐시에 추가](http://static.toastoven.net/toastcloud/static/common/img/cms_img/compute/img_06.jpg)
<center>[그림 5]서버에 연결하고 호스트 키를 캐시에 추가</center>

호스트 키를 추가를 승인하고 나면 파일 전송이 가능합니다.

![[그림 6] 파일 전송 화면](http://static.toastoven.net/toastcloud/static/common/img/cms_img/compute/img_07.jpg)
<center>[그림 6] 파일 전송 화면</center>

## 마치며

다음과 같이 윈도우즈에서 SFTP 사용하는 방법을 알아보았습니다.

- WinSCP 설치
- .ppk 등록 후 접속
