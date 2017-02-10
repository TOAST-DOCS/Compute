## Infrastructure > Compute & Network > Release Notes

### 2017.02.23

#### 기능 개선/변경

##### Instance

* Flavor 정보 노출 변경
    * 기존 툴팁 형식에서 컬럼에 노출하도록 변경

##### LoadBalancer

* 등록된 리스너가 1개일 때 삭제 불가 알림 팝업이 뜨도록 변경

##### Floating IP

* Floating IP 삭제 시 인스턴스 혹은 로드밸런서가 연결되어 있을 경우 삭제 할 수 없도록 변경
* 명칭변경 : "포트" -> "네트워크 인터페이스"
    * 인스턴스에 Floating IP를 붙일 때 대상이 되는 명칭을 기존 “포트”에서 “네트워크 인터페이스”로 변경

### 2017.01.19

#### 기능 개선/변경

##### Instance

* 인스턴스 기본 정보의 IP 주소 정보에서 Subnet Network 명칭을 표시하지 않음
    * 명칭 표기로 줄이 길어지는 것을 방지
* 인스턴스 이름 길이 및 특수문자 제한
    * 20자 이하 영숫자와 ‘.’, ‘-‘ 문자만 허용하도록 변경

##### Image

* “Instance 생성” 기능을 “Image 생성” 기능으로 변경

##### Volume

* Volume 연결관리 기능에 같은 존의 인스턴스에만 연결이 가능함을 명시

#### 버그 수정

##### Image

* 이미지 탭(Private, Shared, Public) 변경시 이미지 선택이 해제되지 않던 문제 수정

##### Volume

* Snapshot을 이용하여 Volume 생성시 간헐적으로 실패하는 문제 수정

##### Load Balancer

* Load Balancer 생성시 연결 제한 설정이 적용되지 않는 문제 수정

### 2016.12.22

#### 기능 개선/변경

##### Instance
* 정지된 Instance의 Security Group 수정이 가능하도록 변경
* Instance 생성시 선택 가능한 Security Group이 하나일 경우 자동 선택되도록 변경

#### 버그 수정

##### Load Balancer
* Health Check Protocol이 TCP인 경우 Listener 내용 수정이 안되는 문제 수정

##### Floating IP
* Floating IP에 연결된 Load Balancer의 이름이 노출되지 않는 문제 수정

##### Security Group
* 중복된 Rule 추가 시 Security Group 목록이 사라지는 문제 수정

### 2016.12.08

#### 버그 수정

##### Load Balancer

* Load Balancer의 Heath check url 미노출 문제 수정
* Listener 수정 버튼 클릭시 기등록한 Health Check URL이 아닌 "/"로 노출되는 문제 수정

### 2016.11.29

#### 버그 수정

##### Load Balancer

* TERMINATED_HTTPS type의 Load Balancer 생성 실패하던 문제 수정

### 2016.11.24

#### 기능 개선/변경

##### Load Balancer

* Load Balancer의 Listener별 세션 제한 값 노출

#### 버그 수정 

##### Load Balancer

* 특정 Project에서 Load Balancer 생성 실패하던 문제 수정

### 2016.10.06

#### 버그 수정

##### Monitoring

*  Monitoring의 알람 설정시 receiver 추가가 불가능하던 문제 수정

### 2016.08.04

#### 기능 개선/변경

##### Load Balancer

* Load Balancer의 SSL offloading 기능 추가

#### 버그 수정

##### Load Balancer

* Load Balancer 제거 시 간헐적으로 정상 종료되지 않던 문제 수정
