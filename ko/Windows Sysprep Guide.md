## Infrastructure > Compute & Network > Windows Sysprep Guide

Windows Image를 생성하려면 일련의 준비 과정이 선행되어야 합니다. 이 과정을 통해 PC별 종속된 정보를 제거하여 일반화된 Windows Image을 생성하게 됩니다.

이 문서에서는 다음과 같은 내용을 다룹니다.

- Sysprep 개요
- Sysprep 사용 방법

## Sysprep (System Preparation)

Sysprep은 Microsoft 사에서 Windows OS를 배포하기 위해 제공하는 시스템 준비 유틸리티입니다. 이 Sysprep을 사용하여 사용자로부터 지정된 Windows 설정 또는 사용자 응용프로그램의 내용을 기록하게 됩니다. 일반적으로 Sysprep은 Windows image를 생성하여 여러 PC로 배포할 때 사용합니다.

### Sysprep 실행 단계

Sysprep은 아래의 단계를 순차적으로 실행 합니다. 각 단계는 Sysprep에 실행 옵션을 줌으로써 지정하게 됩니다.

#### generalize
Windows에 등록된 고유 시스템 정보를 제거합니다. 이 단계에서 SID(Security ID)가 다시 설정되고, 시스템 복원 지점이 모두 지워지며, 이벤트 로그가 삭제됩니다. 이 단계를 거친 후 재부팅을 하면 Windows 구성 단계를 시도하게 됩니다.

```
[Notice]
이 단계에서 SID 및 사용자 정보와 고유 정보를 삭제하여, 기존 프로그램의 동작에 영향을 줄 수 있습니다.
```

#### oobe
Windows를 재부팅하여 시작 모드로 진입 후 사용자가 미리 지정한 설정을 적용합니다. 이 때 적용할 수 있는 설정으로는 대표적으로 국가별 설정, 네트워크 위치, 언어 설정, 시간대 등이 있습니다.

#### shutdown
Windows를 종료합니다.

#### unattend
Windows를 재설치한 뒤, 앞서 단계에서 기록한 사용자 설정을 복구합니다. 이 단계에서 Windows 사용자 정보를 등록하고, 드라이버 및 제품 업데이트 및 추가 소프트웨어 설치가 이뤄집니다. 또한 응답파일을 통해 기본적으로 제공하는 설정외에 사용자가 원하는 설정을 지정할 수 있습니다.

```
[Notice]
TOAST Cloud의 Windows Image에서 응답파일은 C:\Program Files\Cloud Solutions\Cloudbase-Init\conf\Unattend.xml 에 위치하고 있습니다.
필요한 설정은 모두 준비되었기 때문에 특별한 용도를 제외하면 수정이 필요하지 않습니다.
```

## Sysprep 사용 방법

Windows Image 생성 하기전 다음과 같이 Sysprep을 통한 전처리 과정을 거칩니다.

1. Windows  Instance 접속 후 명령 프롬프트를 실행합니다. <br/>
![[그림 1 명령 프롬프트 실행]](http://static.toastoven.net/prod_infrastructure/compute/sysprep/001_170524_800px.PNG)
<center>[그림 1 명령 프롬프트 실행]</center>
2. Sysprep을 실행합니다.
```
cd C:\Program Files\Cloudbase Solutions\Cloudbase-Init\conf
C:\Windows\System32\Sysprep\sysprep.exe /generalize /oobe /shutdown /unattend:Unattend.xml
```
![[그림 2 Sysprep 실행]](http://static.toastoven.net/prod_infrastructure/compute/sysprep/002_170524_800px.PNG)
<center>[그림 2 Sysprep 실행]</center>
![[그림 3 Sysprep 실행 화면]](http://static.toastoven.net/prod_infrastructure/compute/sysprep/003_170524_800px.PNG)
<center>[그림 3 Sysprep 실행 화면]</center>
3. Sysprep 실행 후 Instance 상태가 shutdown으로 변하는 것을 확인합니다. <br />
![[그림 4 Instance 상태 확인]](http://static.toastoven.net/prod_infrastructure/compute/sysprep/004_170524_800px.PNG)
<center>[그림 4 Instance 상태 확인]</center>
4. 이후 Image 가이드에 따라 사용자 Image를 생성하시면 됩니다.
