## Infrastructure > Compute & Network > Getting Started

Infrastructure > Compute & Network를 통해 사용자의 서비스를 위한 인프라를 제공합니다. 준비된 예제를 따라 하면 자신만의 서버 인프라를 구성할 수 있습니다.

이 문서에서는 예제로서 다음과 같은 내용을 다룹니다.

- Infrastructure 상품 활성화
- Instance 생성
- Floating IP 할당
- Block Storage 생성
- Image 생성
- Load Balancer 생성

## Infrastructure 상품 활성화

Project List화면에서 권한이 있는 프로젝트의 목록을 확인하고 Infrastructure 상품을 추가할 프로젝트를 선택하여 [그림 1]의 프로젝트 상세 관리화면으로 이동합니다.

```
[프로젝트명] 클릭
```

![[그림 1] 프로젝트 상세 관리화면](http://static.toastoven.net/prod_infrastructure/compute/img_201.png)
<center>[그림 1] 프로젝트 상세 관리화면</center>

```
[Infrastructure] > [Compute & Network] 클릭
```

![[그림 2] Infrastructure 활성화](http://static.toastoven.net/prod_infrastructure/compute/img_04.jpg)
<center>[그림 2] Compute & Network 활성화</center>

```
[상품이용] 클릭
```

![[그림 3] Instance 생성](http://static.toastoven.net/prod_infrastructure/compute/img_203.png)
<center>[그림 3] Instance 생성</center>

```
[+ Instance 생성] 클릭
```

### Image 선택

![[그림 4] Public Image 선택](http://static.toastoven.net/prod_infrastructure/compute/img_251.png)
<center>[그림 4] Public Image 선택</center>

### 상세 정보 입력

![[그림 5] 상세 정보 입력](http://static.toastoven.net/prod_infrastructure/compute/img_204.png)
<center>[그림 5] 상세 정보 입력</center>

```
[이름]항목에서 서버 Instance명 입력
```

### 접근 & 보안

#### Key Pair 생성

서버 Instance 에 접근하려면 ssh key Pair가 필요합니다. [그림 6]의 Key Pair 항목에 ‘가용 가능한 key pairs가 없습니다.’가 조회되면 다음의 순서로 Key Pair를 생성합니다.

![[그림 6] Key Pair와 Security Group 선택](http://static.toastoven.net/prod_infrastructure/compute/img_206.png)
<center>[그림 6] Key Pair와 Security Group 선택</center>

```
 [+ 생성] 클릭
```

![[그림 7] Key Pair 생성](http://static.toastoven.net/prod_infrastructure/compute/img_207.png)
<center>[그림 7] Key Pair 생성</center>

```
Key Pair 이름 입력
[Key Pair 생성] 버튼 클릭한 후 Key Pair 파일을 다운로드 받음
```

Key Pair(.pem파일)를 다운로드 합니다.

> [주의]
> .pem파일은 다시 다운받을 수 없으므로 보관에 유의해 주십시오.

![[그림 8] 생성된 Key-Pair 선택](http://static.toastoven.net/prod_infrastructure/compute/img_208.png)
<center>[그림 8] 생성된 Key-Pair 선택</center>

```
[Key Pair]항목에 생성한 Key Pair 확인
```

### Security Group

[그림 8]의 [Security Groups]항목에는 default가 기본으로 체크되어 있습니다. 지금은 default Security Group을 그대로 사용하겠습니다.

>[참고]
> default Security Group은 모든 외부 접속을 허용하고 있지 않습니다. 따라서 외부 접속을 위한 별도의 작업이 필요합니다.

### Network

```
"Default Network" 선택
```

![[그림 9] Network 선택](http://static.toastoven.net/prod_infrastructure/compute/img_11.jpg)
<center>[그림 9] Network 선택</center>

```
[Instance 생성] 버튼 클릭
```

Instance 생성을 위한 입력을 마쳤으므로 잠시 기다리면 Instance 생성을 완료합니다.

## Network Topology 확인

![[그림 10] Instance IP 확인](http://static.toastoven.net/prod_infrastructure/compute/img_210.png)
<center>[그림 10] Instance IP 확인</center>

현재 Instance는 사설IP(위 예에서는 192.168.0.4)만 할당되어 있어 외부에서 접속이 불가능합니다. 현재 프로젝트에 생성한 Instance의 Network Topology를 확인해보겠습니다.

```
[Infrastructure] > [Computer & Network] > [Network] > [Network Topology] 탭 클릭
```

![[그림 11] Network Topology](http://static.toastoven.net/prod_infrastructure/compute/img_211.png)
<center>[그림 11] Network Topology</center>

앞서 확인했다시피 현재 생성한 Instance는 IP는 192.168.0.4로 사설Network인 default network의 IP를 가지고 있습니다. 외부로부터의 접속을 가능하게 하려면 Public Network에 Floating IP를 부여하고 현재 Instance와 연결해야 합니다.

## Floating IP 부여

```
[Infrastructure] > [Compute & Network] > [Instances] > Instance 선택 > [추가기능] > [Floating IP 연결] 클릭
```

![[그림 12] Floating IP 연결 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_14.jpg)
<center>[그림 12] Floating IP 연결 대화창</center>

“현재 사용 가능한 IP 주소가 없습니다.”라고 나오고 있습니다. [+생성] 버튼을 클릭하여 Floating IP를 할당합니다.

```
[+생성] 버튼 클릭
```

![[그림 13] Floating IP 연결](http://static.toastoven.net/prod_infrastructure/compute/img_214.png)
<center>[그림 13] Floating IP 연결</center>

할당 받은 Floating IP주소와 Instance를 연결합니다.

```
[IP 주소] 항목에서 생성한 Floating IP주소를 선택
[연결될 포트] 항목에서 연결할 Instance를 선택
[확인]버튼 클릭
```

![[그림 14] Floating IP 할당 확인](http://static.toastoven.net/prod_infrastructure/compute/img_215.png)
<center>[그림 14] Floating IP 할당 확인</center>

이제 외부에서 접속할 수 있는 준비를 마쳤습니다.

## Security Group에 Rule 추가

아래 예제에서 133.186.132.47로 ping을 확인해보면 반응이 없습니다.

```
[~]# ping 133.186.132.47

Ping 133.186.132.47 32바이트 데이터 사용:
요청 시간이 만료되었습니다.
요청 시간이 만료되었습니다.
요청 시간이 만료되었습니다.
요청 시간이 만료되었습니다.

133.186.132.47에 대한 Ping 통계:
패킷: 보냄 = 4, 받음 = 0, 손실 = 4 (100% 손실),
[~]#
```

위와 같이 나오는 이유는”default” Security Group에서 들어오는 모든 요청을 막고 있기 때문입니다. ”Default” Security Group의 상태를 살펴보겠습니다.

```
[Infrastructure] > [Compute & Network] > [Security Groups] > “default” 선택
```

![[그림 15] Security Group 확인](http://static.toastoven.net/prod_infrastructure/compute/img_216.png)
<center>[그림 15] Security Group 확인</center>

현재 들어오는(Ingress) IP는 다 막혀있습니다. 여기에 ICMP 접속을 허용하는 보안규칙을 추가해보겠습니다.

```
[+ Rule 추가] 버튼 클릭
```

![[그림 16] Rule 추가 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_19.jpg)
<center>[그림 16] Rule 추가 대화창</center>

```
[Rule] 항목에서 ALL ICMP 선택
[Direction] 항목 에서 Ingress 선택
[원격] 항목에서 CIDR 선택
[CIDR] 항목에서 0.0.0.0/0 선택
[추가] 버튼 클릭
```

![[그림 17] Rule 추가 확인](http://static.toastoven.net/prod_infrastructure/compute/img_218.png)
<center>[그림 17] Rule 추가 확인</center>

[그림 15] ~ [그림 16]에서 ICMP 외부 접속을 허용하도록 Rule을 추가했으므로 ping 테스트를 다시 해봅니다.

```
[~]# ping 133.186.132.47

Ping 133.186.132.47바이트 데이터 사용:
 133.186.132.47의 응답: 바이트=32 시간=3ms TTL=50
133.186.132.47의 응답: 바이트=32 시간=2ms TTL=50
133.186.132.47의 응답: 바이트=32 시간=2ms TTL=50
133.186.132.47의 응답: 바이트=32 시간=2ms TTL=50

133.186.132.47에 대한 Ping 통계:
패킷: 보냄 = 4, 받음 = 4, 손실 = 0 (0% 손실), 왕복
시간(밀리초):
최소 = 2ms, 최대 = 3ms, 평균 = 2ms [~]#
```

ping 테스트를 완료했습니다. 추가로 SSH 접속을 허용해보겠습니다.

```
[+ Rule 추가] 버튼 클릭
[Rule] 항목에서 SSH 선택
[원격] 항목에서 CIDR 선택
[CIDR] 항목에서 0.0.0.0/0 선택
[추가] 버튼 클릭
```

![[그림 18] SSH 규칙](http://static.toastoven.net/prod_infrastructure/compute/img_219.png)
<center>[그림 18] SSH 규칙</center>

SSH 접속 테스트를 수행하겠습니다. 접속을 하려면 앞서 다운로드한 Key Pair 파일(*.pem)이 필요합니다. Key Pair 파일을 통해 SSH 접속을 하려면 Key Pair 파일의 접근 속성을 변경해야 합니다.

```
[~]# chmod 0400 my_keypair.pem
```

> [참고]
> Windows 사용자는 Cygwin을 설치하면 콘솔 작업이 가능합니다. 그 외 접속방법은 [Windows SSH Guide]를 참고해주십시오.

이제 ssh로 접속합니다.

```
[~]# ssh -i my_keypair.pem root@133.186.151.245
Last login: Fri Oct 10 14:38:36 2014
[root@host-192-168-0-2 ~]#
```

> [참고]
> 위 예에서는 모든 주소로 접속할 수 있도록 했습니다. 하지만 가능하면 CIDR값으로 접속 대역을 지정해 주는 것이 좋습니다. CIDR 설정에 익숙하지 않다면 IP to CIDR(http://ip2cidr.com/)에서 변환하여 입력해 주십시오.

현재까지의 가상 인프라 구성은 다음과 같습니다.

![[그림 19] 가상 Instance 구성도](http://static.toastoven.net/prod_infrastructure/compute/img_22.jpg)
<center>[그림 19] 가상 Instance 구성도</center>

## 웹 서버 구동

Instance를 간단한 웹서버로 사용해보겠습니다. 우선 Security Group에 HTTP 접속 허용을 추가합니다.

```
[+ Rule 추가] 클릭
[Rule] 항목에서 HTTP 선택
[원격] 항목에서 CIDR 선택
[CIDR] 항목에서 0.0.0.0/0 선택
[추가] 버튼 클릭
```

80포트로 웹서버를 실행해 보기 위해 index.html이라는 웹페이지를 하나 생성합니다. (입력을 다 마친 후 CTRL+D를 누르면 저장됩니다.)

```
[root@host-192-168-0-4 ~]# cat > index.html
<html>
<body>
hello world!
</body>
</html>
```

웹서버를 실행합니다.

```
[root@host-192-168-0-4 ~]# python -m SimpleHTTPServer 80
Serving HTTP on 0.0.0.0 port 80 ..
```

![[그림 20] 웹브라우저 접속](http://static.toastoven.net/prod_infrastructure/compute/img_221.png)
<center>[그림 20] 웹브라우저 접속</center>

웹서버에서 접속을 하면 다음과 같은 로그가 출력됩니다.

```
[root@host-192-168-0-4 ~]# python -m SimpleHTTPServer 80
 Serving HTTP on 0.0.0.0 port 80 ...
103.243.200.42 - - [11/Nov/2015 17:03:15] "GET / HTTP/1.1" 200 -
```

## Block Storage 생성하기

Instance에 접속하여 Disk 용량을 확인해보겠습니다.

```
[root@host-192-168-0-4 ~]# df -h
Filesystem            Size  Used Avail Use% Mounted on
/dev/vda2              18G  988M   16G   6% /
tmpfs                 499M     0  499M   0% /dev/shm
[root@host-192-168-0-4 ~]#
```

현재 Instance는 16G정도의 여유공간이 있습니다. 좀더 많은 Disk 공간을 확보하고 싶으면 Block Storage를 추가하면 됩니다. 우선 Block Storage를 생성해보겠습니다.

### Block Storage 생성

![[그림 21] Block Storage 생성](http://static.toastoven.net/prod_infrastructure/compute/blockstorage/img001.png)
<center>[그림 21] Block Storage 생성</center>

```
[Infrastructure] > [Compute & Network] > [Block Storage] > [+Block Storage 생성] 버튼 클릭.
```

![[그림 22] Block Storage 생성 정보 입력](http://static.toastoven.net/prod_infrastructure/compute/blockstorage/img002.png)
<center>[그림 22] Block Storage 생성 정보 입력</center>

```
[Block Storage 이름] 항목에서 Block Storage명 입력
[크기(GB)] 항목에서 Disk 크기 입력
[Zone] 항목에서 기본값 유지
[Block Storage 생성] 버튼 클릭
```

Block Storage는 Instance와 연결해야 사용 가능합니다. [그림 24]의 [연결 관리]을 클릭하여 Block Storage와 연결할 Instance를 선택합니다.

![[그림 23] Block Storage 생성 확인](http://static.toastoven.net/prod_infrastructure/compute/blockstorage/img005.png)
<center>[그림 23] Block Storage 생성 확인</center>

```
연결할 Block Storage 선택
[연결관리] 버튼 클릭.
```

![[그림 24] Block Storage 연결 관리 대화창](http://static.toastoven.net/prod_infrastructure/compute/blockstorage/img006.png)
<center>[그림 24] Block Storage 연결 관리 대화창</center>

```
<Block Storage 연결 관리> 대화창의 [Instance에 연결] 항목에서 Block Storage을 연결할 Instance 선택
```

Instance에 Block Storage가 연결되었는지 리스트의 ‘연결 정보’에서 확인합니다.

![[그림 25] 연결 정보 확인](http://static.toastoven.net/prod_infrastructure/compute/blockstorage/img007.png)
<center>[그림 25] 연결 정보 확인</center>

### Instance 접속 및 Block Storage 마운트

물리적인 연결은 마쳤으므로 Instance에 접속하여 파일시스템 생성 및 마운트를 해보겠습니다. Instance에 접속하여 파일시스템을 생성합니다.

```
[root@host-192-168-0-4 ~]# mkfs.ext4 /dev/vdb
mke2fs 1.41.12 (17-May-2010)
Filesystem label=
OS type: Linux
Block size=4096 (log=2)
Fragment size=4096 (log=2)
Stride=0 blocks, Stripe width=0 blocks
655360 inodes, 2621440 blocks
131072 blocks (5.00%) reserved for the super user
First data block=0
Maximum filesystem blocks=2684354560
80 block groups
32768 blocks per group, 32768 fragments per group
8192 inodes per group
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632

Writing inode tables: done
Creating journal (32768 blocks): done
Writing superblocks and filesystem accounting information: done

This filesystem will be automatically checked every 32 mounts or
180 days, whichever comes first.  Use tune2fs -c or -i to override.
```

마운트를 수행합니다.

```
[root@host-192-168-0-4 ~]# mkdir external
[root@host-192-168-0-4 ~]# mount /dev/vdb external
```

연결이 제대로 되었는지 확인합니다.

```
[root@host-192-168-0-4 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/vda2        18G  988M   16G   6% /
tmpfs           499M     0  499M   0% /dev/shm
/dev/vdb        9.9G  151M  9.2G   2% /root/external
```

위 예에서는 /dev/vdb가 /root/external과 연결되어 있고 사용 가능용량은 9.2G입니다.

### Block Storage 해제하기

사용중인 Block Storage를 반납할 경우 다음 순서로 진행합니다.

- 언마운트
- Block Storage 연결 해제

> [주의]
> 언마운트를 하지 않으면 데이터가 유실되므로 Block Storage 해제 전 반드시 언마운트를 수행해 주십시오.

Instance에서 언마운트를 수행한 후 연결 상태를 확인합니다.

```
[root@host-192-168-0-4 ~]# umount external/
[root@host-192-168-0-4 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/vda2        18G  989M   16G   6% /
tmpfs           499M     0  499M   0% /dev/shm
[root@host-192-168-0-4 ~]#
```

Block Storage를 Instance에서 연결 해제합니다.

```
[Infrastructure] > [Compute & Network] > Block Storage 선택 > [연결 관리] 버튼 클릭
<연결 관리 > 대화창에서 Instance 선택
[Block Storage 연결 해제] 버튼 클릭
```

![[그림 26] Block Storage 연결 해제](http://static.toastoven.net/prod_infrastructure/compute/blockstorage/img009.png)
<center>[그림 26] Block Storage 연결 해제</center>

Block Storage 해제 최종 확인을 수행합니다.

```
[Block Storage 연결 해제] 버튼 클릭
```

![[그림 27] Block Storage 연결 해제 확인](http://static.toastoven.net/prod_infrastructure/compute/blockstorage/img010.png)
<center>[그림 27] Block Storage 연결 해제 확인</center>

Block Storage 연결 해제를 마쳤습니다. [그림 29]의 Block Storage 리스트에서 연결 정보가 비어있는지 확인합니다.

![[그림 28] Block Storage 연결 해제 확인](http://static.toastoven.net/prod_infrastructure/compute/blockstorage/img011.png)
<center>[그림 28] Block Storage 연결 해제 확인</center>

## Image 생성하기

기존 Instance를 Image로 만들고 재사용 해보겠습니다. Image를 생성하려면 Instance를 정지해야 합니다.

```
[Infrastructure] > [Compute & Network] > [Instances]
Image를 생성할 Instance를 선택한 후 [추가기능] > [Instance Shutdown] 선택
Instance 목록에서 Image를 생성할 Instance의 전원상태 확인
```

Instance의 전원상태가 회색으로 SHUTDOWN상태인지 확인합니다.

![[그림 29] Instance의 전원상태 확인](http://static.toastoven.net/prod_infrastructure/compute/img_230.png)
<center>[그림 29] Instance의 전원상태 확인</center>

Image 생성을 수행합니다.

```
Image를 생성할 Instance를 선택
[추가기능] > [Image 생성] 선택
```

![[그림 30] Image 생성](http://static.toastoven.net/prod_infrastructure/compute/img_231.png)
<center>[그림 30] Image 생성</center>

![[그림 31] Image 생성](http://static.toastoven.net/prod_infrastructure/compute/img_232.png)
<center>[그림 31] Image 생성</center>

```
[이름]항목에 Image명 입력
[Image 생성] 버튼 클릭
```

잠시 후 Image 생성이 완료됩니다. 생성한 Image를 리스트에서 확인합니다.

```
[Infrastructure] > [Compute & Network] > [Images] 선택
```

![[그림 32] Image 생성 확인](http://static.toastoven.net/prod_infrastructure/compute/img_233.png)
<center>[그림 32] Image 생성 확인</center>

## Image로 Instance 생성

방금 생성한 Image로 Instance를 2개 생성해 보겠습니다.

```
[Infrastructure] > [Compute & Network] > [Instance] > [Instance 생성] 클릭
```

![[그림 33] Private Image 선택](http://static.toastoven.net/prod_infrastructure/compute/img_235.png)
<center>[그림 33] Private Image 선택</center>

Instance 생성에 사용할 Private Image를 선택하고 나머지 Instance 정보를 입력합니다.

```
[Zone] 항목에서 Instance를 생성할 Zone 선택
[이름] 항목에서 Instance명 입력
[Flavor] 항목에서 생성할 Instance의 규격 선택
[Instance 수]에 2로 변경
[Key Pair], [Security Groups], [Network] 항목에서 적절한 값을 선택
[Instance 생성] 버튼 클릭
```

![[그림 34] Instance 정보 입력(Instance 2개)](http://static.toastoven.net/prod_infrastructure/compute/img_236.png)
<center>[그림 34] Instance 정보 입력(Instance 2개)</center>

잠시 후 Instance 2개 생성을 완료합니다. Instance 목록에서 생성한 Instance를 확인합니다.

![[그림 35] Instance 2개 생성 확인](http://static.toastoven.net/prod_infrastructure/compute/img_237.png)
<center>[그림 35] Instance 2개 생성 확인</center>

각 Instance에 Floating IP를 연결합니다.

```
첫 번째 Instance 선택 후 [추가 기능] > [Floating IP 연결] 클릭
[IP주소] 항목에서 IP주소 선택 (사용 가능한 IP 주소가 없는 경우 [+생성] 버튼 클릭하여 할당 수행)
[연결될 포트] 항목에서 첫 번째 Instance의 private 주소 선택
[확인] 버튼 클릭

두 번째 Instance 선택 후 [추가 기능] > [Floating IP 연결] 클릭
[IP주소] 항목에서 IP주소 선택 (사용 가능한 IP 주소가 없는 경우 [+생성] 버튼 클릭하여 할당 수행)
[연결될 포트] 항목에서 두 번째 Instance의 private 주소 선택
[확인] 버튼 클릭
```

![[그림 36] Instance 2개 Floating IP 확인](http://static.toastoven.net/prod_infrastructure/compute/img_238.png)
<center>[그림 36] Instance 2개 Floating IP 확인</center>

## Load Balancer 붙이기

2대의 웹서버에 부하를 분산할 수 있도록 Load Balancer를 붙여보겠습니다.

```
[Infrastructure] > [Compute & Network] > [Load Balancers] > [+ Load Balancer 생성] 버튼 클릭
```

![[그림 37] Load Balancer 생성](http://static.toastoven.net/prod_infrastructure/compute/img_239.png)
<center>[그림 37] Load Balancer 생성</center>

![[그림 38] Load Balancer 정의](http://static.toastoven.net/prod_infrastructure/compute/img_240.png)
<center>[그림 38] Load Balancer 정의</center>

```
[이름] 항목에서 Load Balancer 이름을 입력
[설명] 항목에서 설명 입력
[Load Balancing 방식] 항목에서 “ROUND_ROBIN” 선택
[Network(Subnet)] 항목에서 “[Default network]192.168.0.0/24” 선택
[프로토콜] 항목에서 “HTTP” 선택
[Load Balancer Port] 항목에서 “80” 입력
[Instance Port]항목에서 “80”입력
[다음] 버튼 클릭
```

연결할 Instance 2대를 추가합니다.

```
좌측 Instance 목록에서 연결할 Instance 2대의 [+] 버튼 클릭
[다음] 버튼 클릭
```

![[그림 39] Instance 연결](http://static.toastoven.net/prod_infrastructure/compute/img_241.png)
<center>[그림 39] Instance 연결</center>

상태 확인을 위한 Health Check 구성 정보를 입력합니다.

![[그림 40] Health Check 설정](http://static.toastoven.net/prod_infrastructure/compute/img_242.png)
<center>[그림 40] Health Check 설정</center>

```
[Health Port] 항목에 “80”입력
[다음] 버튼 클릭
```

![[그림 41] 고급 연결 옵션](http://static.toastoven.net/prod_infrastructure/compute/img_243.png)
<center>[그림 41] 고급 연결 옵션</center>

```
[추가] 버튼 클릭
```

리스트에서 생성 완료한 Load Balancer를 확인합니다.

![[그림 42] Load Balancer 생성 확인](http://static.toastoven.net/prod_infrastructure/compute/img_244.png)
<center>[그림 42] Load Balancer 생성 확인</center>


외부에서 Load Balancer를 액세스할 수 있도록 Floating IP를 연결해보겠습니다.

```
Floating IP를 연결할 Load Balancer 선택 후 [Floating IP 연결] 버튼 클릭
```

![[그림 43] Load Balancer에 Floating IP 연결 대화창](http://static.toastoven.net/prod_infrastructure/compute/img_14.jpg)
<center>[그림 43] Load Balancer에 Floating IP 연결 대화창</center>

```
[IP 주소] 항목에서 [+생성] 버튼을 클릭
[연결될 포트] 항목에서 Load Balancer의 IP를 선택
[연결] 버튼 클릭
```

Floating IP가 연결되었는지 리스트를 확인합니다.

![[그림 44] Load Balancer Floating IP 연결 확인](http://static.toastoven.net/prod_infrastructure/compute/img_246.png)
<center>[그림 44] Load Balancer Floating IP 연결 확인</center>

웹브라우저에서 Load Balancer로 접속해보기 전에 먼저 2대의 웹서버를 구동합니다.

```
# ssh -i my_keypair.pem root@133.186.132.157
…
[root@host-192-168-0-6 ~]# python -m SimpleHTTPServer 80
Serving HTTP on 0.0.0.0 port 80 ...

# ssh -i my_keypair.pem root@133.186.132.225
…
[root@host-192-168-0-7 ~]# python -m SimpleHTTPServer 80
 Serving HTTP on 0.0.0.0 port 80 ...
```

Load Balancer에 할당된 Floating IP로 접속합니다. 새로 고침 하면서 2대의 서버에서 ROUND_ROBIN 설정대로 번갈아 로그가 남는지 확인합니다.

![[그림 45] Load Balancer Floating IP를 통한 접근](http://static.toastoven.net/prod_infrastructure/compute/img_247.png)
<center>[그림 45] Load Balancer Floating IP를 통한 접근</center>

```
[root@host-192-168-0-6 ~]# python -m SimpleHTTPServer 80 Serving HTTP on 0.0.0.0 port 80 ...
192.168.0.10 - - [12/Nov/2015 13:42:03] "GET / HTTP/1.1" 200 -
192.168.0.10 - - [12/Nov/2015 13:42:23] "GET / HTTP/1.1" 200 -
192.168.0.10 - - [12/Nov/2015 13:42:25] "GET / HTTP/1.1" 200 -
192.168.0.10 - - [12/Nov/2015 13:42:26] "GET / HTTP/1.1" 200 -
192.168.0.10 - - [12/Nov/2015 13:42:26] "GET / HTTP/1.1" 200 –
…


[root@host-192-168-0-7 ~]# python -m SimpleHTTPServer 80 Serving HTTP on 0.0.0.0 port 80 ...
192.168.0.10 - - [12/Nov/2015 13:42:24] "GET / HTTP/1.1" 200 -
192.168.0.10 - - [12/Nov/2015 13:42:25] "GET / HTTP/1.1" 200 -
192.168.0.10 - - [12/Nov/2015 13:42:26] "GET / HTTP/1.1" 200 -
192.168.0.10 - - [12/Nov/2015 13:42:27] "GET / HTTP/1.1" 200 -
192.168.0.10 - - [12/Nov/2015 13:42:28] "GET / HTTP/1.1" 200 –
…
```

지금까지 구축한 내용은 다음과 같습니다.

![[그림 46] Load Balancer 연동 구성도](http://static.toastoven.net/prod_infrastructure/compute/img_248.png)
<center>[그림 46] Load Balancer 연동 구성도</center>

## 맺음말

TOAST Cloud > Infrastructure 서비스에서 제공하는 가상 인프라 사용법에 대하여 알아보았습니다. 지금까지의 내용을 요약해 보았습니다.

### 가상 Instance

- 처음 생성시 내부 사설IP만 할당되어 있습니다. 외부에서 접속을 하고자 하는 경우에는 Floating IP를 할당해야 합니다.

### 기본 Security Group

- 초기 기본 Security Group은 외부접속을 모두 허용하지 않습니다. 따라서 외부 접속을 허용할 IP, PORT에 대한 룰을 추가해야 합니다.

### Block Storage

- Image로 제공하는 Disk 용량이 모자랄 경우 Block Storage를 사용합니다.
- Block Storage를 생성한 후에는 Instance 연결, 파일시스템 생성, 마운트 과정을 거치면 사용 가능합니다.
- Block Storage를 반납 할 때는 언마운트, 연결해제 순으로 진행합니다.

### Image
- Instance를 Shutdown 시킨 후에 Private Image를 생성할 수 있습니다.
- Private Image로 원하는 만큼 Instance를 생성할 수 있습니다.

### Load Balancer
- 서비스 부하가 증가하는 경우 Private Image로 Instance를 생성한 후 Load Balancer에 연결하면 부하가 분산됩니다.
