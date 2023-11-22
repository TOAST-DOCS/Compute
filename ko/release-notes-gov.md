## Compute > 릴리스 노트


### 2023. 11. 30.
#### Instance
* 인스턴스 종료 기능 추가

#### Public API
* 인스턴스 종료, 종료된 인스턴스 시작 API 추가

#### Image
* 이미지 공유 멤버 수 제한 해제

* 신규 이미지 추가
	* Ubuntu Server 22.04.3 LTS with NVIDIA(2023.11.21.)
	* Ubuntu Server 22.04.3 LTS - Container(2023.11.21.)

* GPU 및 container 관련(Linux)
    * debian 11 container - gpu driver 추가 / gpu flavor 선택 후 클러스터 생성 가능
    * nvidia driver 업데이트: 470.199.02 > 535.104.12
    * cuda 업데이트: 11.4 > 12.2
    * mig manager: 0.5.4 > 0.5.5

* GPU(Windows)
	* nvidia driver 업데이트: 474.44 > 537.13

* 보안업데이트(Linux)
	* CentOS 7.9: /usr/bin/newgrp, /sbin/unix_chkpwd SetUID 제거

* 보안업데이트(Windows)
	* windows 2016: kb5031362
		* https://support.microsoft.com/en-au/topic/october-10-2023-kb5031362-os-build-14393-6351-0c6e713e-3d6a-4593-8a75-af0a605f249c
	* windows 2019: kb5031361
		* https://support.microsoft.com/en-gb/topic/october-10-2023-kb5031361-os-build-17763-4974-766593db-b47a-4b18-a698-906426860313
	* windows 2022: kb5031364
		* https://support.microsoft.com/en-us/topic/october-10-2023-kb5031364-os-build-20348-2031-7f1d69e7-c468-4566-887a-1902af791bbc

* 이미지 업데이트(Linux)
	* CentOS 7.9(2023.11.21.)
	* Debian 10.13 Buster(2023.11.21.)
	* Debian 11.8 Bullseye(2023.11.21.)
	* Rocky Linux 8.8(2023.11.21.)
	* Ubuntu Server 20.04.6 LTS(2023.11.21.)
	* Ubuntu Server 22.04.3 LTS(2023.11.21.)
	* CentOS 7.9 - Container(2023.11.21.)
	* Debian 11.8 Bullseye - Container(2023.11.21.)
	* Rocky Linux 8.8 - Container(2023.11.21.)
	* Ubuntu Server 20.04.6 LTS - Container(2023.11.21.)
	* Ubuntu Server 20.04.6 LTS with NVIDIA(2023.11.21.)

* 이미지 업데이트(Windows)
	* Windows 2016 STD(2023.11.21.) EN
	* Windows 2016 STD(2023.11.21.) KO
	* Windows 2019 STD(2023.11.21.) EN
	* Windows 2019 STD(2023.11.21.) KO
	* Windows 2022 STD(2023.11.21.) EN
	* Windows 2022 STD(2023.11.21.) KO
	* Windows 2016 STD with MS-SQL 2016 Standard(2023.11.21.) EN
	* Windows 2016 STD with MS-SQL 2016 Standard(2023.11.21.) KO
	* Windows 2016 STD with MS-SQL 2017 Standard(2023.11.21.) EN
	* Windows 2016 STD with MS-SQL 2017 Standard(2023.11.21.) KO
	* Windows 2016 STD with MS-SQL 2019 Express(2023.11.21.) EN
	* Windows 2016 STD with MS-SQL 2019 Express(2023.11.21.) KO
	* Windows 2016 STD with MS-SQL 2019 Standard(2023.11.21.) EN
	* Windows 2016 STD with MS-SQL 2019 Standard(2023.11.21.) KO
	* Windows 2019 STD with MS-SQL 2019 Standard(2023.11.21.) EN
	* Windows 2019 STD with MS-SQL 2019 Standard(2023.11.21.) KO


#### Image Builder
* 애플리케이션 추가
    * NHN Kubernetes Service(NKS) Worker Node
    * NHN Kubernetes Service(NKS) Worker Node(GPU)


### 2023. 10. 31.
#### Image
* 신규 이미지 추가
    * CentOS 7.9 with Tibero 7 CSE(2023.10.31.)
    * CentOS 7.9 with Tibero 7 CEE(2023.10.31.)

* 이미지 지원 종료
    * CentOS 7.9 with Tibero 6(2022.12.20.)



### 2023. 09. 26.
#### Image
* 이미지 지원 종료
    * Windows 2012 R2 STD(2023.08.22.) KO
    * Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) KO

* PIOLINK WEBFRONT-KS 4.0.6.61.28(2023.04.25.)
    * 이미지 이름 변경 PLOS-WAF-KS-v4.0.6.61.28(2023.04.25.) > PIOLINK WEBFRONT-KS 4.0.6.61.28(2023.04.25.)

#### Image Builder
* Image Builder 서비스 추가
    * OS 이미지와 애플리케이션 설치 구성 요소, 사용자 스크립트를 조합해 개인 이미지 제작


### 2023. 08. 31.
#### Public API
* 이미지 업로드/다운로드 API 추가

#### Image
* 신규 이미지 추가
    * Rocky Linux 8.8(2023.08.22.)

* 이미지 지원 종료
    * Rocky Linux 8.7(2023.05.25.)

* GPU
    * NVIDIA 드라이버 업데이트(Linux): 470.182.03 > 470.199.02
    * dcgm 업데이트(Linux): 3.1.7 > 3.1.8

* CentOS 7.9(2023.08.22.)
    * 이미지 업데이트
* Debian 10.13 Buster(2023.08.22.)
    * 이미지 업데이트
* Debian 11.7 Bullseye(2023.08.22.)
    * 이미지 업데이트
* Ubuntu Server 20.04.6 LTS(2023.08.22.)
    * 이미지 업데이트
* Ubuntu Server 20.04.6 LTS with NVIDIA(2023.08.22.)
    * 이미지 업데이트
* Ubuntu Server 22.04.2 LTS(2023.08.22.)
    * 이미지 업데이트
* Windows 2012 R2 STD(2023.08.22.) EN
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2012 R2 STD(2023.08.22.) KO
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) EN
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.08.22.) KO
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/july-11-2023-kb5028228-monthly-rollup-b7ee35a2-91ab-4e36-8e46-7c616d1bd4e4
* Windows 2016 STD(2023.08.22.) EN
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD(2023.08.22.) KO
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2016 Standard(2023.08.22.) EN
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2016 Standard(2023.08.22.) KO
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2017 Standard(2023.08.22.) EN
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2017 Standard(2023.08.22.) KO
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Express(2023.08.22.) EN
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Express(2023.08.22.) KO
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Standard(2023.08.22.) EN
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2016 STD with MS-SQL 2019 Standard(2023.08.22.) KO
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/july-11-2023-kb5028169-os-build-14393-6085-fa5b6c30-1ac8-4b99-b58b-9c434d8a8b98
* Windows 2019 STD(2023.08.22.) EN
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD(2023.08.22.) KO
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD with MS-SQL 2019 Standard(2023.08.22.) EN
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2019 STD with MS-SQL 2019 Standard(2023.08.22.) KO
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-gb/topic/july-11-2023-kb5028168-os-build-17763-4645-eff2d1e1-5f91-4d9a-aef1-ae26bdf51321
* Windows 2022 STD(2023.08.22.) EN
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/july-11-2023-security-update-kb5028171-34557119-e00c-4678-bb87-048a36ed8585
* Windows 2022 STD(2023.08.22.) KO
    * 이미지 업데이트
    * 23년 7월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/july-11-2023-security-update-kb5028171-34557119-e00c-4678-bb87-048a36ed8585

#### Instance
* 인스턴스 삭제 시 인스턴스에 연결되어 있는 플로팅 IP와 추가 블록 스토리지를 함께 삭제하는 기능 추가


