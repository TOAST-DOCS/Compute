## Infrastructure > Compute & Network > Load Balancers Guide Guide

Load Balancer는 여러 대의 Instance에 Network 트래픽을 분산시키는 장비입니다. 사용자는 TOAST Cloud 웹 콘솔을 통해 Load Balancer를 생성한 뒤 여러 Instance를 연결하여 부하를 분산시킬 수 있습니다. 뿐만 아니라 고객이 설정한 health check 패턴에 따라 장애가 발생한 Instance를 자동으로 검출하여 트래픽을 분산 제어하기 때문에 HA상황에 대한 보완책으로서도 이용할 수 있습니다.

이 문서에서는 다음과 같은 내용을 다룹니다.

- Load Balancer 생성
- Load Balancer 상세 정보 변경
- Instance 연결, 해제
- Floating IP

## Load Balancer 생성

1.[Infrastructure] > [Compute & Network] > [Load Balancers]으로 이동한 후 [그림 1]의 [+ Load Balancer 생성] 버튼을 클릭합니다.

![[그림 1] Load Balancer 생성](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_001.png)
<center>[그림 1] Load Balancer 생성</center>

2.<Load Balancer 생성> 대화창에서 Load Balancer 정보를 입력합니다. 필요한 정보는 다음과 같습니다.

- **이름**  
  생성할 Load Balancer의 이름을 입력합니다.
- **설명**  
  생성할 Load Balancer에 대한 설명을 입력합니다.
- **Network (Subnet)**  
  Load Balancer가 연결될 Network를 선택합니다. Load Balancer와 Instance들은 반드시 같은 Network에 있어야 합니다.

![[그림 2] Load Balancer 정보 입력](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_002.png)
<center>[그림 2] Load Balancer 정보 입력</center>

3.다음으로 Listener를 등록합니다. Listener 등록 시 필요한 정보는 크게 세 가지로 구분됩니다. 각각은 다음과 같습니다.

**Listener 등록**

- **Load Balancing이름**  
Network 트래픽을 분산시키는 방법을 선택합니다. TOAST Cloud에서 지원하는 방식은 총 3가지 입니다. Round Robin: Load Balancer에 연결된 Instance들 중 트래픽을 보낼 Instance를 순차적으로 선택합니다. Least Connection: Load Balancer에 연결된 Instance들 중 현재 가장 connection이 적은 Instance에게 트래픽을 전달합니다. Source IP: Load Balancer에 연결된 Instance들에게 가중치를 부여하고, 가중치에 따라 요청 IP와 Instance간의 관계를 맺습니다. 이 후 요청 IP를 보고 정해진 Instance에게 트래픽을 전달하게 됩니다.
- **Protocol**
Load Balancing하려는 Protocol을 선택합니다. TCP, HTTP, HTTPS, TERMINATED_HTTPS 중 하나를 선택할 수 있습니다.
- **Network (Subnet)**
Load Balancer가 연결될 Network를 선택합니다. Load Balancer와 Instance들은 반드시 같은 Network에 있어야 합니다.
- **Load Balancer Port**
외부로 서비스할 Load Balancer의 Port를 입력합니다. Instance에 접근하려는 사용자는 반드시 이 Port를 통해 접근해야 합니다.
- **Instance Port**
Instance들의 서비스 Port를 입력합니다. Load Balancer는 Load Balancer Port를 통해 들어온 외부 트래픽을 Load Balancing 방식에서 지정한 알고리즘을 통해 선택된 Instance의 Instance Port로 전달하게 됩니다.
- **SSL 인증서**
Protocol 항목을 TERMINATED_HTTPS로 선택했을 때 사용할 인증서와 사설키를 등록합니다. Load Balancer에 인증서와 사설키를 등록하는 경우 외부 HTTPS 트래픽을 해석하여 HTTP 형태로 변환해주는 SSL Offloading 기능을 사용할 수 있습니다.

**Health Check**

- **Health Check Protocol**
Health check에 사용할 Protocol 종류를 선택합니다. TCP, HTTP, HTTPS 중 하나를 선택할 수 있습니다.
- **Health Check Port**
Health check에 사용할 Instance의 Port를 입력합니다.
- **HTTP Method**
Health check에 사용할 HTTP method를 선택합니다. Health Check Protocol을 HTTP 또는 HTTPS로 선택했을 때 사용가능하며, 현재는 GET만을 지원합니다.
- **HTTP Status Code**
Health Check Protocol로 HTTP 또는 HTTPS를 선택했을 때, health check 를 시도한 뒤 Instance 로부터 받을 HTTP 상태 코드를 입력합니다.
- **URL**
Health Check Protocol로 HTTP 또는 HTTPS를 선택했을 때, health check 를 시도할 URL을 입력합니다.
- **Health Check 주기**
Health check 주기를 입력합니다. 이 항목에 입력된 시간 마다 Instance의 상태를 확인합니다. 단위는 초입니다.
- **최대 응답 대기시간**
Instance  응답 대기 시간을 입력합니다. Instance 상태를 확인했을 때 이 항목에 입력된 시간만큼 기다립니다. 단위는 초입니다.
- **최대 재시도 횟수**
Health check의 재시도 횟수를 입력합니다. Instance 의 응답이 없을 경우 이 항목에 입력된 횟수만큼 재시도합니다. 지정된 횟수만큼 시도했음에도 응답이 없다면, 해당 Instance를 Load Balancing 대상에서 제외합니다. 1에서 10 사이의 수를 지정할 수 있습니다.

