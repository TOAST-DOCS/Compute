## Compute > 릴리스 노트

### 2020. 02. 25.
#### Image
* 개인 이미지와 공유받은 이미지가 이미지 목록에 함께 노출되도록 변경
* 신규 이미지 추가 
    * Debian 10.2 Buster(2020.02.18)

* CentOS 6.10(2020.02.18)
    * 이미지 업데이트
* CentOS 7.5(2020.02.18)
    * 이미지 업데이트
* CentOS Linux 6.10 with MySQL 5.6.38(2020.02.18)
    * 이미지 업데이트
* CentOS Linux 6.10 with MySQL 5.7.20(2020.02.18)
    * 이미지 업데이트
* Debian 9.9 Stretch(2020.02.18)
    * 이미지 업데이트
* Ubuntu Server 16.04.2 LTS(2020.02.18)
    * 이미지 업데이트
* Ubuntu Server 18.04.2 LTS(2020.02.18)
    * 이미지 업데이트
* Windows 2012 R2 STD(2020. 02.18)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2012 Standard(2020.02.18)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2014 Standard(2020.02.18)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2016 Express(2020.02.18)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2020.02.18)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2016 STD(2020.02.18)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530689/windows-10-update-kb4530689
* Windows 2016 R2 STD with MS-SQL 2016 Standard(2020.02.18)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530689/windows-10-update-kb4530689
* Windows 2019 STD(2020.02.18)
    * 이미지 업데이트

* 이미지 지원 종료
    * Debian 8.11 Jessie(2019.07.23)

#### System Monitoring
* 이벤트 현황 페이지 개선
    * 각 리전별로 이벤트를 조회할 수 있도록 개선
    * 이벤트 검색 필터 중 상태 항목에 All 옵션 추가
    * 사용자가 직접 이벤트를 종료할 수 있는 **강제 종료** 버튼 추가
* Agent 개선
    * System Monitoring 서버와의 통신 경로 최적화
        * 인터넷 게이트웨이, 보안 그룹 설정과 무관하게 지표 수집 가능
    * CPU, 메모리 사용량 개선

### 2020. 01. 31.
#### Image
* 신규 이미지 추가
    * Windows 2019 STD (2020.01.31)

### 2020. 01. 21.
#### System Monitoring
* 이벤트 조회 페이지 추가
    * 설정한 **감시 설정**에 의해 발생한 이벤트를 조회하는 기능 제공
* 서버 대시보드의 **서버 목록** 기능 개선
    * **Compute > Instance**의 모든 인스턴스를 조회할 수 있도록 개선
    * 인스턴스 상태가 정확하게 표시되도록 개선
* 알림 그룹의 **서버 및 사용자 그룹 연동** 기능 개선
    * 서버 및 사용자 그룹을 선택하고 **저장** 버튼을 클릭해야 변경 사항이 저장되도록 변경

### 2019. 12. 17.
#### Auto Scale
* 인스턴스 템플릿 목록 및 상세 정보에서, 생성할 때 입력한 모든 정보를 볼 수 있도록 수정
    * 목록 테이블: 가용성 영역
    * 상세 정보: 설정한 모든 네트워크 정보, 예약 스크립트 내용

### 2019. 11. 26.
#### Auto Scale
* Auto Scaling 자동 복구
    * Scaling Group에 속한 개별 인스턴스에 네트워크 단절 등의 장애가 발생하면 자동으로 새로운 인스턴스를 생성해 장애가 발생한 인스턴스를 대체하는 기능 추가

#### Instance
* 인스턴스 목록에서 IP를 이용하여 인스턴스를 검색할 때, 일부 특수 문자 입력시 오류가 발생하는 문제 해결

#### System Monitoring
* 서버 대시보드의 인스턴스 검색 기능 개선: 대소문자를 구분하지 않도록 수정


### 2019. 10. 29.
#### Image
* PLOS-WFK-KS-v2.0.60.0.14 (2019.10.22)
    * WF-KS 페이지의 Storage 크기 표기 오류 수정

* Windows 2012 R2 STD (2019.10.22)
    * 언어별 이미지 제공 (KO,EN,JP)
