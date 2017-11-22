## Infrastructure > Compute & Network > Release Notes

### 2017.11.23

#### 버그 수정
* Load Balancer 생성시 리스너의 연결 제한값이 잘못 표기되는 현상을 수정하였습니다.

### 2017.10.26

#### 버그 수정
* Load Balancer 생성시 인증서가 등록되지 않는 버그가 수정되었습니다.

### 2017.09.21

#### 기능 추가
* Public API 추가
    * Object Storage에 이어 Compute&Network 상품을 API를 이용해 관리할 수 있습니다.
    * 현재 제한적인 기능만 이용할 수 있으며, 추후 API 추가를 통해 기능이 확장될 예정입니다.
    * 지원되는 API는 Developer Guide를 참고하시기 바랍니다.

#### 버그 수정
* Keypair를 지정하지 않고 Instance를 생성할 수 있었던 버그가 수정되었습니다.
* Member 권한 제한
    * Project에 Admin 권한이 없는 사용자가 security group을 수정할 수 없도록 수정되었습니다.
    * Project에 Admin 권한이 없는 사용자에게는 Network 메뉴가 노출되지 않도록 수정되었습니다.

### 2017.08.24

#### 기능 추가
* Instance Flavor를 변경할 수 있도록 기능이 추가되었습니다.
    * 사용하던 Instance의 data는 그대로 보존하면서 CPU/Memory를 업그레이드 하거나 다운그레이드 할 수 있습니다.

    * 제약 사항
        * Block Storage size는 변경이 불가능합니다.
        * Flavor 변경을 위해 Instance는 shutdown 상태여야 합니다.
        * 자세한 제약 사항은 홈페이지 참조(https://cloud.toast.com/pricing)

* Low IOPS SSD Flavor가 추가되었습니다.
    * 좀 더 낮은 가격에 Instance를 이용할 수 있도록 저사양 Flavor가 추가되었습니다.
    * 제약 사항
        * 리눅스 계열 OS 만 지원합니다.
        * Local Disk를 이용하기 때문에 하드웨어 장애시 데이터 복구가 불가능할 수 있습니다.
        * 자세한 제약 사항은 홈페이지 참조(https://cloud.toast.com/pricing)

* High IOPS SSD Flavor 추가되었습니다.
    * 높은 IOPS가 필요한 경우 High IOPS SSD Flavor를 이용하면 수준의 높은 IOPS를 보장 받을 수 있습니다. (보장 IOPS는 가격표 참조)
    * 제약 사항
        * 리눅스 계열 OS 만 지원합니다.
        * Local Disk를 이용하기 때문에 하드웨어 장애시 데이터 복구가 불가능할 수 있습니다.
        * 자세한 제약 사항은 홈페이지 참조(https://cloud.toast.com/pricing)

#### 버그 수정
* Instance 사용량 조회시 값이 조회되지 않는 버그가 수정되었습니다.
* Load Balancer 서비스의 세션 지속성 항목이 제대로 표시되지 않던 버그가 수정되었습니다.

### 2017.07.20

#### 버그 수정

##### Image

* 대용량 이미지 생성시 간헐적으로 생성이 완료되지 않던 버그가 수정되었습니다.

##### Volume

* 볼륨 생성시 간헐적으로 생성이 완료되지 않던 버그가 수정되었습니다.

### 2017.07.10

#### 기능 추가

##### NAS(Offline)

* NAS(Offline) 서비스가 추가됩니다.
    * NAS(Offline) 서비스는 고성능의 NAS(Network Attached Storage)를 TOAST Cloud 서버 고객이 사용할 수 있도록 제공하는 서비스입니다.

### 2017.05.25

#### 기능 추가

##### Instance

* 윈도우 이미지(Windows 2012 r2)가 추가됩니다.

#### 버그 수정

##### Instance

* 서비스 종료된 이미지로 생성된 인스턴스가 조회 되지 않는 버그가 수정되었습니다.

### 2017.04.25

#### 기능 개선

##### Instance

* 인스턴스 생성시 초기 불륨 크기의 최대값이 600GB에서 1TB(1000GB)로 변경됩니다.

### 2017.04.20

#### 버그 수정

##### Monitoring

* 추가 볼륨이 없는 인스턴스의 사용량 조회가 불가능하던 버그가 수정됩니다.

##### Load Balancer

* Listener에 인증서 파일 업로드시 간헐적으로 인증서 등록창이 사라지는 버그가 수정됩니다.

### 2017.03.23

#### 기능 개선

##### Instance

* 인스턴스 생성시 사용자가 초기 볼륨의 크기를 지정할 수 있게 됩니다.
    * [기존] Flavor에 지정된 크기로 초기 볼륨 생성 -> [변경] 사용자가 지정한 크기 만큼 초기 볼륨을 생성
    * 볼륨의 크기는 이미지 최소 요구 사항에서 최대 600GB 까지 설정할 수 있습니다.

#### 버그 수정

##### Floating IP

* Floating IP 연결 팝업에서 "생성" 버튼이 노출되지 않는 문제가 수정됩니다.

### 2017.02.23

#### 기능 개선/변경

##### Load Balancer

* 로드밸런서에 등록된 리스너가 1개일 경우 삭제할 수 없다는 것을 알리도록 변경합니다.
    * 기존에도 삭제가 되지 않았으나 사용자에게 별다른 알림이 없어 혼동을 주었습니다.<br/>이제 사용자에게 명시적으로 삭제할 수 없다고 메시지를 공지하도록 변경합니다.

##### Floating IP

* Floating IP 삭제 시 인스턴스 혹은 로드밸런서가 연결되어 있을 경우 삭제 할 수 없도록 변경합니다.
    * 기존에는 인스턴스나 로드밸런서가 연결되어 있는 Floating IP를 삭제할 수 있어 서비스에 장애를 일으킬 수 있었습니다.<br/>이런 실수를 미연에 방지할 수 있도록 연결이 있는 Floating IP는 삭제할 수 없도록 변경합니다.
* 명칭변경 : '포트' -> '네트워크 인터페이스'
    * 인스턴스에 Floating IP를 붙일 때 대상이 되는 명칭을 기존 “포트”에서 “네트워크 인터페이스”로 변경합니다.

### 2017.01.19

#### 기능 개선/변경

##### Instance

* 인스턴스 기본 정보의 IP 주소 정보에서 Subnet Network 명칭을 표시하지 않습니다.
    * 명칭 표기로 행의 넓이가 넓어져 가독성이 떨어지는 것을 방지합니다.
* 인스턴스 이름 길이 및 특수문자 제한합니다.
    * 이제부터 생성 및 수정되는 인스턴스의 이름은 20자 이하 영숫자와 ‘.’, ‘-‘ 문자만 허용합니다.

##### Image

* “Instance 생성” 기능을 “Image 생성” 기능으로 변경합니다.
    * 탭과 일관된 기능으로 변경하였습니다.

##### Volume

* Volume 연결관리 기능에 같은 존의 인스턴스에만 연결이 가능함을 명시합니다.
    

#### 버그 수정

##### Image

* 이미지 탭(Private, Shared, Public) 변경시 이미지 선택이 해제되지 않던 문제를 수정하였습니다.

##### Volume

* Snapshot을 이용하여 Volume 생성시 간헐적으로 실패하는 문제를 수정하였습니다.

##### Load Balancer

* Load Balancer 생성시 연결 제한 설정이 적용되지 않는 문제를 수정하였습니다.

### 2016.12.22

#### 기능 개선/변경

##### Instance
* 정지된 Instance의 Security Group 수정이 가능하도록 변경합니다.
    * 의도와 다르게 기존에는 정지되어 있는 인스턴스에 Security Group 수정이 불가능하였습니다.<br/>이를 수정하여 정지된 인스턴스도 Security Group을 변경할 수 있도록 하였습니다.
* Instance 생성시 선택 가능한 Security Group이 하나일 경우 자동 선택되도록 변경합니다.

#### 버그 수정

##### Load Balancer
* Health Check Protocol이 TCP인 경우 Listener 내용 수정이 안되는 문제를 수정하였습니다.

##### Floating IP
* Floating IP에 연결된 Load Balancer의 이름이 노출되지 않는 문제를 수정하였습니다.

##### Security Group
* 중복된 Rule 추가 시 Security Group 목록이 사라지는 문제를 수정하였습니다.

### 2016.12.08

#### 버그 수정

##### Load Balancer

* Load Balancer의 Heath check url이 미노출되는 문제를 수정하였습니다.
* Listener 수정 버튼 클릭시 기등록한 Health Check URL이 아닌 "/"로 노출되는 문제를 수정하였습니다.

### 2016.11.29

#### 버그 수정

##### Load Balancer

* TERMINATED_HTTPS type의 Load Balancer 생성이 실패하던 문제를 수정하였습니다.

### 2016.11.24

#### 기능 개선/변경

##### Load Balancer

* Load Balancer의 Listener별 세션 제한 값을 노출하도록 변경하였습니다.

#### 버그 수정 

##### Load Balancer

* 특정 Project에서 Load Balancer 생성 실패하던 문제를 수정하였습니다.

### 2016.10.06

#### 버그 수정

##### Monitoring

*  Monitoring의 알람 설정시 receiver 추가가 불가능하던 문제를 수정하였습니다.

### 2016.08.04

#### 기능 개선/변경

##### Load Balancer

* Load Balancer의 SSL offloading 기능을 추가하였습니다.

#### 버그 수정

##### Load Balancer

* Load Balancer 제거 시 간헐적으로 정상 종료되지 않던 문제를 수정하였습니다.