**Connection**

- **세션 지속성**
외부에서 들어온 요청의 session을 유지하기 위한 방법을 선택합니다. 서비스에 따라 특정 요청은 같은 Instance로 연결되어야 할 때가 있습니다. 이를 위해 TOAST Cloud에서는 Source IP, HTTP Cookie, APP Cookie 방식을 지원합니다.
- **연결 제한**
Load Balancer가 처리할 수 있는 최대 connection 수를 설정합니다. 아무런 값도 입력하지 않으면 2000개로 설정됩니다. 필요한 경우 Listener 정보 보기 화면에서 조정할 수 있습니다.

![[그림 3] Listener 등록](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_003.png)
<center>[그림 3] Listener 등록</center>

![[그림 4] TERMINATED_HTTPS 방식으로 설정된 Listener](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_004.png)
<center>[그림 4] TERMINATED_HTTPS 방식으로 설정된 Listener</center>

![[그림 5] SSL 인증서 등록 대화창](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_005.png)
<center>[그림 5] SSL 인증서 등록 대화창</center>

4.Load Balancer에 연결할 Instance를 선택합니다. 앞서 선택한 Network에 있는 Instance들만 선택할 수 있습니다.

![[그림 6] Instance 선택](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_006.png)
<center>[그림 6] Instance 선택</center>

5.입력한 설정을 저장하기 위해 [그림 7]의 [Load Balancer 생성] 버튼을 누릅니다.

![[그림 7] Load Balancer 생성](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_007.png)
<center>[그림 7] Load Balancer 생성</center>

6.잠시 기다리면 [그림 8]과 같이 [Infrastructure] > [Compute & Network] > [Load Balancers]에서 Load Balancer가 생성됨을 확인할 수 있습니다.

![[그림 8] Load Balancer 생성 확인](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_008.png)
<center>[그림 8] Load Balancer 생성 확인</center>

## Load Balancer 상세 정보 수정

필요한 경우 이미 생성된 Load Balancer의 속성을 변경할 수 있습니다.

### Load Balancer 속성 변경

1.[Infrastructure] > [Compute & Network] > [Load Balancers]에서 수정할 Load Balancer를 선택합니다.

![[그림 9] 수정할 Load Balancer 선택](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_009.png)
<center>[그림 9] 수정할 Load Balancer 선택</center>

2.[그림 9] 하단의 <Load Balancer 상세 정보> 탭에서 수정할 속성 옆의 “(Edit)”를 클릭합니다. “(Edit)”가 없는 속성은 변경이 불가능합니다.

![[그림 10] Load Balancer 속성 수정](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_010.png)
<center>[그림 10] Load Balancer 속성 수정</center>

3.<Load Balancer 수정> 대화창에서 원하는 항목을 수정한 후, "변경사항을 저장" 버튼을 누르면 반영됩니다.

### Listener 속성 변경

1.보다 세부적인 구성을 변경하기 위해 <Listener> 탭을 선택합니다.

![[그림 11] Listener 탭](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_011.png)
<center>[그림 11] Listener 탭</center>

2.<Listener> 탭에서는 현재 선택된 Load Balancer에 정의된 Listener들의 설정을 확인하고 수정할 수 있습니다. 수정하기 원하는 Listener의 [수정] 버튼을 선택합니다.

![[그림 12] Listener 수정 버튼](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_012.png)
<center>[그림 12] Listener 수정 버튼</center>

3.설정을 수정한 후 [변경] 버튼을 선택합니다.

![[그림 13] Listener 수정 대화창](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_013.png)
<center>[그림 13] Listener 수정 대화창</center>

4.설정이 변경되었음을 확인합니다.

![[그림 14] Listener 수정 확인](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_014.png)
<center>[그림 14] Listener 수정 확인</center>

5.새로운 Listener를 추가하려면 상단의 [+ Listener 추가] 버튼을 누릅니다.

![[그림 15] Listener 추가 버튼](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_031.png)
<center>[그림 15] Listener  추가 버튼</center>