### 2023. 06. 08.

#### Instance
* **CloudTrail**의 인스턴스 생성 및 인스턴스 삭제 로그 개선
* 인스턴스 생성 시 기존 네트워크 인터페이스를 여러 개 지정할 수 있도록 UI 개선

#### Image
* 신규 이미지 추가
    * Rocky Linux 8.7(2023.05.25.)
    * Ubuntu Server 20.04.6 LTS for NAT(2023.05.25.)

* 이미지 지원 종료
    * Rocky Linux 8.6(2023.03.21.)
    * Ubuntu Server 18.04.6 LTS(2023.02.21.)
    * Ubuntu Server 18.04.6 LTS for NAT(2023.02.21.)
    * Ubuntu Server 18.04.5 LTS for AI(2021.06.22.)
    * Ubuntu Server 18.04.6 LTS with NVIDIA(2023.03.21.)

* GPU
    * NVIDIA 드라이버 업데이트(Linux): 450.216.04 > 470.182.03
    * NVIDIA 드라이버 업데이트: 453.94 > 474.30

* CentOS 7.9(2023.05.25.)
    * 이미지 업데이트
* Debian 10.13 Buster(2023.05.25.)
    * 이미지 업데이트
    * Multi NIC 설정 시 접근 불가 이슈 처리
* Debian 11.6 Bullseye(2023.05.25.)
    * 이미지 업데이트
    * cgroup v2 disable 설정
* Ubuntu Server 20.04.6 LTS(2023.05.25.)
    * 이미지 업데이트
* Ubuntu Server 20.04.6 LTS with NVIDIA(2023.05.25.)
    * 이미지 업데이트
* Ubuntu Server 22.04.2 LTS(2023.05.25.)
    * 이미지 업데이트
* Windows 2012 R2 STD(2023.05.25.) EN
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2012 R2 STD(2023.05.25.) KO
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2016 STD(2023.05.25.) EN
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD(2023.05.25.) KO
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2019 STD(2023.05.25.) EN
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f
* Windows 2019 STD(2023.05.25.) KO
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f
* Windows 2022 STD(2023.05.25.) EN
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-gb/topic/april-11-2023-kb5025230-os-build-20348-1668-28a5446e-6389-4a5b-ae3f-e942a604f2d3
* Windows 2022 STD(2023.05.25.) KO
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-gb/topic/april-11-2023-kb5025230-os-build-20348-1668-28a5446e-6389-4a5b-ae3f-e942a604f2d3
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.05.25.) EN
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.05.25.) KO
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025285-monthly-rollup-79639041-a60e-423b-845d-64c251ea656c
* Windows 2016 STD with MS-SQL 2016 Standard(2023.05.25.) EN
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2016 Standard(2023.05.25.) KO
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2017 Standard(2023.05.25.) EN
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2017 Standard(2023.05.25.) KO
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Express(2023.05.25.) EN
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Express(2023.05.25.) KO
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Standard(2023.05.25.) EN
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2016 STD with MS-SQL 2019 Standard(2023.05.25.) KO
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-11-2023-kb5025228-os-build-14393-5850-23f04722-1b4f-4786-8c06-67e73de414d5
* Windows 2019 STD with MS-SQL 2019 Standard(2023.05.25.) EN
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f
* Windows 2019 STD with MS-SQL 2019 Standard(2023.05.25.) KO
    * 이미지 업데이트
    * 23년 11월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/april-11-2023-kb5025229-os-build-17763-4252-e8ead788-2cd3-4c9b-8c77-d677e2d8744f

### 2023. 04. 25.

#### Image
* 신규 이미지 추가
    * Ubuntu Server 20.04.6 LTS for Deep Learning(2023.04.25.)
    * PLOS-WFK-KS-v4.0.6.61.28(2023.04.25.)

* 이미지 지원 종료
    * Ubuntu Server 18.04.6 LTS for Deep Learning(2022.01.25.)
    * PLOS-WFK-KS-v4.0.6.61.25(2022.09.20.)


### 2023. 04. 04.

