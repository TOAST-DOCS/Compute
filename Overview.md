## Infrastructure > Compute & Network > Overview

Infrastructure > Compute & Network는 서비스 인프라 구축에 필요한 기본 리소스인 Instance와 Network관리 기능을 제공합니다. 유연한 인프라 구성이 가능하며 사용한 만큼만 지불하므로 비용을 절감할 수 있습니다.

## 주요 기능

- 신속한 인프라 구성이 가능하며 필요에 따라 규모를 자유롭게 변경할 수 있습니다.
- 사용한만큼만 지불하므로 서버 구축에 따른 초기 비용을 절감할 수 있습니다.
- console을 통해 간편하게 이용할 수 있습니다.

## 용어 설명

### Instance

Infrastructure 서비스의 Compute 상품 중 기본이 되는 리소스로서 사용자의 필요에 따라 다양한 타입의 Instance를 사용할 수 있습니다. Instance는 하드웨어 템플릿(Flavor)과 소프트웨어 템플릿(Image)을 이용하여 생성할 수 있습니다.
Flavor는 [표 1]과 같이 vCPU, Disk, RAM 의 세가지 하드웨어 조합으로 이루어집니다.

|Flavor|	vCPU|	Disk|	RAM|
|---|---|---|---|
|m2.small|	1|	20GB|	2GB|
|m2.medium|	4|	20GB|	4GB|
|m2.large|	4|	20GB|	8GB|
|m2.xlarge|	8|	20GB|	16GB|
|m2.2xlarge|	16|	20GB|	32GB|
|c2.small|	2|	20GB|	2GB|
|c2.medium|	4|	20GB|	4GB|
|c2.large|	8|	20GB|	8GB|
|c2.xlarge|	16|	20GB|	16GB|
|r2.small|	2|	20GB|	8GB|
|r2.medium|	4|	20GB|	16GB|
|r2.large|	8|	20GB|	32GB|
|t2.tiny|	1|	20GB|	1GB|

[표 1 Flavor]

### Image

소프트웨어 템플릿(Image)는 하드웨어 템플릿(Flavor)와 더불어 Instance를 구성하는 중요한 요소입니다. OS와 기본적으로 설치되는 애플리케이션의 템플릿이며 Public Image를 기본 제공합니다. 사용자는 필요에 따라 기본 제공한 Image를 이용하여 사용자화 Image를 새롭게 생성하여 사용할 수 있습니다.


|이미지 종류|설명|
|---|---|
|Public Image|	TOAST Cloud가 제공하는 Image로서 기본적인 보안 검증을 마친 안전한 Image입니다.|
|Private Image|	Public Image를 토대로 새롭게 생성한 사용자 고유의 Image입니다. 사용자의 필요에 따라 각종 OS 설정과 애플리케이션 설치 등을 변경하여 사용할 수 있습니다.|
|공유 Image|	Private Image는 사용자가 소유한 프로젝트 간 공유가 가능하도록 설정할 수 있습니다. 이렇게 공유한 Image를 공유 Image라고 부릅니다.|

[표 2 Image 종류]

### Volume

Volume은 Instance에 연결할 수 있는 Disk로서 기본으로 제공하는 Instance의 저장공간이 부족한 경우 추가로 연결 할 수 있습니다. Instance를 삭제할 경우 기본으로 제공된 Disk의 모든 데이터는 삭제되지만 Volume 서비스를 통해 생성된 Volume은 연결 된 Instance를 삭제하더라도 데이터가 삭제되지 않고 남아있습니다. 
하나의 Volume은 여러 개의 Instance가 동시에 공유 할 수는 없으나 Instance 간 이동은 가능합니다. 
또한 생성한 Volume을 통해 Snapshot을 만들 수도 있고, 이 Snapshot을 이용하여 새로운 Volume을 생성할 수 도 있습니다.

### Security Group

Security Group은 Instance에 대한 네트워크 접속을 제어하는데 사용합니다. 
하나의 Security Group 안에 여러 개의 Rule을 지정할 수 있으며 각 Rule은 들어오고(Ingress), 나가는(Egress) Network 트래픽을 적용 할 수 있습니다. 
하나의 Instance 에 여러 개의 Security Group을 적용함으로써 효율적으로 트래픽 제어를 할 수 있습니다.

### Key-Pair

Instance 에 접속을 하기 위해 Key-Pair 인증을 제공합니다. Instance 생성 시 반드시 Key-Pair 를 지정해야 하며 생성한 Key-Pair 가 없을 시 Key-Pair 생성 메뉴를 통해 새로운 Key-Pair 를 생성해야 합니다. 
생성한 Key-Pair 는 외부에 노출되지 않도록 관리상 주의가 필요합니다.

### Network

사용자는 자신만의 가상 Network를 정의할 수 있습니다. 가상 Network내에서 Router생성을 통한 Gateway 설정과 Subnet분리를 통해 Network를 제어할 수 있습니다. 외부 연결 Network와 사용자 정의 사설 Network를 이용해 완벽한 인프라 구성이 가능합니다. 또한 Network Topology 기능을 통해 한눈에 Network설정을 확인할 수 있습니다.

### Floating IP

Instance 생성과 Load Balancer 생성시 기본적으로 Public IP를 할당하지 않습니다. 생성된 Instance 와 Load Balancer 는 외부에서 접속하기 위해 Public IP가 있어야 하는데 이때 Floating IP를 이용하여 할당받게 됩니다. Floating IP는 사용자의 계정과 연결되어 Instance를 삭제하더라도 해제되지 않으며, 같은 프로젝트 내 다른 Instance에 할당할 수 있습니다. DNS와 연결하여 사용하면 Instance 장애 시 단순히 사용하던 Floating IP를 정상 Instance에 연결하는 것만으로 빠른 장애 복구가 가능하여 지속적인 서비스를 제공할 수 있습니다.

### Load Balancer

Load Balancer를 이용해 Network 트래픽을 여러 Instance에 분산할 수 있습니다. 부하 분산뿐만 아니라 사용자가 설정한 Health Check 패턴에 따라 장애 Instance를 자동으로 검출하여 트래픽을 분산 제어함으로써 서비스의 고가용성 (High Availability)을 보장할 수 있습니다. 또한 하나의 Network 안에 서비스 별로 여러 개의 Load Balancer를 생성할 수 있습니다.