* Windows 2016 STD (2019.10.22)
    * 언어별 이미지 제공 (KO,EN,JP)
* Windows 2012 R2 STD with MS-SQL 2012 Standard (2019.10.22)
    * 언어별 이미지 제공 (KO,EN,JP)
* Windows 2012 R2 STD with MS-SQL 2014 Standard (2019.10.22)
    * 언어별 이미지 제공 (KO,EN,JP)
* Windows 2012 R2 STD with MS-SQL 2016 Express (2019.10.22)
    * 언어별 이미지 제공 (KO,EN,JP)
* Windows 2012 R2 STD with MS-SQL 2016 Standard (2019.10.22)
    * 언어별 이미지 제공 (KO,EN,JP)
* Windows 2016 R2 STD with MS-SQL 2016 Standard (2019.10.22)
    * 언어별 이미지 제공 (KO,EN,JP)

#### System Monitoring
* 사용자 상호작용 UI 개선
    * 사용자 그룹, 감시 그룹, 감시 설정 등 모니터링 정보 조회/추가/수정/삭제 시 로딩 바가 노출되도록 수정
    * 상호작용 중 불필요한 버튼은 비활성화되도록 수정
* 해외 리전 버그 수정
    * 일본, 미국 리전에서 감시 설정을 변경한 서버의 지표 수집이 일시적으로 중단되던 문제 수정
    * 미국 리전에서 사용자 그룹과 감시 그룹의 추가/수정 날짜가 잘못 출력되던 문제 수정

#### VPC
* Default VPC 삭제 기능 추가
    * Default VPC를 사용자가 삭제할 수 있도록 수정

### 2019. 09. 24.
#### System Monitoring
* 웹 콘솔 영어 메시지 지원
* Internet Explorer 11 브라우저 환경에서 서버 대시보드 레이아웃 선택에 실패하던 현상 수정

### 2019. 08. 27.
#### Image
* 이미지 관리 화면에서 공용 이미지 탭이 제거됨

* Windows 2012 R2 STD (2019.08.27)
    * 2019년 7월 10일 보안 업데이트 반영 : https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2012 Standard (2019.08.27)
    * 2019년 7월 10일 보안 업데이트 반영 : https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2014 Standard (2019.08.27)
    * 2019년 7월 10일 보안 업데이트 반영 : https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2016 Express (2019.08.27)
    * 2019년 7월 10일 보안 업데이트 반영 : https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448
* Windows 2012 R2 STD with MS-SQL 2016 Standard (2019.08.27)
    * 2019년 7월 10일 보안 업데이트 반영 : https://support.microsoft.com/en-gb/help/4507448/windows-8-1-update-kb4507448

* Windows 2016 STD (2019.08.27)
    * 2019년 7월 10일 보안 업데이트 반영 : https://support.microsoft.com/en-us/help/4507460/windows-10-update-kb4507460
* Windows 2016 R2 STD with MS-SQL 2016 Standard (2019.08.27)
    * 2019년 7월 10일 보안 업데이트 반영 : https://support.microsoft.com/en-us/help/4507460/windows-10-update-kb4507460

* OS 이미지 지원 종료
    * Windows 2012 R2 STD with MS-SQL 2008 R2 Standard

#### System Monitoring
* 서버 대시보드 차트 조회 성능 개선
* Internet Explorer 11 브라우저 환경 UI 개선

### 2019. 07. 23.
#### System Monitoring
* System Monitoring 서비스 추가
    * 생성된 가상 서버의 시스템 지표 차트를 제공
    * 각 시스템 지표 차트를 원하는 레이아웃으로 구성
    * 지표가 특정 임계치에 도달할 경우 원하는 특정 사용자 그룹에게 알림을 보내도록 설정

### 2019. 06. 25.
#### Instance
* 인스턴스가 구동 중일 때도 이미지를 생성할 수 있도록 수정

### 2019. 05. 28.
#### Auto Scale
* Scaling Group의 사용량을 확인할 수 있는 통계 그래프 추가

