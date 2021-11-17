## Compute > Release Notes

### November 23, 2021
#### Image
* Supports creating a private image that you can use to create a GPU instance

### October 26, 2021
#### Image Builder
* Image Builder service added
    * Creates a private image by combining an OS image, application installation components, and user scripts

#### System Monitoring

* OpenMetrics Dashboard > Query
    * Changed to allow users to select only up to the date one year ago when selecting a query period.
    * Changed so that guide text regarding data unavailable status or errors is displayed in the chart
* OpenMetrics Dashboard > Add/Modify Charts
    * Changed so that, when the user clicks the **Add** button without selecting any metrics, guide text shows up and the location is highlighted.

### September 14, 2021
#### System Monitoring
- Added new APIs: added APIs to view, add, or delete workspaces and collection targets
- Added @Linux, @Windows default workspaces
    - @Linux: Collects metrics of node exporter installed on an instance. When you create a Linux OS type instance, it is automatically added as the collection target of @Linux.
    - @Windows: Collects metrics of windows exporter installed on an instance. When you create a Windows OS type instance, it is automatically added as the collection target of @Windows.

### July 27, 2021

#### Instance
* Supports creating instances using Instance Template

#### Instance Template
* Instance Template service added
    * Predefines and keeps frequently used instance component information in the form of a template
    * Uses a user-defined template for creating an Instance or Scaling Group

#### Auto Scale
* Instance Template tab removed
    * Scaling Group created using the template made by the Instance Template service
* Added the option of selecting the auto restoration policy option

#### System Monitoring

* Bug fixed: Fixed the problem of selecting ‘There are no entries.’ when adding server of notification group and user group.
* Bug fixed: Fixed the problem of creating more than 5 when creating advanced monitoring layout quickly
* Bug fixed: Fixed the problem of not being able to add other instances with same name to the same port as the collection target in **Advanced Monitoring > Workspace > Collection Target**

### Jun 29, 2021

#### Image

* Node exporter
    * The tool is automatically installed upon creating an instance to support Advanced Monitoring.

* CentOS 7.8(2021. 06. 22.)
    * Image updated
* CentOS 7.8 for NAT(2021. 06. 22.)
    * Image updated
* CentOS 7.8 with MySQL 5.6.38(2021. 06. 22.)
    * Image updated
* CentOS 7.8 with MySQL 5.6.50(2021. 06. 22.)
    * Image updated
* CentOS 7.8 with MySQL 5.7.20(2021. 06. 22.)
    * Image updated
* CentOS 7.8 with MySQL 5.7.32(2021. 06. 22.)
    * Image updated
* CentOS 7.8 with MySQL 8.0.22(2021. 06. 22.)
    * Image updated
* Debian 9.13 Stretch(2021. 06. 22.)
    * Image updated
* Debian 10.9 Buster(2021. 06. 22.)
    * Image updated
* Ubuntu Server 18.04.5 LTS(2021. 06. 22.)
    * Image updated
* Ubuntu Server 18.04.5 LTS for NAT(2021. 06. 22.)
    * Image updated
* Ubuntu Server 18.04.5 LTS with NVIDIA(2021. 06. 22.)
    * Image updated
* Ubuntu Server 20.04.2 LTS(2021. 06. 22.)
    * Image updated
* Windows 2012 R2 STD(2021. 06. 22.)
    * May 2021 security update applied: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003209-monthly-rollup-6be347aa-f8f3-4d26-8260-58d0636f3fe7
* Windows 2016 STD(2021. 06. 22.)
    * May 2021 security update applied: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2019 STD(2021. 06. 22.)
    * May 2021 security update applied: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003171-os-build-17763-1935-3f03e74b-4759-4ca3-b9f1-4bc0d5ab5d27
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2021. 06. 22.)
    * May 2021 security update applied: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003209-monthly-rollup-6be347aa-f8f3-4d26-8260-58d0636f3fe7
* Windows 2016 STD with MS-SQL 2016 Standard(2021. 06. 22.)
    * May 2021 security update applied: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2019 Express(2021. 06. 22.)
    * May 2021 security update applied: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2017 Standard(2021. 06. 22.)
    * May 2021 security update applied: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2019 Standard(2021. 06. 22.)
    * May 2021 security update applied: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2019 STD with MS-SQL 2019 Standard(2021. 06. 22.)
    * May 2021 security update applied: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003171-os-build-17763-1935-3f03e74b-4759-4ca3-b9f1-4bc0d5ab5d27

#### System Monitoring

* Improved OpenMetrics notification group input guide text
* Improved server/agent status tooltip size in server dashboard
* Fixed the problem in which some dropdown menu buttons were displayed abnormally on the event status screen
* Modified the instance name changed in **Compute > Instance** to be reflected in the server list on the server dashboard
* Modified loading bar
* Added API compatible to Prometheus (Beta)


### April 27, 2021

#### Image

* Added new image (Pyeongchon region)
    * CentOS 7.8 for NAT(2021. 04. 22.)
    * Ubuntu Server 18.04.5 LTS for NAT(2021. 04. 22.)
* Image support ended
    * Ubuntu Server 16.04.7 LTS(2020. 12. 22.)

### February 23, 2021

#### Image

* New images added
    * CentOS 7.8 with MySQL 5.6.38(2021. 02. 23.)
    * CentOS 7.8 with MySQL 5.6.50(2021. 02. 23.)
    * CentOS 7.8 with MySQL 5.7.20(2021. 02. 23.)
    * CentOS 7.8 with MySQL 5.7.32(2021. 02. 23.)
    * CentOS 7.8 with MySQL 8.0.22(2021. 02. 23.)

