## Infrastructure > Compute & Network > Release Notes

### 2016.12.22

#### 기능 개선/변경

##### Instance
* [Console] 정지된 Instance의 Security Group 수정이 가능하도록 변경
* [Console] Instance 생성시 선택 가능한 Security Group이 하나일 경우 자동 선택되도록 변경

#### 버그 수정

##### Load Balancer
* [Console] Health Check Protocol이 TCP인 경우 Listener 내용 수정이 안되는 문제 수정

##### Floating IP
* [Console] Floating IP에 연결된 Load Balancer의 이름이 노출되지 않는 문제 수정

##### Security Group
* [Console] 중복된 Rule 추가 시 Security Group 목록이 사라지는 문제 수정

### 2016.12.08

#### 버그 수정

##### Load Balancer

* [Console] Load Balancer의 Heath check url 미노출 문제 수정
* [Console] Listener 수정 버튼 클릭시 기등록한 Health Check URL이 아닌 "/"로 노출되는 문제 수정

### 2016.11.29

#### 버그 수정

##### Load Balancer

* [API] TERMINATED_HTTPS type의 Load Balancer 생성 실패하던 문제 수정

### 2016.11.24

#### 기능 개선/변경

##### Load Balancer

* [Console] Load Balancer의 Listener별 세션 제한 값 노출

#### 버그 수정 

##### Load Balancer

* [API] 특정 Project에서 Load Balancer 생성 실패하던 문제 수정

### 2016.10.06

#### 버그 수정

##### Monitoring

* [Console]  Monitoring의 알람 설정시 receiver 추가가 불가능하던 문제 수정

### 2016.08.04

#### 기능 개선/변경

##### Load Balancer

* [API] Load Balancer의 SSL offloading 기능 추가

#### 버그 수정

##### Load Balancer

* [API] Load Balancer 제거 시 간헐적으로 정상 종료되지 않던 문제 수정