#### Image
* CentOS 6.10 (2019.05.28)
    * 리전에 따른 timezone 변경 적용
* CentOS 7.5 (2019.05.28)
    * 리전에 따른 timezone 변경 적용
* Debian 8.11 Jessie (2019.05.28)
    * 리전에 따른 timezone 변경 적용
* Debian 9.9 Stretch (2019.05.28)
    * 리전에 따른 timezone 변경 적용
* Ubuntu Server 16.04.6 LTS (2019.05.28)
    * 리전에 따른 timezone 변경 적용
    * 커널 업데이트 : 4.4.0-142.168
* Ubuntu Server 18.04.2 LTS (2019.05.28)
    * 리전에 따른 timezone 변경 적용

* Debian 9.9 Stretch (2019.05.28)
    * 커널 업데이트 : 4.9.168-1

* Windows 2012 R2 STD (2019.05.28)
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트 : https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2008 R2 Standard (2019.05.28)
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트 : https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2012 Standard (2019.05.28)
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트 : https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2014 Standard (2019.05.28)
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트 : https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2016 Express (2019.05.28)
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트 : https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 R2 STD with MS-SQL 2016 Standard (2019.05.28)
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트 : https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151

* Windows 2016 STD (2019.05.28)
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트 : https://support.microsoft.com/ko-kr/help/4498947/windows-10-update-kb4498947

* 신규 이미지 추가
    * Windows 2016 STD with MS-SQL 2016 Standard (2019.05.28)


### 2019. 05. 14.
#### Image
* CentOS 6.10 with MySQL 5.6.38 (2019.05.14)
    * 이미지 업데이트
* CentOS 6.10 with MySQL 5.7.20 (2019.05.14)
    * 이미지 업데이트

* OS 이미지 지원 종료
    * CentOS 6.5
    * CentOS 7.1
    * Ubuntu 14.04
    * Windows 2008 R2 STD


### 2019. 04. 25.
#### Auto Scale
* 예약 작업 생성 시 타임존 설정 기능 추가

#### Image
* CentOS 6.5 (2019.04.25)
    * yum update 시 발생하는 에러현상 개선
* CentOS 6.10 (2019.04.25)
    * yum update 시 발생하는 에러현상 개선
* CentOS 7.1 (2019.04.25)
    * yum update 시 발생하는 에러현상 개선
    * 시간 동기화 데몬 변경 (ntpd)
* CentOS 7.5 (2019.04.25)
    * yum update 시 발생하는 에러현상 개선
    * 시간 동기화 데몬 변경 (ntpd)

* Windows 2008 R2 STD (2019.04.25)
    * Windows Bootstrap 과정 기능 개선
* Windows 2012 R2 STD (2019.04.25)
    * Windows Bootstrap 과정 기능 개선
* Windows 2016 STD (2019.04.25)
    * Windows Bootstrap 과정 기능 개선
* Windows 2012 R2 STD with MS-SQL 2008 R2 Standard (2019.04.25)
    * Windows Bootstrap 과정 기능 개선
* Windows 2012 R2 STD with MS-SQL 2012 Standard (2019.04.25)
    * Windows Bootstrap 과정 기능 개선
* Windows 2012 R2 STD with MS-SQL 2014 Standard (2019.04.25)
    * Windows Bootstrap 과정 기능 개선
* Windows 2012 R2 STD with MS-SQL 2016 Express (2019.04.25)
    * Windows Bootstrap 과정 기능 개선
* Windows 2012 R2 STD with MS-SQL 2016 Standard (2019.04.25)
    * Windows Bootstrap 과정 기능 개선


### 2019. 03. 26.
#### Image
* CentOS 6.5 (2019.03.26)
    * Bootstrap 과정의 기능 개선
* CentOS 6.10 (2019.03.26)
    * Bootstrap 과정의 기능 개선
* CentOS 7.1 (2019.03.26)
    * Bootstrap 과정의 기능 개선
* CentOS 7.5 (2019.03.26)
    * Bootstrap 과정의 기능 개선
* CentOS 6.5 with MySQL 5.6.38 (2019.03.26)
    * Bootstrap 과정의 기능 개선