* Image support ended
    * CentOS 6.10(2020. 12. 22.)
    * CentOS 7.5(2020. 12. 22.)
    * CentOS Linux 6.10 with MySQL 5.6.38(2020. 12. 22.)
    * CentOS Linux 6.10 with MySQL 5.7.20(2020. 12. 22.)

* CentOS 7.8(2021. 02. 23.)
    * Image updated

* Linux security vulnerability patch applied
    * Heap-based buffer overflow in Sudo(CVE-2021-3156)
    * Applied when creating a new instance

### January 26, 2021

#### System Monitoring

- Added new feature: Advanced Monitoring (OpenMetrics)
  - Provides the OpenMetrics (Prometheus exposition format) index collection, retrieval, and notification features
  
### December 29, 2020

#### Image
* CentOS 6.10(2020. 12. 22.)
    * Image Update
* CentOS 7.5(2020. 12. 22.)
    * Image Update
* CentOS 7.8(2020. 12. 22.)
    * Image Update
* CentOS Linux 6.10 with MySQL 5.6.38(2020. 12. 22.)
    * Image Update
* CentOS Linux 6.10 with MySQL 5.7.20(2020. 12. 22.)
    * Image Update
* Debian 9.13 Stretch(2020. 12. 22.)
    * Image Update
* Debian 10.7 Buster(2020. 12. 22.)
    * Image Update
* Ubuntu Server 16.04.7 LTS(2020. 12. 22.)
    * Image Update
* Ubuntu Server 18.04.5 LTS(2020. 12. 22.)
    * Image Update
* Ubuntu Server 20.04.1 LTS(2020. 12. 22.)
    * Image Update
* Ubuntu Server 18.04.5 LTS with NVIDIA(2020. 12. 22.)
    * Image Update
* Windows 2012 R2 STD(2020. 12. 22.)
    * November 2020 security updates applied: https://support.microsoft.com/ko-kr/help/4586845/windows-8-1-update
* Windows 2016 STD(2020. 12. 22.)
    * November 2020 security updates applied: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2019 STD(2020. 12. 22.)
    * November 2020 security updates applied: https://support.microsoft.com/ko-kr/help/4586839/windows-10-update-kb4586839
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2020. 12. 22.)
    * November 2020 security updates applied: https://support.microsoft.com/ko-kr/help/4586845/windows-8-1-update
* Windows 2016 STD with MS-SQL 2016 Standard(2020. 12. 22.)
    * November 2020 security updates applied: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2019 Express(2020. 12. 22.)
    * November 2020 security updates applied: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2017 Standard(2020. 12. 22.)
    * November 2020 security updates applied: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2019 Standard(2020. 12. 22.)
    * November 2020 security updates applied: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2019 STD with MS-SQL 2019 Standard(2020. 12. 22.)
    * November 2020 security updates applied: https://support.microsoft.com/ko-kr/help/4586839/windows-10-update-kb4586839

### November 24, 2020

#### Auto Scale
* Added the feature of associating with Deploy

### August 25, 2020

#### Instance
* Added the **Initialize Password** button on the **Windows Instance Access Information** tab.  
* Added the feature of initializing password of original instance when creating a Windows image

#### Image
* Added New Images
    * Cent OS 7.8 (Aug.18,2020)
    * Ubuntu 20.04 LTS (Aug.18,2020)
    * Windows 2016 STD with MS-SQL 2019 Express (Aug.18,2020)
    * Windows 2016 STD with MS-SQL 2017 Standard (Aug.18,2020)
    * Windows 2016 STD with MS-SQL 2019 Standard (Aug.18,2020)
    * Windows 2019 STD with MS-SQL 2019 Standard (Aug.18,2020)

* CentOS 6.10 (Aug.18,2020)
    * Updated image
* CentOS 7.5 (Aug.18,2020)
    * Updated image
* CentOS Linux 6.10 with MySQL 5.6.38 (Aug.18,2020)
    * Updated image
* CentOS Linux 6.10 with MySQL 5.7.20 (Aug.18,2020)
    * Updated image
* Debian 9.9 Stretch (Aug.18,2020)
    * Updated image
* Debian 10.5 Buster (Aug.18,2020)
    * Updated image
* Ubuntu Server 16.04.6 LTS (Aug.18,2020)
    * Updated image
* Ubuntu Server 18.04.4 LTS (Aug.18,2020)
    * Updated image
* Ubuntu Server 18.04.4 LTS with NVIDIA (Aug.18,2020)
    * Updated image
* Windows 2012 R2 STD (Aug.18,2020)
    * Updated image
* Windows 2016 STD (Aug.18,2020)
    * Updated image
* Windows 2019 STD (Aug.18,2020)
    * Updated image
* Windows 2012 R2 STD with MS-SQL 2016 Standard (Aug.18,2020)
    * Updated image
* Windows 2016 STD with MS-SQL 2016 Standard (Aug.18,2020)
    * Updated image

* Closed support for image
    * Windows 2012 R2 STD with MS-SQL 2012 Standard (Feb.18,2020)
    * Windows 2012 R2 STD with MS-SQL 2014 Standard (Feb.18,2020)
    * Windows 2012 R2 STD with MS-SQL 2016 Express (Feb.18,2020)

### June 23, 2020

#### System Monitoring

* Updated chart and legend names to clarify  
* Added detail indications on a chart for items with more details

#### Instance
* Added the feature of querying public keys registered at keypair
* Released the service of creating GPU instances readily on console
* Removed the Delete button from the dialogue box of suspending instances

### May 26, 2020

#### Instance

* Released Public API v2
    * Updated API specifications to be compatible with Openstack
    * Supports Terraform

#### Image

* Released Public API v2
    * Updated API specifications to be compatible with Openstack

### February 25, 2020

