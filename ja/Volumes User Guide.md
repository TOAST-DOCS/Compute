## Infrastructure > Compute & Network > Volumes User Guide

Volume은 Instance에 추가할 수 있는 disk입니다. 기본 제공되는 disk 외에 추가적인 저장 공간이 더 필요한 경우 기존 Instance에 연결하여 사용할 수 있습니다. 또한 Instance 간 자료 이동 시에도 사용할 수 있습니다.

이 문서에서는 다음과 같은 내용을 다룹니다.

- Volume 생성, 연결, 삭제
- Volume Snapshot 생성, 사용, 삭제

## Volume 생성

1.[Infrastructure] > [Compute & Network] > [Volumes]으로 이동한 뒤, [+ Volume 생성]버튼을 클릭합니다.

![[그림 1] Volume 목록 보기](http://static.toastoven.net/prod_infrastructure/compute/img_266.png)
<center>[그림 1] Volume 목록 보기</center>

2.[그림 2]의 <Volume 생성> 대화창에서 Volume 관련 정보를 입력합니다. 필요한 정보는 다음과 같습니다.

- **Volume 이름**    
  생성할 Volume의 이름을 입력합니다.
- **설명**  
  생성할 Volume에 대한 설명을 입력합니다.
- **크기**  
  생성할 Volume의 크기를 입력합니다. 단위는 GB입니다.
- **Zone**  
  생성할 Volume이 사용될 Availability Zone을 지정합니다. 생성한 Volume은 같은 Zone 에 있는 Instance에만 연결할 수 있습니다.

![[그림 2] Volume 생성 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_72.jpg)
<center>[그림 2] Volume 생성 대화창</center>

3.[Infrastructure] > [Compute & Network] > [Volumes]에서 생성된 Volume을 확인할 수 있습니다.

![[그림 3] 생성된 Volume 확인](http://static.toastoven.net/prod_infrastructure/compute/img_267.png)
<center>[그림 3] 생성된 Volume 확인</center>

## Volumes 연결

생성한 Volume을 Instance에서 사용하기 위해서는 Instance에 Volume을 연결해야 합니다.

1.[Infrastructure] > [Compute & Network] > [Volumes]으로 이동한 뒤, 연결할 Volume 을 선택합니다.

![[그림 4] 연결할 Volume 선택](http://static.toastoven.net/prod_infrastructure/compute/img_268.png)
<center>[그림 4] 연결할 Volume 선택</center>

2.[연결 관리]버튼을 선택합니다.

![[그림 5] 연결 관리](http://static.toastoven.net/prod_infrastructure/compute/img_269.png)
<center>[그림 5] 연결 관리</center>

3.&lt;Volume 연결 관리> 대화창에서 연결할 Instance를 선택합니다

![[그림 6] 연결 관리 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_76.jpg)
<center>[그림 6] 연결 관리 대화창</center>

4.[Infrastructure] > [Compute & Network] > [Volumes]에서, 선택한Volume이 연결되었음을 확인합니다.

![[그림 7] Volume 연결 확인](http://static.toastoven.net/prod_infrastructure/compute/img_270.png)
<center>[그림 7] Volume 연결 확인</center>

5.연결된 Volume을 해제하고 싶을 때에는 연결을 해제할 Volume을 선택하고 [연결 관리]버튼을 선택합니다.

![[그림 8] 연결된 Volume 해제](http://static.toastoven.net/prod_infrastructure/compute/img_271.png)
<center>[그림 8] 연결된 Volume 해제</center>

6.&lt;Volume 연결 관리> 대화창에서 Instance를 선택한 후 [Volumes 연결 해제] 버튼을 클릭합니다.

![[그림 9] Volume 연결 관리 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_79.jpg)
<center>[그림 9] Volume 연결 관리 대화창</center>

7.&lt;Volume 연결 해제를 확인하세요.> 대화창에서 [Volumes 연결 해제] 버튼을 클릭합니다.

![[그림 10] Volume 연결 관리 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_80.jpg)
<center>[그림 10] Volume 연결 관리 대화창</center>

8.[Infrastructure] > [Compute & Network] > [Volumes]에서, 선택한 Volume이 해제되었음을 확인합니다.

![[그림 11] Volume 연결 관리 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_272.png)
<center>[그림 11] Volume 연결 관리 대화창</center>

## Volumes 삭제

더 이상 사용하지 않는 Volume들은 불필요한 과금을 막기 위해 삭제하도록 합니다.

1.[Infrastructure] > [Compute & Network] > [Volumes]으로 이동한 뒤, 삭제할 Volume 을 선택합니다.

![[그림 12] 삭제할 Volume 선택](http://static.toastoven.net/prod_infrastructure/compute/img_273.png)
<center>[그림 12] 삭제할 Volume 선택</center>

2.[Volumes 삭제]버튼을 클릭합니다.

![[그림 13] Volumes 삭제](http://static.toastoven.net/prod_infrastructure/compute/img_274.png)
<center>[그림 13] Volumes 삭제</center>

3.&lt;Volumes 삭제를 확인하세요.> 대화창에서 [Volumes 삭제]버튼을 클릭합니다.

![[그림 14] Volume 삭제 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_84.jpg)
<center>[그림 14] Volume 삭제 대화창</center>

4.[Infrastructure] > [Compute & Network] > [Volumes]에서 선택한 Volume이 삭제되었음을 확인합니다.

![[그림 15] Volume 삭제 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_275.png)
<center>[그림 15] Volume 삭제 대화창</center>

## Volume Snapshot 생성

Volume Snapshot은 현재 Volume의 상태를 그대로 저장해둡니다. Volume Snapshot을 통해 새 Volume을 생성함으로써 특정 시점의 Volume을 그대로 복구 가능합니다.

1.[Infrastructure] > [Compute & Network] > [Volumes]으로 이동한 뒤, 삭제할 Volume 을 선택합니다.

![[그림 16] Snapshot을 생성할 Volume 선택](http://static.toastoven.net/prod_infrastructure/compute/img_276.png)
<center>[그림 16] Snapshot을 생성할 Volume 선택</center>

2.[Snapshot 생성]버튼을 클릭합니다.

![[그림 17] Snapshot 생성](http://static.toastoven.net/prod_infrastructure/compute/img_277.png)
<center>[그림 17] Snapshot 생성</center>

3.&lt;Volume Snapshot 생성> 대화창에서 Snapshot의 이름과 설명을 입력한 뒤, [Volume Snapshot 생성]버튼을 클릭합니다.

![[그림 18] Volume Snapshot 생성 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_88.jpg)
<center>[그림 18] Volume Snapshot 생성 대화창</center>

4.[Infrastructure] > [Compute & Network] > [Volumes]의 Volume Snapshots 탭에서 정상적으로 Snapshot이 생성되었음을 확인합니다.

![[그림 19] Volume Snapshot 생성 완료 알림](http://static.toastoven.net/prod_infrastructure/compute/img_278.png)
<center>[그림 19] Volume Snapshot 생성 완료 알림</center>

![[그림 20] Volume Snapshot 생성 확인](http://static.toastoven.net/prod_infrastructure/compute/img_279.png)
<center>[그림 20] Volume Snapshot 생성 확인</center>

## Volume Snapshot을 통한 Volume 생성

1.[Infrastructure] > [Compute & Network] > [Volumes]에서, Volume Snapshot탭을 선택합니다.

![[그림 21] Snapshot을 생성할 Volume 선택](http://static.toastoven.net/prod_infrastructure/compute/img_280.png)
<center>[그림 21] Snapshot을 생성할 Volume 선택</center>

2.Volumes을 생성할 Volume Snapshot을 선택합니다.

![[그림 22] Volume을 생성할 Volume Snapshot 선택](http://static.toastoven.net/prod_infrastructure/compute/img_281.png)
<center>[그림 22] Volume을 생성할 Volume Snapshot 선택</center>

3.[Actions]에서 [Volume 생성]을 선택합니다.

![[그림 23] Volume을 생성할 Volume Snapshot 선택](http://static.toastoven.net/prod_infrastructure/compute/img_282.png)
<center></center>

4.&lt;Volume 생성> 대화창에서 생성할 Volume에 관련된 정보를 입력한 후 [Volume 생성]버튼을 클릭합니다.

![[그림 24] Volume 생성 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_283.png)
<center>[그림 24] Volume 생성 대화창</center>

> [주의]  
> Snapshot을 통해 Volume을 생성하는 경우, Volume의 크기가 Snapshot의 크기보다 반드시 크거나 같아야 합니다.

5.[Infrastructure] > [Compute & Network] > [Volumes]에서 정상적으로 Volume이 생성되었음을 확인합니다.

![[그림 25] Volume 생성 확인](http://static.toastoven.net/prod_infrastructure/compute/img_284.png)
<center>[그림 25] Volume 생성 확인</center>

## Volume Snapshot 삭제

1.[Infrastructure] > [Compute & Network] > [Volumes]에서 Volume Snapshot탭을 선택합니다.

![[그림 26] Volume Snapshot탭으로 이동](http://static.toastoven.net/prod_infrastructure/compute/img_285.png)
<center>[그림 26] Volume Snapshot탭으로 이동</center>

2.삭제할 Volume Snapshot을 선택합니다.

![[그림 27] 삭제할 Volume Snapshot 선택](http://static.toastoven.net/prod_infrastructure/compute/img_286.png)
<center>[그림 27] 삭제할 Volume Snapshot 선택</center>

3.[Volume Snapshots 삭제]버튼을 클릭합니다.

![[그림 28] Volume Snapshots 삭제 버튼 선택](http://static.toastoven.net/prod_infrastructure/compute/img_287.png)
<center>[그림 28] Volume Snapshots 삭제 버튼 선택</center>

4.&lt;Volume Snapshot삭제를 확인하세요.> 대화창에서 [Volume Snapshots 삭제]버튼을 클릭합니다.

![[그림 29] Volume Snapshot 삭제](http://static.toastoven.net/prod_infrastructure/compute/img_99.png)
<center>[그림 29] Volume Snapshot 삭제</center>

5.[Infrastructure] > [Compute & Network] > [Volumes]에서 Volume Snapshot가 삭제되었음을 확인합니다.

![[그림 30] Volume Snapshot 삭제 확인](http://static.toastoven.net/prod_infrastructure/compute/img_288.png)
<center>[그림 30] Volume Snapshot 삭제 확인</center>
