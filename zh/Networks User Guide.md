## Infrastructure > Compute & Network > Networks User Guide

TOAST Cloud에서 Network는 Instance들을 연결하는 가상 Network로서 사용됩니다. TOAST Cloud의 Network는 하위에 하나의 Subnet만을 가지고 있습니다. 여러 개의 Subnet을 이용하고 싶은 경우 새로운 Network를 생성해야 합니다. 또한 Router를 통해 다른 Network와 연결함으로써 논리적으로 확장 가능합니다.

이 문서에서는 다음과 같은 내용을 다룹니다.

- Network 생성, 삭제
- Router 생성, 삭제
- Router의 게이트웨이 설정, 제거 및 Interface 추가, 삭제
- Network Topology 보기

> 참고  
> Network 생성하기는 Admin 권한을 가진 사용자만이 이용 가능합니다.

## Network 생성

1.[Infrastructure] > [Compute & Network] > [Networks]으로 이동한 후 [그림 1]의 [+ Network 생성] 버튼을 클릭합니다.

![[그림 1] Network 생성](http://static.toastoven.net/prod_infrastructure/compute/img_301.png)
<center>[그림 1] Network 생성</center>

2.[그림 2]의 &lt;Network 생성> 대화창에서 Network 생성에 필요한 정보를 입력합니다. 필요한 정보는 다음과 같습니다.

- **Network 이름**  
생성할 Network의 이름을 입력합니다.
- **Subnet 이름**  
생성할 Network의 Subnet의 이름을 입력합니다.
- **Network 주소**  
생성할 Network의 Subnet에 부여할 IP 주소 대역을 입력합니다. CIDR 형태로 입력해야 합니다.
- **IP 버전**  
생성할 Network의 IP 주소 체계를 선택합니다. IPv4 또는 IPv6 중 하나를 선택할 수 있습니다.
- **게이트웨이 비활성**  
생성할 Network의 게이트웨이를 비활성화합니다. 기본적으로 Network를 생성하면 Subnet의 게이트웨이 IP가 할당됩니다. 이를 비활성 상태로 만들 수 있으며 이렇게 만들어진 Network는 L2 Network로만 동작하게 되며 Router 생성이 불가능합니다. 게이트웨이 지정 없이 L2 Network로만 동작하기 원할 때는 이 옵션을 활성화 시켜주시기 바랍니다.

모든 정보를 입력한 후, [생성]버튼을 클릭합니다.

![[그림 2] Network 생성](http://static.toastoven.net/prod_infrastructure/compute/img_116.jpg)
<center>[그림 2] Network 생성</center>

3.[Infrastructure] > [Compute & Network] > [Networks]에서 Network가 정상적으로 생성되었음을 확인합니다.

![[그림 3] Network 생성 확인](http://static.toastoven.net/prod_infrastructure/compute/img_302.png)
<center>[그림 3] Network 생성 확인</center>

## Network 삭제

1.[Infrastructure] > [Compute & Network] > [Networks]으로 이동한 후 Network 탭을 선택합니다.

![[그림 4] Networks 탭으로 이동](http://static.toastoven.net/prod_infrastructure/compute/img_303.png)
<center>[그림 4] Networks 탭으로 이동</center>

2.삭제할 Network를 선택합니다.

![[그림 5] 삭제할 Network 선택](http://static.toastoven.net/prod_infrastructure/compute/img_304.png)
<center>[그림 5] 삭제할 Network 선택</center>

3.[Networks  삭제]버튼을 클릭합니다.

![[그림 6] Network 삭제](http://static.toastoven.net/prod_infrastructure/compute/img_305.png)
<center>[그림 6] Network 삭제</center>

4.&lt;Networks 삭제를 확인하세요.> 대화창에서 [Networks 삭제]버튼을 클릭합니다.

![[그림 7] Networks 삭제 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_121.jpg)
<center>[그림 7] Networks 삭제 대화창</center>

5.[Infrastructure] > [Compute & Network] > [Networks]으로 이동한 후 Networks 탭에서 정상적으로 Network가 삭제된 것을 확인합니다.

![[그림 8] Network 삭제 확인](http://static.toastoven.net/prod_infrastructure/compute/img_306.png)
<center>[그림 8] Network 삭제 확인</center>

> [주의]  
> 삭제하려는 Network에 Interface가 추가되어 있는 경우, 삭제가 진행되지 않습니다. 해당 Interface를 먼저 삭제하고 Network 삭제를 시도하시기 바랍니다.

## Router 생성

생성된 Network는 Network 내 Instance들 간의 통신은 지원하지만 아직 다른 Network와 연결되지 않아서 외부와의 통신이 불가능합니다. 다른 Network와 연결하기 위해서는 Router를 생성해야 합니다.

1.[Infrastructure] > [Compute & Network] > [Networks]으로 이동한 후 Routers 탭을 선택합니다.

![[그림 9] Routers 탭](http://static.toastoven.net/prod_infrastructure/compute/img_307.png)
<center>[그림 9] Routers 탭</center>

2.[+ Router 생성]버튼을 클릭합니다.

![[그림 10] Routers 생성](http://static.toastoven.net/prod_infrastructure/compute/img_308.png)
<center>[그림 10] Routers 생성</center>

3.&lt;Router 생성> 대화창에서 Router 이름을 입력한 후 [Router 생성]버튼을 클릭합니다.

![[그림 11] Router 생성 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_125.jpg)
<center>[그림 11] Router 생성 대화창</center>

4.[Infrastructure] > [Compute & Network] > [Networks]의 Routers탭에서 Router가 정상적으로 생성되었음을 확인합니다.

![[그림 12] Router 생성 확인](http://static.toastoven.net/prod_infrastructure/compute/img_309.png)
<center>[그림 12] Router 생성 확인</center>

## Router 게이트웨이 설정

사용자가 생성한 Network는 생성 직후에는 격리되어 외부와 통신이 불가능합니다. 이를 해결하기 위해서는 Router를 통해 외부 Network와 연결해야 합니다. 먼저 Router의 게이트웨이 설정을 함으로써 외부 Network와 연결되도록 설정할 수 있습니다.

1.[Infrastructure] > [Compute & Network] > [Networks]의 Routers 탭으로 이동합니다.

![[그림 13] Routers 탭으로 이동](http://static.toastoven.net/prod_infrastructure/compute/img_310.png)
<center>[그림 13] Routers 탭으로 이동</center>

2.게이트웨이를 설정할 Router를 선택합니다.

![[그림 14] 게이트웨이를 설정할 Router 선택](http://static.toastoven.net/prod_infrastructure/compute/img_311.png)
<center>[그림 14] 게이트웨이를 설정할 Router 선택</center>

3.[Actions] 목록에서 [게이트웨이 설정]을 선택합니다.

![[그림 15] 게이트웨이 설정 선택](http://static.toastoven.net/prod_infrastructure/compute/img_312.png)
<center>[그림 15] 게이트웨이 설정 선택</center>

4.&lt;게이트웨이 설정> 대화창에서 연결할 외부 Network를 선택합니다. 기본적으로 “Public Network”만 설정 가능합니다. 선택이 끝나면 [게이트웨이 설정]버튼을 클릭합니다.

![[그림 16] 게이트웨이 설정 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_313.png)
<center>[그림 16] 게이트웨이 설정 대화창</center>

![[그림 17] 외부 Network 선택](http://static.toastoven.net/prod_infrastructure/compute/img_314.png)
<center>[그림 17] 외부 Network 선택</center>

5.&lt;[Infrastructure] > [Compute & Network] > [Networks]의 Routers 탭에서 정상적으로 게이트웨이가 설정된 것을 확인합니다.

![[그림 18] 게이트웨이 설정 확인](http://static.toastoven.net/prod_infrastructure/compute/img_315.png)
<center>[그림 18] 게이트웨이 설정 확인</center>


## Router 게이트웨이 제거

외부 Network와의 연결을 해제하기 위해서는 Router의 게이트웨이를 제거해야 합니다.

1.[Infrastructure] > [Compute & Network] > [Networks]의 Routers 탭으로 이동합니다.

![[그림 19] Routers 탭으로 이동](http://static.toastoven.net/prod_infrastructure/compute/img_316.png)
<center>[그림 19] Routers 탭으로 이동</center>

2.게이트웨이를 제거할 Router를 선택합니다.

![[그림 20] 게이트웨이를 제거할 Routers 선택](http://static.toastoven.net/prod_infrastructure/compute/img_317.png)
<center>[그림 20] 게이트웨이를 제거할 Routers 선택</center>

3.[Actions] 목록의 [게이트웨이 제거]를 선택합니다.

![[그림 21] 게이트웨이 제거 선택](http://static.toastoven.net/prod_infrastructure/compute/img_318.png)
<center>[그림 21] 게이트웨이 제거 선택</center>

4.&lt;게이트웨이 제거를 확인하세요.> 대화창에서 [게이트웨이 제거]버튼을 클릭합니다.

![[그림 22] 게이트웨이 제거 선택](http://static.toastoven.net/prod_infrastructure/compute/img_136.jpg)
<center>[그림 22] 게이트웨이 제거 선택</center>

5.[Infrastructure] > [Compute & Network] > [Networks]의 Routers 탭에서 게이트웨이가 정상적으로 제거된 것을 확인합니다

![[그림 23] 게이트웨이 제거 확인](http://static.toastoven.net/prod_infrastructure/compute/img_319.png)
<center>[그림 23] 게이트웨이 제거 확인</center>

## Router Interface 추가

생성한 Router를 외부 Network가 아닌 다른 특정 Network에게 연결하기 위해서는 Interface를 추가해야 합니다.

1.[Infrastructure] > [Compute & Network] > [Networks]의 Routers 탭으로 이동한 후 Interface를 추가할 Router를 선택합니다.

![[그림 24] Interface를 추가할 Router 선택](http://static.toastoven.net/prod_infrastructure/compute/img_320.png)
<center>[그림 24] Interface를 추가할 Router 선택</center>

2.[+ 인터페이스 추가]버튼을 클릭합니다.

![[그림 25] Interface 추가](http://static.toastoven.net/prod_infrastructure/compute/img_321.png)
<center>[그림 25] Interface 추가</center>

3.&lt;인터페이스 추가> 대화창에서 Interface를 추가할 Subnet을 선택합니다. 여기서는 Router를 연결할 Network의 Subnet을 선택합니다.

![[그림 26] Interface 추가 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_322.png)
<center>[그림 26] Interface 추가 대화창</center>

4. [Infrastructure] > [Compute & Network] > [Networks]의 Routers 탭에서 Interface를 추가한 Router를 선택하여 정상적으로 Interface가 추가된 것을 확인합니다.

![[그림 27] Interface 추가 확인](http://static.toastoven.net/prod_infrastructure/compute/img_323.png)
<center>[그림 27] Interface 추가 확인</center>

## Router Interface 삭제

Router를 삭제하기 위해서는 먼저 해당 Router에 추가된 Interface들을 삭제해야 합니다.

1.[Infrastructure] > [Compute & Network] > [Networks]의 Routers 탭으로 이동한 후 Interface를 삭제할 Router를 선택합니다.

![[그림 13] Interface를 삭제할 Router 선택](http://static.toastoven.net/prod_infrastructure/compute/img_324.png)
<center>[그림 13] Interface를 삭제할 Router 선택</center>

2.삭제할 Interface를 선택합니다.

![[그림 14] 삭제할 Interface 선택](http://static.toastoven.net/prod_infrastructure/compute/img_325.png)
<center>[그림 14] 삭제할 Interface 선택</center>

3.[Interface 삭제]버튼을 클릭합니다.

![[그림 15] Interface 삭제](http://static.toastoven.net/prod_infrastructure/compute/img_326.png)
<center>[그림 15] Interface 삭제</center>

4.&lt;인터페이스 삭제를 확인하세요.> 대화창에서 [인터페이스 삭제]버튼을 클릭합니다.

![[그림 16] Interface 삭제 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_327.png)
<center>[그림 16] Interface 삭제 대화창</center>

5.[Infrastructure] > [Compute & Network] > [Networks]의 Routers 탭에서 Interface를 삭제한 Router를 선택하여 정상적으로 Interface가 삭제된 것을 확인합니다.

![[그림 17] Interface 삭제 확인](http://static.toastoven.net/prod_infrastructure/compute/img_328.png)
<center>[그림 17] Interface 삭제 확인</center>

## Router 삭제
1.[Infrastructure] > [Compute & Network] > [Networks]의 Routers 탭으로 이동합니다.

![[그림 18] Router 목록](http://static.toastoven.net/prod_infrastructure/compute/img_329.png)
<center>[그림 18] Router 목록</center>

2.삭제할 Router를 선택합니다.

![[그림 19] 삭제할 Router 선택](http://static.toastoven.net/prod_infrastructure/compute/img_330.png)
<center>[그림 19] 삭제할 Router 선택</center>

3.[Routers 삭제]버튼을 클릭합니다.

![[그림 20] Router 삭제](http://static.toastoven.net/prod_infrastructure/compute/img_331.png)
<center>[그림 20] Router 삭제</center>

4.&lt;Routers 삭제> 대화창에서 [Routers 삭제]버튼을 클릭합니다.

![[그림 21] Router 삭제 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_150.jpg)
<center>[그림 21] Router 삭제 대화창</center>

5.[Infrastructure] > [Compute & Network] > [Networks]의 Routers 탭에서 Router가 정상적으로 삭제된 것을 확인합니다.

![[그림 22] Router 삭제 확인](http://static.toastoven.net/prod_infrastructure/compute/img_332.png)
<center>[그림 22] Router 삭제 확인</center>

> [주의]  
> 삭제하려는 Router에 Interface가 추가되어 있는 경우, 삭제가 진행되지 않습니다. 해당 Interface를 먼저 삭제하고 Router 삭제를 시도하시기 바랍니다.

## Network Topology 확인

현재 Network 구성을 TOAST Cloud 웹 콘솔에서 시각적으로 확인할 수 있습니다.

1.[Infrastructure] > [Compute & Network] > [Networks]의 Network Topology탭으로 이동합니다.

현재 프로젝트 내 Instance, Network, Router 사이의 관계를 아이콘을 통해 표현한 그림을 볼 수 있습니다. 그림 18의 경우 총 2개의 Network로 “Default Network”와 “TOAST-NETWORK”를 확인할 수 있습니다. “Default Network”의 경우 Router를 통해 “Public Network”와 연결되어 있습니다. 따라서 “Default Network”에 연결될 Instance의 경우 외부와의 통신이 가능합니다. 그러나 “TOAST-NETWORK”의 경우 격리되어 있어 외부와 통신이 불가능합니다. 이를 해결하려면 앞서 설명한 것처럼 Router를 생성하고 Interface를 추가하여 “Public Network”와 연결해야 합니다.

![[그림 23] Network Topology](http://static.toastoven.net/prod_infrastructure/compute/img_333.png)
<center>[그림 23] Network Topology</center>

2.경우에 따라 다양한 동작을 수행할 수 있습니다.

구성도 내의 아이콘에 마우스 커서를 올려두면 [그림 24]와 같이 간략한 요약과 상세 정보 보기 링크를 보여줍니다.

![[그림 24] Instance 요약 보기](http://static.toastoven.net/prod_infrastructure/compute/img_334.png)
<center>[그림 24] Instance 요약 보기</center>

구성도 내에서 즉시 Instance, Network, Router 생성 화면으로 이동할 수 있는 바로 가기를 제공합니다.

![[그림 25] 바로 가기 지원](http://static.toastoven.net/prod_infrastructure/compute/img_335.png)
<center>[그림 25] 바로 가기 지원</center>

[그림 26]과 같이 기본 보기 모드로 변경할 수 있습니다.

![[그림 26] 기본 보기 모드](http://static.toastoven.net/prod_infrastructure/compute/img_336.png)
<center>[그림 26] 기본 보기 모드</center>