#### System Monitoring
* Updates in Event Status Page
    * Updated to query events by each region
    * Added 'All' as status item for event search filters
    * Added the **Forced Stop** button, by which user can  directly close events
* Agent Updates
    * Optimized communication paths with System Monitoring servers
        * Indicators can be collected, regardless of internet gateway or security group settings
    * Upgraded usage volume for CPU and memory


### January 21, 2020

#### System Monitoring
* Added Query Event Page
    * Query events occurred out of surveillance setup
* Updated **Server List** on Server Dashboard
    * Upgraded to query all instances in **Compute > Instance**
    * Updated to show instance status more precisely
* Updated **Server - User Integration** for Alarm Groups
    * Updated to save changes, by selecting a server and user group and clicking the save button


### December 17, 2019

#### Auto Scale
* Updated to show all input data created on the instance template list and detail information
    * List Table: Availability area
    * Detail Information: All configured network data, and script for reservation


### November 26, 2019

#### System Monitoring

##### Feature Updates

* Instance Search Updated on Server Dashboard: No distinction is required between upper and lower cases


### Oct 29, 2019

#### Image
* Application Image

    * Updates
        * PLOS-WFK-KS-v2.0.60.0.14(2019. 10. 22.)
    * Change Details
        * Fixed size error for storage on the WF-KS page

* Common Windows Image

    * Updates
        * Windows 2012 R2 STD(2019. 10. 22.)
        * Windows 2016 STD(2019. 10. 22.)
        * Windows 2012 R2 STD with MS-SQL 2012 Standard(2019. 10. 22.)
        * Windows 2012 R2 STD with MS-SQL 2014 Standard(2019. 10. 22.)
        * Windows 2012 R2 STD with MS-SQL 2016 Express(2019. 10. 22.)
        * Windows 2012 R2 STD with MS-SQL 2016 Standard(2019. 10. 22.)
        * Windows 2016 R2 STD with MS-SQL 2016 Standard(2019. 10. 22.)
    * Change Details
        * Provides images for each language (e.g. KO, EN, JP)

#### System Monitoring

##### Feature Updates
- Updated UI for User Interactions
    - Updated to show the loading bar to search/add/modify/delete monitoring data, including user group, monitoring group, or monitoring setting.
    - Allowed to disable unnecessary buttons for interactions

##### Bug Fixes
- Fixed the error in the Japan and US region, where indicator collecting was temporarily suspended for servers with changed monitoring setting
- Fixed the issue of invalid output of dates for the adding/modifying user/monitoring groups, especially in the US region


### September 24, 2019

#### System Monitoring
- Supports English for web console messages
- Fixed failure in the layout selection for server dashboard on Internet Explorer 11

### August 27, 2019

#### System Monitoring
- Improved performance for the query of charts on server dashboard
- UI improved for the Internet Explorer 11 browser environment

#### Updates
* Removed the common usage tab from the image management page.

### July 23, 2019

#### Release of New Service: System Monitoring

- System metrics are provided on a chart for a newly created virtual server  
- Each chart of system metrics can be configured under a layout of choice; you may set a notification to be sent to a group of particular users via email or SMS, when a metric reaches a specific threshold.

### June 25, 2019

#### Updates

* Image creation is available even when instance is running.

### May 28, 2019

#### Updates

- **KR Region**
- Image Updated for Debian 9 Stretch
  - Image Information
    - Debian 9 Stretch
    - Description: Debian 9.9 Stretch(2019. 05. 28.)
    - Language: EN
    - Bit: 64bit
    - Kernel: 4.9.168-1
  - Feature Updates
    - Kernel updated
    - Minor version updated
- Image Updated for Ubuntu Server 16.04 LTS  
  - Image Information
    - Ubuntu Server 16.04 LTS
    - Description: Ubuntu Server 16.04.6 LTS(2019. 05. 28.)
    - Language: EN
    - Bit: 64bit
    - Kernel: 4.4.0-142.168
  - Feature Updates
    - Kernel updated
  - Minor version updated
- Common Image of Linux CentOS Type
  - Updates
    - CentOS 6.10(2019. 05. 28.)
    - CentOS 7.5(2019. 05. 28.)
    - Debian 8.11 Jessie(2019. 05. 28.)
    - Debian 9.9 Stretch(2019. 05. 28.)
    - Ubuntu Server 16.04.6 LTS(2019. 05. 28.)
    - Ubuntu Server 18.04.2 LTS(2019. 05. 28.)
  - Application
    - Change of timezone according to each region
