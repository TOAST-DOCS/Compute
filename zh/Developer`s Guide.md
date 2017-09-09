## Infrastructure > Compute & Network > Developer's Guide

## 사전 준비

### App Key 확인

1. [Infrastructure] > [Compute & Network] 메뉴 클릭
2. 상단에 보이는 [URL & Appkey] 클릭
3. 대화창에 기재 된 [Appkey] 값 복사 후 사용

### API Password 설정

1. [Infrastructure] > [Compute & Network] 메뉴 클릭
2. 상단에 보이는 [API Endpoint 설정] 버튼 클릭
3. &lt;API Endpoint&gt; 대화창에서 원하는 API 비밀번호를 지정

## 기본 정보
### API Endpoint
```
http://api-compute.cloud.toast.com/v1.0/appkeys/{appkey}
```
###### Parameters
| Name | In | Type | Description |
| -- | -- | -- | -- |
| appkey | Path Variable | String | 상품 이용시 발급받은 앱키 |

### API Response
##### Response HTTP Status Code
모든 API 요청에 대해 200 OK로 응답하며, JSON 형태의 Response Body를 포함합니다.

##### Response Body
Response Body에는 "header" 정보가 기본으로 포함되어 있으며, 이를 통해 자세한 응답 결과를 확인할 수 있습니다.
API에 따라 "header" 외 추가적인 정보가 포함될 수 있습니다.

```json
{
    "header" : {
        "isSuccessful" : true,
        "resultCode": 0,
        "resultMessage" : "SUCCESS"
    }
}
```
| isSuccessfu | resultCode | resultMessage |
| --- | --- | --- |
| true | 0 | SUCCESS |
| false  | -1 | FAIL [: detail description] |
| false | -2 | UNKNOWN EXCEPTION |
| false | -3 | Permission denied [: detail description] |
| false | -4 | Invalid parameters [: detail description] |
| false | -5 | Nonexistent [: detail description] |
| false | -6 | Failed to query internal db [: detail description] |
| false | -7 | Not supported [: detail description] |
| false | -8 | JSON parsing error [: detail description] |
| false | 10000~10999| Server API 관련 에러 메시지 |
| false | 11000~11999| Flavor API 관련 에러 메시지 |
| false | 12000~12999| Availability Zone API 관련 에러 메시지 |
| false | 13000~13999| Keypair API 관련 에러 메시지 |
| false | 20000~20999| Network API 관련 에러 메시지 |
| false | 21000~21999| Subnet API 관련 에러 메시지 |
| false | 22000~22999| Floating IP API 관련 에러 메시지 |
| false | 23000~23999| Load Balancer API 관련 에러 메시지 |
| false | 24000~24999| Security Group API 관련 에러 메시지 |
| false | 30000~30999| Image API 관련 에러 메시지 |
| false | 40000~40999| Volume API 관련 에러 메시지 |
| false | 50000~50999| Token API 관련 에러 메시지 |

## Token 
**Token** 은 Compute & Network의 RESTful API 사용을 위해 발급받아야 하는 인증키이며, 이후 모든 API 요청 시 Request에 **X-Auth-Token** Header로 입력하여 요청해야 합니다.
### Token API
#### Token 발급
##### Method, URL
```
POST /v1.0/appkeys/{appkey}/tokens
Content-Type: application/json;charset=UTF-8
```


##### Request Body
```json
{
	"auth" : {
    	"username" : "User Name",
        "password" : "API Password"
    }
}
```
###### Parameters
| Name | In | Type | Optional | Description |
| -- | -- | -- | -- | -- |
| username | Body | String | - | TOAST Cloud 사용자 계정 ID |
| password | Body | String | - | API 패스워드 |

##### Response Body
```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    },
    "access" : {
        "token" : {
            "expires" :  "{Expires}",
            "id" :  "{Token ID}",
            "issued_at" :  "{Issued at}"
        },
        "user" : {
            "id" :  "{User ID}",
            "roles" : [
                {
                    "name" :  "{Role name}"
                }
            ]
        }
    }    
}
```
###### Parameters
| Name | In | Type | Optional | Description |
| -- | -- | -- | -- | -- |
| Token ID | Body | String | - | API 요청 시 HTTP 헤더(X-Auth-Token) 에 기재해야 하는 UUID |
| Issued at | Body | String | - | 토큰 발급 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Expires | Body | String | - | 발급한 Token의 만료 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T03:17:50Z |
| User ID | Body | String | - | 토큰을 발급받은 사용자의 UUID | 
| Role name | Body | String | - | 토큰을 발급받은 사용자에게 부여된 Role |

#### Token 정보 조회
##### Method, URL
```
GET /v1.0/appkey/{appkey}/tokens/{tokenId}
```
###### Parameters
|  Name | In | Type | Optional |Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "access": {
        "token": {
            "expires": "{Expires}",
            "id": "{Token ID}",
            "issued_at": "{Issued at}"
        },
        "user": {
            "id": "{User ID}",
            "roles": [
                {
                    "name": "{Role name}"
                }
            ]
        }
    }
}
```
###### Parameters
| Name | In | Type | Optional | Description |
| -- | -- | -- | -- | -- |
| Token ID | Body | String | - | API 요청 시 HTTP 헤더(X-Auth-Token) 에 기재해야 하는 UUID |
| Issued at | Body | String | - | 토큰 발급 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Expires | Body | String | - | 발급한 Token의 만료 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T03:17:50Z |
| User ID | Body | String | - | 토큰을 발급받은 사용자의 UUID | 
| Role name | Body | String | - | 토큰을 발급받은 사용자에게 부여된 Role |


## Server
### Server API
Server 생성, 삭제, 정보 조회 및 Block Storage 연결관리 기능을 제공합니다.

