## Infrastructure > Compute & Network > Instances User Guide

Infrastructure 서비스의 Compute & Network상품 중 기본이 되는 리소스로서 사용자의 필요에 따라 다양한 타입의 Instance를 사용할 수 있습니다.

이 문서에서는 다음과 같은 내용을 다룹니다.

- Instance 생성
- Instance 정보 및 로그 보기
- Instance 접속 안내

## Instance 생성

[Infrastructure] > [Compute & Network] > [Instances] > [+ Instance 생성]버튼을 클릭합니다.

![[그림 1 Instance 생성]](http://static.toastoven.net/prod_infrastructure/compute/instances/001_170523_800px.PNG)
<center>[그림 1 Instance 생성]</center>

<Instance 생성> 대화창에서 [Image]탭을 선택하여 [그림 2]과 같이 Instance 가 사용할 이미지를 선택합니다.

![[그림 2 사용할 Image 선택]](http://static.toastoven.net/prod_infrastructure/compute/instances/002_170523_800px.PNG)
<center>[그림 2 사용할 Image 선택]</center>

```
[Notice]
2017년 5월 25일부터 Windows Image가 추가되었습니다. Windows Image는 최소 2GB 이상의 RAM, 50GB 이상의 Disk를 필요로 합니다.
TOAST Cloud G 서비스는 Windows Instance를 제공하지 않습니다.
```

팝업된 Instance 생성 대화창에서 [그림 3]의 Instance 정보를 입력합니다. 입력해야 하는 정보는 다음과 같습니다.

- **Zone (Availability Zone, 이하 AZ)**  
  Instance가 생성될 논리적인 구역을 의미합니다. 선택하지 않을 경우 사용 가능한 AZ를 임의로 선택하여 Instance를 생성하게 됩니다.
- **이름**  
  Instance 생성 후 생성한 Instance를 구별하기 위한 이름을 나타냅니다.
- **Flavor**  
  Flavor는 vCPU, Memory 조합으로 이루어진 하드웨어 템플릿으로서 Instance 생성의 기본이 됩니다. Flavor 마다 금액이 차이가 나므로 알맞은 Flavor를 선택합니다.
- **장치 크기 (GB)** <br />
  Instance의 root 디스크 크기입니다. 앞서 선택한 Image의 최소 디스크 크기보다 큰 값이어야 하며, 최대 1TB 까지 설정할 수 있습니다.
- **Instance 수**  
  같은 Flavor와 Image를 이용하여 여러 개의 Instance 를 동시에 생성할 수 있습니다. 여러 개의 Instance 를 동시에 생성할 경우 Instance 이름은 순차적으로 번호를 부여합니다. 기본값은 1이며 원하는 숫자를 입력합니다.

![[그림 3 Instance 정보 입력]](http://static.toastoven.net/prod_infrastructure/compute/instances/003_170523.PNG)
<center>[그림 3 Instance 정보 입력]</center>

Instance에 접속할 때 사용할 Key-Pair와 Security Group을 지정합니다. Key-Pair가 없는 경우 [+생성] 버튼을 눌러 새롭게 생성할 수 있습니다. Security Group은 Instance 의 Network 트래픽을 제어합니다. 기본 제공하는 “default” Security Group을 이용하거나 사용자가 생성한 Security Group을 지정 가능합니다. 또한 여러 개의 Security Group을 동시에 적용할 수 있습니다.

![[그림 4 Key-Pair 지정]](http://static.toastoven.net/prod_infrastructure/compute/img_54.jpg)
<center>[그림 4 Key-Pair 지정]</center>

<Instance 생성> 대화창의 [Network] 탭을 선택하여 Instance가 연결될 Network 를 선택할 수 있습니다. Instance에 적용할 Network 를 선택하는 단계로 직접 생성한 사설 Network 와 공용 Network 를 선택 할 수 있습니다. “사용 가능한 Network”에 있는 Network 중 원하는 Network 를 “선택된 Network”로 끌어다 놓습니다. 또는 [+] 버튼을 눌러 추가할 수도 있습니다. 여러 개의 Network 를 선택 가능하며, “선택된 Network” 안에서 끌어다 놓음으로써 Network 의 순서 조정도 가능합니다.

![[그림 5 Network 선택]](http://static.toastoven.net/prod_infrastructure/compute/instances/005_170523.PNG)
<center>[그림 5 Network 선택]</center>

<Instance 생성> 대화창에서 기본정보 입력, 사용할 Image 선택, Network 선택 후 [Instance 생성] 버튼을 클릭하면 Instance가 생성됩니다. 잠시 뒤 [그림 6]의 Instance 목록에서 생성된 Instance를 확인할 수 있습니다.

![[그림 6 Instance 생성 확인]](http://static.toastoven.net/prod_infrastructure/compute/instances/006_170523_800px.PNG)
<center>[그림 6 Instance 생성 확인]</center>

## 외부 Network와 통신 설정

외부 Network와 통신을 위해서는 Floating IP를 Instance에 연결하는 작업이 추가로 필요합니다. [그림 7]과 같이 Instance 목록에서 Floating IP를 부여할 Instance를 하나 선택합니다.

![[그림 7 선택한 Instance에 Floating IP연결]](http://static.toastoven.net/prod_infrastructure/compute/instances/007_170523_800px.PNG)
<center>[그림 7 선택한 Instance에 Floating IP연결]</center>

[추가기능] 드롭 다운의 [Floating IP 연결]을 선택합니다.
미리 할당 받은 Floating IP가 없다면 [+생성] 버튼을 눌러 새로운 Floating IP를 할당 받습니다

![[그림 8 Floating IP 연결 대화창]](http://static.toastoven.net/prod_infrastructure/compute/img_254.png)
<center>[그림 8 Floating IP 연결 대화창]</center>

[그림 8]의 <Floating IP 연결> 대화창에 필수 정보를 입력하고 [확인] 버튼을 클릭하여 Instance에 IP 를 연결합니다.

![[그림 9 Floating IP 할당 확인]](http://static.toastoven.net/prod_infrastructure/compute/instances/009_170523_800px.PNG)
<center>[그림 9 Floating IP 할당 확인]</center>

## Instance 로그 확인

TOAST Cloud의 웹 콘솔은 각 Instance들의 로그 보기를 지원합니다. 부팅 과정에서 발생한 메시지로 Instance의 현재 상태를 확인할 수 있습니다.

![[그림 10 Instance의 로그 확인]](http://static.toastoven.net/prod_infrastructure/compute/img_257.png)
<center>[그림 10 Instance의 로그 확인]</center>

## Instance 접속

### Linux
Linux 기반의 OS Image (= CentOS, Debian, Ubuntu)를 사용해 Instance를 생성한 경우 SSH를 사용하여 Instance에 접속합니다. Instance 목록에서 원하는 Instance를 선택하고 화면 하단에 [인스턴스 접속] 탭을 클릭하면 [그림 12]와 같은 Instance 접속 정보 화면을 볼 수 있습니다.

![[그림 11 Instance 접속방법 안내]](http://static.toastoven.net/prod_infrastructure/compute/instances/011_170523_800px.PNG)
<center>[그림 11 Instance 접속방법 안내]</center>

[인스턴스 접속] 탭에서 제시한 ssh 명령어를 이용하여 Instance에 접속합니다. Security Group에 SSH 포트가 열려있지 않으면 접속이 불가능할 수 있습니다. 부팅중인 Instance는 부팅 완료 이후에 접속할 수 있습니다.

### Windows
```
[Notice]
TOAST Cloud G 서비스는 해당 기능을 제공하지 않습니다.
```

Windows Image를 사용해 Instance를 생성한 경우 원격데스크톱 연결을 사용해 연결합니다. Instance 목록에서 원하는 Instance를 선택하고 화면 하단의 [인스턴스 접속] 탭을 클릭하면 [그림 12]와 같이 Instance 접속 정보 화면을 볼 수 있습니다.

![[그림 12 Windows Instance의 접속방법 안내]](http://static.toastoven.net/prod_infrastructure/compute/instances/012_170523_800px.PNG)
<center>[그림 12 Windows Instance의 접속방법 안내]</center>

Windows Instance에 접속하기 위해서 먼저 로그인 비밀번호를 확인해야 합니다. [인스턴스 접속] 탭에서 [Password 확인] 버튼을 클릭하면 [그림 13]과 같이 [Instance Password 가져오기] 대화창을 확인할 수 있습니다.

![[그림 13 Instance Password 가져오기 대화창]](http://static.toastoven.net/prod_infrastructure/compute/instances/013_170523.PNG)
<center>[그림 13 Instance Password 가져오기 대화창]</center>

[Instance Password 가져오기] 대화창에서는 암호화된 Password를 보여줍니다. 앞서 내려받은 Key-Pair 파일을 올리거나 복사한 뒤 붙여넣습니다. 그 후 하단의 [비밀번호 확인] 버튼을 누르면 복호화된 Password를 얻을 수 있습니다.

![[그림 14 Instance Password 가져오기 예]](http://static.toastoven.net/prod_infrastructure/compute/instances/014_170523.PNG)
<center>[그림 14 Instance Password 가져오기 예]</center>

이제 원격데스크톱 클라이언트를 사용하여 대상 Instance의 정보를 기입한 후 접속하시면 됩니다. TOAST Cloud에서는 사용자 편의성을 위해서 원격데스크톱 설정을 위한 RDP 파일을 제공하고 있습니다. [그림 15]의 [연결] 버튼을 클릭하면 RDP 파일을 다운로드 받습니다.

![[그림 15 RDP 파일 다운로드]](http://static.toastoven.net/prod_infrastructure/compute/instances/015_170523_800px.PNG)
<center>[그림 15 RDP 파일 다운로드]</center>

RDP 파일을 실행하면 원격데스크톱 클라이언트를 통해 Windows Instance에 접속할 수 있습니다.

![[그림 16 원격 데스크톱 연결 확인]](http://static.toastoven.net/prod_infrastructure/compute/instances/016_170523.PNG)
<center>[그림 16 원격 데스크톱 연결 확인]</center>

[사용자 자격 증명 입력] 대화창에서는 [인스턴스 접속] 탭에 나와 있는 계정명과 앞에서 얻은 비밀번호를 입력합니다.

![[그림 17 사용자 자격 증명 입력]](http://static.toastoven.net/prod_infrastructure/compute/instances/017_170523.PNG)
<center>[그림 17 사용자 자격 증명 입력]</center>

최종으로 Windows Instance에 접속한 화면은 다음과 같습니다.

![[그림 18 원격 데스크톱 접속 화면]](http://static.toastoven.net/prod_infrastructure/compute/instances/018_170523_800px.PNG)
<center>[그림 18 원격 데스크톱 접속 화면]</center>
