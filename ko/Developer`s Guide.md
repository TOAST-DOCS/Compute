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
| Name | In | Type | Description |
| -- | -- | -- | -- |
| appkey | Path Variable | String | 상품 이용시 발급받은 앱키 |

### Response
#### Response HTTP Status Code
모든 API 요청에 대해 200 OK로 응답하며, JSON 형태의 Response Body를 포함합니다.

#### Response Body
Response Body에는 "header" 정보가 기본으로 포함되어 있으며, 이를 통해 자세한 응답 결과를 확인할 수 있습니다.
API에 따라 "header" 외 추가적인 정보가 포함될 수 있습니다.

```jso
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

## Token API
**Token** 은 Compute & Network의 RESTful API 사용을 위해 발급받아야 하는 인증키이며, 이후 모든 API 요청 시 Request에 ```X-Auth-Token``` Header로 입력하여 요청해야 합니다.

### Token 발급
#### Method, URL
```
POST /v1.0/appkeys/{appkey}/tokens
Content-Type: application/json;charset=UTF-8
```


#### Request Body
```json
{
	"auth" : {
    	"username" : "User Name",
        "password" : "API Password"
    }
}
```
| Name | In | Type | Optional | Description |
| -- | -- | -- | -- | -- |
| username | Body | String | - | TOAST Cloud 사용자 계정 ID |
| password | Body | String | - | API 패스워드 |

#### Response Body
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
| Name | In | Type | Optional | Description |
| -- | -- | -- | -- | -- |
| Token ID | Body | String | - | API 요청 시 HTTP 헤더(X-Auth-Token) 에 기재해야 하는 UUID |
| Issued at | Body | String | - | 토큰 발급 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Expires | Body | String | - | 발급한 Token의 만료 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T03:17:50Z |
| User ID | Body | String | - | 토큰을 발급받은 사용자의 UUID | 
| Role name | Body | String | - | 토큰을 발급받은 사용자에게 부여된 Role |

### Token 정보 조회
#### Method, URL
```
GET /v1.0/appkey/{appkey}/tokens/{tokenId}
```
|  Name | In | Type | Optional |Description |
|--|--|--|--|--|
| tokenId | header | string | - | Token ID |

#### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

### Response Body
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

| Name | In | Type | Optional | Description |
| -- | -- | -- | -- | -- |
| Token ID | Body | String | - | API 요청 시 HTTP 헤더(X-Auth-Token) 에 기재해야 하는 UUID |
| Issued at | Body | String | - | 토큰 발급 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Expires | Body | String | - | 발급한 Token의 만료 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T03:17:50Z |
| User ID | Body | String | - | 토큰을 발급받은 사용자의 UUID | 
| Role name | Body | String | - | 토큰을 발급받은 사용자에게 부여된 Role |


## Server API
Server 생성, 삭제, 정보 조회 및 Block Storage 연결관리 기능을 제공합니다.

### Server Status
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

### Server 목록 간략 조회
생성되어 있는 Server들의 간략한 정보(ID, Name, Status)를 조회합니다.
#### Method, URL
```
GET /v1.0/appkeys/{appkey}/servers
X-Auth-Token: {tokenId}
```
|  Name | In | Type | Optional |Description |
|--|--|--|--|--|
| tokenId | header | string | - | Token ID |

#### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

#### Response Body
```json
{
    "servers": [
        {
            "id": "{Server ID}",
            "name": "{Server Name}",
            "status": "{Server Status}"
        }
    ]
}
```

|  Name | In | Type | Description |
|--|--|--|--|
| Server ID | Body | String | Server 식별자 |
| Server Name | Body | String | Server 이름 (Linux의 경우 최대 255자, Windows의 경우 최대 12자) |
| Server Status | Body | String | Server의 상태 |

### Server 목록 상세 조회
생성되어 있는 모든 Server들의 상세한 정보를 조회합니다.
#### Method, URL
```
GET /v1.0/appkeys/{appkey}/servers/detail
X-Auth-Token: {tokenId}
```
|  Name | In | Type | Optional |Description |
|--|--|--|--|--|
| tokenId | header | string | - | Token ID |

#### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

