## Infrastructure > Compute & Network > Windows Sysprep Guide

## Sysprep을 이용한 ToastCloud 윈도우즈 이미지 생성

### Sysprep (System Preparation) 개요

사용자로부터 지정된 윈도우 설정 또는 어플리케이션의 내용을 반영하기 위해 이미징하는 작업. Microsoft Windows에서 제공되는 Sysprep을 수행하므로서 PC별 종속된 정보를 제거하여 일반화된 Windows이미지를 여러 PC로 배포할수 있습니다.

### Sysprep 단계별 기능

* 일반화 : 표준화된 Windows 이미지를 생성하기 위해 기존의 PC SID 제거

* OOBE : 기본 제공 관리자 계정으로 컴퓨터를 시작합니다. 국가별 설정 그리고 언어 및 바탕화면과 같은 기본값들이 설정됩니다.

* Unattend : 기존 설치후 응답파일을 사용하여 설정을 추가하는 역할을 합니다. OOBE의 설정을 적용할수 있으며 사용자로부터 특수한 어플리케이션 세팅을 Unattend.xml파일을 통해 sysprep과정에서 설정 할수있습니다.

### 사용자 이미지를 통한 운영시 주의사항

Sysprep는 새로 설치한 Windows를 사용하는데만 필요합니다. Windows 이미지를 다른 컴퓨터로 전송하려면 하드웨어 구성이 같더라도 일반화(“generalize”) 를 실행해야 합니다.

ToastCloud는 Sysprep 관련기술로서 “무인 설치 응답 파일” 방식을 도입하여 Unattend.xml 이라고 하는 Windows 설치용 응답파일을 기본화된 형식으로 제공하고 있으며, Windows 사용자 정보와 드라이버 및 제품 업데이트등 기본 제공되는 기능과 서비스에 필요한 추가 소프트웨어 제공을 지원하고 있습니다.

Note)

-   ToastCloud는 sysprep 실행시 기본으로 사용할수 있는 응답파일을 C:\\Program Files\\Cloud Solutions\\Cloudbase-Init\\conf\\Unattend.xml 에 제공하고 있습니다.

-   Sysprep은 SID 및 사용자 정보와 고유 정보를 삭제한다는 것을 유념해 주시기 바랍니다.

## Sysprep 단계

Sysprep는 다음과 같은 단계를 실행하여 사용자 이미지를 준비해 드립니다.

| 옵션        | 설명 |
|-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /generalize | Windows 설치를 이미징할 준비를 합니다. 이 옵션을 지정하면 Windows 설치에서 고유 시스템 정보가 모두 제거됩니다. SID(보안 ID)가 다시 설정되고 시스템 복원 지점이 모두 지워지며 이벤트 로그가 삭제됩니다. 다음에 컴퓨터가 시작될 때 specialize 구성 단계가 실행됩니다. 새 SID(보안 ID)가 만들어지며, Windows 정품 인증용 시계가 이미 세 번 다시 설정되지 않았다면 시계가 다시 설정됩니다. |
| /oobe       | 컴퓨터를 Windows 시작 모드로 다시 시작합니다. Windows 시작에서는 최종 사용자가 Windows 운영 체제를 사용자 지정하고, 사용자 계정을 만들며, 컴퓨터 이름을 지정하는 등 다양한 작업을 수행할 수 있습니다. 응답 파일에 있는 oobeSystem 구성 단계의 설정은 Windows 시작 실행 직전에 처리됩니다. |
| /shutdown   | Sysprep이 완료되면 컴퓨터를 종료합니다. |
| /unattend   | 무인 설치 동안 Windows에 응답 파일의 설정을 적용합니다. |

## ToastCloud Sysprep이 제공하는 기능들

새로운 이미지설정을 하기위해 다음과 같은 작업이 수행됩니다.

KMS Activation : 최초 인스턴스 시작시 KMS(Key management system) 클라이언트 호출을 통해 정품인증 실행

Inject Password : 최초 인스턴스 시작시 무작위 패스워드를 설정하고 이를 사용자 인증키로 암호화하여 콘솔에서 전달받을 수 있는 정보란에 기입합니다

Drive Extension : 인스턴스는 최초 생성 될 경우 플레이버의 디스크 사이즈로 변동 됩니다.

SID 초기화 : 일반화 단계를 거치면서 기존의 컴퓨터에서 사용하던 이름과 SID등 고유 정보는 삭제되며 차후 특수화 단계에서 새로운 정보로 할당되게 됩니다.

### OOBE단계 (Out-of-Box Experience)

Windows 설치에 최소 필요버전을 사용해 시스템언어 , 시간 , 그룹정보등을 입력합니다.

응답파일을 통해 호출이 가능하며 ToastCloud 는 아래와 같은 단계를 제공하고 있습니다.

```
 <HideEULAPage>true</HideEULAPage>       
                                                      
 <NetworkLocation>Work</NetworkLocation>  
                                                      
 <ProtectYourPC>1</ProtectYourPC>         
                                                      
 <SkipMachineOOBE>true</SkipMachineOOBE>  
                                                      
 <SkipUserOOBE>true</SkipUserOOBE>        
                                                      
 <InputLocale>en-US</InputLocale>         
                                                      
 <SystemLocale>en-US</SystemLocale>       
                                                      
 <UILanguage>en-US</UILanguage>           
                                                      
 <UserLocale>en-US</UserLocale>           
                                                      
 <TimeZone>UTC</TimeZone>
```

## ToastCloud Sysprep 실행하기

Sysprep 서비스로 고객용 이미지 생성절차에 대해 설명해드리겠습니다.

1. ToastCloud 콘솔의 가이드

2. ToastCloud Unattend 파일 구성 설정

    * 기본제공되어 있기 때문에 특별한 용도를 제외하면 수정이 필요하지 않습니다.

3. Windows 접속후 명령 프롬프트 실행

4. Cloudbase-init sysprep 실행

    1. Cd C:\\Program Files\\Cloudbase Solutions\\Cloudbase-Init\\conf

    2. C:\\Windows\\System32\\Sysprep\\sysprep.exe /generalize /oobe /shutdown /unattend:Unattend.xml

    ![](http://static.toastoven.net/prod_infrastructure/compute/sysprep/img_001.png)

5. Sysprep 수행 완료후 인스턴스 상태가 shutdown 로 변한 것을 확인

6. 사용자 이미지 생성 콘솔의 가이드

감사합니다.