#### Server Status
Server는 생성, 변경, 삭제, 운영 중 다음과 같은 Status를 갖습니다.
![[그림 1] Server Status Diagram](http://static.toastoven.net/prod_infrastructure/compute/developersguide/img_001.png)
<center>[그림 1] Server Status Diagram</center>

| Status | Description |
| --- | --- |
| BUILD | Server 생성 중 |
| POWERING_ON | Server 부팅 중 |
| ACTIVE | Server 구동 중 |
| POWERING_OFF | Server 종료 중 |
| STOP | Server 종료 상태 |
| REBOOTING | Server Rebooting 중 |
| RESIZING | Server Resize 작업 중 |
| MIGRATING | Server Migration 작업 중 |
| DELETING | Server 삭제 중 |
| ERROR | 오류 상태 |

#### Server 목록 간략 조회
생성되어 있는 Server들의 간략한 정보(ID, Name, Status)를 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/servers
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional |Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "servers": [
        {
            "id": "{Server ID}",
            "name": "{Server Name}",
            "status": "{Server Status}"
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| Server ID | Body | String | Server 식별자 |
| Server Name | Body | String | Server 이름 (Linux의 경우 최대 255자, Windows의 경우 최대 12자) |
| Server Status | Body | String | Server의 상태 |

#### Server 목록 상세 조회
생성되어 있는 모든 Server들의 상세한 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/servers/detail
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional |Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "servers": [
        {
            "addresses": [
                {
                    "macAddress": "{MAC Address}",
                    "ipAddress": "{IP Address}",
                    "version": "{IP Version}",
                    "floatingIpAddress": "{Floating IP Address}"
                }
            ],
            "availabilityZone": "{Zone Name}",
            "flavor": {
                "id": "{Flavor ID}",
                "name": "{Flavor Name}",
                "cpu": "{Flavor CPU}",
                "ram": "{Flavor RAM}"
            },
            "status": "{Status}",
            "id": "{Server ID}",
            "name": "{Server Name}",
            "image": "{Image ID}",
            "metadata": {
                "key": "value"
            },
            "keyName": "{PEM Key Name}",
            "volumes": {
                "root" : {
                    "size" : "{Root Volume Size}"
                },
                "attachments" : [
                    {
                        "id" : "{Attached Volume ID}",
                        "name": "{Attached Volume Name}",
                        "size": "{Attached Volume Size}"
                    }
                ]
            },
            "securityGroups": [
                {
                    "name": "{Security Group Name}"
                }
            ],
            "launchedAt": "{Launched Time}",
            "createdAt": "{Created Time}",
            "updatedAt": "{Updated Time}"
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| MAC Address | Body | String | - | NIC의 MAC address |
| IP Address | Body | String | - | NIC의 IP Address |
| version | Body | Integer | - | IP Version. TOAST Cloud에서는 IP v4만 지원 |
| Floating IP Address | Body | String | O | NIC에 할당된 Floatin IP Address |
| Zone Name | Body | String | - | Availability Zone |
| Flavor ID | Body | String | - | Flavor 식별자 |
| Flavor Name | Body | String | - | Flavor name |
| Flavor CPU | Body | Integer | - | CPU 개수 |
| Flavor RAM | Body | Integer | - | RAM 크기, MB 단위 |
| Status | Body | String | - | Server의 상태 |
| Server ID | Body | String | - | Server 식별자 |
| Server Name | Body | String | - | Server 이름 (Linux의 경우 최대 255자, Windows의 경우 최대 12자) |
| Image ID | Body | String | - | Server에 설치된 Image ID |
| metadata | Body | Object | - | Server에 설정할 사용자 metadata, "key": "value" 형태로 저장 |
| PEM Key Name | Body | String | - | Server에 등록할 Key-pair 이름 |
| Root Volume Size | Body | Integer | - | Root Disk 크기, GB 단위 |
| Attached Volume ID | Body | String | O | 추가 Block Storage 식별자 |
| Attached Volume Name | Body | String | O | 추가 Block Storage 이름 |
| Attached Volume Size | Body | Integer | O | 추가 Block Storage 크기, GB 단위 |
| Security Group Name | Body | String | - | Server에 등록된 Security Group의 이름 |
| Launched Time | Body | String | - | Server 최근 부팅 시각. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Created Time | Body | String | - | Server 생성 시각. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Updated Time | Body | String | - | Server 수정 시각. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |

#### Server 단건 조회
특정 Server의 상세 정보를 조회합니다.

##### Method, URL
```
GET /v1.0/appkeys/{appkey}/servers/{serverId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| serverId | Path | String | - | 정보를 조회 할 Server의 식별자 |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "server":  {
        "addresses": [
            {
                "macAddress": "{MAC Address}",
                "ipAddress": "{IP Address}",
                "version": "{IP Version}",
                "floatingIpAddress": "{Floating IP Address}"
            }
        ],
        "availabilityZone": "{Zone Name}",
        "flavor": {
            "id": "{Flavor ID}",
            "name": "{Flavor Name}",
            "cpu": "{Flavor CPU}",
            "ram": "{Flavor RAM}"
        },
        "status": "{Status}",
        "id": "{Server ID}",
        "name": "{Server Name}",
        "image": "{Image ID}",
        "metadata": {
            "key": "value"
        },
        "keyName": "{Key Name}",
        "volumes": {
            "root" : {
                "size" : "{Volume Size}"
            },
            "attachments" : [
                {
                    "id" : "{Volume ID}",
                    "name": "{Volume Name}",
                    "size": "{Volume Size}"
                }
            ]
        },
        "securityGroups": [
            {
                "name": "default"
            }
        ],
        "launchedAt": "{Launched Time}",
        "createdAt": "{Created Time}",
        "updateAt": "{Updated Time}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| MAC Address | Body | String | - | NIC의 MAC address |
| IP Address | Body | String | - | NIC의 IP Address |
| version | Body | Integer | - | IP Version. TOAST Cloud에서는 IP v4만 지원 |
| Floating IP Address | Body | String | O | NIC에 할당된 Floatin IP Address |
| Zone Name | Body | String | - | Availability Zone |
| Flavor ID | Body | String | - | Flavor 식별자 |
| Flavor Name | Body | String | - | Flavor name |
| Flavor CPU | Body | Integer | - | CPU 갯수 |
| Flavor RAM | Body | Integer | - | RAM 크기, MB 단위 |
| Status | Body | String | - | Server의 상태 |
| Server ID | Body | String | - | Server 식별자 |
| Server Name | Body | String | - | Server 이름 (Linux의 경우 최대 255자, Windows의 경우 최대 12자) |
| Image ID | Body | String | - | Server에 설치된 Image ID |
| metadata | Body | Object | - | Server에 설정할 사용자 metadata, "key": "value" 형태로 저장 |
| PEM Key Name | Body | String | - | Server에 등록할 Key-pair 이름 |
| Root Volume Size | Body | Integer | - | Root Disk의 크기, GB 단위 |
| Attached Volume ID | Body | String | O | 추가 Block Storage 식별자 |
| Attached Volume Name | Body | String | O | 추가 Block Storage 이름 |
| Attached Volume Size | Body | Integer | O | 추가 Block Storage 크기, GB 단위 |
| Security Group Name | Body | String | - | Server에 등록된 Security Group의 이름 |
| Launched Time | Body | String | - | Server 최근 부팅 시각. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Created Time | Body | String | - | Server 생성 시각. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Updated Time | Body | String | - | Server 수정 시각. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |

#### Server 생성
새로운 Server를 생성합니다.

##### Method, URL
```
POST /v1.0/appkeys/{appkey}/servers
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

##### Request Body
```json
{
    "server": {
        "name": "{Server Name}",
        "image": "{Image ID}",
        "flavor": "{Flavor ID}",
        "networks": [
        	{
            	"id": "{Network ID}"
        	}
        ],
        "availabilityZone": "{Availability Zone}",
        "keyName": "{Key Name}",
        "count": "{Count}",
        "volumes": [
        	{
            	"size": "{Volume Size}"
        	}
        ],
        "securityGroups": [
        	{
            	"name": "{Security Group Name}"
        	}
		]
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Server Name | Body | String | - | Server 이름 (Linux의 경우 최대 255자, Windows의 경우 최대 12자) |
| Image ID | Body | String | - | Server에 설치할 Image 식별자 |
| Flavor ID | Body | String | - | Server의 Flavor 식별자 |
| Network ID | Body | String | - | Server가 연결될 Network 식별자 |
| Availability Zone | Body | String | - | Server가 생성될 Availability Zone |
| Key Name | Body | String | - | Server에 등록할 Key-pair 이름 |
| Count | Body | Integer | - | 동시 생성할 Server의 대수, 최대 10대로 제한 |
| Volume Size | Body | Integer | - | Server의 Root Disk 크기, 허용가능한 Volume size는 Flavor에 따라 정해짐 |
| Security Group Name | Body | String | - | Server에 등록할 Security Group 이름 |

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "server": {
        "id": "{Server ID}",
        "name": "{Server Name}",
        "status": "{Server Status}"
    }
}
```
###### Parameters
| Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Server ID | body | String | - |생성된 Server 식별자 |
| Server Name | body | String | - |Server 이름 (Linux의 경우 최대 255자, Windows의 경우 최대 12자) |
| Server Status | Body | String | - |Server의 상태 |

#### Server 삭제
특정 Server를 삭제합니다.
##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/servers/{serverId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | Header | String | Token ID |
| serverId | Path | String | 삭제할 Server의 고유 ID |

#### Block Storage 연결
Server에 추가적인 Block Strorage를 연결합니다.

##### Method, URL
```
POST infrastructure/v1.0/appkeys/{appkey}/servers/{serverId}/attachments
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| serverId | Path | String | - | Block Strorage를 연결 할 Server의 고유 ID |

##### Request Body
```json
{
    "attachment":{
        "volumeId":"{Volume ID}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Volume ID | body | String | - | Server에 연결할 Block Strorage 식별자 |

##### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "attachment": {
        "device": "{Device ID}",
        "id": "{Attachment ID}",
        "volumeId": "{Volume ID}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Device ID | body | String | - | Server에 등록된 장치 이름, 예) "/dev/vdc" |
| Attachement ID | body | String | - | Attachment 식별자 |
| Volume ID | body | String | - | Block Strorage 식별자, 연결 해제 시 필요 |

#### Block Storage 연결 해제
Server에 연결되어 있는 추가적인 Block Strorage의 연결을 해제합니다.

##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/servers/{serverId}/attachments/{volumeId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | Header | String| Token ID |
| serverId | Path | String | Server 식별자 |
| volumeId | Path | String | Block Storage 식별자 |

##### Request body
이 Request는 Body를 필요로 하지 않습니다.

##### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

### Server Action API
다음과 같은 Server 제어 및 부가기능을 제공합니다.<br />
- Server 시작/정지/재시작<br />
- Server Flavor 변경(Resize)<br />
- Server Image 생성<br />
- Floating IP 연결/해제<br />
- Security Group 등록/해제<br />

#### 공통
모든 Server Action API는 동일한 Method, URL로 호출하며, Request Body로 각 Action을 구분합니다.
##### Method, URL
```
POST /v1.0/appkeys/{appkey}/servers/{serverId}/action
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | Header | String| Token ID |
| serverId | Path | String | Action을 수행할 Server의 식별자 |

#### Server 시작
정지(STOP) 상태의 서버를 시작합니다.
##### Request Body
```json
{
    "os-start" : null
}
```
      
##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

#### Server 정지
동작중(ACTIVE) 또는 오류(ERROR) 상태의 Server를 정지합니다.
##### Request Body
```json
{
    "os-stop" : null
}
```
     
##### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

#### Server 리부팅
Server를 리부팅합니다. 다음과 같은 리부팅 방식을 지정할 수 있습니다.<br />
 - SOFT - Graceful Shutdown 수행 후 Server를 재시작합니다.<br />
 - HARD - 강제 Shutdown 수행 후 Server를 재시작합니다.

##### Request Body

```json
{
    "reboot":{
        "type":"{Reboot Type}"
    }
}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| Reboot Type | body | String |  Reboot 타입. "HARD" or "SOFT" |
      
##### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

#### Server Resize
Server의 Flavor를 변경하여 Resize를 수행합니다.
##### Request Body
```json
{
    "resize":{
        "flavor":"{Flavor ID}"
    }
}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
|  Flavor ID | body | String |  변경할 Flavor 식별자 |
      
##### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

#### Image 생성
지정한 Server로 부터 Image를 생성합니다. 생성된 Image는 Image API를 통해 조회할 수 있습니다.
##### Request Body
```json
{
    "uploadImage":{
        "name": "{Image Name}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| ImageName | body | String | - | 생성할 Image 이름 |

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "createdImage": {
        "id" : "{Created Image ID}",
        "name" : "{Created Image Name}"
    }
}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| Created Image ID | body | String | 생성된 Image 식별자 |
| Created Image Name | body | String | 생성된 Image 이름 |

#### Floating IP 연결
외부 네트워크에서 접근 가능한 Floating IP를 Server에 연결합니다.

##### Request Body
```json
{
    "addFloatingIp" : {
        "address": "{Floating IP Address}",
        "ipAddress": "{IP Address of the server}"
    }
}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| Floating IP Address | body | String | Server에 연결할 Floating IP 주소 |
| IP Address of the server | body | String | Floating IP를 연결할 Server의 IP 주소 |

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

#### Floating IP 연결 해제
Server에 연결되어 있는 Floating IP의 연결을 해제합니다.

##### Request Body
```json
{
    "removeFloatingIp" : {
        "address": "{Floating IP Address}"
    }
}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| Floating IP Address | body | String | 연결을 해제할 Floating IP 주소 |

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

#### Security Group 등록
Server에 Security Group을 추가 등록합니다.

##### Request Body
```json
{
    "addSecurityGroup": {
        "name": "{Security Group Name}"
    }
}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| Security Group Name | body | String | 서버에 추가할 Security Group 이름 |

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

#### Security Group 해제
Server에 등록되어 있는 Security Group을 제거합니다.

##### Request Body
```json
{
    "removeSecurityGroup": {
        "name": "{Security Group Name}"
    }
}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| Security Group Name | body | String | 서버에서 제거할 Security Group 이름 |

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

### Flavor API
#### Flavor 목록 조회
Flavor의 목록 및 상세 정보를 조회합니다.

##### Method, URL
```
GET /v1.0/appkeys/{appkey}/flavors
X-Auth-Token: {tokenID}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | Header | String| Token ID |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
	"header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "flavors": [
        {
            "disabled": "{Disabled}",
            "ephemeral": "{Ephermeral}",
            "type": "{Type}",
            "maxVolumeSize": "{Max Volume Size}",
            "id": "{Flavor ID}",
            "name": "{Flavor Name}",
            "isPublic": "{Is Public}",
            "ram": "{RAM}",
            "vcpus": "{VCPUs}"
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Disabled | Body | Boolean | O | Flavor 비활성화 여부 |
| Ephermeral | Body | Integer | - | 임시 디스크 사이즈, GB |
| Type | Body | String | O | Flavor 최적화 특성에 따라 구분되는 Type값. "general, "compute", "memory" |
| Max Volume Size | Body | Integer | - | Root Disk로 만들 수 있는 최대 Disk 사이즈. GB |
| Flavor ID | Body | String | - | Flavor 식별자 |
| Flavor Name | Body | String | - | Flavor 이름 |
| Is Public | Body | Boolean | - | 모든 Project에서 사용 가능한 공용 Flavor 여부 |
| RAM | Body | Integer | - | Flavor가 갖는 RAM 총량. MB |
| VCPUs | Body | Integer | - | Server에 할당되는 가상 CPU 코어 개수 |

### Availability Zone API
#### Availability Zone 조회
Server를 생성할 수 있는 Zone의 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkey/{appkey}/availability-zones
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | Header | String | Token ID |

##### Request Body
이 API는 request body를 필요로 하지 않습니다.

##### Response Body
```json
{
	"header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "zones": [
        {
            "zoneName": "{Zone Name}",
            "zoneState": {
                "available": "{Available}"
            }
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Zone Name | Body | String | - | Availability Zone 이름 |
| Available | Body | Boolean | - | Availability Zone 가용 여부 |

## Image
### Image API
#### Image Status
Image는 다음의 Status 값을 갖습니다.

| Status | Description |
| -- | -- |
| queued | Image ID는 발급되었으나 아직 Image 데이터가 업로드 되지 못한 상태 |
| saving | Image 데이터를 저장 중인 상태 |
| active | Image 사용 가능 상태 |
| killed | Image 데이터 업로드 중 에러 발생 |
| deleted | Image에 대한 정보는 남아있으나 더 이상 가용하지 않은 상태 |
| pending_delete | deleted 상태와 유사, Image가 회복 불가능한 상태 |
| deactivated | Image 데이터가 사용 불가한 상태 |

#### Image 목록 조회
Image의 목록 및 상세 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkey/{appkey}/images
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | Header | String | Token ID |

##### Request Body
이 API는 request body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "images": [
        {
            "createdAt": "{Created At}",
            "diskFormat": "{Disk Format}",
            "id": "{Image ID}",
            "isPublic": "{Is Public}",
            "minDisk": "{Min Disk}",
            "minRam": "{Min RAM}",
            "name": "Image Name",
            "properties": {
            	"{Prop Key}" : "{Prop Value}"
            },
            "protected": "{Protected}",
            "size": "{Image Size}",
            "status": "{Image Status}",
            "updatedAt": "{Updated At}"
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Created At | Body | String  | - | Image 생성 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Disk Format | Body | String | - | Image의 Disk Format. <br \>"ami", "ari", "aki", "vhd", "vhdx", "vmdk", "raw", "qcow2", "vdi", "ploop", "iso" |
| Image ID | Body | String | - | Image 식별자 |
| Is Public | Body | Boolean | - | 모든 Project에서 사용 가능한 공용 Image 여부 |
| Min Disk | Body | Integer | - | Image 부팅에 필요한 최소 Disk 크기. GB |
| Min RAM | Body | Integer | - | Image 부팅에 필요한 최소 RAN 크기. MB |
| Image Name | Body | String | - | Image 이름 |
| Prop Key / Prop Value | Body | String | O | Image의 추가적인 속정 정보 |
| Protected | Body | Boolean | - | 삭제 보호 설정 여부 |
| Image Size | Body | Integer | - | Image 데이터의 크기. bytes |
| Image Status | Body | String | - | Image의 상태 |
| Updated At | Body | String | - | Image가 업데이트 된 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |

### Keypair API
Server 접근에 필요한 Keypair에 대한 생성, 삭제, 조회 기능을 제공합니다.
#### Keypair 목록 조회
계정에 속한 Keypair 목록을 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/keypairs
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - |Token ID |

##### Request Body
이 API는 request body를 필요로 하지 않습니다.

##### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "keypairs": [
        {
            "name": "{Keypair Name}",
            "publicKey": "{Public Key Value}",
            "fingerprint": "{Fingerprint Value}"
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Keypair Name | Body | String | - |Keypair 이름 |
| Public Key Value | Body | String | - | Keypair의 Public Key 값 |
| Fingerprint Value | Body | String | - |Fingerprint 값 |

#### Keypair 조회
지정한 Keypair의 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/keypairs/{keypairName}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| keypairName | Path | String | - | 조회할 Keypair 이름

##### Request Body
이 API는 request body를 필요로 하지 않습니다.

##### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "keypair": {
        "name": "{Keypair Name}",
        "publicKey": "{Public Key Value}",
        "fingerprint": "{Fingerprint Value}",
        "createdAt": "{Created At}"
    }
}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| Keypair Name | Body | String | Keypair 이름 |
| Public Key Value | Body | String | Keypair의 Public Key 값 |
| Fingerprint Value | Body | String | Fingerprint 값 |
| Created At | Body | DateTime | Keypair 생성 시간 |

#### Keypair 생성 or 업로드
Keypair를 생성하거나, ssh로 생성한 Keypair를 업로드 합니다.

##### Method, URL
```
POST /v1.0/appkeys/{appkey}/keypairs
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

##### Request Body

```json
{
    "keypair": {
        "name": "{Keypair Name}",
        "publicKey": "{Public Key Value}"
    }
}
```
###### Parameters
| Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| Keypair Name | Body | String | - | Keypair 이름 |
| Public Key Value | Body | String | O | 업로드할 Public ssh key. 생략 시 새로운 keypair가 만들어지며, 만들어진 Keypair의 Private Key가 Response로 함께 전달됩니다. |

##### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "keypair": {
        "name": "{Keypair Name}",
        "publicKey": "{Public Key Value}",
        "privateKey": "{Private Key Value}",
        "fingerprint": "{Fingerprint Value}"
    }
}
```
###### Parameters
| Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| Keypair Name | Body | String | - | Keypair 이름 |
| Public Key Value | Body | String | - | Keypair의 Public ssh key |
| Private Key Value | Body | String | O | Keypair의 Private ssh key. Keypair 업로드(Request에 "publicKey" 항목이 포함)인 경우 생략됩니다. |
| Public Key Value | Body | String | - | Fingerprint 값 |

#### Keypair 삭제
지정한 Keypair를 삭제합니다.
##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/keypairs/{keypairName}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| keypairName | Path | String | - | 삭제할 Keypair 이름 |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

## Block Storage
### Block Storage API
Block Stroage 생성/삭제 및 조회 기능을 제공합니다. Block Storage를 Server에 연결/해제하는 기능은 Server API를 통해 제공됩니다.

#### Block Storage Status
Block Storage는 다음과 같은 Status 값을 갖습니다.

| Status | Description |
| --- | --- |
| creating | 생성 중 |
| available | Server에 연결 가능한 상태 |
| attaching | Server에 연결 중 |
| detaching | Server에서 연결 해제 중 |
| in-use | Server에 연결되어 사용 중인 상태 |
| deleting | 삭제 중 |
| error | 생성 중 에러 발생 |
| error_deleting | 삭제 중 에러 발생 |
| backing-up | 백업 진행 중 |
| restoring-backup | 백업 복구 중 |
| error_backing-up | 백업 진행 중 에러 발생 |
| error_restoring | 백업 복구 중 에러 발생 |
| downloading | Image 다운로드 중 |
| uploading | Image로 업로드 중 |


#### Block Storage 목록 조회
Block Storage 목록 및 정보를 조회합니다.

##### Method, URL
```
GET /v1.0/appkeys/{appkey}/volumes
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | Header | String | Token ID |

##### Request Body
이 API는 request body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "volumes": [
        {
            "attachments": [
                {
                    "device": "{Device Name}",
                    "serverId": "{Attached Server ID}",
                    "attachmentId": "{Attachment ID}"
                }
            ],
            "availabilityZone": "{Availability Zone Name}",
            "createdAt": "Created At",
            "description": "{Description}",
            "id": "{Block Storage ID}",
            "metadata": {
                "Metadata Key": "{Metadata Value}"
            },
            "name": "{Block Storage Name}",
            "size": "{Size}",
            "status": "{Status}"
        }    
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Device Name | Body | String  | O | Server에 연결되어 있는 경우, Server에서의 장치명. ex) "/dev/vdb" |
| Attached Server ID | Body | String | O | Server에 연결되어 있는 경우, 연결된 Server의 ID |
| Attachment ID | Body | String | O | Server에 연결되어 있는 경우, 연결 식별자 |
| Availability Zone Name | Body | String | - | Block Storage가 위치한 Zone 이름 |
| Created At | Body | String | - | Block Storage 생성 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Description | Body | String | O | Block Storage 설명 |
| Block Storage ID | Body | String | - | Block Storage 식별자 |
| Metadata Key / Value | Body | Boolean | O | Block Storage에 기재된 Meta data |
| Block Storage Name | Body | String | - | Block Storage 이름 |
| Size | Body | Integer | - | Block Storage 크기. GB |
| Status | Body | String | - | Block Strage 상태 |

#### Block Storage 조회
특정 Block Storage의 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkey/{appkey}/volumes/{volumeId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | Header | String | Token ID |
| volumeId | Path | String | 조회할 Volume ID |

##### Request Body
이 API는 request body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "volume": {
        "attachments": [
            {
                "device": "{Device Name}",
                "serverId": "{Attached Server ID}",
                "attachmentId": "{Attachment ID}"
            }
        ],
        "availabilityZone": "{Availability Zone Name}",
        "createdAt": "Created At",
        "description": "{Description}",
        "id": "{Block Storage ID}",
        "metadata": {
            "Metadata Key": "{Metadata Value}"
        },
        "name": "{Block Storage Name}",
        "size": "{Size}",
        "status": "{Status}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Device Name | Body | String  | O | Server에 연결되어 있는 경우, Server에서의 장치명. ex) "/dev/vdb" |
| Attached Server ID | Body | String | O | Server에 연결되어 있는 경우, 연결된 Server의 ID |
| Attachment ID | Body | String | O | Server에 연결되어 있는 경우, 연결 식별자 |
| Availability Zone Name | Body | String | - | Block Storage가 위치한 Zone 이름 |
| Created At | Body | String | - | Block Storage 생성 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Description | Body | String | O | Block Storage 설명 |
| Block Storage ID | Body | String | - | Block Storage 식별자 |
| Metadata Key / Value | Body | Boolean | O | Block Storage에 기재된 Meta data |
| Block Storage Name | Body | String | - | Block Storage 이름 |
| Size | Body | Integer | - | Block Storage 크기. GB |
| Status | Body | String | - | Block Strage 상태 |

#### Block Storage 생성
새로운 Block Storage를 생성합니다.

##### Method, URL
```
POST /v1.0/appkey/{appkey}/volumes
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```
###### Parameters
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | Header | String | Token ID |

##### Request Body
```
{
    "volume": {
        "description": "{Description}",
        "availabilityZone":"{Availability Zone Name}",
        "snapshotId":"{Snapshot ID}",
        "size":"{Size}",
        "name":"{Block Storage Name}",
        "volumeType":"{Volume Type}",
        "metadata": {
        	"{Metadata Key}" : "{Metadata Value}"
        }
    }
}
```
###### Parameters
| Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| Description | Body | String | O | Block Storage 설명 |
| Availability Zone Name | Body | String | - | Block Storage를 생성할 Availability Zone 이름 |
| Snaptshot ID | Body | String | O | 스냅샷으로부터 Block Storage를 생성하고자 할 경우 사용하는 스냅샷 ID |
| Size | Body | Integer | - | Block Storage 크기. GB |
| Volume Type | Body | String | - | 생성할 Block Storage의 종류, 현재는 별도로 타입이 제공되지 않으므로 빈 문자열로 설정.  |
| Metadata Key / Metadata Value | Body | String | O | Block Storage에 기입하고자 하는 메타데이터 정보 |
| Block Storage Name | Body | String | - | Block Storage 이름 |

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "volume": {
        "attachments": [],
        "availabilityZone": "{Availability Zone Name}",
        "createdAt": "Created At",
        "description": "{Description}",
        "id": "{Block Storage ID}",
        "metadata": {
            "Metadata Key": "{Metadata Value}"
        },
        "name": "{Block Storage Name}",
        "size": "{Size}",
        "status": "{Status}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Availability Zone Name | Body | String | - | Block Storage가 위치한 Zone 이름 |
| Created At | Body | String | - | Block Storage 생성 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Description | Body | String | O | Block Storage 설명 |
| Block Storage ID | Body | String | - | Block Storage 식별자 |
| Metadata Key / Value | Body | Boolean | O | Block Storage에 기재된 Meta data |
| Block Storage Name | Body | String | - | Block Storage 이름 |
| Size | Body | Integer | - | Block Storage 크기. GB |
| Status | Body | String | - | Block Strage 상태 |

#### Block Storage 삭제
Block Storage를 삭제합니다. Status가 "available" "in-use" "error" "error_restoring" 인 Block Storage만 삭제할 수 있습니다.

##### Method, URL
```
DELETE /v1.0/appkey/{appkey}/volumes/{volumeId}
X-Auth-Token: {tokenId}
```
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | Header | String | Token ID |
| volumeId | Path | String | 삭제할 Volume ID |

##### Request Body
이 API는 request body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

## Security Group
### Security Group API
Security Group 생성, 삭제, 조회 및 업데이트 기능을 제공합니다.

#### Security Group 목록 조회
접근 가능한 Security Group들의 간략한 정보 목록을 조회합니다. "detail" Query Parameter를 통해 목록 내 Security Group들에 대한 상세한 정보를 조회할 수 있습니다.

##### Method, URL
```
GET /v1.0/appkeys/{appkey}/security-groups
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |
| detail | query | Boolean | O | 각 security-group의 상세 정보 표시, default는 false |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    },
    "securityGroups": [
        {
            "description": "{Desctiption}",
            "id": "{Security Group ID}",
            "name": "{Name}",
            "securityGroupRules": [
                {
                    "direction": "egress",
                    "ethertype": "IPv4",
                    "id": "3c0e45ff-adaf-4124-b083-bf390e5482ff",
                    "portRangeMax": null,
                    "portRangeMin": null,
                    "protocol": null,
                    "remoteGroupId": null,
                    "remoteIpPrefix": null,
                    "securityGroupId": "85cc3048-abc3-43cc-89b3-377341426ac5",
                    "description": ""
                }
            ]
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Description | Body | String | - | Security Group 설명 |
| Security Group ID | Body | String | - | Security Group 식별자 |
| Name | Body | String | - |Security Group 이름 |
| securityGroupRules | Body | List | O | Security Group Rule 목록, "detail=true" 일 때에만 표시.<br />Security Group Rule에 대한 자세한 사항은 Security Group Rules API 참조 |

#### Security Group 조회
지정한 Security Group의 간략한 정보를 조회합니다. "detail" Query Parameter를 통해 상세한 정보를 조회할 수 있습니다.

##### Method, URL
```
GET /v1.0/appkeys/{appkey}/security-groups/{securityGroupId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |
| securityGroupId | Path | String | - | 조회할 security-group 식별자 |
| detail | query | Boolean | O | 각 security-group의 상세 정보 표시, default는 false |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body

```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    },
    "securityGroups": {
        "description": "{Description}",
        "id": "{Security Group ID}",
        "name": "{Name}",
        "securityGroupRules": [
            {
                "direction": "egress",
                "ethertype": "IPv4",
                "id": "3c0e45ff-adaf-4124-b083-bf390e5482ff",
                "portRangeMax": null,
                "portRangeMin": null,
                "protocol": null,
                "remoteGroupId": null,
                "remoteIpPrefix": null,
                "securityGroupId": "85cc3048-abc3-43cc-89b3-377341426ac5",
                "description": ""
            }
        ]
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Description | Body | String | O | Security Group 설명 |
| Security Group ID | Body | String | - | Security Group 식별자 |
| Name | Body | String | - |Security Group 이름 |
| securityGroupRules | Body | List | O | Security Group Rule 목록, "detail=true" 일 때에만 표시.<br />Security Group Rule에 대한 자세한 사항은 Security Group Rules API 참조 |

#### Security Group 생성
새로운 Security Group을 생성합니다.

##### Method, URL
```
POST /v1.0/appkeys/{appkey}/security-groups
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |

##### Request Body
```json
{
    "securityGroup": {
        "name": "{Name}",
        "description": "{Description}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| name | Body | String | - |Security Group 이름 |
| description | Body | String | O | Security Group 설명 |

##### Response Body
```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    },
    "securityGroup": {
            "description": "{Description}",
            "id": "{Security Group ID}",
            "name": "{Name}",
            "securityGroupRules": [
                {
                    "direction": "egress",
                    "ethertype": "IPv4",
                    "id": "3c0e45ff-adaf-4124-b083-bf390e5482ff",
                    "portRangeMax": null,
                    "portRangeMin": null,
                    "protocol": null,
                    "remoteGroupId": null,
                    "remoteIpPrefix": null,
                    "securityGroupId": "85cc3048-abc3-43cc-89b3-377341426ac5",
                    "description": ""
                }
            ]
        }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Description | Body | String | O | Security Group 설명 |
| Security Group ID | Body | String | - | Security Group 식별자 |
| Name | Body | String | - |Security Group 이름 |
| securityGroupRules | Body | List | - | Security Group Rule 목록, Security Group Rules API 참조 |

#### Security Group 업데이트
Security Group의 이름, 설명을 변경합니다.

##### Method, URL
```
PUT /v1.0/appkeys/{appkey}/security-groups/{securityGroupId}
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |
| securityGroupId | Path | String | - | 변경할 Security Group의 식별자 |

##### Request Body
```json
{
    "securityGroup": {
        "name": "{Name}",
        "description": "{Description}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Name | Body | String | - | Security Group 이름 |
| Description | Body | String | O | Security Group 설명 |

##### Response Body
```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    },
    "securityGroup": {
        "id": "{Security Group ID}",
        "name": "{Name}",
        "description": "{Description}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Security Group ID | Body | String | - | Security Group 식별자 |
| Name | Body | String | - |Security Group 이름 |
| Description | Body | String | O | Security Group 설명 |

#### Security Group 삭제
지정한 Security Group을 삭제합니다.

##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/security-groups/{securityGroupId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |
| securityGroupId | Path | String | - | 삭제할 Security Group의 식별자 |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    }
}
```


### Security Group Rules API
Security Group Rule 추가/삭제 및 조회 기능을 제공합니다.

#### Security Group Rule 목록 조회
접근 가능한 모든 Security Group Rule 목록을 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/security-group-rules
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    },
    "securityGroupRules": [
        {
            "direction": "{Direction}",
            "ethertype": "{Ethernet Type}",
            "id": "{Rule ID}",
            "portRangeMax": "{Port Range MAX}",
            "portRangeMin": "{Port Range MIN}",
            "protocol": "{Protocol}",
            "remoteGroupId": "{Remote Group ID}",
            "remoteIpPrefix": "{Remote IP Prefix}",
            "securityGroupId": "{Security Group ID}"
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| Direction | Body | String | - | Rule이 적용되는 방향, "ingress" or "egress" |
| Ethernet Type | Body | String | O | "IPv4" or "IPv6" |
| Rule ID | Body | String | - | Security Group Rule 식별자 |
| Port Range MAX | Body | Integer | O | Rule이 적용되는 최대 Port 번호 |
| Port Range MIN | Body | Integer | O | Rule이 적용되는 최소 Port 번호 |
| Protocol | Body | String | O | IP Protocol. "icmp" "tcp" "udp" or "null" |
| Remote Group ID | Body | String | O | Rule이 적용되는 Remote Group의 식별자 |
| Remote IP Prefix | Body | String | O | Rule이 적용되는 Remote IP의 Prefix |
| Security Group ID | Body | String | O | Rule이 적용되는 Security Group의 식별자 |

#### Security Group Rule 조회
지정한 Security Group Rule의 정보를 조회합니다.

##### Method, URL
```
GET /v1.0/appkeys/{appkey}/security-group-rules/{securityGroupRuleId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |
| securityGroupRuleId | Path | String | - | 조회할 Security Group Rule 식별자 |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    },
    "securityGroupRules": {
        "direction": "{Direction}",
        "ethertype": "{Ethernet Type}",
        "id": "{Rule ID}",
        "portRangeMax": "{Port Range MAX}",
        "portRangeMin": "{Port Range MIN}",
        "protocol": "{Protocol}",
        "remoteGroupId": "{Remote Group ID}",
        "remoteIpPrefix": "{Remote IP Prefix}",
        "securityGroupId": "{Security Group ID}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| Direction | Body | String | - | Rule이 적용되는 방향, "ingress" or "egress" |
| Ethernet Type | Body | String | O | "IPv4" or "IPv6" |
| Rule ID | Body | String | - | Security Group Rule 식별자 |
| Port Range MAX | Body | Integer | O | Rule이 적용되는 최대 Port 번호 |
| Port Range MIN | Body | Integer | O | Rule이 적용되는 최소 Port 번호 |
| Protocol | Body | String | O | IP Protocol. "icmp" "tcp" "udp" or "null" |
| Remote Group ID | Body | String | O | Rule이 적용되는 Remote Security Group의 식별자 |
| Remote IP Prefix | Body | String | - | Rule이 적용되는 Remote IP의 Prefix |
| Security Group ID | Body | String | - | Rule이 적용되는 Security Group의 식별자 |

#### Security Group Rule 생성
새로운 Security Group Rule을 생성합니다.
##### Method, URL
```
POST /v1.0/appkeys/{appkey}/security-group-rules
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |

##### Request Body
```json
{
    "securityGroupRule": {
        "direction": "{Direction}",
        "ethertype": "{Ethernet Type}",
        "portRangeMin": "{Port Range MAX}",
        "portRangeMax": "{Port Range MIN}",
        "protocol": "{Protocol}",
        "remoteGroupId": "{Remote Group ID}",
        "remoteIpPrefix": "{Remote IP Prefix}",
        "securityGroupId": "{Security Group ID}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| Direction | Body | String | - | Rule이 적용되는 방향, "ingress" or "egress" |
| Ethernet Type | Body | String | O | "IPv4" or "IPv6" |
| Port Range MAX | Body | Integer | O | Rule이 적용되는 최대 Port 번호 |
| Port Range MIN | Body | Integer | O | Rule이 적용되는 최소 Port 번호 |
| Protocol | Body | String | O | IP Protocol. "icmp" "tcp" "udp" or "null" |
| Remote Group ID | Body | String | O | Rule이 적용되는 Remote Security Group의 식별자 |
| Remote IP Prefix | Body | String | - | Rule이 적용되는 Remote IP의 Prefix. |
| Security Group ID | Body | String | - | Rule이 적용되는 Security Group의 식별자 |

##### Response Body
```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    },
    "securityGroupRules": {
        "direction": "{Direction}",
        "ethertype": "{Ethernet Type}",
        "id": "{Rule ID}",
        "portRangeMax": "{Port Range MAX}",
        "portRangeMin": "{Port Range MIN}",
        "protocol": "{Protocol}",
        "remoteGroupId": "{Remote Group ID}",
        "remoteIpPrefix": "{Remote IP Prefix}",
        "securityGroupId": "{Security Group ID}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| Direction | Body | String | - | Rule이 적용되는 방향, "ingress" or "egress" |
| Ethernet Type | Body | String | O | "IPv4" or "IPv6" |
| Rule ID | Body | String | - | Security Group Rule 식별자 |
| Port Range MAX | Body | Integer | O | Rule이 적용되는 최대 Port 번호 |
| Port Range MIN | Body | Integer | O | Rule이 적용되는 최소 Port 번호 |
| Protocol | Body | String | O | IP Protocol. "icmp" "tcp" "udp" or "null" |
| Remote Group ID | Body | String | O | Rule이 적용되는 Remote Security Group의 식별자 |
| Remote IP Prefix | Body | String | - | Rule이 적용되는 Remote IP의 Prefix |
| Security Group ID | Body | String | - | Rule이 적용되는 Security Group의 식별자 |

#### Security Group Rule 삭제
지정한 Security Group Rule을 삭제합니다.
##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/security-group-rules/{securityGroupRuelsId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    }
}
```

## Network
### Network API
#### Network Status
Network는 다음 Status 값을 같습니다.

| Status | Description |
| -- | -- |
| BUILD | Network 구축 중 |
| ACTIVE | Network 활성화 상태 |
| DOWN | Network 비활성화 상태 |
| ERROR | 에러 발생 |

#### Network 목록 조회
접근 가능한 Network의 목록을 조회합니다.

##### Method, URL
```
GET /v1.0/appkey/{appkey}/networks
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional |Description |
| -- | -- | -- | -- | -- |
| tokenId | Header | String | - | Token ID |

##### Request Body
이 Request는 Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "networks": [
        {
            "adminStateUp": "{Administrative State}",
            "id": "{Network ID}",
            "name": "{Network Name}",
            "router:external": "{External Router Provided}",
            "status": "{Network Status}",
            "subnets": [
                "{Subnet ID}"
            ]
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Administrative State | Body | Boolean | - |네트워크 관리 상태. true: up, false: down |
| Network ID | Body | String | - | 네트워크 식별자 |
| Network Name | Body | String | - |네트워크 이름 |
| External Router Provided | Body | Boolean | - |Router를 통한 Floating IP 제공 가능 여부 |
| Network Status | Body | String | - |네트워크 상태. ACTIVE, DOWN, BUILD or ERROR |
| Subnet ID | Body | String | - | Subnet 식별자 |

#### Network 조회
지정한 Network의 정보를 조회합니다.

##### Method, URL
```
GET /v1.0/appkey/{appkey}/networks/{networkId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional |Description |
| -- | -- | -- | -- | -- |
| tokenId | Header | String | - | Token ID |
| networkId | Path | String | - | 조회할 Network 식별자 |

##### Request Body
이 API는 request body를 필요로 하지 않습니다.

##### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "network": {
        "adminStateUp": "{Administrative State}",
        "id": "{Network ID}",
        "name": "{Network Name}",
        "router:external": "{External Router Provided}",
        "status": "{Network Status}",
        "subnets": [
            "{Subnet ID}"
        ]
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Administrative State | Body | Boolean | - |네트워크 관리 상태. true: up, false: down |
| Network ID | Body | String | - | 네트워크 식별자 |
| Network Name | Body | String | - |네트워크 이름 |
| External Router Provided | Body | Boolean | - |Router를 통한 Floating IP 제공 가능 여부 |
| Network Status | Body | String | - |네트워크 상태. ACTIVE, DOWN, BUILD or ERROR |
| Subnet ID | Body | String | - | Subnet 식별자 |

## Subnet API
#### Subnet 목록 조회
접근 가능한 Subnet의 목록을 조회합니다.
##### Method, URL
```
GET /v1.0/appkey/{appkey}/subnets
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional |Description |
| -- | -- | -- | -- | -- |
| tokenId | Header | String | - | Token ID |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "subnets": [
        {
            "allocationPools": [
                {
                    "start": "{Start IP}",
                    "end": "{End IP}"
                }
            ],
            "cidr": "{CIDR}",
            "enableDhcp": "{Enable DHCP}",
            "gatewayIp": "{Gateway IP}",
            "hostRoutes": [],
            "id": "{Subnet ID}",
            "ipVersion": "{IP version}",
            "name": "{Subnet Name}",
            "networkId": "{Network ID}"
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Start IP | Body | String | - | 할당 Pool의 시작 IP. 예) 10.161.244.13 |
| End IP | Body | String | - | 할당 Pool의 마지막 IP. 예) 10.161.244.121 |
| CIDR | Body | String | - |Classless Inter-Domain Routing. 예) 10.161.244.0/25 |
| Enable DHCP | Body | Boolean | - | DHCP 활성화 여부 |
| Subnet ID | Body | String | - | Subnet 식별자 |
| IP Version | Body | Integer | - | Subnet의 IP version |
| Subnet Name | Body | Integer | - | Subnet 이름 |
| Network ID | Body | Integer | - | Subnet이 속한 네트워크 식별자 |

### Floating IP API
Floating IP 생성, 삭제, 정보 조회 기능을 제공합니다.

#### Floating IP Status
Floating IP는 다음 상태값을 갖습니다.

| Status | Description |
| -- | -- |
| ACTIVE | Floating IP가 Server와 연결되어 사용중인 상태 |
| DOWN | Floating IP가 연결되어 있지 않은 상태 |
| ERROR | 에러 발생 |

#### Floating IP 목록 조회
사용 가능한, 또는 사용 중인 Floating IP 목록을 조회합니다.
##### Method, URL
```
GET /v1.0/appkey/{appkey}/floatingips
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - |Token ID |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
	"header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "floatingips": [
        {
        	"id": "{Floating IP ID}",
            "floatingIpAddress": "{Floating IP Address}",
            "fixedIpAddress": "{Fixed IP Address}",
            "floatingNetworkId": "{Floating IP Network ID}",
            "portId": "{Port ID}",
            "routerId": "{Router ID}",
            "status": "{Status}"
        }
    ]
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Floating IP ID | Body | String | - | Floating IP 식별자 |
| Floating IP Address | Body | String | - | Floating IP 주소 |
| Fixed IP Address | Body | String | O | Floating IP가 연결된 Server NIC의 IP 주소. Status가 "ACTIVE" 인 경우에만 표시 |
| Floating Network ID | Body | String | - | Floating IP가 연결된 Network의 식별자 |
| Port ID | Body | String | O | Floting IP가 연결된 Port의 식별자. Status가 "ACTIVE" 인 경우에만 표시 |
| Router ID | Body | String | O | Floating IP의 Router 식별자. Status가 "ACTIVE" 인 경우에만 표시 |
| Status | Body | String | - | Floating IP의 상태 |

#### Floating IP 조회
지정한 Floating IP의 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkey/{appkey}/floatingips/{floatingIpId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| floatingIpId | Path | String | - | 조회할 Floating IP 식별자 |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
	"header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "floatingips": {
        "id": "{Floating IP ID}",
        "floatingIpAddress": "{Floating IP Address}",
        "fixedIpAddress": "{Fixed IP Address}",
        "floatingNetworkId": "{Floating IP Network ID}",
        "portId": "{Port ID}",
        "routerId": "{Router ID}",
        "status": "{Status}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Floating IP ID | Body | String | - | Floating IP 식별자 |
| Floating IP Address | Body | String | - | Floating IP 주소 |
| Fixed IP Address | Body | String | O | Floating IP가 연결된 Server NIC의 IP 주소. Status가 "ACTIVE" 인 경우에만 표시 |
| Floating Network ID | Body | String | - | Floating IP가 연결된 Network의 식별자 |
| Port ID | Body | String | O | Floting IP가 연결된 Port의 식별자. Status가 "ACTIVE" 인 경우에만 표시 |
| Router ID | Body | String | O | Floating IP의 Router 식별자. Status가 "ACTIVE" 인 경우에만 표시 |
| Status | Body | String | - | Floating IP의 상태 |

#### Floating IP 생성
Floating IP를 생성합니다.
##### Method, URL
```
POST /v1.0/appkey/{appkey}/floatingips
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
	"header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "floatingip": {
    	"id": "{Floating IP ID}",
        "floatingIpAddress": "{Floating IP Address",
        "floatingNetworkId": "{Floating IP Network ID}",
        "status": "{Status}"
    }
}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Floating IP ID | Body | String | - | Floating IP 식별자 |
| Floating IP Address | Body | String | - | Floating IP 주소 |
| Floating Network ID | Body | String | - | Floating IP가 연결된 Network의 식별자 |
| Status | Body | String | - | Floating IP의 상태 |

#### Floating IP 삭제
지정한 Floating IP를 삭제합니다.
##### Method, URL
```
DELETE /v1.0/appkey/{appkey}/floatingips/{floatingIpId}
X-Auth-Token: {tokenId}
```
###### Parameters
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| floatingIpId | Path | String | - | 조회할 Floating IP 식별자 |

##### Request Body
이 API는 request body를 필요로 하지 않습니다.

##### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```