#### Response Body
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
| Root Volume Size | Body | Integer | - | Root Disk 크기, GB 단위 |
| Attached Volume ID | Body | String | O | 추가 Block Storage 식별자 |
| Attached Volume Name | Body | String | O | 추가 Block Storage 이름 |
| Attached Volume Size | Body | Integer | O | 추가 Block Storage 크기, GB 단위 |
| Security Group Name | Body | String | - | Server에 등록된 Security Group의 이름 |
| Launched Time | Body | Datetime | - | Server 최근 부팅 시각 |
| Created Time | Body | Datetime | - | Server 생성 시각 |
| Updated Time | Body | Datetime | - | Server 수정 시각 |

### Server 단건 조회
특정 Server의 상세 정보를 조회합니다.

#### Method, URL
```
GET /v1.0/appkeys/{appkey}/servers/{serverId}
X-Auth-Token: {tokenId}
```
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | header | String | - | Token ID |
| serverId | path | String | - | 정보를 조회 할 Server의 식별자 |

#### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

#### Response Body
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
| Launched Time | Body | Datetime | - | Server 최근 부팅 시각 |
| Created Time | Body | Datetime | - | Server 생성 시각 |
| Updated Time | Body | Datetime | - | Server 수정 시각 |

### Server 생성
새로운 Server를 생성합니다.

#### Method, URL
```
PUT /v1.0/appkeys/{appkey}/servers
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | header | String | - | Token ID |

#### Request Body
```json
{
    "server": {
        "name": "{Server Name}",
        "image": "{Image ID}",
        "flavor": "{Flavor ID}",
        "networks": [{
            "id": "{Network ID}"
        }],
        "availabilityZone": "{Availability Zone}",
        "keyName": "{Key Name}",
        "count": "{Count}",
        "volumes": [{
            "size": "{Volume Size}"
        }],
        "securityGroups": [
        	{
            	"name": "{Security Group Name}"
        	}
		]
    }
}
```
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Server Name | Body | String | - | Server 이름 (Linux의 경우 최대 255자, Windows의 경우 최대 12자) |
| Image ID | Body | String | - | Server에 설치할 Image 식별자 |
| Flavor ID | Body | String | - | Server의 Flavor 식별자 |
| Network ID | Body | String | - | Server가 연결될 Network 식별자 |
| Availability Zone | Body | String | - | Server가 생성될 Availability Zone |
| Key Name | Body | String | - | Server에 등록할 Key-pair 이름 |
| Count | Body | Integer | - | 동시 생성할 Server의 댓수, 최대 10대로 제한 |
| Volume Size | Body | Integer | - | Server의 Root Disk 크기, 허용가능한 Volume size는 Flavor에 따라 정해짐 |
| Security Group Name | Body | String | - | Server에 등록할 Security Group 이름 |

#### Response Body
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
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|--|
| Server ID | body | String | - |생성된 Server 식별자 |
| Server Name | body | String | - |Server 이름 (Linux의 경우 최대 255자, Windows의 경우 최대 12자) |
| Server Status | Body | String | - |Server의 상태 |

### Server 삭제
특정 Server를 삭제합니다.
#### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/servers/{serverId}
X-Auth-Token: {tokenId}
```
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | header | String | Token ID |
| serverId | path | String | 삭제할 Server의 고유 ID |

### Block Storage 연결
Server에 추가적인 Block Strorage를 연결합니다.

#### Method, URL
```
POST infrastructure/v1.0/appkeys/{appkey}/servers/{serverId}/attachments
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | header | String | - | Token ID |
| serverId | path | String | - | Block Strorage를 연결 할 Server의 고유 ID |

### Request Body
```json
{
    "attachment":{
        "volumeId":"{Volume ID}"
    }
}
```
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Volume ID | body | String | - | Server에 연결할 Block Strorage 식별자 |

### Response Body

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

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Device ID | body | String | - | Server에 등록된 장치 이름, 예) ```/dev/vdc``` |
| Attachement ID | body | String | - | Attachment 식별자 |
| Volume ID | body | String | - | Block Strorage 식별자, 연결 해제 시 필요 |

### Block Storage 연결 해제
Server에 연결되어 있는 추가적인 Block Strorage의 연결을 해제합니다.

#### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/servers/{serverId}/attachments/{volumeId}
X-Auth-Token: {tokenId}
```
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | header | String| Token ID |
| serverId | path | String | Server 식별자 |
| volumeId | path | String | Block Storage 식별자 |