#### Image
* 신규 이미지 추가
    * CentOS 7.9 with CUBRID 10.2.10(2023.03.21.)
    * CentOS 7.9 with CUBRID 11.0.10(2023.03.21.)
    * CentOS 7.9 with MariaDB 10.6.11(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with MySQL 8.0.27(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with Redis 7.0.5(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with Apache Kafka 3.3.1(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 10.2.10(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with CUBRID 11.0.10(2023.03.21.)
    * Ubuntu Server 20.04.6 LTS with MariaDB 10.6.11(2023.03.21.)

* 이미지 지원 종료
    * CentOS 7.9 with CUBRID 10.2.4(2022.12.20.)
    * CentOS 7.9 with CUBRID 11.0.2(2022.12.20.)

* Debian 10.13 Buster(2023.03.21.)
    * 이미지 업데이트
* Debian 11.6 Bullseye(2023.03.21.)
    * 이미지 업데이트
* Rocky Linux 8.6(2023.03.21.)
    * 이미지 업데이트
* Ubuntu Server 18.04.6 LTS(2023.03.21.)
    * 이미지 업데이트
* Ubuntu Server 18.04.6 LTS with NVIDIA(2023.03.21.)
    * 이미지 업데이트
* Ubuntu Server 20.04.6 LTS(2023.03.21.)
    * 이미지 업데이트
* Ubuntu Server 20.04.6 LTS with NVIDIA(2023.03.21.)
    * 이미지 업데이트
* Ubuntu Server 22.04.2 LTS(2023.03.21.)
    * 이미지 업데이트

#### Public API
* API 엔드포인트 변경

### 2023. 03. 28.

#### System Monitoring
* 월간 지표 보고서의 주기 선택 조건에서 `1분` 옵션 제외

### 2023. 03. 07.

#### Image
* 신규 이미지 추가
    * Ubuntu Server 22.04.1 LTS(2023.02.21.)
    * Ubuntu Server 20.04.5 LTS with NVIDIA(2023.02.21.)

* 커널 업데이트

* GPU
    * nvidia driver 업데이트(Windows): 453.51 > 453.94
    * nvidia driver 업데이트(Linux): 450.191.01 > 450.216.04

* Rocky Linux 8.6(2023.02.21.)
    * 이미지 업데이트
* Debian 10.13 Buster(2023.02.21.)
    * 이미지 업데이트
* Debian 11.6 Bullseye(2023.02.21.)
    * 이미지 업데이트
* Ubuntu Server 18.04.6 LTS(2023.02.21.)
    * 이미지 업데이트
* Ubuntu Server 20.04.5 LTS(2023.02.21.)
    * 이미지 업데이트
* Ubuntu Server 18.04.6 LTS with NVIDIA(2023.02.21.)
    * 이미지 업데이트
* Windows 2012 R2 STD(2023.02.14.)
    * 이미지 업데이트
    * 23년 1월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022352-monthly-rollup-cf299bf2-707b-47db-89a5-4e22c5ce4e26
* Windows 2016 STD(2023.02.14.)
    * 이미지 업데이트: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
    * 23년 1월 보안 업데이트 반영
* Windows 2019 STD(2023.02.14.)
    * 이미지 업데이트: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022286-os-build-17763-3887-48683103-7b22-4f36-aa98-0049c7a6e579
    * 23년 1월 보안 업데이트 반영
* Windows 2022 STD(2023.02.14.)
    * 이미지 업데이트
    * 23년 1월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022291-os-build-20348-1487-38772acf-103f-463e-9d60-486174e806b2
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2023.02.14.)
    * 이미지 업데이트
    * 23년 1월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022352-monthly-rollup-cf299bf2-707b-47db-89a5-4e22c5ce4e26
* Windows 2016 STD with MS-SQL 2016 Standard(2023.02.14.)
    * 이미지 업데이트
    * 23년 1월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2016 STD with MS-SQL 2017 Standard(2023.02.14.)
    * 이미지 업데이트
    * 23년 1월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2016 STD with MS-SQL 2019 Express(2023.02.14.)
    * 이미지 업데이트
    * 23년 1월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2016 STD with MS-SQL 2019 Standard(2023.02.14.)
    * 이미지 업데이트
    * 23년 1월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022289-os-build-14393-5648-36de3673-55d0-4e0f-8b77-d06326b58456
* Windows 2019 STD with MS-SQL 2019 Standard(2023.02.14.)
    * 이미지 업데이트
    * 23년 1월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/january-10-2023-kb5022286-os-build-17763-3887-48683103-7b22-4f36-aa98-0049c7a6e579

### 2023. 02. 07.

#### Image
* 신규 이미지 추가
    * CentOS 7.9 with Apache Kafka 3.3.1(2022. 12. 20.)
    * CentOS 7.9 with Redis 7.0.5(2022. 12. 20.)

#### Instance
* **인스턴스 템플릿**으로 인스턴스 생성 시 설정값 변경 가능하도록 UI 개선

#### Instance Template
* **인스턴스 템플릿 오너 변경** 기능 추가

#### Auto Scale
* **스케일링 그룹 오너 변경** 기능 추가
* **인스턴스 템플릿**으로 스케일링 그룹 생성 시 설정값 변경 가능하도록 UI 개선

### 2023. 01. 03.

#### Image
* 신규 이미지 추가
    * CentOS 7.9 with CUBRID 10.2.4(2022. 12. 20.)
    * CentOS 7.9 with CUBRID 11.0.2(2022. 12. 20.)
    * CentOS 7.9 with MariaDB 10.3.31(2022. 12. 20.)
    * CentOS 7.9 with MySQL 5.7.35(2022. 12. 20.)
    * CentOS 7.9 with MySQL 8.0.27(2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 10.20(2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 11.15(2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 12.10(2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 13.6(2022. 12. 20.)
    * CentOS 7.9 with PostgreSQL 14.2(2022. 12. 20.)
    * CentOS 7.9 with Tibero 6(2022. 12. 20.)
* 이미지 지원 종료
    * CentOS 7.8(2021. 12. 21.)
    * CentOS 7.8 with CUBRID 10.2.4(2021. 12. 21.)
    * CentOS 7.8 with CUBRID 11.0.2(2021. 12. 21.)
    * CentOS 7.8 with MariaDB 10.3.31(2022.11.4)
    * CentOS 7.8 with MySQL 5.7.20(2021. 12. 21.)
    * CentOS 7.8 with MySQL 5.7.32(2021. 12. 21.)
    * CentOS 7.8 with MySQL 8.0.22(2021. 12. 21.)
    * CentOS 7.8 with PostgreSQL 10.20(2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 11.15(2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 12.10(2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 13.6(2022. 05. 17.)
    * CentOS 7.8 with PostgreSQL 14.2(2022. 05. 17.)
    * CentOS 7.8 with Tibero 6(2022. 01. 25.)

### 2022. 12. 06.
#### Instance
* 인스턴스 관리의 **필터 조건**에 삭제 보호(전체/설정/미설정) 추가
* 네트워크 인터페이스 별로 설정된 보안 그룹 변경 기능 개선 
* 인스턴스 정보 UI 개선
* 삭제 보호 토글 버튼 추가 
* 삭제 보호 일괄 설정 기능 개선

#### Image
* 신규 이미지 추가
    * CentOS 7.9(2022. 11. 22.)
    * Rocky Linux 8.6(2022. 11. 22.)
* 이미지 지원 종료
    * Rocky Linux 8.5(2022. 05. 17.)
* Debian 10.13 Buster(2022. 11. 22.)
    * 이미지 업데이트
* Debian 11.5 Bullseye(2022. 11. 22.)
    * 이미지 업데이트
* Ubuntu Server 18.04.6 LTS(2022. 11. 22.)
    * 이미지 업데이트
* Ubuntu Server 20.04.5 LTS(2022. 11. 22.)
    * 이미지 업데이트
* Ubuntu Server 18.04.6 LTS with NVIDIA(2022. 11. 22.)
    * 이미지 업데이트
* Windows 2012 R2 STD(2022. 11. 22.)
    * 22년 10월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018474-monthly-rollup-21182931-4a5f-4085-a37b-2e63ac3c8c0a
* Windows 2016 STD(2022. 11. 22.)
    * 22년 10월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2019 STD(2022. 11. 22.)
    * 22년 10월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018419-os-build-17763-3532-ca62cca7-b599-44c4-a2a6-347996662623
* Windows 2022 STD(2022. 11. 22.)
    * 22년 10월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018421-os-build-20348-1129-115b1147-9568-4924-83b8-d27ab5b495be
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2022. 11. 22.)
    * 22년 10월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/kb5012672-servicing-stack-update-for-windows-8-1-rt-8-1-and-server-2012-r2-april-12-2022-0f0b0460-2483-4d89-868a-56997d1202a5
* Windows 2016 STD with MS-SQL 2016 Standard(2022. 11. 22.)
    * 22년 10월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018474-monthly-rollup-21182931-4a5f-4085-a37b-2e63ac3c8c0a
* Windows 2016 STD with MS-SQL 2019 Express(2022. 11. 22.)
    * 22년 10월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2016 STD with MS-SQL 2017 Standard(2022. 11. 22.)
    * 22년 10월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2016 STD with MS-SQL 2019 Standard(2022. 11. 22.)
    * 22년 10월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018411-os-build-14393-5427-a59be55a-b368-4284-a643-28fc0b9b8314
* Windows 2019 STD with MS-SQL 2019 Standard(2022. 11. 22.)
    * 22년 10월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/october-11-2022-kb5018419-os-build-17763-3532-ca62cca7-b599-44c4-a2a6-347996662623

### 2022. 11. 02.
#### Image
* 이미지 지원 종료
    * CentOS 7.8 with MySQL 5.6.38(2021. 12. 21.)
    * CentOS 7.8 with MySQL 5.6.50(2021. 12. 21.)

### 2022. 10. 11.
#### Image
* 신규 이미지 추가
    * Windows 2022 STD(2022. 09. 20.)

* PLOS-WFK-KS-v4.0.6.61.25
    * 이미지 업데이트

### 2022. 09. 14.
#### Image
* 신규 이미지 추가
    * Tibero
        * CentOS 7.8 with Tibero 6(2022. 01. 25.)
    * MariaDB
        * CentOS 7.8 with MariaDB 10.3.31(2021. 12. 21.)
    * CUBRID
        * CentOS 7.8 with CUBRID 10.2.4(2021. 12. 21.)
        * CentOS 7.8 with CUBRID 11.0.2(2021. 12. 21.)

### 2022. 08. 02.

#### Instance
* 인스턴스 생성에서 인스턴스 타입(Instance, Ephemeral Storage Instance) 선택 기능 추가
* 인스턴스 관리에서 이미지 타입(OS, Application, DBMS 등) 검색 기능 추가

#### Image

* 신규 이미지 추가
    * Rocky Linux 8.5(2022. 05. 17.)

* Windows 이미지 Administrator 계정명을 변경하여도 비밀번호 초기화 가능하도록 변경

* Windows 2012 R2 STD(2022. 07. 19.)
    * 22년 5월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/kb5012672-servicing-stack-update-for-windows-8-1-rt-8-1-and-server-2012-r2-april-12-2022-0f0b0460-2483-4d89-868a-56997d1202a5
* Windows 2016 STD(2022. 07. 19.)
    * 22년 5월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
* Windows 2019 STD(2022. 07. 19.)
    * 22년 5월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-12-2022-kb5012647-os-build-17763-2803-9a10c5c9-e65f-4ae1-a9c4-2db9a8eca4fc
* Windows Server 2012 R2 with SQL Server 2016 Standard(2022. 07. 19.)
    * 22년 5월 보안 업데이트 반영: https://support.microsoft.com/en-au/topic/kb5012672-servicing-stack-update-for-windows-8-1-rt-8-1-and-server-2012-r2-april-12-2022-0f0b0460-2483-4d89-868a-56997d1202a5
* Windows Server 2016 with SQL Server 2016 Standard(2022. 07. 19.)
    * 22년 5월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
* Windows Server 2016 with SQL Server 2019 Express(2022. 07. 19.)
    * 22년 5월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
    * SQL Server 누적 업데이트 16 반영: https://support.microsoft.com/en-us/topic/kb5011644-cumulative-update-16-for-sql-server-2019-74377be1-4340-4445-93a7-ff843d346896
* Windows Server 2016 with SQL Server 2017 Standard(2022. 07. 19.)
    * 22년 5월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
* Windows Server 2016 with SQL Server 2019 Standard(2022. 07. 19.)
    * 22년 5월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/kb5011570-servicing-stack-update-for-windows-10-version-1607-and-server-2016-march-8-2022-ac6cb59b-d9c1-4b5a-95bc-cf88c9d3e216
    * SQL Server 누적 업데이트 16 반영: https://support.microsoft.com/en-us/topic/kb5011644-cumulative-update-16-for-sql-server-2019-74377be1-4340-4445-93a7-ff843d346896
* Windows Server 2019 with SQL Server 2019 Standard(2022. 07. 19.)
    * 22년 5월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/april-12-2022-kb5012647-os-build-17763-2803-9a10c5c9-e65f-4ae1-a9c4-2db9a8eca4fc
    * SQL Server 누적 업데이트 16 반영: https://support.microsoft.com/en-us/topic/kb5011644-cumulative-update-16-for-sql-server-2019-74377be1-4340-4445-93a7-ff843d346896

### 2022. 05. 31.
#### Instance
* 인스턴스 스크린숏 기능 추가
* 인스턴스 삭제 보호 기능 추가
* API로 인스턴스 조회 시 인스턴스 삭제 보호 속성(NHN-EXT-ATTR:protect) 나타나도록 변경
* 한 번에 생성된 다수의 인스턴스 이름에서 붙임표(`-`) 제거
    * 기존: instance-1, instance-2, ...
    * 변경: instance1, instance2, ...
* 인스턴스 생성 시 OS 이미지 선택 UI 개선

### 2022. 04. 05.
#### Image
* 신규 이미지 추가
    * Debian 11.2 Bullseye(2022. 03. 22.)

* 이미지 지원 종료
    * Debian 9.13 Stretch(2021. 12. 21.)

### 2022. 01. 04.

#### Image
* 인스턴스 생성 시 Prometheus 호환 exporter가 자동으로 설치되지 않도록 변경

* CentOS 7.8(2021. 12. 21.)
    * 이미지 업데이트
* CentOS 7.8 with MySQL 5.6.38(2021. 12. 21.)
    * 이미지 업데이트
* CentOS 7.8 with MySQL 5.6.50(2021. 12. 21.)
    * 이미지 업데이트
* CentOS 7.8 with MySQL 5.7.20(2021. 12. 21.)
    * 이미지 업데이트
* CentOS 7.8 with MySQL 5.7.32(2021. 12. 21.)
    * 이미지 업데이트
* CentOS 7.8 with MySQL 8.0.22(2021. 12. 21.)
    * 이미지 업데이트
* Debian 9.13 Stretch(2021. 12. 21.)
    * 이미지 업데이트
* Debian 10.11 Buster(2021. 12. 21.)
    * 이미지 업데이트
* Ubuntu Server 18.04.6 LTS(2021. 12. 21.)
    * 이미지 업데이트
* Ubuntu Server 20.04.3 LTS(2021. 12. 21.)
    * 이미지 업데이트
* Ubuntu Server 18.04.6 LTS with NVIDIA(2021. 12. 21.)
    * 이미지 업데이트
* Windows 2012 R2 STD(2021. 12. 21.)
    * 21년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007247-monthly-rollup-2c3b6017-82f4-4102-b1e2-36f366bf3520
* Windows 2016 STD(2021. 12. 21.)
    * 21년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows 2019 STD(2021. 12. 21.)
    * 21년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007206-os-build-17763-2300-c63b76fa-a9b4-4685-b17c-7d866bb50e48
* Windows Server 2012 R2 with SQL Server 2016 Standard(2021. 12. 21.)
    * 21년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007247-monthly-rollup-2c3b6017-82f4-4102-b1e2-36f366bf3520
* Windows Server 2016 with SQL Server 2016 Standard(2021. 12. 21.)
    * 21년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2016 with SQL Server 2019 Express(2021. 12. 21.)
    * 21년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2016 with SQL Server 2017 Standard(2021. 12. 21.)
    * 21년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2016 with SQL Server 2019 Standard(2021. 12. 21.)
    * 21년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007192-os-build-14393-4770-f534a33a-ed00-4bd2-8248-9424c53e9bde
* Windows Server 2019 with SQL Server 2019 Standard(2021. 12. 21.)
    * 21년 11월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/november-9-2021-kb5007206-os-build-17763-2300-c63b76fa-a9b4-4685-b17c-7d866bb50e48


### 2021. 12. 07

#### Instance
* 인스턴스 템플릿을 이용한 인스턴스 생성 지원

#### Instance Template
* Instance Template 서비스 추가
    * 자주 사용하는 인스턴스 구성 요소 정보를 템플릿 형태로 미리 정의해 보관
    * 사용자가 정의한 템플릿을 Instance 또는 Scaling Group 생성에 사용


#### Auto Scale
* Instance Template 탭 제거
    * Instance Template 서비스에서 만든 템플릿으로 Scaling Group 생성
* 자동 복구 정책 옵션 선택 옵션 추가


#### Image
* GPU 인스턴스를 만들 수 있는 개인 이미지 생성 지원


#### System Monitoring
* 신규 기능 추가: Advanced Monitoring(OpenMetrics)
    * OpenMetrics(Prometheus exposition format) 지표 수집, 조회, 알림 기능 제공

### 2021. 07. 05.

#### Image

* 신규 이미지 추가
    * CentOS 7.8 with MySQL 5.6.38(2021. 06. 22.)
    * CentOS 7.8 with MySQL 5.6.50(2021. 06. 22.)
    * CentOS 7.8 with MySQL 5.7.20(2021. 06. 22.)
    * CentOS 7.8 with MySQL 5.7.32(2021. 06. 22.)
    * CentOS 7.8 with MySQL 8.0.22(2021. 06. 22.)

* 이미지 지원 종료
    * CentOS 6.10(2020. 12. 22.)
    * CentOS 7.5(2020. 12. 22.)
    * CentOS Linux 6.10 with MySQL 5.6.38(2020. 12. 22.)
    * CentOS Linux 6.10 with MySQL 5.7.20(2020. 12. 22.)
    * Ubuntu Server 16.04.7 LTS(2020. 12. 22.)

* Prometheus 호환 exporter
    * Advanced Monitoring 지원을 위해 인스턴스 생성 시 해당 도구가 자동으로 설치됩니다.

* Linux 보안 취약점 패치 적용
    * Heap-based buffer overflow in Sudo(CVE-2021-3156)

* CentOS 7.8(2021. 06. 22.)
    * 이미지 업데이트
* Debian 9.13 Stretch(2021. 06. 22.)
    * 이미지 업데이트
* Debian 10.9 Buster(2021. 06. 22.)
    * 이미지 업데이트
* Ubuntu Server 18.04.5 LTS(2021. 06. 22.)
    * 이미지 업데이트
* Ubuntu Server 18.04.5 LTS with NVIDIA(2021. 06. 22.)
    * 이미지 업데이트
* Ubuntu Server 20.04.2 LTS(2021. 06. 22.)
    * 이미지 업데이트
* Windows 2012 R2 STD(2021. 06. 22.)
    * 2021년 05월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003209-monthly-rollup-6be347aa-f8f3-4d26-8260-58d0636f3fe7
* Windows 2016 STD(2021. 06. 22.)
    * 2021년 05월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2019 STD(2021. 06. 22.)
    * 2021년 05월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003171-os-build-17763-1935-3f03e74b-4759-4ca3-b9f1-4bc0d5ab5d27
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2021. 06. 22.)
    * 2021년 05월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003209-monthly-rollup-6be347aa-f8f3-4d26-8260-58d0636f3fe7
* Windows 2016 STD with MS-SQL 2016 Standard(2021. 06. 22.)
    * 2021년 05월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2019 Express(2021. 06. 22.)
    * 2021년 05월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2017 Standard(2021. 06. 22.)
    * 2021년 05월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2016 STD with MS-SQL 2019 Standard(2021. 06. 22.)
    * 2021년 05월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/kb5001402-servicing-stack-update-for-windows-10-version-1607-april-13-2021-0c0367b8-2389-4154-a17e-6df57123423d
* Windows 2019 STD with MS-SQL 2019 Standard(2021. 06. 22.)
    * 2021년 05월 보안 업데이트 반영: https://support.microsoft.com/en-us/topic/may-11-2021-kb5003171-os-build-17763-1935-3f03e74b-4759-4ca3-b9f1-4bc0d5ab5d27

#### System Monitoring

* CloudTrail 연동

### 2021. 01. 19.

#### Image
* CentOS 6.10(2020. 12. 22.)
    * 이미지 업데이트
* CentOS 7.5(2020. 12. 22.)
    * 이미지 업데이트
* CentOS 7.8(2020. 12. 22.)
    * 이미지 업데이트
* CentOS Linux 6.10 with MySQL 5.6.38(2020. 12. 22.)
    * 이미지 업데이트
* CentOS Linux 6.10 with MySQL 5.7.20(2020. 12. 22.)
    * 이미지 업데이트
* Debian 9.13 Stretch(2020. 12. 22.)
    * 이미지 업데이트
* Debian 10.7 Buster(2020. 12. 22.)
    * 이미지 업데이트
* Ubuntu Server 16.04.7 LTS(2020. 12. 22.)
    * 이미지 업데이트
* Ubuntu Server 18.04.5 LTS(2020. 12. 22.)
    * 이미지 업데이트
* Ubuntu Server 20.04.1 LTS(2020. 12. 22.)
    * 이미지 업데이트
* Ubuntu Server 18.04.5 LTS with NVIDIA(2020. 12. 22.)
    * 이미지 업데이트
* Windows 2012 R2 STD(2020. 12. 22.)
    * 2020년 11월 보안업데이트 반영: https://support.microsoft.com/ko-kr/help/4586845/windows-8-1-update
* Windows 2016 STD(2020. 12. 22.)
    * 2020년 11월 보안업데이트 반영: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2019 STD(2020. 12. 22.)
    * 2020년 11월 보안업데이트 반영: https://support.microsoft.com/ko-kr/help/4586839/windows-10-update-kb4586839
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2020. 12. 22.)
    * 2020년 11월 보안업데이트 반영: https://support.microsoft.com/ko-kr/help/4586845/windows-8-1-update
* Windows 2016 STD with MS-SQL 2016 Standard(2020. 12. 22.)
    * 2020년 11월 보안업데이트 반영: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2019 Express(2020. 12. 22.)
    * 2020년 11월 보안업데이트 반영: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2017 Standard(2020. 12. 22.)
    * 2020년 11월 보안업데이트 반영: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2016 STD with MS-SQL 2019 Standard(2020. 12. 22.)
    * 2020년 11월 보안업데이트 반영: https://support.microsoft.com/ko-kr/help/4586830/windows-10-update-kb4586830
* Windows 2019 STD with MS-SQL 2019 Standard(2020. 12. 22.)
    * 2020년 11월 보안업데이트 반영: https://support.microsoft.com/ko-kr/help/4586839/windows-10-update-kb4586839

### 2020. 11. 03.

#### Instance
* 키페어에 등록된 공개 키 조회 기능 추가
* GPU 인스턴스를 콘솔에서 직접 생성할 수 있도록 서비스 오픈
* **인스턴스 정지** 대화 상자에서 **삭제** 버튼 제거
* **Windows 인스턴스 접속 정보** 탭에 **비밀번호 초기화** 버튼 추가
* Windows 이미지 생성 시 원본 인스턴스 비밀번호 초기화 기능 추가

#### Image

* 신규 이미지 추가 
    * Cent OS 7.8(2020. 08. 18.)
    * Ubuntu 20.04 LTS(2020. 08. 18.)
    * Windows 2016 STD with MS-SQL 2019 Express(2020. 08. 18.)
    * Windows 2016 STD with MS-SQL 2017 Standard(2020. 08. 18.)
    * Windows 2016 STD with MS-SQL 2019 Standard(2020. 08. 18.)
    * Windows 2019 STD with MS-SQL 2019 Standard(2020. 08. 18.)

* CentOS 6.10(2020. 08. 18.)
    * 이미지 업데이트
* CentOS 7.5(2020. 08. 18.)
    * 이미지 업데이트
* CentOS Linux 6.10 with MySQL 5.6.38(2020. 08. 18.)
    * 이미지 업데이트
* CentOS Linux 6.10 with MySQL 5.7.20(2020. 08. 18.)
    * 이미지 업데이트
* Debian 9.9 Stretch(2020. 08. 18.)
    * 이미지 업데이트
* Debian 10.5 Buster(2020. 08. 18.)
    * 이미지 업데이트
* Ubuntu Server 16.04.6 LTS(2020. 08. 18.)
    * 이미지 업데이트
* Ubuntu Server 18.04.4 LTS(2020. 08. 18.)
    * 이미지 업데이트
* Ubuntu Server 18.04.4 LTS with NVIDIA(2020. 08. 18.)
    * 이미지 업데이트
* Windows 2012 R2 STD(2020. 08. 18.)
    * 이미지 업데이트
* Windows 2016 STD(2020. 08. 18.)
    * 이미지 업데이트
* Windows 2019 STD(2020. 08. 18.)
    * 이미지 업데이트
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2020. 08. 18.)
    * 이미지 업데이트
* Windows 2016 STD with MS-SQL 2016 Standard(2020. 08. 18.)
    * 이미지 업데이트

* 이미지 지원 종료
    * Windows 2012 R2 STD with MS-SQL 2012 Standard(2020. 02. 18.)
    * Windows 2012 R2 STD with MS-SQL 2014 Standard(2020. 02. 18.)
    * Windows 2012 R2 STD with MS-SQL 2016 Express(2020. 02. 18.)

### 2020. 06. 16.

#### Instance

* Public API v2 출시
    * Openstack 호환 API 스펙으로 변경
    * Terraform 지원

#### Image

* Public API v2 출시
    * Openstack 호환 API 스펙으로 변경

### 2020. 04. 07.
#### System Monitoring
* System Monitoring 서비스 추가
    * 생성된 가상 서버의 시스템 지표 차트를 제공
    * 각 시스템 지표 차트를 원하는 레이아웃으로 구성
    * 지표가 특정 임계치에 도달할 경우 원하는 특정 사용자 그룹에게 알림을 보내도록 설정

### 2020. 03. 10.
#### Image
* 개인 이미지와 공유받은 이미지가 이미지 목록에 함께 노출되도록 변경
* 신규 이미지 추가 
    * Debian 10.2 Buster(2020. 02. 18.)
    * Windows 2019 STD(2020. 02. 18.)

* CentOS 6.10(2020. 02. 18.)
    * 이미지 업데이트
* CentOS 7.5(2020. 02. 18.)
    * 이미지 업데이트
* CentOS Linux 6.10 with MySQL 5.6.38(2020. 02. 18.)
    * 이미지 업데이트
* CentOS Linux 6.10 with MySQL 5.7.20(2020. 02. 18.)
    * 이미지 업데이트
* Debian 9.9 Stretch(2020. 02. 18.)
    * 이미지 업데이트
* Ubuntu Server 16.04.2 LTS(2020. 02. 18.)
    * 이미지 업데이트
* Ubuntu Server 18.04.2 LTS(2020. 02. 18.)
    * 이미지 업데이트
* Windows 2012 R2 STD(2020. 02.18)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2012 Standard(2020. 02. 18.)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2014 Standard(2020. 02. 18.)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2016 Express(2020. 02. 18.)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2012 R2 STD with MS-SQL 2016 Standard(2020. 02. 18.)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530702/windows-8-1-kb4530702
* Windows 2016 STD(2020. 02. 18.)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530689/windows-10-update-kb4530689
* Windows 2016 R2 STD with MS-SQL 2016 Standard(2020. 02. 18.)
    * 2019년 12월 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4530689/windows-10-update-kb4530689

* 이미지 지원 종료
    * Debian 8.11 Jessie(2019. 07. 23.)

### 2019. 11. 12.
#### Image
* PLOS-WFK-KS-v2.0.60.0.14(2019. 10. 22.)
    * WF-KS 페이지의 Storage 크기 표기 오류 수정

### 2019. 08. 13.
#### Auto Scale
* Scaling Group의 사용량을 확인할 수 있는 통계 그래프 추가
* 예약 작업 생성 시 타임존 설정 기능 추가

#### Instance
* 인스턴스가 구동 중일 때도 이미지를 생성할 수 있도록 기능 추가

#### Image
* CentOS 6.10(2018. 08. 13.)
    * yum update 시 발생하는 에러현상 개선
    * 리전에 따른 timezone 변경 적용
* CentOS 7.5(2018. 08. 13.)
    * yum update 시 발생하는 에러현상 개선
    * 시간 동기화 데몬 변경(ntpd)
    * 리전에 따른 timezone 변경 적용

* Debian 8.11 Jessie(2018. 08. 13.)
    * 리전에 따른 timezone 변경 적용

* Debian 9.9 Stretch(2018. 08. 13.)
    * 리전에 따른 timezone 변경 적용
    * 커널 업데이트: 4.9.168-1

* Ubuntu Server 16.04.6 LTS(2018. 08. 13.)
    * 리전에 따른 timezone 변경 적용
    * 커널 업데이트: 4.4.0-142.168

* Ubuntu Server 18.04.2 LTS(2018. 08. 13.)
    * 리전에 따른 timezone 변경 적용

* CentOS Linux 6.10 with MySQL 5.6.38(2018. 08. 13.)
    * 이미지 업데이트
* CentOS Linux 6.10 with MySQL 5.7.20(2018. 08. 13.)
    * 이미지 업데이트

* Windows 2012 R2 STD(2018. 08. 13.)
    * Windows Bootstrap 과정 기능 개선
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트 반영: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151

* Windows 2012 STD with MS-SQL 2008 Standard(2019. 05. 14.)
    * Windows Bootstrap 과정 기능 개선
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 STD with MS-SQL 2012 Standard(2018. 08. 13.)
    * Windows Bootstrap 과정 기능 개선
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 STD with MS-SQL 2014 Standard(2018. 08. 13.)
    * Windows Bootstrap 과정 기능 개선
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 STD with MS-SQL 2016 Express(2018. 08. 13.)
    * Windows Bootstrap 과정 기능 개선
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151
* Windows 2012 STD with MS-SQL 2016 Standard(2018. 08. 13.)
    * Windows Bootstrap 과정 기능 개선
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트: https://support.microsoft.com/ko-kr/help/4499151/windows-8-1-update-kb4499151

* Windows 2016 STD(2018. 08. 13.)
    * Windows Bootstrap 과정 기능 개선
    * Region에 따른 timezone 변경 적용
    * 2019년 5월 14일 보안 업데이트: https://support.microsoft.com/ko-kr/help/4498947/windows-10-update-kb4498947

* 신규 이미지 추가
    * Windows 2016 STD with MS-SQL 2016 Standard(2018. 08. 13.)

* OS 이미지 지원 종료
    * CentOS 6.5
    * CentOS 7.1
    * Ubuntu 14.04
    * Windows 2008 R2 STD

### 2019. 03. 26.
#### Image
* Debian 9.8 Stretch(2019. 03. 26.)
    * 커널 업데이트: 4.9.144-3

* CentOS 6.5(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선
* CentOS 6.10(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선
* CentOS 7.1(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선
* CentOS 7.5(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선
* CentOS 6.5 with MySQL 5.6.38(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선
* CentOS 6.5 with MySQL 5.7.20(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선
* Ubuntu Server 14.04.5 LTS(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선
* Ubuntu Server 16.04.5 LTS(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선
* Ubuntu Server 18.04.2 LTS(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선
* Debian 8.11 Jessie(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선
* Debian 9.8 Stretch(2019. 03. 26.)
    * Bootstrap 과정의 기능 개선


### 2019. 02. 26.
#### Image
* Ubuntu Server 18.04.2 LTS(2019. 02. 26.)
    * 커널 업데이트: 4.15.0-45
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 추가 해결


### 2018. 12. 27.
#### Image
* Ubuntu Server 14.04.5 LTS(2018. 12. 27.)
    * default 설정을 "en_US.UTF-8"로 변경
    * /etc/default/locale 수정
        * LC_ALL="en_US.UTF-8"
        * LC_CTYPE="en_US.UTF-8"
* Ubuntu Server 16.04.5 LTS(2018. 12. 27.)
    * default 설정을 "en_US.UTF-8"로 변경
    * /etc/default/locale 수정
        * LC_ALL="en_US.UTF-8"
        * LC_CTYPE="en_US.UTF-8"
* Ubuntu Server 18.04.2 LTS(2018. 12. 27.)
    * default 설정을 "en_US.UTF-8"로 변경
    * /etc/default/locale 수정
        * LC_ALL="en_US.UTF-8"
        * LC_CTYPE="en_US.UTF-8"
* Debian 8.11 Jessie(2018. 12. 27.)
    * default 설정을 "en_US.UTF-8"로 변경
    * /etc/default/locale 수정
        * LC_ALL="en_US.UTF-8"
        * LC_CTYPE="en_US.UTF-8"
* Debian 9.8 Stretch(2018. 12. 27.)
    * default 설정을 "en_US.UTF-8"로 변경
    * /etc/default/locale 수정
        * LC_ALL="en_US.UTF-8"
        * LC_CTYPE="en_US.UTF-8"


### 2018. 12. 11.
#### Image
* CentOS 6.5(2018. 12. 11.)
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결
* CentOS 6.10(2018. 12. 11.)
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결
* CentOS 7.1(2018. 12. 11.)
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결
* CentOS 7.5(2018. 12. 11.)
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결  
* Debian 8.11 Jessie(2018. 12. 11.)
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결
* Debian 9.6 Stretch(2018. 12. 11.)
    * 커널 업데이트: 4.9.0-8
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결
* Ubuntu Server 14.04.5 LTS(2018. 12. 11.)
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결
* Ubuntu Server 16.04.5 LTS(2018. 12. 11.)
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결
* Ubuntu Server 18.04.1 LTS(2018. 12. 11.)
    * 네트워크 인터페이스 또는 Subnet 추가/삭제 시 간헐적으로 발생하는 통신 오류 해결


### 2018. 11. 13.
#### Image
* CentOS 6.5(2018. 11. 13.)
    * 커널 업데이트: 2.6.32-754.6.3
    * Yum repository 대상을 최신 repository로 변경

* CentOS 7.1(2018. 11. 13.)
    * 커널 업데이트:  3.10.0-693.21.1
    * Yum repository 대상을 최신 repository로 변경


### 2018. 10. 23.
#### Image
* CentOS 6.5(2018. 10. 23.)
    * 패스워드 복잡도 설정: 숫자,영문,특문 조합 + 8자리 이상)(/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경(/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경(/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 CentOS Upstream을 유지함
    * 접근 보안성 강화를 위한 root 계정 접속 제한
        * 기존: root 계정의 ssh 접속 허용
        * 변경: 일반 User 계정인 "centos" 로 접속 후 전환
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지

* CentOS 6.10(2018. 10. 23.)
    * 패스워드 복잡도 설정: 숫자,영문,특문 조합 + 8자리 이상)(/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경(/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경(/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 CentOS Upstream을 유지함
    * 접근 보안성 강화를 위한 root 계정 접속 제한
        * 기존: root 계정의 ssh 접속 허용
        * 변경: 일반 User 계정인 "centos" 로 접속 후 전환
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지

* CentOS 7.1(2018. 10. 23.)
    * 패스워드 복잡도 설정: 숫자,영문,특문 조합 + 8자리 이상)(/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경(/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경(/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 CentOS Upstream을 유지함
    * 접근 보안성 강화를 위한 root 계정 접속 제한
        * 기존: root 계정의 ssh 접속 허용
        * 변경: 일반 User 계정인 "centos" 로 접속 후 전환
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지

* CentOS 7.5(2018. 10. 23.)
    * 패스워드 복잡도 설정: 숫자,영문,특문 조합 + 8자리 이상)(/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경(/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경(/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 CentOS Upstream을 유지함
    * 접근 보안성 강화를 위한 root 계정 접속 제한
        * 기존: root 계정의 ssh 접속 허용
        * 변경: 일반 User 계정인 "centos" 로 접속 후 전환
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지

* Ubuntu Server 14.04.5 LTS(2018. 10. 23.)
    * 패스워드 복잡도 설정: 숫자,영문,특문 조합 + 8자리 이상)(/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경(/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경(/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 Ubuntu Server 14.04 LTS Upstream을 유지함
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지

* Ubuntu Server 16.04.5 LTS(2018. 10. 23.)
    * 패스워드 복잡도 설정: 숫자,영문,특문 조합 + 8자리 이상)(/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경(/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경(/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 Ubuntu Server 16.04 LTS Upstream을 유지함
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지

* Debian 8.11 Jessie(2018. 10. 23.)
    * 패스워드 복잡도 설정: 숫자,영문,특문 조합 + 8자리 이상)(/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경(/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경(/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 Debian 8 Upstream을 유지함
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지

* Debian 9.5 Stretch(2018. 10. 23.)
    * 패스워드 복잡도 설정: 숫자,영문,특문 조합 + 8자리 이상)(/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경(/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경(/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * 나머지 설정은 Debian 9 Upstream을 유지함
    * 인스턴스 생성시 swap partition 을  생성하지 않음
    * /etc/hosts 파일의 사용자 추가 설정 유지

### 2018. 09. 20.
#### Instance
* Instance 관리 화면 UX/UI 개선
    * 인스턴스 이름 조회 기능 추가
    * 가용성 영역, 인스턴스 상태로 필터 추가
* Instance 생성 화면 기능 및 UX/UI 개선
    * 플로팅 IP 사용 여부 선택 기능 추가
    * 보안 그룹 생성 및 정책 확인 기능 추가
    * 추가 블록 스토리지 연결 기능 추가
    * 사용자 스크립트 등록 기능 추가

#### Image
* Ubuntu Linux 14.04.5(2018. 09. 20.)
    * 2018. 09. 20. 신규로 적용되는 사용자 스크립트 기능이 정상적으로 적용되지 않는 부분 해결

* Ubuntu Server 18.04.1 LTS(2018. 09. 20.)
    * 취약점 패치를 위한 관련 커널 업데이트
        * Kernel 4.15.0-29
        * meltdown/spectre variant 1,2,3(CVE-2017-5753, 5715, 5754) 패치(retpoline)
    * 패스워드 복잡도 설정: 숫자,영문,특문 조합 + 8자리 이상)(/etc/pam.d/common-password 수정)
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * ssh 설정 변경(/etc/ssh/sshd_config 수정)
        * PermitRootLogin no                # root 접속 비활성화
        * PasswordAuthentication no         # 패스워드 인증 비활성화
    * 취약점 대비 커널 파라메터 변경(/etc/sysctl.conf 수정)
        * net.ipv4.conf.all.accept_redirects = 0 # icmp redirect 공격 차단
        * net.ipv4.conf.all.accept_source_route = 0 # 소스라우팅 차단을 통한 ip 스푸핑 방지
        * net.ipv4.conf.all.log_martians = 1 # 스푸핑 로깅
        * net.ipv4.icmp_echo_ignore_broadcasts = 1 # smurf dos 공격 방어
        * net.ipv4.icmp_ignore_bogus_error_responses = 1 # ip 혹은 tcp 헤더가 깨진 bad icmp 패킷 무시
        * net.ipv4.tcp_syncookies=1 # syn 플루딩 공격 방어를 위한 syn cookies 사용
    * 터미널 접근 제한( /etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * 추가 변경 사항
        * Instance 생성시 swap partition 을 생성하지 않음( 필요시 사용자가 별도 생성 )
    * 나머지 설정은 Ubuntu Server 18.04 LTS upstream 을 유지함

### 2018. 08. 09.
#### Image
* Debian 9.4.0(2018. 08. 09.)
    * 취약점 패치를 위한 관련 커널 업데이트
        * Kernel 4.9
        * meltdown/spectre variant 1,2,3(CVE-2017-5753, 5715, 5754) 패치(retpoline)
    * 패스워드 복잡도 설정(숫자,영문,특문 조합 + 8자리 이상): /etc/pam.d/common-password에 아래 line 추가
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * 불필요 계정/그룹 삭제
        * user: lp, sync, uucp, games
        * group: dip
    * 취약점 대비 커널 파라메터 변경(sysctl)
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
    * Profile 추가(/etc/profile)
    * 터미널 접근 제한(/etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * HISTSIZE=500       # history list에 저장될 command 수 제한
    * HISTFILESIZE=0     # history file에 저장될 command 없음
    * 시스템 로그인전 배너 설정 제거
        * /etc/issue, /etc/issue.net 삭제

* Windows 2012 R2 STD(2018. 08. 09.)
    * 기본으로 영문 버전 제공, 한글 사용시 사용자가 한글 언어팩을 설치하도록 변경
    * 2018년 7월 10일 보안업데이트 적용( https://support.microsoft.com/en-us/help/4338815/windows-81-update-kb4338815 )
    * 계정 관리
        * Interactive logon: Display user information when the session is locked : User display name only
        * Interactive logon: Do not display last user name :  Enabled
        * Interactive logon: Prompt user to change password before expiration : 14days
        * Shut down the system : Administrators
    * 서비스 관리
        * NTP 설정: 1.pool.ntp.org, time,windows.com
        * NTP 동기화 주기:  256초
    * 시스템 관리
        * Network access: Do not allow anonymous enumeration of SAM accounts : Enabled
        * Network access: Do not allow anonymous enumeration of SAM accounts and shares : Enabled
        * Autologin 기능 제한:  AutoAdminLogon 값을 0 으로 설정

* Windows 2016 STD(2018. 08. 09.)
    * 2018년 7월 24일(https://support.microsoft.com/en-us/help/4338822/windows-10-update-kb4338822)
    * 계정 관리
        * Interactive logon: Display user information when the session is locked : User display name only
        * Interactive logon: Do not display last user name :  Enabled
        * Interactive logon: Prompt user to change password before expiration : 14days
        * Shut down the system : Administrators
    * 서비스 관리
        * NTP 설정: 1.pool.ntp.org, time,windows.com
        * NTP 동기화 주기:  256초
    * 시스템 관리
        * Network access: Do not allow anonymous enumeration of SAM accounts : Enabled
        * Network access: Do not allow anonymous enumeration of SAM accounts and shares : Enabled


### 2018. 07. 16.
#### Image
* Ubuntu 16.04.4 LTS(2018. 07. 16.)
    * 취약점 패치를 위한 관련 커널 업데이트
        * Kernel 4.4.0-130
        * meltdown/spectre variant 1,2,3(CVE-2017-5753, 5715, 5754) 패치(retpoline)
    * 패스워드 복잡도 설정(숫자,영문,특문 조합 + 8자리 이상): /etc/pam.d/common-password에 아래 line 추가
        * password requisite  pam_cracklib.so try_first_pass retry=3 minlen=8 lcredit=-1 dcredit=-1 ocredit=-1 type=
    * 불필요 계정/그룹 삭제
        * user: lp, sync, uucp, games
        * group: dip
    * 취약점 대비 커널 파라메터 변경(sysctl)
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
    * Profile 추가(/etc/profile)
    * 터미널 접근 제한(/etc/securetty 수정)
        * console, vc/1, vc/2, tty1, tty2, ttyS0 외 접근 불가
    * 터미널로부터 120분 이상 사용자입력 없을시 세션 종료(/etc/profile 수정)
        * TMOUT=7200
    * HISTSIZE=500       # history list에 저장될 command 수 제한
    * HISTFILESIZE=0     # history file에 저장될 command 없음
    * 시스템 로그인전 배너 설정 제거
        * /etc/issue, /etc/issue.net 삭제

* Windows 2008 R2 STD(2018. 07. 16.)
    * 2018년 6월 12일자 보안 업데이트 적용( https://support.microsoft.com/ko-kr/help/4284826 )
    * 계정 관리
        * Guest 계정 사용 제한: Guest 계정 사용 안함으로 변경
        * 마지막 사용자 로그인 이름 표시:  표시 안함으로 설정
        * 세션이 잠긴경우 사용자 정보표시: 사용자 이름만 표시로 설정
        * 암호만료 전에 변경 알림: 변경 알림 14일로 설정
        * 일반 사용자의 시스템 종료 제한: 시스템 종료 정책을 Administrator 로 설정
    * 서비스 관리
        * NTP 설정: 1.pool.ntp.org, time,windows.com
        * NTP 동기화 주기:  256초
    * 시스템 관리
        * SAM 계정과 공유의 익명열거 허용 안함:  SAM 계정관련  익명열거 허용 안함 항목 사용
        * 로그온 하지 않고 시스템 종료허용  제한:  로그온하지 않고 시스템 종료 허용 정책을 사용 안함으로 설정
        * Autologin 기능 제한:  AutoAdminLogon 값을 0 으로 설정

* Windows 2012 R2 STD(2018. 07. 16.)
    * Auto scale 기능으로 백신이 포함된 인스턴스 생성시 발생하는 에러 현상 수정
    * CPU 설정 변경( CPU Socket 최대 개수  4개 )
    * Network  인터페이스 속도  10G 로 표시

### 2018. 05. 29.
#### Auto Scale
* Auto Scale의 반복성 예약 작업(cron expression 기반) 관련 오류 수정
    * 반복성 예약 작업 실행 시점이  UTC를 기반으로  동작하는 오류 수정
    * 반복성 예약 작업의 최초 실행이 cron expression을 따르지 않고, 예약 작업 생성 시 설정한 '시작 시각'에 수행되는 오류 수정

#### Instance
* Instance 생성 시 volume type 설정 기능 추가


### 2018. 04. 24.
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
* CentOS Linux 6.5(2018. 02. 22.)
    * 호스트명 설정 변경
        * 인스턴스 생성시 지정한 이름으로 호스트명 적용되도록 수정
        * [기존] localhost-192.168.0.x > [변경] 콘솔에서 지정한 이름
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version: [기존] 2.6.32-431 > [변경] 2.6.32-696.20.1
        * Variant 1(CVE-2017-5753) - patched
        * Variant 3(CVE-2017-5754) - patched

* CentOS Linux 7.1(2018. 02. 22.)
    * 호스트명 설정 변경
        * 인스턴스 생성시 지정한 이름으로 호스트명 적용되도록 수정
        * [기존] localhost-192.168.0.x > [변경] 콘솔에서 지정한 이름
    * Firewall daemon default 값 변경
        * 인스턴스 부팅시 Firewall daemon 자동 시작되지 않도록 설정 변경
    * Swap Disk Mount 설정 변경
        * 신규 인스턴스 생성시 swap 파티션 자동 마운트되도록 설정 변경
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version: [기존] 3.10.0-229.20.1 > [변경] 3.10.0-693.17.1
        * Variant 1(CVE-2017-5753) - patched
        * Variant 3(CVE-2017-5754) - patched

* Debian Linux 8.2.0(2018. 02. 22.)
    * 호스트명 설정 변경
        * 인스턴스 생성시 지정한 이름으로 호스트명 적용되도록 수정
        * [기존] localhost-192.168.0.x > [변경] 콘솔에서 지정한 이름
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version: [기존] 3.16.0-4 > [변경] 3.16.0-5
        * Variant 3(CVE-2017-5754) - patched

* Ubuntu Linux 14.04.5(2018. 02. 22.)
    * 취약점 패치를 위한 관련 커널 업데이트
        * Linux Kernel Version: [기존] 3.13.0-32 > [변경] 3.13.0-141
        * Variant 1(CVE-2017-5753) - patched
        * Variant 3(CVE-2017-5754) - patched

* Windows 2012 R2 STD(2018. 02. 22.)
    * Windows Time Zone 설정 변경
        * 동기화 주기 변경: [기존) 604800초(7일) > [변경] 256초
        * Time Zone Peer 도메인 변경: [기존] 1.kr.pool.ntp.org , 1.pool.ntp.org > [변경] 1.pool.ntp.org , time.windows.com
    * 2018년 02월 13일 보안 업데이트: https://support.microsoft.com/ko-kr/help/4074594/windows-81-update-kb-4074594

* 신규 이미지 추가
    * CentOS Linux 6.5 with MySQL 5.6.38(2018. 02. 22.)
        * MySQL 5.6.38 패키지 설치됨
        * 그외 설정은 CentOS Linux 6.5 이미지와 동일함
    * CentOS Linux 6.5 with MySQL 5.7.20(2018. 02. 22.)
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
    * 사양 변경을 위해 인스턴스는 중지 상태여야 함
    * 자세한 제약 사항은 가이드 문서 [인스턴스 사양 변경](/Compute/Instance/ko/console-guide/#_14) 참조
* Low IOPS SSD 사양(U 타입)이 추가
    * 합리적인 가격의 저사양 인스턴스 지원
    * Linux 계열 OS만 지원
    * Local Disk를 이용하기 때문에 하드웨어 장애시 데이터 복구가 불가능
* High IOPS SSD 사양(I 타입)이 추가
    * 높은 IOPS를 보장(보장 IOPS는 가격표 참조)
    * Linux 계열 OS만 지원
* 인스턴스 사용량 조회시 값이 조회되지 않는 버그가 수정


### 2017. 05. 25.
#### Instance
* 서비스 종료된 이미지로 생성된 인스턴스가 조회 되지 않는 버그 수정

#### Image
* Windows 계열 이미지 업데이트
    * Windows 2012 R2 STD(2017. 05. 25.) 추가


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
    * 인스턴스의 이름은 20자 이하 영숫자와 **.**(dot),**-**(dash) 문자만 허용
* 인스턴스 생성 기능을 이미지 생성 기능으로 변경
    * 탭과 일관된 기능으로 변경

#### Image
* 이미지 탭(Private, Shared, Public) 변경시 이미지 선택이 해제되지 않던 문제 수정


### 2016. 12. 22.
#### Instance
* 정지된 인스턴스의 보안 그룹 수정이 가능하도록 변경
* 인스턴스 생성시 선택 가능한 보안 그룹이 하나일 경우 자동 선택되도록 변경
