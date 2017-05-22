## Infrastructure > Compute & Network > Volumes User Guide

Volume은 Instance에 추가할 수 있는 disk입니다. 기본 제공되는 disk 외에 추가적인 저장 공간이 더 필요한 경우 기존 Instance에 연결하여 사용할 수 있습니다. 또한 Instance 간 자료 이동 시에도 사용할 수 있습니다.

이 문서에서는 다음과 같은 내용을 다룹니다.

- Volume 생성, 연결, 삭제
- Volume Snapshot 생성, 사용, 삭제
- 리눅스, 윈도우 추가 볼륨 적용 방법

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

## 리눅스 추가 볼륨 적용 방법

1.인스턴스에 접속 후 ’fdisk -l’ 을 통해 추가 볼륨이 구성되어 있는지 확인합니다.

![[그림 31] 리눅스 추가 볼륨 구성 확인](http://static.toastoven.net/prod_infrastructure/compute/volume/img_001.png)

2.추가된 볼륨을 사용할 수 있도록 ‘mkfs.ext4 {볼륨 이름}’ 을 통해 디스크 포맷을 진행합니다.

![[그림 32] 디스크 포맷](http://static.toastoven.net/prod_infrastructure/compute/volume/img_002.png)

3.위에서 설정한 볼륨을 시스템에 마운트 합니다.

* mount -t ext4 {볼륨 이름} {마운트 디렉토리}

![[그림 33] 볼륨 마운트](http://static.toastoven.net/prod_infrastructure/compute/volume/img_003.png)

4.인스턴스 재시작 시 볼륨을 자동으로 mount 하도록 ‘/etc/fstab’에 볼륨 정보를 추가합니다.

![[그림 34] 볼륨 자동 마운트](http://static.toastoven.net/prod_infrastructure/compute/volume/img_004.png)

5.볼륨 해제시에 ‘unmount {마운트 디렉토리}’로 해제하실 수 있습니다.

## 윈도우 추가 볼륨 적용 방법

1.서버관리자 > 파일 및 저장소 서비스 > 볼륨 > 디스크로 이동하여 추가 볼륨을 확인합니다.

2.오프라인 상태로 되어있는 추가 볼륨을 온라인으로 업데이트합니다.

* 화면이 바로 바뀌지 않으면 서버관리자 창을 업데이트 하십시오.

![[그림 35] 윈도우 추가 볼륨 구성 확인](http://static.toastoven.net/prod_infrastructure/compute/volume/img_005.png)

3.이후 온라인 상태로 변경된 볼륨에서 오른쪽 클릭 -> 새 볼륨 버튼을 선택합니다.

![[그림 36] 새 볼륨 추가](http://static.toastoven.net/prod_infrastructure/compute/volume/img_006.png)

4.새 볼륨 마법사를 진행하여 추가 볼륨을 마운트합니다.

- **1.시작하기 전**

![[그림 37] 시작하기 전](http://static.toastoven.net/prod_infrastructure/compute/volume/img_007.png)

- **2. 서버 및 디스크**

![[그림 38] 서버 및 디스크](http://static.toastoven.net/prod_infrastructure/compute/volume/img_008.png)

- **3. 크기**

![[그림 39] 크기](http://static.toastoven.net/prod_infrastructure/compute/volume/img_009.png)

- **4. 드라이브 문자 또는 폴더**

![[그림 40] 드라이브 문자 또는 폴더](http://static.toastoven.net/prod_infrastructure/compute/volume/img_010.png)

- **5. 파일 시스템 설정**

![[그림 41] 파일 시스템 설정](http://static.toastoven.net/prod_infrastructure/compute/volume/img_011.png)

- **6. 확인**

![[그림 42] 확인](http://static.toastoven.net/prod_infrastructure/compute/volume/img_012.png)

- **7. 완료**

![[그림 43] 완료](http://static.toastoven.net/prod_infrastructure/compute/volume/img_013.png)

5.완료 후 아래와 같이 추가 볼륨이 생성된 것을 확인하실 수 있습니다.

![[그림 44] 추가 볼륨 생성 확인](http://static.toastoven.net/prod_infrastructure/compute/volume/img_014.png)

**※추가 확장 후 액세스 경로 추가가 실패할 경우**

1.서버관리자 > 파일 및 저장소 서비스 > 볼륨 > 디스크 > 볼륨 > 드라이브 문자 및 액세스 경로 관리를 선택합니다.

![[그림 45] 드라이브 문자 및 액세스 경로 관리](http://static.toastoven.net/prod_infrastructure/compute/volume/img_015.png)

2.드라이브 문자와 액세스 경로를 설정하신 후 확인을 선택합니다.

![[그림 46] 액세스 경로를 설정](http://static.toastoven.net/prod_infrastructure/compute/volume/img_016.png)