* CentOS 6.5 with MySQL 5.7.20 (2019.03.26)
    * Bootstrap 과정의 기능 개선
* Ubuntu Server 14.04.5 LTS (2019.03.26)
    * Bootstrap 과정의 기능 개선
* Ubuntu Server 16.04.5 LTS (2019.03.26)
    * Bootstrap 과정의 기능 개선
* Ubuntu Server 18.04.2 LTS (2019.03.26)
    * Bootstrap 과정의 기능 개선
* Debian 8.11 Jessie (2019.03.26)
    * Bootstrap 과정의 기능 개선
* Debian 9.8 Stretch (2019.03.26)
    * Bootstrap 과정의 기능 개선
    * 커널 업데이트: 4.9.144-3


### 2019. 02. 26.
#### Image
* Ubuntu Server 18.04.2 LTS (2019.02.26)
    * 커널 업데이트 : 4.15.0-45
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 추가 해결


### 2019. 01. 29.
#### Public API
* Instance 생성시 Subnet을 지정할 수 있도록 수정
* Image 조회 API에 pagination을 위한 쿼리 파라미터 추가
* Image 삭제 API 추가


### 2018. 12. 27.

#### Image
* Ubuntu Server 14.04.5 LTS (2018.12.27)
    * shell 상에서 자동완성 (tab) 기능 사용시 LC_CTYPE 관련 warning message 발생 하는 현상 수정
        * default 설정을 "en_US.UTF-8"로 변경
        * /etc/default/locale 수정
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Ubuntu Server 16.04.5 LTS (2018.12.27)
    * shell 상에서 자동완성 (tab) 기능 사용시 LC_CTYPE 관련 warning message 발생 하는 현상 수정
        * default 설정을 "en_US.UTF-8"로 변경
        * /etc/default/locale 수정
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Ubuntu Server 18.04.2 LTS (2018.12.27)
    * shell 상에서 자동완성 (tab) 기능 사용시 LC_CTYPE 관련 warning message 발생 하는 현상 수정
        * default 설정을 "en_US.UTF-8"로 변경
        * /etc/default/locale 수정
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Debian 8.11 Jessie (2019.03.26)
    * shell 상에서 자동완성 (tab) 기능 사용시 LC_CTYPE 관련 warning message 발생 하는 현상 수정
        * default 설정을 "en_US.UTF-8"로 변경
        * /etc/default/locale 수정
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"
* Debian 9.8 Stretch (2019.03.26)
    * shell 상에서 자동완성 (tab) 기능 사용시 LC_CTYPE 관련 warning message 발생 하는 현상 수정
        * default 설정을 "en_US.UTF-8"로 변경
        * /etc/default/locale 수정
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"


### 2018. 12. 11.
#### Image
* 네트워크 인터페이스 또는 Subnet 추가 삭제 시 간헐적으로 발생하는 통신 오류 해결
* Debian 8.11 Jessie (2018.12.11)
    * 커널 업데이트 : 3.16-0-6
* Debian 9.6 Stretch (2018.12.11)
    * 커널 업데이트 : 4.9.0-8

* CentOS 6.5 (2018.12.11)
    * 커널 업데이트 : 2.6.32-754
* CentOS 6.10 (2018.12.11)
    * 커널 업데이트 : 2.6.32-754
* CentOS 7.5 (2018.12.11)
    * 커널 업데이트 : 3.10.0-862
* CentOS 7.1 (2018.12.11)
    * 커널 업데이트 : 3.10.0-693

* Ubuntu Server 18.04.1 LTS (2018.12.11)
    * 커널 업데이트 : 4.15.0-29
* Ubuntu Server 16.04.5 LTS (2018.12.11)
    * 커널 업데이트 : 4.4.0-131
* Ubuntu Server 14.04.5 LTS (2018.12.11)
    * 커널 업데이트 : 4.4.0-31


### 2018. 11. 13.
#### Image
* CentOS 6.5 (2018.11.13)
    * 커널 업데이트 : 2.6.32-754.6.3
    * Yum repository 대상을 최신 repository로 변경