> [주의]  
> 이미 존재하는 Listener와 동일한 Load Balancer Port를 갖는 Listener는 만들 수 없습니다.

6.필요없는 Listener를 삭제하려면 Listener별 [삭제] 버튼을 누릅니다.

![[그림 16] Listener 삭제 버튼](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_032.png)
<center>[그림 16] Listener 삭제 버튼</center>

> [주의]
> Listener가 하나인 경우에는 삭제할 수 없습니다.

## Load Balancer와 Instance 연결

필요한 경우 새로운 Instance를 추가로 연결하거나 기존에 연결된 Instance를 제거 할 수 있습니다.

1.[Infrastructure] > [Compute & Network] > [Load Balancers]에서 수정할 Load Balancer를 선택합니다.

![[그림 17] 수정할 load Balancer](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_015.png)
<center>[그림 17] 수정할 load Balancer</center>

2.[그림 17]의 [Instance]탭을 선택합니다.

![[그림 18] Instance 탭 선택](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_016.png)
<center>[그림 18] Instance 탭 선택</center>

3.새로운 Instance를 추가하려는 경우 [+Instance 추가]버튼을 선택합니다.

![[그림 19] Instance 추가](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_017.png)
<center>[그림 19] Instance 추가</center>

4.<Instance 추가> 대화창에서 연결할 Instance를 선택합니다.

![[그림 20] Instance 추가 대화창](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_018.png)
<center>[그림 20] Instance 추가 대화창</center>

5.[Infrastructure] > [Compute & Network] > [Load Balancers]에서 Instance를 추가한 Load Balancer를 선택하여 [그림 17]와 같이 Instance가 정상적으로 추가되었음을 확인합니다.

![[그림 21] Instance 추가 확인](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_019.png)
<center>[그림 21] Instance 추가 확인</center>

6.Instance를 삭제하기 위해서는 [Infrastructure] > [Compute & Network] > [Load Balancers]에서 Instance를 삭제할 Load Balancer를 선택합니다. 그리고 Instance탭에서 삭제할 Instance를 선택한 뒤 [Instances 연결 해제]버튼을 클릭합니다.

![[그림 22] 삭제할 Instance 선택](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_020.png)
<center>[그림 22] 삭제할 Instance 선택</center>

7.<Instances 연결 해제를 확인하세요.> 대화창에서 [Instance연결 해제] 버튼을 클릭합니다.

![[그림 23] Instance 연결 해제 대화창](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_021.png)
<center>[그림 23] Instance 연결 해제 대화창</center>

8.[그림 24]과 같이 Instance가 삭제되었음을 확인합니다.

![[그림 24] Instance 삭제 확인](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_022.png)
<center>[그림 24] Instance 삭제 확인</center>

## Floating IP 연결

외부 서비스를 하기 위해서는 Load Balancer에게 Floating IP를 부여해야 합니다.

1.[Infrastructure] > [Compute & Network] > [Load Balancers]에서 Health Check 구성을 변경할 Load Balancer를 선택합니다.

![[그림 25] Floating IP를 할당할 Load Balancer 선택](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_023.png)
<center>[그림 25] Floating IP를 할당할 Load Balancer 선택</center>

2.[Floating IP 연결]버튼을 클릭합니다.

![[그림 26] Floating IP 연결](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_024.png)
<center>[그림 26] Floating IP 연결</center>

3.<Floating IP 연결> 대화창에서 IP를 할당합니다.

![[그림 27] Floating IP 연결 대화창](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_025.png)
<center>[그림 27] Floating IP 연결 대화창</center>

4.사용 가능한 IP주소가 없는 경우, [+생성] 버튼을 클릭합니다.

![[그림 28] IP Pool 항목](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_026.png)
<center>[그림 28] IP Pool 항목</center>

5.[그림 28]의 IP Pool 항목에서 [Floating IP 할당]버튼을 클릭합니다.

![[그림 29] 새로운 Floating IP 할당](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_027.png)
<center>[그림 29] 새로운 Floating IP 할당</center>

![[그림 30] 새로운 Floating IP 할당 확인](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_028.png)
<center>[그림 30] 새로운 Floating IP 할당 확인</center>

6.[확인]버튼을 눌러 Floating IP를 Load Balancer에 연결 합니다.

![[그림 31] Floating IP 연결](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_029.png)
<center>[그림 31] Floating IP 연결</center>

7.[Infrastructure] > [Compute & Network] > [Load Balancers]에서 결과를 확인합니다.

![[그림 32] Floating IP 연결 확인](http://static.toastoven.net/prod_infrastructure/compute/loadbalancer/img_030.png)
<center>[그림 32] Floating IP 연결 확인</center>
