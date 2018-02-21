## Infrastructure > Compute & Network > Image User Guide

Image는 OS와 각종 애플리케이션 및 설정들이 포함된 파일입니다. 기본 제공 Image 이외에 사용자가 생성한 Instance로부터 새로운 Image를 생성 할 수 있습니다. 서비스의 부하가 늘어나는 경우, Instance를 복제하여 부하를 분산시킬 때 사용할 수 있습니다.

이 문서에서는 다음과 같은 내용을 다룹니다.

- Image 종류
- Image 생성, 공유

## Image의 종류

Image 는 [표 1]의 3가지 종류가 있으며 고객이 생성한 Image는 기본적으로 Private Image입니다. Private Image는 공유 기능을 이용해 공유 Image로 전환할 수 있습니다.

[표 1] Image의 종류

|종류|설명|
|---|---|
|Public Image|TOAST Cloud가 제공하는 Image로서 기본적인 보안 검증을 마친 안전한 Image입니다.|
|Private Image|Public Image를 토대로 새롭게 생성한 사용자 고유의 Image입니다. 사용자의 필요에 따라 각종 OS 설정과 애플리케이션 설치 등을 변경하여 사용할 수 있습니다.|
|공유 Image|Private Image는 사용자가 소유한 Project간 공유가 가능하고, 이렇게 공유한 Image를 공유 Image라고 부릅니다.|
```
[Notice]
TOAST Cloud G 서비스는 이미지 공유 기능을 제공하지 않습니다.
```

## Image 생성

Image를 생성하기 위해서는 먼저 Image를 생성할 Instance를 정지해야 합니다.

1.[Infrastructure] > [Compute & Network] > [Instances]로 이동한 후 Image를 생성할 Instance를 선택합니다. [그림 1]과 같이 [추가기능] 드롭다운 메뉴 > [Instance Shutdown]을 선택하여 해당 Instance를 정지합니다.

![[그림 1] Instance Shutdown 선택](http://static.toastoven.net/prod_infrastructure/compute/img_259.png)
<center>[그림 1] Instance Shutdown 선택</center>

2.[그림 2]의 [상태] 항목에서 Image를 생성할 Instance가 종료된 것을 확인한 뒤, [추가기능] 드롭다운 메뉴 > [Image 생성]을 선택합니다.

![[그림 2] Image 생성 선택](http://static.toastoven.net/prod_infrastructure/compute/img_260.png)
<center>[그림 2] Image 생성 선택</center>

3.생성할 Image의 이름을 입력한 뒤, [Image 생성] 버튼을 클릭합니다.

![[그림 3] Image 이름 입력](http://static.toastoven.net/prod_infrastructure/compute/images/003_170524.PNG)
<center>[그림 3] Image 이름 입력</center>

```
[Notice]
Windows Instance의 경우 Image 생성하기 전에 Sysprep을 이용하여 사용자화 과정을 거쳐야 합니다. Windows Sysprep 가이드를 참고해주시기 바랍니다.
```

4.[Infrastructure] > [Compute & Network] > [Images]에서 생성된 Image를 확인할 수 있습니다.

![[그림 4] 생성된 Image 확인](http://static.toastoven.net/prod_infrastructure/compute/img_261.png)
<center>[그림 4] 생성된 Image 확인</center>

## Image 공유
```
[Notice]
TOAST Cloud G 서비스는 이미지 공유 기능을 제공하지 않습니다.
```

생성된 Image는 다른 프로젝트에서 사용할 수 있도록 설정할 수 있습니다.

1.[Infrastructure] > [Compute & Network] > [Images]로 이동한 후 공유할 Image를 선택합니다. [그림 5]와 같이 [다른 프로젝트에 공유] 버튼을 클릭합니다.

![[그림 5] 공유할 Image 선택](http://static.toastoven.net/prod_infrastructure/compute/img_262.png)
<center>[그림 5] 공유할 Image 선택</center>

2.<Share Image> 대화창에서 공유할 프로젝트를 선택합니다.

![[그림 6] <Share Image> 대화창에서 공유할 프로젝트 선택](http://static.toastoven.net/prod_infrastructure/compute/img_263.png)
<center>[그림 6] <Share Image> 대화창에서 공유할 프로젝트 선택</center>

3.<Share Image> 대화창에서 공유할 프로젝트를 클릭하여 [그림 6]의 우측 "Shared Projects" 영역으로 이동시킵니다. 이 후 [다른 프로젝트에 공유] 버튼을 클릭합니다.

![[그림 7] 공유할 프로젝트 추가](http://static.toastoven.net/prod_infrastructure/compute/img_264.png)
<center>[그림 7] 공유할 프로젝트 추가</center>

4.[그림 6] ~ [그림 7]의 과정으로 Image를 공유한 프로젝트의 [공유된 Image]를 확인하면 1개의 Image가 공유된 것을 확인할 수 있습니다.

![[그림 8] 공유한 Image확인](http://static.toastoven.net/prod_infrastructure/compute/img_265.png)
<center>[그림 8] 공유한 Image확인</center>
