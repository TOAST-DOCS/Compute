## Infrastructure > Compute & Network > Security Groups User Guide

Security Group은 IP 필터 Rule의 집합입니다. 이 필터 Rule들은 Project 내 Instance들의 inbound 및 outbound Network 트래픽에 적용되어, 허용되지 않은 외부로부터의 접근을 막는 데 사용할 수 있습니다. 사용자는 기본 제공하는 Security Group 이외에 새로운 Security Group을 생성하여 자신만의 Network 제어를 위한 Rule들을 관리할 수 있습니다.

이 문서에서는 다음과 같은 내용을 다룹니다.

- Security Group 생성, 추가
- Rule 생성, 추가


> 참고  
> Security Group 설정하기는 Admin 권한을 가진 사용자만이 이용 가능합니다. 다만 Member 권한을 가진 사용자도 Security Group 목록과 규칙은 조회 가능합니다.

## Security Group 생성

1.[Infrastructure] > [Compute & Network] > [Security Groups]으로 이동한 후 [+ Security Group 생성] 버튼을 클릭합니다.

![[그림1] Security Group 목록](http://static.toastoven.net/prod_infrastructure/compute/img_289.png)
<center>[그림1] Security Group 목록</center>

2.<Security Group 생성> 대화창에서 Security Groups의 이름과 설명을 입력한 후, [Security Group 생성] 버튼을 클릭합니다.

![[그림2] Security Group 생성 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_102.jpg)
<center>[그림2] Security Group 생성 대화창</center>

3.[Infrastructure] > [Compute & Network] > [Security Groups]에서 생성된 Security Group을 확인할 수 있습니다. 생성된 Security Group은 기본 Security Group과 동일합니다.

![[그림3] 생성된 Security Group 확인](http://static.toastoven.net/prod_infrastructure/compute/img_290.png)
<center>[그림3] 생성된 Security Group 확인</center>

## Security Group 삭제

1.[Infrastructure] > [Compute & Network] > [Security Groups]에서 삭제할 Security Group을 선택합니다.

![[그림4] 삭제할 Security Group 선택](http://static.toastoven.net/prod_infrastructure/compute/img_291.png)
<center>[그림4] 삭제할 Security Group 선택</center>

2.[Security Groups 삭제]버튼을 클릭합니다.

![[그림5] Security Group 삭제](http://static.toastoven.net/prod_infrastructure/compute/img_292.png)
<center>[그림5] Security Group 삭제</center>

3.&lt;Security Groups 삭제> 대화창에서 삭제할 Security Groups을 확인한 후, [Security Groups 삭제] 버튼을 클릭합니다.

![[그림6] Security Group 삭제 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_293.png)
<center>[그림6] Security Group 삭제 대화창</center>

4.[Infrastructure] > [Compute & Network] > [Security Groups]에서 선택한 Security Group가 삭제되었음을 확인합니다.

![[그림7] Security Group 삭제 확인](http://static.toastoven.net/prod_infrastructure/compute/img_294.png)
<center>[그림7] Security Group 삭제 확인</center>

## Rule 추가

1.[Infrastructure] > [Compute & Network] > [Security Groups]에서 Rule을 추가할 Security Group을 선택합니다. 그러면 웹 콘솔 하단에 해당 Security Group에 포함된 Rule들의 목록을 보여줍니다. [그림 4]에서 알 수 있듯이, 현재 추가된 Rule은 외부로 나가는(‘Engress’) 모든(포트 범위: ‘-‘, 원격 주소: ‘0.0.0.0/0’, ‘::/0’) IPv4 혹은 IPv6 트래픽을 허용합니다. 다만 외부에서 들어오는 트래픽에 대한 Rule이 없으므로, 현재 어떠한 방식으로도 접근할 수 없습니다. Rule을 추가하기 위해서 [Rule 추가]버튼을 클릭합니다.

![[그림8] Rule 추가](http://static.toastoven.net/prod_infrastructure/compute/img_295.png)
<center>[그림8] Rule 추가</center>

2.<Rule추가> 대화창에서 을 추가할 의 상세 정보를 입력합니다. 입력이 필요한 상세 정보는 다음과 같습니다.

- Rule  
  - 생성할 Rule의 형식을 선택합니다. 필요에 따라 SSH, HTTP와 같은 사전에 정의된 Rule 형식을 이용할 수 있습니다.
  - 기본적으로 “사용자 정의 TCP Rule”이 지정됩니다.
- Direction  
  - Ingress (외부로부터 들어오는 트래픽에 대한 Rule)/Egress(외부로 나가는 트래픽에 대한 Rule)를 선택할 수 있습니다.
- 포트 오픈  
  - 단일 포트 또는 특정 범위의 포트를 열 수 있습니다. “포트 범위” 옵션을 선택하면 포트 범위 시작 값과 최종 값을 설정할 수 있습니다.
- 포트  
  - 1부터 65536까지의 포트를 선택 가능합니다.
- 원격  
  - 생성하려는 Rule이 허용하려는 트래픽 소스를 지정합니다. CIDR 형태 또는 Security Group 중 하나를 선택하여 지정할 수 있습니다. Security Group을 선택하면 지정한 Security Group이 적용된 Instance의 접근을 허용합니다.
- CIDR  
  - 허용할 IP 대역을 CIDR형태로 입력합니다.
  - Ex) 192.168.0.0/24, 192.168.0.0/16

![[그림9] Rule 추가 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_109.jpg)
<center>[그림9] Rule 추가 대화창</center>


3.[Infrastructure] > [Compute & Network] > [Security Groups]에서 정상적으로 Rule이 생성되었음을 확인합니다.

![[그림10] Rule 추가 성공](http://static.toastoven.net/prod_infrastructure/compute/img_296.png)
<center>[그림10] Rule 추가 성공</center>

## Rule 삭제

1.[Infrastructure] > [Compute & Network] > [Security Groups]에서 [그림 11]와 같이 상단 영역의 Security Group목록에서 Rule을 삭제할 Security Group을 선택하여 하단 영역에 Rule 목록을 조회합니다.

![[그림11] Rule 삭제할 Security Group 선택](http://static.toastoven.net/prod_infrastructure/compute/img_297.png)
<center>[그림11] Rule 삭제할 Security Group 선택</center>

2.선택한 Security Group의 Rule 목록에서 [그림 12]와 같이 삭제할 Rule을 선택합니다.

![[그림12] 삭제할 Rule 선택](http://static.toastoven.net/prod_infrastructure/compute/img_298.png)
<center>[그림12] 삭제할 Rule 선택</center>

3.[x Rule 삭제]버튼을 클릭합니다. 이 후 나타나는 <Rules 삭제를 확인하세요.> 대화창에서 [Rules 삭제] 버튼을 클릭합니다.

![[그림13] Rule 삭제](http://static.toastoven.net/prod_infrastructure/compute/img_299.png)
<center>[그림13] Rule 삭제</center>

4.[그림 14]와 같이 지정한 Rule이 정상적으로 삭제되었음을 확인합니다.

![[그림14] Rule 삭제 확인](http://static.toastoven.net/prod_infrastructure/compute/img_300.png)
<center>[그림14] Rule 삭제 확인</center>