#### Request body
이 Request는 Body를 필요로 하지 않습니다.

#### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

## Server Action API
다음과 같은 Server 제어 및 부가기능을 제공합니다.
* Server 시작/정지/재시작
* Server Flavor 변경(Resize)
* Server Image 생성
* Floating IP 연결/해제
* Security Group 등록/해제

### 공통
모든 Server Action API는 동일한 URL로 호출하며, Request Body에 기재하는 Action 내용으로 구분합니다.
#### Method, URL
```
POST /v1.0/appkeys/{appkey}/servers/{serverId}/action
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```
|  Name | In | Type | Description |
|--|--|--|--|
| tokenId | header | String| Token ID |
| serverId | path | String | Action을 수행할 Server의 식별자 |

### Server 시작
정지(STOP) 상태의 서버를 시작합니다.
#### Request Body
```json
{
    "os-start" : null
}
```
      
#### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

### Server 정지
동작중(ACTIVE) 또는 오류(ERROR) 상태의 Server를 정지합니다.
#### Request Body
```json
{
    "os-stop" : null
}
```
     
#### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

### Server 리부팅
Server를 리부팅합니다. 다음과 같은 리부팅 방식을 지정할 수 있습니다.
* SOFT - Graceful Shutdown 수행 후 Server를 재시작합니다.
* HARD - 강제 Shutdown 수행 후 Server를 재시작합니다.

#### Request Body

```json
{
    "reboot":{
        "type":"{Reboot Type}"
    }
}
```
|  Name | In | Type | Description |
|--|--|--|--|
| Reboot Type | body | String |  Reboot 타입. "HARD" or "SOFT" |
      
#### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

### Server Resize
Server의 Flavor를 변경하여 Resize를 수행합니다.
#### Request Body
```json
{
    "resize":{
        "flavor":"{Flavor ID}"
    }
}
```
|  Name | In | Type | Description |
|--|--|--|--|
|  Flavor ID | body | String |  변경할 Flavor 식별자 |
      
### Response Body

```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

### Image 생성
지정한 Server로 부터 Image를 생성합니다. 생성된 Image는 Image API를 통해 조회할 수 있습니다.
#### Request Body
```json
{
    "uploadImage":{
        "name": "{Image Name}"
    }
}
```
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| ImageName | body | String | - | 생성할 Image 이름 |

#### Response Body
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

|  Name | In | Type | Description |
|--|--|--|--|
| Created Image ID | body | String | 생성된 Image 식별자 |
| Created Image Name | body | String | 생성된 Image 이름 |

### Floating IP 연결
외부 네트워크에서 접근 가능한 Floating IP를 Server에 연결합니다.

#### Request Body
```json
{
    "addFloatingIp" : {
        "address": "{Floating IP Address}",
        "ipAddress": "{IP Address of the server}"
    }
}
```
|  Name | In | Type | Description |
|--|--|--|--|
| Floating IP Address | body | String | Server에 연결할 Floating IP 주소 |
| IP Address of the server | body | String | Floating IP를 연결할 Server의 IP 주소 |

### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

### Floating IP 연결 해제
Server에 연결되어 있는 Floating IP의 연결을 해제합니다.

#### Request Body
```json
{
    "removeFloatingIp" : {
        "address": "{Floating IP Address}"
    }
}
```
|  Name | In | Type | Description |
|--|--|--|--|
| Floating IP Address | body | String | 연결을 해제할 Floating IP 주소 |

#### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

### Security Group 등록
Server에 Security Group을 추가 등록합니다.

#### Request Body
```json
{
    "addSecurityGroup": {
        "name": "{Security Group Name}"
    }
}
```
|  Name | In | Type | Description |
|--|--|--|--|
| Security Group Name | body | String | 서버에 추가할 Security Group 이름 |

#### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```

### Security Group 해제
Server에 등록되어 있는 Security Group을 제거합니다.

### Request Body
```json
{
    "removeSecurityGroup": {
        "name": "{Security Group Name}"
    }
}
```
|  Name | In | Type | Description |
|--|--|--|--|
| Security Group Name | body | String | 서버에서 제거할 Security Group 이름 |

### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    }
}
```