* CentOS 7.1 (2018.11.13)
    * 커널 업데이트 : 3.10.0-693.21.1
    * Yum repository 대상을 최신 repository로 변경

### 2018. 10. 23.
#### Image
* CentOS 7.5 (2018.10.23), CentOS 7.1 (2018.10.23), CentOS 6.10 (2018.10.23), CentOS 6.5 (2018.10.23)
    * 패스워드 복잡도 설정 : 숫자,영문,특문 조합 + 8자리 이상) (/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경 (/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경 (/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한 (/etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료 (/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 CentOS Upstream을 유지함
    * 접근 보안성 강화를 위한 root 계정 접속 제한
        * 기존 : root 계정의 ssh 접속 허용
        * 변경 : 일반 User 계정인 "centos" 로 접속 후 전환
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지

* Ubuntu Server 16.04.5 LTS (2018.10.23)
    * 패스워드 복잡도 설정 : 숫자,영문,특문 조합 + 8자리 이상) (/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경 (/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경 (/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한 ( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료 (/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 Ubuntu Server 16.04 LTS Upstream을 유지함
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지

* Debian 9.5 Stretch (2018.10.23), Debian 8.11 Jessie (2018.10.23)
    * 패스워드 복잡도 설정 : 숫자,영문,특문 조합 + 8자리 이상) (/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경 (/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경 (/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한 ( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료 (/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 Debian 9 Upstream을 유지함
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지


### 2018. 09. 20.
#### Instance
* Instance 관리 화면 UX/UI 개선
    * 인스턴스 이름 조회 기능 추가
    * 가용성 영역, 인스턴스 상태 필터 추가
* Instance 생성 화면 기능 및 UX/UI 개선
    * 플로팅 IP 사용 여부 선택 기능 추가
    * 보안 그룹 생성 및 정책 확인 기능 추가
    * 추가 블록 스토리지 연결 기능 추가
    * 예약 스크립트 등록 기능 추가

#### Image
* 예약스크립트 기능이 정상적으로 적용되지 않는 부분 수정

* Ubuntu Server 18.04.1 LTS (2018.09.20)
    * Kernel 4.15.0-29:  meltdown/spectre variant 1,2,3 (CVE-2017-5753, 5715, 5754) 패치 (retpoline)
    * 패스워드 복잡도 설정 : 숫자,영문,특문 조합 + 8자리 이상) (/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경 (/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경 (/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한 ( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료 (/etc/profile 수정)
        * TMOUT=7200
    * Instance 생성시 swap partition 을 생성하지 않음 (필요시 사용자가 별도 생성)
    * 나머지 설정은 Ubuntu Server 18.04 LTS upstream 을 유지함

* 신규 이미지 추가
    * Ubuntu Linux 14.04.5 (2018.09.20) 추가


### 2018. 08. 09.
#### Image
* Windows 2012 R2 STD (2018.08.09)
    * 한글 사용시 사용자가 한글 언어팩을 설치 (기본으로 영문 버전 제공)
    * 2018년 7월 10일 보안업데이트 : https://support.microsoft.com/en-us/help/4338815/windows-81-update-kb4338815
    * 계정 관리
        * Interactive logon: Display user information when the session is locked : User display name only
        * Interactive logon: Do not display last user name :  Enabled
        * Interactive logon: Prompt user to change password before expiration : 14days
        * Shut down the system : Administrators
    * 서비스 관리
        * NTP 설정 : 1.pool.ntp.org, time,windows.com
        * NTP 동기화 주기 :  256초
    * 시스템 관리
        * Network access: Do not allow anonymous enumeration of SAM accounts : Enabled
        * Network access: Do not allow anonymous enumeration of SAM accounts and shares : Enabled
        * Autologin 기능 제한 :  AutoAdminLogon 값을 0 으로 설정

* Windows 2016 STD (2018.08.09)
    * 2018년 7월 24일 보안 업데이트 : https://support.microsoft.com/en-us/help/4338822/windows-10-update-kb4338822
    * 계정 관리
        * Interactive logon: Display user information when the session is locked : User display name only
        * Interactive logon: Do not display last user name :  Enabled
        * Interactive logon: Prompt user to change password before expiration : 14days
        * Shut down the system : Administrators
    * 서비스 관리
        * NTP 설정 : 1.pool.ntp.org, time,windows.com
        * NTP 동기화 주기 :  256초
    * 시스템 관리
        * Network access: Do not allow anonymous enumeration of SAM accounts : Enabled
        * Network access: Do not allow anonymous enumeration of SAM accounts and shares : Enabled

* Debian 9.4.0 (2018.08.09)
    * Kernel 4.9 업데이트: meltdown/spectre variant 1,2,3 (CVE-2017-5753, 5715, 5754) 패치 (retpoline)
    * 패스워드 복잡도 설정 (숫자,영문,특문 조합 + 8자리 이상) : /etc/pam.d/common-password에 아래 line 추가
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * 불필요 계정/그룹 삭제
        * user : lp, sync, uucp, games
        * group : dip
    * 취약점 대비 커널 파라메터 변경 (sysctl)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4\.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * ssh 설정 변경
        * PermitRootLogin 비활성화
        * /etc/ssh/sshd_config immutable 속성 부여
    * setuid/setgid 제거
        * /usr/bin/chag
        * /usr/bin/gpasswd
        * /usr/bin/wall
        * /usr/bin/chfn
        * /usr/bin/chsh
        * /usr/bin/newgrp
        * /bin/mount
        * /bin/umount
        * /sbin/unix_chkpwd
    * 퍼미션 설정
        * /etc/passwd 644
        * /etc/hosts 644
        * /etc/rsyslog.conf 644
        * /etc/services 644
        * /etc/group 644
        * /etc/shadow 400
        * /etc/gshadow 400
        * /etc/login.defs 400
    * 터미널 접근 제한 : /etc/securetty 수정
    * profile 추가 (/etc/profile)
        * TMOUT=7200      # 터미널로 부터 사용자입력없을때 세선 종료
        * HISTSIZE=500       # history list에 저장될 command 수 제한
        * HISTFILESIZE=0     # history file에 저장될 command 없음
    * 시스템 로그인전 배너 설정 제거
        * /etc/issue, /etc/issue.net 삭제


### 2018. 07. 16.
#### Image
* Windows 2012 R2 STD (2018.07.16)
    * Auto scale 기능으로 백신이 포함된 인스턴스 생성시 발생하는 에러 현상 수정
    * CPU 설정 변경  (CPU Socket 최대 개수  4개)
    * Network  인터페이스 속도  10G로 표시되도록 수정

* Windows 2008 R2 STD (2018.07.16)
    * 2018년 6월 12일자 보안 업데이트 : https://support.microsoft.com/ko-kr/help/4284826
    * 계정 관리
        * Guest 계정 사용 제한 : Guest 계정 사용 안함으로 변경
        * 마지막 사용자 로그인 이름 표시 :  표시 안함으로 설정
        * 세션이 잠긴경우 사용자 정보표시 : 사용자 이름만 표시로 설정
        * 암호만료 전에 변경 알림 : 변경 알림 14일로 설정
        * 일반 사용자의 시스템 종료 제한 : 시스템 종료 정책을 Administrator 로 설정
    * 서비스 관리
        * NTP 설정 : 1.pool.ntp.org, time,windows.com
        * NTP 동기화 주기 :  256초
    * 시스템 관리
        * SAM 계정과 공유의 익명열거 허용 안함 :  SAM 계정관련  익명열거 허용 안함 항목 사용
        * 로그온 하지 않고 시스템 종료허용  제한 :  로그온하지 않고 시스템 종료 허용 정책을 사용 안함으로 설정
        * Autologin 기능 제한 :  AutoAdminLogon 값을 0 으로 설정

* Ubuntu 16.04.4 LTS  (2018.07.16)
    * Kernel 4.4.0-130: meltdown/spectre variant 1,2,3 (CVE-2017-5753, 5715, 5754) 패치 (retpoline)
    * 패스워드 복잡도 설정 (숫자,영문,특문 조합 + 8자리 이상) : /etc/pam.d/common-password에 아래 line 추가
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * 불필요 계정/그룹 삭제
        * user : lp, sync, uucp, games
        * group : dip
    * 취약점 대비 커널 파라메터 변경 (sysctl)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4\.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * ssh 설정 변경
        * PermitRootLogin 비활성화
        * /etc/ssh/sshd_config immutable 속성 부여
    * setuid/setgid 제거
        * /usr/bin/chag
        * /usr/bin/gpasswd
        * /usr/bin/wall
        * /usr/bin/chfn
        * /usr/bin/chsh
        * /usr/bin/newgrp
        * /bin/mount
        * /bin/umount
        * /sbin/unix_chkpwd
    * 퍼미션 설정
        * /etc/passwd 644
        * /etc/hosts 644
        * /etc/rsyslog.conf 644
        * /etc/services 644
        * /etc/group 644
        * /etc/shadow 400
        * /etc/gshadow 400
        * /etc/login.defs 400
    * 터미널 접근 제한 : /etc/securetty 수정
    * profile 추가 (/etc/profile)
        * TMOUT=7200      # 터미널로 부터 사용자입력없을때 세선 종료
        * HISTSIZE=500       # history list에 저장될 command 수 제한
        * HISTFILESIZE=0     # history file에 저장될 command 없음
    * 시스템 로그인전 배너 설정 제거
        * /etc/issue, /etc/issue.net 삭제

### 2018. 05. 29.
#### Auto Scale
* 반복성 예약 작업(cron expression 기반) 관련 오류 수정
    * 반복성 예약 작업 실행 시점이  UTC를 기반으로  동작하는 오류 수정
    * 반복성 예약 작업의 최초 실행이 cron expression을 따르지 않고, 예약 작업 생성 시 설정한 '시작 시각'에 수행되는 오류 수정

#### Instance
* Instance 생성 시 volume type 설정 기능 추가

### 2018.04.24
#### Instance
* Windows 인스턴스 로그 보기 기능 삭제

### 2018. 03. 22.
#### Auto Scale
* Auto Scale 서비스 추가
    * 사용자가 생성한 Instance Template을 바탕으로, Scaling Group을 생성
    * Scaling Group에 속한 인스턴스의 개수를 인스턴스 상태 혹은 예약 작업을 통해 동적으로 관리
    * 자세한 내용은 가이드 문서 참고

### 2018. 02. 22.
#### Instance
* VPC 기능이 추가됨에 따라 인스턴스 생성 시에 서브넷을 지정하도록 변경

#### Image
* Windows 2012 R2 STD (2018.02.22)
    * Windows Time Zone 설정 변경
        * 동기화 주기 변경 : [기존) 604800초 (7일) -> [변경] 256초
        * Time Zone Peer 도메인 변경 : [기존] 1.kr.pool.ntp.org , 1.pool.ntp.org -> [변경] 1.pool.ntp.org , time.windows.com
    * 2018년 2월 13일자 보안 업데이트 : https://support.microsoft.com/ko-kr/help/4074594/windows-81-update-kb-4074594

* Ubuntu Linux 14.04.5 (2018.02.22)
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version : 3.13.0-141
        * Variant 1 (CVE-2017-5753) - patched
        * Variant 3 (CVE-2017-5754) - patched

* Debian Linux 8.2.0 (2018.02.22)
    * 인스턴스 생성시 지정한 이름으로 호스트명 적용되도록 수정
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version : 3.16.0-5
        * Variant 3 (CVE-2017-5754) - patched

* CentOS Linux 6.5 (2018.02.22)
    * 인스턴스 생성시 지정한 이름으로 호스트명 적용되도록 수정
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version : 2.6.32-696.20.1
        * Variant 1 (CVE-2017-5753) - patched
        * Variant 3 (CVE-2017-5754) - patched

* CentOS Linux 7.1 (2018.02.22)
    * 인스턴스 생성시 지정한 이름으로 호스트명 적용되도록 수정
    * Firewall daemon default 값 변경
        * 인스턴스 부팅시 Firewall daemon 자동 시작되지 않도록 설정 변경
    * Swap Disk Mount 설정 변경
        * 신규 인스턴스 생성시 swap 파티션 자동 마운트되도록 설정 변경
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version : 3.10.0-693.17.1
        * Variant 1 (CVE-2017-5753) - patched
        * Variant 3 (CVE-2017-5754) - patched

* 신규 이미지 추가
    * CentOS Linux 6.5 with MySQL 5.6.38 (2018.02.22)
        * MySQL 5.6.38 패키지 설치됨
        * 그외 설정은 CentOS Linux 6.5 이미지와 동일함
    * CentOS Linux 6.5 with MySQL 5.7.20 (2018.02.22)
        * MySQL 5.7.20 패키지 설치됨
        * 그외 설정은 CentOS Linux 6.5 이미지와 동일함


### 2017. 09. 21.
#### Public API
* TOAST Compute 서비스에 대한 API 제공
    * 현재 제한적인 기능만 이용할 수 있으며, 추후 API 추가를 통해 기능 확장 예정
    * 지원되는 API는 가이드 문서 참고

#### Instance
* 키페어를 지정하지 않고 인스턴스를 생성할 수 있었던 버그 수정


### 2017. 07. 20.
#### Image
* 대용량 이미지 생성시 간헐적으로 생성이 완료되지 않던 버그가 수정


### 2017. 08. 24.
#### Instance
* 인스턴스 사양 변경 기능 추가
    * 사용하던 인스턴스의 디스크는 그대로 보존하면서 CPU/Memory를 업그레이드 하거나 다운그레이드 가능
    * 블록 스토리지 크기는 변경 불가
    * 사양 변경을 위해 인스턴스는 종료 상태여야 함
    * 자세한 제약 사항은 가이드 문서 [인스턴스 사양 변경](/Compute/Instance/ko/console-guide/#_14) 참조
* Low IOPS SSD 사양(U 타입)이 추가
    * 합리적인 가격의 저사양 인스턴스 지원
    * Linux 계열 OS만 지원
    * Local Disk를 이용하기 때문에 하드웨어 장애시 데이터 복구가 불가능
* High IOPS SSD 사양(I 타입)이 추가
    * 높은 IOPS를 보장 (보장 IOPS는 가격표 참조)
    * Linux 계열 OS만 지원
* 인스턴스 사용량 조회시 값이 조회되지 않는 버그가 수정


### 2017. 05. 25.
#### Instance
* 서비스 종료된 이미지로 생성된 인스턴스가 조회 되지 않는 버그 수정

#### Image
* Windows 계열 이미지 업데이트
    * Windows 2012 R2 STD (2017.05.25) 추가


### 2017. 04. 25.
#### Instance
* 인스턴스 생성시 초기 불륨 크기의 최대값이 600GB에서 1TB(1000GB)로 변경


### 2017. 03. 23.
#### Instance
* 인스턴스 생성시 초기 볼륨의 크기 지정 기능 추가
    * 사용자가 지정한 크기 만큼 초기 볼륨을 생성
    * 기본 디스크의 크기는 이미지별 최소 요구 사항에서 최대 600GB 까지 설정 가능


### 2017. 01. 19.
#### Instance
* 인스턴스 기본 정보의 IP 주소 정보에서 서브넷 명칭을 제외
    * 명칭 표기로 행의 넓이가 넓어져 가독성이 떨어지는 것을 방지
* 인스턴스 이름 길이 및 특수문자 제한
    * 인스턴스의 이름은 20자 이하 영숫자와 **.** (dot),**-** (dash) 문자만 허용
* 인스턴스 생성 기능을 이미지 생성 기능으로 변경
    * 탭과 일관된 기능으로 변경

#### Image
* 이미지 탭(Private, Shared, Public) 변경시 이미지 선택이 해제되지 않던 문제 수정


### 2016. 12. 22.
#### Instance
* 정지된 인스턴스의 보안 그룹 수정이 가능하도록 변경
* 인스턴스 생성시 선택 가능한 보안 그룹이 하나일 경우 자동 선택되도록 변경