- Common Image of Windows Type
  - Updates
    - Windows 2012 R2 STD(2019. 05. 28.)
    - Windows 2016 STD(2019. 05. 28.)
    - Windows 2012 R2 STD with MS-SQL 2008 R2 Standard(2019. 05. 28.)
    - Windows 2012 R2 STD with MS-SQL 2012 Standard(2019. 05. 28.)
    - Windows 2012 R2 STD with MS-SQL 2014 Standard(2019. 05. 28.)
    - Windows 2012 R2 STD with MS-SQL 2016 Express(2019. 05. 28.)
    - Windows 2012 R2 STD with MS-SQL 2016 Standard(2019. 05. 28.)
  - Application
    - Change of timezone according to each region
    - Security updated as of May 14, 2019
      - Windows 2012 R2 ( https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151 )
      - Windows 2016 ( https://support.microsoft.com/ko-kr/help/4498947/windows-10-update-kb4498947 )
  - New Release
    - Windows 2016 STD with MS-SQL 2016 Standard(2019. 05. 28.)


### 2019. 05. 14.

#### 기능 개선

* MySQL 이미지 변경
	* CentOS Linux 6.5 with MySQL 5.6.38  > CentOS 6.10 with MySQL 5.6.38(2019. 05. 14.)
	* CentOS Linux 6.5 with MySQL 5.7.20  > CentOS 6.10 with MySQL 5.7.20(2019. 05. 14.)

* OS 이미지 지원 종료
	* CentOS 6.5
	* CentOS 7.1
	* Ubuntu 14.04
	* Windows 2008 R2 STD


### 2019. 04. 25.

#### 기능 개선

* Auto Scaling 예약 작업
	* 예약 작업 생성 시 타임존 설정 기능 추가

* Linux CentOS 계열 공용 이미지
	* 업데이트 이미지 명
		* CentOS 6.5(2019. 04. 25.)
		* CentOS 6.10(2019. 04. 25.)
		* CentOS 7.1(2019. 04. 25.)
		* CentOS 7.5(2019. 04. 25.)
	* 반영내용
		* yum update 시 발생하는 에러현상 개선
		* CentOS 7.X  OS이미지 시간 동기화 데몬 변경 (ntpd)
* Windows 계열 공용 이미지
	* 업데이트 이미지 명
		* Windows 2008 R2 STD(2019. 04. 25.)
		* Windows 2012 R2 STD(2019. 04. 25.)
		* Windows 2016 STD(2019. 04. 25.)
		* Windows 2012 R2 STD with MS-SQL 2008 R2 Standard(2019. 04. 25.)
		* Windows 2012 R2 STD with MS-SQL 2012 Standard(2019. 04. 25.)
		* Windows 2012 R2 STD with MS-SQL 2014 Standard(2019. 04. 25.)
		* Windows 2012 R2 STD with MS-SQL 2016 Express(2019. 04. 25.)
		* Windows 2012 R2 STD with MS-SQL 2016 Standard(2019. 04. 25.)
	* 반영 내용
		* Windows Bootstrap 과정 기능 개선


### 2019. 03. 26.

#### 기능 개선

* Debian 9 Stretch 이미지 업데이트
	* 이미지 정보
		* Debian 9 Stretch
		* 설명 : Debian 9.8 Stretch(2019. 03. 26.)
		* 언어 : EN
		* 비트 : 64bit
		* 커널 : 4.9.144-3
	* 기능 개선
		* 커널 업데이트

* 리눅스 계열 이미지 공통 적용
	* 업데이트 이미지 이름
		* CentOS 7.1(2019. 03. 26.)
		* CentOS 7.5(2019. 03. 26.)
		* CentOS 6.10(2019. 03. 26.)
		* CentOS 6.5(2019. 03. 26.)
		* Ubuntu Server 18.04.2 LTS(2019. 03. 26.)
		* Ubuntu Server 16.04.5 LTS(2019. 03. 26.)
		* Ubuntu Server 14.04.5 LTS(2019. 03. 26.)
		* Debian 9.8 Stretch(2019. 03. 26.)
		* Debian 8.11 Jessie(2019. 03. 26.)
		* CentOS 6.5 with MySQL 5.6.38(2019. 03. 26.)
		* CentOS 6.5 with MySQL 5.7.20(2019. 03. 26.)

	* 반영내용
		* Bootstrap 과정의 기능 개선

### 2019. 02. 26.

#### 기능 개선

* Ubuntu Server 18.04 LTS 이미지 업데이트
    * 이미지 정보
        * Ubuntu Server 18.04 LTS
        * 설명 : Ubuntu Server 18.04.2 LTS(2019. 02. 26.)
        * 언어 : EN
        * 비트 : 64bit
        * 커널 : 4.15.0-45
    * 기능 개선
        * 커널 업데이트 ( 4.15.0-29 -> 4.15.0-45 )
        * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 추가 해결


### 2019.01.29

#### 기능 개선

* Public API 변경
  * Instance 생성시 Subnet을 지정할 수 있도록 수정
  * Image 조회 API에 pagination을 위한 쿼리 파라미터 추가
  * Image 삭제 API 추가

### 2018. 12. 27.

#### 기능 개선

* Ubuntu Server 18.04 LTS 이미지 업데이트
* Ubuntu Server 16.04 LTS 이미지 업데이트
* Ubuntu Server 14.04 LTS 이미지 업데이트
* Debian 9 Stretch 이미지 업데이트
* Debian 8 Jessie 이미지 업데이트
* (공통) 이미지 업데이트 변경 내용
    * 현상
        * shell 상에서 자동완성 (tab) 기능 사용시 LC_CTYPE 관련 warning message 발생
    * 원인
        * 설치되지 않은 "ko_KR.UTF-8"로 설정됨
    * 수정
        * default 설정을 "en_US.UTF-8"로 변경
        * /etc/default/locale 수정
            * LC_ALL="en_US.UTF-8"
            * LC_CTYPE="en_US.UTF-8"


### 2018. 12. 11.

#### 기능 개선

* 이미지 업데이트 관련 주요 변경 사항 요약
    * 이미지 공통 기능개선
        * 네트워크 인터페이스 또는 Subnet 추가 삭제 시 간헐적으로 발생하는 통신 오류 해결
    * Debian 9 Stretch OS 커널 업데이트

* Debian 9 Stretch 이미지 업데이트
    * 이미지 정보
        * Debian 9 Stretch
        * 설명 : Debian 9.6 Stretch(2018. 12. 11.)
        * 언어 : EN
        * 비트 : 64bit
        * 커널 : 4.9.0-8
    * 기능 개선
        * 커널 업데이트 :  기존 4.9.0-7 > 변경 4.9.0-8
        * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결

* Debian 8 Jessie 이미지 업데이트
    * 이미지 정보
        * Debian 8 Jessie
        * 설명 : Debian 8.11 Jessie(2018. 12. 11.)
        * 언어 : EN
        * 비트 : 64bit
        * 커널 : 3.16-0-6
    * 기능 개선
        * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결

* CentOS 7.5 이미지 업데이트
    * 이미지 정보
        * CentOS 7.5
        * 설명 : CentOS 7.5(2018. 12. 11.)
        * 언어 : EN
        * 비트 : 64bit
        * 커널 : 3.10.0-862
    * 기능 개선
        * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결

* CentOS 7.1 이미지 업데이트
    * 이미지 정보
        * CentOS 7.1
        * 설명 : CentOS 7.1(2018. 12. 11.)
        * 언어 : EN
        * 비트 : 64bit
        * 커널 : 3.10.0-693
    * 기능 개선
        * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결

* CentOS 6.10 이미지 업데이트
    * 이미지 정보
        * CentOS 6.10
        * 설명 : CentOS 6.10(2018. 12. 11.)
        * 언어 : EN
        * 비트 : 64bit
        * 커널 : 2.6.32-754
    * 기능 개선
        * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결

* CentOS 6.5 이미지 업데이트
    * 이미지 정보
        * CentOS 6.5
        * 설명 : CentOS 6.5(2018. 12. 11.)
        * 언어 : EN
        * 비트 : 64bit
        * 커널 : 2.6.32-754
    * 기능 개선
        * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결

* Ubuntu Server 18.04 LTS 이미지 업데이트
    * 이미지 정보
        * Ubuntu Server 18.04 LTS
        * 설명 : Ubuntu Server 18.04.1 LTS(2018. 12. 11.)
        * 언어 : EN
        * 비트 : 64bit
        * 커널 : 4.15.0-29
    * 기능 개선
        * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결

* Ubuntu Server 16.04 LTS 이미지 업데이트
    * 이미지 정보
        * Ubuntu Server 16.04 LTS
        * 설명 : Ubuntu Server 16.04.5 LTS(2018. 12. 11.)
        * 언어 : EN
        * 비트 : 64bit
        * 커널 : 4.4.0-131
    * 기능 개선
        * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결

* Ubuntu Server 14.04 LTS 이미지 업데이트
    * 이미지 정보
        * Ubuntu Server 14.04 LTS
        * 설명 : Ubuntu Server 14.04.5 LTS(2018. 12. 11.)
        * 언어 : EN
        * 비트 : 64bit
        * 커널 : 4.4.0-31
    * 기능 개선
        * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결


### 2018. 11. 13.

#### 기능 개선

* CentOS 7.1 이미지 업데이트
    * 이미지 정보
        * CentOS 7.1
        * 언어 : EN
        * 설명 : CentOS 7.1(2018. 11. 13.)
        * 비트 : 64bit
        * 커널 : 3.10.0-693.21.1
    * 커널 업데이트 :  3.10.0-229 -> 3.10.0-693.21.1
    * Yum repository target 변경 : CentOS 최신 repo
* CentOS 6.5 이미지 업데이트
    * 이미지 정보
        * CentOS 6.5
        * 언어 : EN
        * 설명 : CentOS 6.5(2018. 11. 13.)
        * 비트 : 64bit
        * 커널 : 2.6.32-754.6.3
    * 커널 업데이트 :  2.6.32-431 -> 2.6.32-754.6.3
    * Yum repository target 변경 : CentOS 최신 repo

### 2018. 10. 23.

#### 기능 개선

* 이미지 업데이트 관련 주요 변경 사항 요약
    * 신규 이미지 릴리즈 : CentOS 7.5 , CentOS 6.10
    * 인스턴스 생성시 OS Swap Partition을 기본으로 설정하지 않음.
    * CentOS 인스턴스 ssh 접근시 root 계정 접속 허용 에서 일반 계정 "centos" 접속 후 root 전환으로 변경
* CentOS 7.5 신규 이미지 업데이트
    * 이미지 정보
        * CentOS 7.5
        * 언어 : EN
        * 설명 : CentOS 7.5(2018. 10. 23.)
        * 비트 : 64bit
        * 커널 : 3.10.0-862.14.4.el7
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
        * 나머지 설정은 CentOS Upstream을 유지함
    * 기능개선
        * 접근 보안성 강화를 위한 root 계정 접속 제한
            * 기존 : root 계정의 ssh 접속 허용
            * 변경 : 일반 User 계정인 "centos" 로 접속 후 전환
        * 인스턴스 생성시 swap partition 을  생성하지 않음
        * /etc/hosts 파일의 사용자 추가 설정 유지
* CentOS 6.10 신규 이미지 업데이트
    * 이미지 정보
        * CentOS 6.10
        * 언어 : EN
        * 설명 : CentOS 6.10(2018. 10. 23.)
        * 비트 : 64bit
        * 커널 : 2.6.32-754.3.5.el6
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
        * 나머지 설정은 CentOS Upstream을 유지함
    * 기능개선
        * 접근 보안성 강화를 위한 root 계정 접속 제한
            * 기존 : root 계정의 ssh 접속 허용
            * 변경 : 일반 User 계정인 "centos" 로 접속 후 전환
        * 인스턴스 생성시 swap partition 을  생성하지 않음
        * /etc/hosts 파일의 사용자 추가 설정 유지
* CentOS 7.1 이미지 업데이트
    * 이미지 정보
        * CentOS 7.1
        * 언어 : EN
        * 설명 : CentOS 7.1(2018. 10. 23.)
        * 비트 : 64bit
        * 커널 : 3.10.0-229.el7
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
        * 나머지 설정은 CentOS Upstream을 유지함
    * 기능개선
        * 접근 보안성 강화를 위한 root 계정 접속 제한
            * 기존 : root 계정의 ssh 접속 허용
            * 변경 : 일반 User 계정인 "centos" 로 접속 후 전환
        * 인스턴스 생성시 swap partition 을  생성하지 않음
        * /etc/hosts 파일의 사용자 추가 설정 유지
* CentOS 6.5 이미지 업데이트
    * 이미지 정보
        * CentOS 6.5
        * 언어 : EN
        * 설명 : CentOS 6.5(2018. 10. 23.)
        * 비트 : 64bit
        * 커널 : 2.6.32-431.el6
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
        * 나머지 설정은 CentOS Upstream을 유지함
    * 기능개선
        * 접근 보안성 강화를 위한 root 계정 접속 제한
            * 기존 : root 계정의 ssh 접속 허용
            * 변경 : 일반 User 계정인 "centos" 로 접속 후 전환
        * 인스턴스 생성시 swap partition 을  생성하지 않음
        * /etc/hosts 파일의 사용자 추가 설정 유지
* Ubuntu Server 16.04 LTS 이미지 업데이트
    * 이미지 정보
        * Ubuntu Server 16.04 LTS
        * 언어 : EN
        * 설명 : Ubuntu Server 16.04.5 LTS(2018. 10. 23.)
        * 비트 : 64bit
        * 커널 : 4.4.0-131
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
    * 기능개선
        * 인스턴스 생성시 swap partition 을  생성하지 않음
        * /etc/hosts 파일의 사용자 추가 설정 유지
* Ubuntu Server 14.04 LTS 이미지 업데이트
    * 이미지 정보
        * Ubuntu Server 14.04 LTS
        * 언어 : EN
        * 설명 : Ubuntu Server 14.04.5 LTS(2018. 10. 23.)
        * 비트 : 64bit
        * 커널 : 4.4.0-131
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
        * 나머지 설정은 Ubuntu Server 14.04 LTS Upstream을 유지함
    * 기능개선
        * 인스턴스 생성시 swap partition 을  생성하지 않음
        * /etc/hosts 파일의 사용자 추가 설정 유지
* Debian 9 Stretch 이미지 업데이트
    * 이미지 정보
        * Debian 9 Stretch
        * 언어 : EN
        * 설명 : Debian 9.5 Stretch(2018. 10. 23.)
        * 비트 : 64bit
        * 커널 : 4.9.0-7
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
    * 기능개선
        * 인스턴스 생성시 swap partition 을  생성하지 않음
        * /etc/hosts 파일의 사용자 추가 설정 유지
* Debian 8 Jessie 이미지 업데이트
    * 이미지 정보
        * Debian 8 Jessie
        * 언어 : EN
        * 설명 : Debian 8.11 Jessie(2018. 10. 23.)
        * 비트 : 64bit
        * 커널 : 3.16.0-6
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
        * 나머지 설정은 Debian 8 Upstream을 유지함
    * 기능개선
        * 인스턴스 생성시 swap partition 을  생성하지 않음
        * /etc/hosts 파일의 사용자 추가 설정 유지


### 2018. 09. 20.

#### 기능 개선

* Instance 관리 화면 UX/UI가 개선되었습니다.
    * 인스턴스 이름 조회 기능 추가
    * 가용성 영역, 인스턴스 상태로 필터 추가
* Instance 생성 화면 기능 및 UX/UI가 개선되었습니다.
    * 플로팅 IP 사용 여부 선택 기능 추가
    * 보안 그룹 생성 및 정책 확인 기능 추가
    * 추가 블록 스토리지 연결 기능 추가
    * 예약 스크립트 등록 기능 추가
* Ubuntu Server 18.04 LTS 신규 이미지 업데이트
    * 이미지 정보
        * Ubuntu Server 18.04 LTS
        * 언어 : EN
        * 설명 : Ubuntu Server 18.04.1 LTS(2018. 09. 20.)
        * 비트 : 64bit
    * Kernel 4.15.0-29
        * meltdown/spectre variant 1,2,3 (CVE-2017-5753, 5715, 5754) 패치 (retpoline)
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
        * 추가 변경 사항
            * Instance 생성시 swap partition 을 생성하지 않음 ( 필요시 사용자가 별도 생성 )
        * 나머지 설정은 Ubuntu Server 18.04 LTS upstream 을 유지함
* Ubuntu Linux 14.04 LTS 신규 이미지 업데이트
    * 이미지 정보
        * Ubuntu Linux 14.04
        * 언어 : EN
        * 설명 : Ubuntu Linux 14.04.5(2018. 09. 20.)
        * 비트 : 64bit
    * 버그픽스
        * 2018. 09. 20. 신규적용되는 예약스크립트 기능이 정상적으로 적용되지 않는 부분 해결


### 2018. 08. 09.

#### 기능 개선

* Windows 2012 R2 Standard 이미지 업데이트
    * 이미지 정보
        * Windows 2012 R2 STD
        * 언어 : EN
        * 설명 : Windows 2012 R2 STD(2018. 08. 09.)
        * 커널 비트 : 64bit
    * 변경사항
        * 한글 사용시 사용자가 한글 언어팩을 설치 ( 기본으로 영문 버전 제공 )
    * Windows 보안업데이트
        * 2018년 7월 10일 보안업데이트 적용 ( https://support.microsoft.com/en-us/help/4338815/windows-81-update-kb4338815 )
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
* Windows 2016 Standard 신규 이미지 업데이트
    * 이미지 정보
        * Windows 2016 STD
        * 언어 : EN
        * 설명 : Windows 2016 STD(2018. 08. 09.)
        * 비트 : 64bit
    * Windows 보안업데이트
        * 2018년 7월 24일 (https://support.microsoft.com/en-us/help/4338822/windows-10-update-kb4338822)
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
* Debian 9.4 신규 이미지 업데이트
    * 이미지 정보
        * Debian 9.4
        * 언어 : EN
        * 설명 : Debian 9.4.0(2018. 08. 09.)
        * 비트 : 64bit
    * Kernel 4.9
        * meltdown/spectre variant 1,2,3 (CVE-2017-5753, 5715, 5754) 패치 (retpoline)
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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

#### 기능 개선

* Windows 2012 R2 Standard 이미지 업데이트
    * 이미지 정보
        * Windows 2012R2std
        * 언어 : KO
        * 설명 : Windows 2012 R2 STD(2018. 07. 16.)
        * 커널 비트 : 64bit
    * Auto scale 기능으로 백신이 포함된 인스턴스 생성시 발생하는 에러 현상 수정
    * CPU 설정 변경  ( CPU Socket 최대 개수  4개 )
    * Network  인터페이스 속도  10G 로 표시
* Windows 2008 R2 Standard 신규 이미지 업데이트
    * 이미지 정보
        * Windows 2008R2std
        * 언어 : EN
        * 설명 : Windows 2008 R2 STD(2018. 07. 16.)
        * 커널 비트 : 64bit
    * Windows 보안업데이트
        * 2018년 6월 12일자 보안 업데이트 적용 ( https://support.microsoft.com/ko-kr/help/4284826 )
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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
* Ubuntu Linux 16.04 LTS 신규 이미지 업데이트
    * 이미지 정보
        * Ubuntu 16.04 LTS
        * 언어 : EN
        * 설명 : Ubuntu 16.04.4 LTS(2018. 07. 16.)
        * 커널 비트 : 64bit
    * Kernel 4.4.0-130
        * meltdown/spectre variant 1,2,3 (CVE-2017-5753, 5715, 5754) 패치 (retpoline)
    * NHN Cloud Cloud 보안기준으로 OS 하드닝 적용
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

### 2018.05.29

#### 버그 수정
* Auto Scale의 반복성 예약 작업(cron expression 기반) 관련 오류가 수정되었습니다.
    * 반복성 예약 작업 실행 시점이  UTC를 기반으로  동작하는 오류 수정
    * 반복성 예약 작업의 최초 실행이 cron expression을 따르지 않고, 예약 작업 생성 시 설정한 '시작 시각'에 수행되는 오류 수정

#### 기능 추가
* Instance 생성 시 volume type 설정 기능이 추가되었습니다.
* Block Storage 생성 시 volume type 설정 기능이 추가되었습니다.

### 2018.04.24

* Windows 인스턴스 Log 탭이 일시적으로 삭제 되었습니다.

### 2018.03.22

#### 신규 상품 추가

* Auto Scale 상품이 추가되었습니다.
    * 사용자가 생성한 Instance Template을 바탕으로, Scaling Group을 생성할 수 있습니다.
    * Scaling Group에 속한 인스턴스의 개수를 인스턴스 상태 혹은 예약 작업을 통해 동적으로 관리할 수 있습니다.
    * 자세한 내용은 가이드 문서를 참고해 주세요.


### 2018. 02. 22.

#### 기능 개선

* VPC 기능이 추가됨에 따라 인스턴스 생성 시에 서브넷을 지정하도록 변경되었습니다.
* Windows 2012 R2 Standard 이미지 업데이트
    * 이미지 정보
        * Name : Windows 2012R2std
        * Language : KO
        * Description : Windows 2012 R2 STD(2018. 02. 22.)
    * Windows Time Zone 설정 변경
        * 동기화 주기 변경 : [기존) 604800초 (7일) -> [변경] 256초
        * Time Zone Peer 도메인 변경 : [기존] 1.kr.pool.ntp.org , 1.pool.ntp.org -> [변경] 1.pool.ntp.org , time.windows.com
    * MS 2018.02.13 Windows Update 적용
        * https://support.microsoft.com/ko-kr/help/4074594/windows-81-update-kb-4074594
* Ubuntu Linux 14.04 이미지 업데이트
    * 이미지 정보
        * Name : Ubuntu 14.04
        * Description : Ubuntu Linux 14.04.5(2018. 02. 22.)
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version : [기존] 3.13.0-32 --> [변경] 3.13.0-141
        * Variant 1 (CVE-2017-5753) - patched
        * Variant 3 (CVE-2017-5754) - patched
* Debian Linux 8.2 이미지 업데이트
    * 이미지 정보
        * Name : Debian Linux 8.2.0
        * Description : Debian Linux 8.2.0(2018. 02. 22.)
    * 호스트명 설정 변경
        * 인스턴스 생성시 지정한 이름으로 호스트명 적용되도록 수정
        * [기존] localhost-192.168.0.x -> [변경] 콘솔에서 지정한 이름
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version : [기존] 3.16.0-4 --> [변경] 3.16.0-5
        * Variant 3 (CVE-2017-5754) - patched
* CentOS Linux 6.5 이미지 업데이트
    * 이미지 정보
        * Name : CentOS Linux 6.5
        * Description : CentOS Linux 6.5(2018. 02. 22.)
    * 호스트명 설정 변경
        * 인스턴스 생성시 지정한 이름으로 호스트명 적용되도록 수정
        * [기존] localhost-192.168.0.x -> [변경] 콘솔에서 지정한 이름
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version : [기존] 2.6.32-431 --> [변경] 2.6.32-696.20.1
        * Variant 1 (CVE-2017-5753) - patched
        * Variant 3 (CVE-2017-5754) - patched
* CentOS Linux 7.1 이미지 업데이트
    * 이미지 정보
        * Name : CentOS Linux 7.1
        * Description : CentOS Linux 7.1(2018. 02. 22.)
    * 호스트명 설정 변경
        * 인스턴스 생성시 지정한 이름으로 호스트명 적용되도록 수정
        * [기존] localhost-192.168.0.x -> [변경] 콘솔에서 지정한 이름
    * Firewall daemon default 값 변경
        * 인스턴스 부팅시 Firewall daemon 자동 시작되지 않도록 설정 변경
    * Swap Disk Mount 설정 변경
        * 신규 인스턴스 생성시 swap 파티션 자동 마운트되도록 설정 변경
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version : [기존] 3.10.0-229.20.1 --> [변경] 3.10.0-693.17.1
        * Variant 1 (CVE-2017-5753) - patched
        * Variant 3 (CVE-2017-5754) - patched
* CentOS Linux 6.5 with MySQL 5.6.38 신규 이미지 업데이트
    * 이미지 정보
        * Name : CentOS Linux 6.5
        * Description : CentOS Linux 6.5 with MySQL 5.6.38(2018. 02. 22.)
    * MySQL 5.6.38 패키지 설치됨
    * 그외 설정은 CentOS Linux 6.5 이미지와 동일함
* CentOS Linux 6.5 with MySQL 5.7.20 신규 이미지 업데이트
    * 이미지 정보
        * Name : CentOS Linux 6.5
        * Description : CentOS Linux 6.5 with MySQL 5.7.20(2018. 02. 22.)
    * MySQL 5.7.20 패키지 설치됨
    * 그외 설정은 CentOS Linux 6.5 이미지와 동일함


### 2017.09.21

#### 기능 추가
* Public API 추가
    * Object Storage에 이어 NHN Cloud Compute를 API로 관리할 수 있습니다.
    * 현재 제한적인 기능만 이용할 수 있으며, 추후 API 추가를 통해 기능이 확장될 예정입니다.
    * 지원되는 API는 API Guide를 참고하시기 바랍니다.

#### 버그 수정
* 키페어를 지정하지 않고 인스턴스를 생성할 수 있었던 버그가 수정되었습니다.



### 2017.07.20

#### 버그 수정
* 대용량 이미지 생성시 간헐적으로 생성이 완료되지 않던 버그가 수정되었습니다.



### 2017.08.24

#### 기능 추가

* 인스턴스 사양을 변경할 수 있도록 기능이 추가되었습니다.
    * 사용하던 인스턴스의 디스크는 그대로 보존하면서 CPU/Memory를 업그레이드 하거나 다운그레이드 할 수 있습니다.
    * 블록 스토리지 크기는 변경이 불가능합니다.
    * 사양 변경을 위해 인스턴스는 중지 상태여야 합니다.
    * 자세한 제약 사항은 [인스턴스 사양 변경](/Compute/Instance/ko/console-guide/#_14) 참조
* Low IOPS SSD 사양(U 타입)이 추가되었습니다.
    * 좀 더 낮은 가격에 인스턴스를 이용할 수 있도록 저사양 인스턴스 사양이 추가되었습니다.
    * 리눅스 OS만 지원합니다.
    * Local Disk를 이용하기 때문에 하드웨어 장애시 데이터 복구가 불가능할 수 있습니다.
* High IOPS SSD 사양(I 타입)이 추가되었습니다.
    * 높은 IOPS가 필요한 경우 I타입을 이용하면 수준의 높은 IOPS를 보장 받을 수 있습니다. (보장 IOPS는 가격표 참조)
    * 리눅스 OS만 지원합니다.

#### 버그 수정
* 인스턴스 사용량 조회시 값이 조회되지 않는 버그가 수정되었습니다.



### 2017. 05. 25.

#### 기능 추가

* 윈도우 이미지(Windows 2012 r2)가 추가됩니다.

#### 버그 수정

* 서비스 종료된 이미지로 생성된 인스턴스가 조회 되지 않는 버그가 수정되었습니다.



### 2017.04.25

#### 기능 개선

* 인스턴스 생성시 초기 불륨 크기의 최대값이 600GB에서 1TB(1000GB)로 변경됩니다.



### 2017.03.23

#### 기능 개선

* 인스턴스 생성시 사용자가 초기 볼륨의 크기를 지정할 수 있게 됩니다.
    * [기존] 인스턴스 사양에 지정된 크기로 초기 볼륨 생성 -> [변경] 사용자가 지정한 크기 만큼 초기 볼륨을 생성
    * 기본 디스크의 크기는 이미지 최소 요구 사항에서 최대 600GB 까지 설정할 수 있습니다.



### 2017.01.19

#### 기능 개선/변경
- 인스턴스 기본 정보의 IP 주소 정보에서 서브넷 명칭을 표시하지 않습니다.
    - 명칭 표기로 행의 넓이가 넓어져 가독성이 떨어지는 것을 방지합니다.
- 인스턴스 이름 길이 및 특수문자 제한합니다.
    - 이제부터 생성 및 수정되는 인스턴스의 이름은 20자 이하 영숫자와 **.** (dot),**-** (dash) 문자만 허용합니다.
- 인스턴스 생성 기능을 이미지 생성 기능으로 변경합니다.
    - 탭과 일관된 기능으로 변경하였습니다.

#### 버그 수정
* 이미지 탭(Private, Shared, Public) 변경시 이미지 선택이 해제되지 않던 문제를 수정하였습니다.



### 2016.12.22

#### 기능 개선/변경

* 정지된 인스턴스의 보안 그룹 수정이 가능하도록 변경합니다.
    * 의도와 다르게 기존에는 정지되어 있는 인스턴스에 보안 그룹 수정이 불가능하였습니다. 이를 수정하여 정지된 인스턴스도 보안 그룹을 변경할 수 있도록 하였습니다.
* 인스턴스 생성시 선택 가능한 보안 그룹이 하나일 경우 자동 선택되도록 변경합니다.
