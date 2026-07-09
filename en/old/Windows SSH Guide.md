<!-- pre-align:aligned sig=922a7c94c93b -->

<a id="infrastructure-compute-network-windows-ssh-guide"></a>
## Infrastructure > Compute & Network > Windows SSH Guide { #infrastructure-compute-network-windows-ssh-guide }

리눅스에 익숙하지 않은 사용자에게 ssh 접속은 낯설기만 합니다. 이 문서는 윈도우즈 ssh 프로그램인 PuTTY를 사용하여 인스턴스 접속하는 방법에 대하여 설명합니다.

<a id="section-1"></a>
## 사용 파일 { #section-1 }

다음 파일 2개를 사용합니다.

- PuTTY 인스톨러: PuTTY와 PuTTYgen 프로그램을 설치 및 사용합니다.
- .pem 파일: 이 파일은 .ppk 변환에 사용합니다.

<a id="putty-puttygen"></a>
## PuTTY, PuTTYgen 설치 { #putty-puttygen }

[그림 1]과 같이 PuTTY 다운로드 페이지에서 [putty-0.xx-installer.exe]를 다운로드 및 설치합니다.  
다운로드링크: http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html

![[그림 1] PuTTY 인스톨러 다운로드](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_1.gif)
<center>[그림 1] PuTTY 인스톨러 다운로드</center>

<a id="ppk"></a>
## ppk 파일 변환 { #ppk }

pem파일은 인스턴스 생성시 만든 파일을 사용합니다.  
(pem파일 생성 방법은 인스턴스 시작하기 참고)  

putty.exe에서는 pem파일을 바로 사용할 수 없으므로 PuTTYgen을 사용하여 ppk 파일로 변환합니다.

```
[Windows] > [모든 프로그램] > [PuTTY] > [PuTTYgen] 실행
[Load] 버튼 클릭
```

![[그림 2] .pem 파일 로드](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_2.gif)
<center>[그림 2] .pem 파일 로드</center>

```
[All Files(.)]로 변경 후 .pem파일 선택
```

![[그림 3] All Files (.) 변경](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_3.gif)
<center>[그림 3] All Files (.) 변경</center>

![[그림 4] Import 완료 메시지](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_4.gif)
<center>[그림 4] Import 완료 메시지</center>

```
[Save private key] 클릭
```

![[그림 5] 개인키 파일(.ppk) 저장](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_5.gif)
<center>[그림 5] 개인키 파일(.ppk) 저장</center>

```
[예(Y)] 클릭
```

![[그림 6] passphrase 건너뜀](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_6.gif)
<center>[그림 6] passphrase 건너뜀</center>

```
파일명 지정 후 [저장] 버튼 클릭
```

<a id="ssh"></a>
## ssh 접속 { #ssh }

```
[Windows] > [모든 프로그램] > [PuTTY] > [PuTTY] 실행
접속할 VM 인스턴스 Host IP 입력
```

![[그림 7] Host IP 입력](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_7.gif)
<center>[그림 7] Host IP 입력</center>

```
[Category] > [Connection] > [SSH] > [Auth] 클릭
[Browse] 버튼 클릭 후 .ppk 파일 선택
[Open] 버튼 클릭
```

![[그림 8] ppk 파일 로딩](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_8.gif)
<center>[그림 8] ppk 파일 로딩</center>

자동로그인을 위하여 사용자명을 넣습니다.

```
[Category] > [Connection] > [Data] 클릭
[Auto-login username]에 root 입력
```

![[그림 9] 자동로그인 사용자명 설정](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_9.gif)
<center>[그림 9] 자동로그인 사용자명 설정</center>

```
[Category] > [Session] 클릭
[Saved Sessions] > [Default Settings] 선택
[Save] 버튼 클릭
[Open] 버튼 클릭
```

![[그림 10] 세션 저장](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_10.gif)
<center>[그림 10] 세션 저장</center>

```
호스트 키를 캐시에 저장하도록 [예] 버튼 클릭
```

![[그림 11] 호스트 키를 캐시에 저장](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_11.gif)
<center>[그림 11] 호스트 키를 캐시에 저장</center>

![[그림 12] 로그인 성공 화면](http://static.toastoven.net/toastcloud/static/common/img/cms_img/infra/putty_12.gif)
<center>[그림 12] 로그인 성공 화면</center>

<a id="section-2"></a>
## 마치며 { #section-2 }

윈도우즈에서 VM인스턴스로 ssh 접속하기 위하여 다음 단계를 순서대로 수행해보았습니다.

- PuTTY, PuTTYgen 설치
- .pem파일을 .ppk파일로 변환
- PuTTY 실행하여 .ppk파일과 Host IP 입력 후 VM 인스턴스 접속
