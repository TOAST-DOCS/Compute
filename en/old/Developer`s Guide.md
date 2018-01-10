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
### API Endpoint URL
```
https://api-compute.cloud.toast.com/compute/v1.0/appkeys/{appkey}
```

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
| isSuccessful | resultCode | resultMessage | Description |
| --- | --- | --- | --- |
| true | 0 | SUCCESS | 처리 성공. API에 따라 "header" 외 추가 정보 포함 |
| false  | -1 | FAIL [: detail description] | 인증 모듈 연동 실패 또는 요청을 수행할 수 없는 상태인 경우. detail description 내용에 따라 조치 후 재시도 가능 |
| false | -2 | UNKNOWN EXCEPTION | 예기치 못한 오류 발생. TOAST Cloud 담당자 문의 필요 |
| false | -3 | Permission denied [: detail description] | 권한이 없는 사용자, AppKey, 또는 Token ID에 의한 요청. detail description 내용 참조 |
| false | -4 | Invalid parameters [: detail description] | API 호출 시 Request URL 또는 Body에 필요한 값이 없거나, 잘못된 형식의 값이 입력된 경우. detail description 내용에 따라 조치 후 재시도 가능 |
| false | -5 | Nonexistent [: detail description] | 존재하지 않는 Resource에 접근한 경우. detail description 내용 참조 |
| false | -6 | Failed to query internal db [: detail description] | Database Query에 실패한 경우. TOAST Cloud 담당자 문의 필요 |
| false | -7 | Not supported [: detail description] | 지원하지 않는 기능 요청. detail description 내용 참조 |
| false | -8 | JSON parsing error [: detail description] | Request Body의 JSON 파싱 실패. Request Body 확인 필요 |
| false | 10400~10499| Instance API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 11400~11499| Flavor API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 12400~12499| Availability Zone API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 13400~13499| Keypair API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 20001 | No available IP | 할당 가능한 IP가 없음. TOAST Cloud 담당자 문의 필요 |
| false | 20004 | No accessible network | Network 조회 실패. 잘못된 Network ID로 조회, 또는 접근 가능한 Network가 없음. |
| false | 20400~20499| Network API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 21400~21499| Subnet API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 22400~22499| Floating IP API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 23400~23499| Load Balancer API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 24400~24499| Security Group API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 30400~30499| Image API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 40400~40499| Block Storage API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |
| false | 50400~50499| Token API 관련 에러 메시지 | resultCode의 뒤 세자리는 HTTP Status Code이며, resultMessage 내용에 따라 조치 후 재시도 가능 |

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
    	"username" : "{User Name}",
        "password" : "{API Password}"
    }
}
```

| Name | In | Type | Optional | Description |
| -- | -- | -- | -- | -- |
| User Name | Body | String | - | TOAST Cloud 사용자 계정 ID |
| API Password | Body | String | - | [API 패스워드](#api-password) |

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

| Name | In | Type | Description |
| -- | -- | -- | -- |
| Token ID | Body | String | API 요청 시 HTTP 헤더(X-Auth-Token) 에 기재해야 하는 UUID |
| Issued at | Body | String | 토큰 발급 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Expires | Body | String | 발급한 Token의 만료 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T03:17:50Z |
| User ID | Body | String | 토큰을 발급받은 사용자의 UUID |
| Role name | Body | String | 토큰을 발급받은 사용자에게 부여된 Role |

#### Token 정보 조회
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/tokens?id={tokenId}
```

|  Name | In | Type | Optional |Description |
|--|--|--|--|--|
| tokenId | Query | String | - | 조회할 Token ID |

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

| Name | In | Type | Description |
| -- | -- | -- | -- |
| Token ID | Body | String | API 요청 시 HTTP 헤더(X-Auth-Token) 에 기재해야 하는 UUID |
| Issued at | Body | String | 토큰 발급 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Expires | Body | String | 발급한 Token의 만료 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T03:17:50Z |
| User ID | Body | String | 토큰을 발급받은 사용자의 UUID | 
| Role name | Body | String | 토큰을 발급받은 사용자에게 부여된 Role |

## Availability Zone
### Availability Zone API
#### Availability Zone 조회
Instance, Block Storage를 생성할 수 있는 Zone의 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/availability-zones
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

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

|  Name | In | Type | Description |
|--|--|--|--|
| Zone Name | Body | String | Availability Zone 이름 |
| Available | Body | Boolean | Availability Zone 가용 여부 |

## Instance
### Instance API
Instance 생성, 삭제, 정보 조회 및 Block Storage 연결관리 기능을 제공합니다.

#### Instance Status
Instance는 생성, 변경, 삭제, 운영 중 다음과 같은 Status를 갖습니다.
![[그림 1] Instance Status Diagram](http://static.toastoven.net/prod_infrastructure/compute/developersguide/img_001.png)
<center>[그림 1] Instance Status Diagram</center>

| Status | Description |
| --- | --- |
| BUILD | Instance 생성 중 |
| POWERING_ON | Instance 부팅 중 |
| ACTIVE | Instance 구동 중 |
| POWERING_OFF | Instance 종료 중 |
| STOP | Instance 종료 상태 |
| REBOOTING | Instance Rebooting 중 |
| RESIZING | Instance Resize 작업 중 |
| MIGRATING | Instance Migration 작업 중 |
| DELETING | Instance 삭제 중 |
| ERROR | 오류 상태 |

#### Instance 정보 간략 조회
생성되어 있는 Instance의 간략한 정보(ID, Name, Status)를 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/instances?id={instanceId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional |Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| instanceId | Query | String | O | 조회할 Instance 식별자. 기재하지 않을 경우 모든 Instance들의 간략 정보를 조회합니다. |

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
    "instances": [
        {
            "id": "{Instance ID}",
            "name": "{Instance Name}",
            "status": "{Instance Status}"
        }
    ]
}
```

|  Name | In | Type | Description |
|--|--|--|--|
| Instance ID | Body | String | Instance 식별자 |
| Instance Name | Body | String | Instance 이름 |
| Instance Status | Body | String | Instance의 상태 |

#### Instance 상세 조회
Instance의 상세한 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/instances-detail?id={instanceId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional |Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| instanceId | Query | String | O | 조회할 Instance의 식별자. 생략 시 모든 Instance들의 상세 정보를 조회합니다. |

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
    "instances": [
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
            "id": "{Instance ID}",
            "name": "{Instance Name}",
            "image": "{Image ID}",
            "metadata": {
                "{key}": "{value}"
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

|  Name | In | Type | Description |
|--|--|--|--|
| MAC Address | Body | String | NIC의 MAC address |
| IP Address | Body | String | NIC의 IP Address |
| version | Body | Integer | IP Version. TOAST Cloud에서는 IP v4만 지원 |
| Floating IP Address | Body | String | NIC에 할당된 Floatin IP Address |
| Zone Name | Body | String | Availability Zone |
| Flavor ID | Body | String | Flavor 식별자 |
| Flavor Name | Body | String | Flavor name |
| Flavor CPU | Body | Integer | CPU 개수 |
| Flavor RAM | Body | Integer | RAM 크기, MB 단위 |
| Status | Body | String | Instance의 상태 |
| Instance ID | Body | String | Instance 식별자 |
| Instance Name | Body | String | Instance 이름 |
| Image ID | Body | String | Instance에 설치된 Image ID |
| metadata | Body | Object | Instance에 설정할 사용자 metadata, "key": "value" 형태로 저장 |
| PEM Key Name | Body | String | Instance에 등록할 Key-pair 이름 |
| Root Volume Size | Body | Integer | Root Disk 크기, GB 단위 |
| Attached Volume ID | Body | String | 추가 Block Storage 식별자 |
| Attached Volume Name | Body | String | 추가 Block Storage 이름 |
| Attached Volume Size | Body | Integer | 추가 Block Storage 크기, GB 단위 |
| Security Group Name | Body | String | Instance에 등록된 Security Group의 이름 |
| Launched Time | Body | String | Instance 최근 부팅 시각. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Created Time | Body | String | Instance 생성 시각. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Updated Time | Body | String | Instance 수정 시각. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |

#### Instance 생성
새로운 Instance를 생성합니다.

##### Method, URL
```
POST /v1.0/appkeys/{appkey}/instances
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

##### Request Body
```json
{
    "instance": {
        "name": "{Instance Name}",
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
        "volume": {
            "size": "{Volume Size}"
        },
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
| Instance Name | Body | String | - | Instance 이름 (Linux의 경우 최대 20자, Windows의 경우 최대 12자, 영문자와 숫자, '-', '.' 만 가능) |
| Image ID | Body | String | - | Instance에 설치할 Image 식별자. [Image API](#image-api) 참조 |
| Flavor ID | Body | String | - | Instance의 Flavor 식별자. [Flavor API](#flavor-api) 참조|
| Network ID | Body | String | - | Instance가 연결될 Network 식별자. [Network API](#network-api) 참조|
| Availability Zone | Body | String | - | Instance가 생성될 Availability Zone 이름. [Availability Zone API](#availability-zone-api) 참조 |
| Key Name | Body | String | - | Instance에 등록할 Key-pair 이름. [Keypair API](#keypair-api) 참조|
| Count | Body | Integer | O | 동시 생성할 Instance의 대수, 1 ~ 10 범위. 생략 시 1대 생성 |
| Volume Size | Body | Integer | O | Instance의 Root Disk 크기, [Instance Volume Size](#Instance Volume Size) 참조 |
| Security Group Name | Body | String | - | Instance에 등록할 Security Group 이름 |

###### Instance Volume Size
* **"volumeSize" 파라미터 값을 갖는 Flavor(u2.\* / i2.\*) 로 Instance 생성 시**
	* "instance.volume.size" 파라미터를 생략해야 합니다.
	* Flavor에 설정된 고정 Volume Size 크기의 Root Disk가 생성됩니다.

* **"volumeSize" 파라미터 값을 갖지 않는 Flavor로 Instance 생성 시**
	* "instance.volume.size" 파라미터가 반드시 기재되어야 합니다.
	* **사용할 Image의 "minDisk" 값 ~ 1000의 범위 내에서 10 단위**로 설정되어야 하며, 설정된 크기의 Root Disk가 생성됩니다.

##### Response Body
```json
{
    "header": {
        "isSuccessful": true,
        "resultCode": 0,
        "resultMessage": "SUCCESS"
    },
    "instance": {
        "id": "{Instance ID}",
        "name": "{Instance Name}",
        "status": "{Instance Status}"
    }
}
```

| Name | In | Type | Description |
|--|--|--|--|
| Instance ID | body | String |생성된 Instance 식별자 |
| Instance Name | body | String | Instance 이름 |
| Instance Status | Body | String | Instance의 상태 |

#### Instance 삭제
특정 Instance를 삭제합니다.
##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/instances?id={instanceId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| instanceId | Query | String | - | 삭제할 Instance 식별자 |

#### Block Storage 연결
Instance에 추가적인 [Block Strorage](#block-storage-api)를 연결합니다.

##### Method, URL
```
POST /v1.0/appkeys/{appkey}/instances/{instanceId}/attachments
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| instanceId | Path | String | - | Block Strorage를 연결 할 Instance의 식별자 |

##### Request Body
```json
{
    "attachment":{
        "volumeId":"{Volume ID}"
    }
}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Volume ID | body | String | - | Instance에 연결할 [Block Strorage](#block-storage-api) 식별자. |

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

|  Name | In | Type | Description |
|--|--|--|--|
| Device ID | body | String | Instance에 등록된 장치 이름, 예) "/dev/vdc" |
| Attachement ID | body | String | Attachment 식별자 |
| Volume ID | body | String | Block Strorage 식별자, 연결 해제 시 필요 |

#### Block Storage 연결 해제
Instance에 연결되어 있는 추가적인 Block Strorage의 연결을 해제합니다.

##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/instances/{instanceId}/attachments?volumeId={volumeId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String| - | Token ID |
| instanceId | Path | String | - | Instance 식별자 |
| volumeId | Path | String | - | Block Storage 식별자 |

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

### Instance Action API
다음과 같은 Instance 제어 및 부가기능을 제공합니다.<br />
- Instance 시작/정지/재시작<br />
- Instance Flavor 변경(Resize)<br />
- Instance Image 생성<br />
- Floating IP 연결/해제<br />
- Security Group 등록/해제<br />

#### 공통
모든 Instance Action API는 동일한 Method, URL로 호출하며, Request Body로 각 Action을 구분합니다.
##### Method, URL
```
POST /v1.0/appkeys/{appkey}/instances/{instanceId}/action
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String| - | Token ID |
| instanceId | Path | String | - | Action을 수행할 Instance의 식별자 |

##### Request Body Template
```json
{
	"action": "{Action Name}",
    "parameters" : {
    	"{key}": "{value}"
    }
}
```
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Action Name | Body | String | - | Instance에서 실행할 Action명 |
| parameters | Body | Object| O | Action 수행에 필요한 Parameter. Action에 따라 필요한 값을 기재하거나 없을 수 있습니다. |

#### Instance 시작
정지(STOP) 상태의 Instance를 시작합니다.
##### Request Body
```json
{
    "action" : "start"
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

#### Instance 정지
동작중(ACTIVE) 또는 오류(ERROR) 상태의 Instance를 정지합니다.
##### Request Body
```json
{
    "action" : "stop"
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

#### Instance 리부팅
Instance를 리부팅합니다. 다음과 같은 리부팅 방식을 지정할 수 있습니다.<br />
 - SOFT - Graceful Shutdown 수행 후 Instance를 재시작합니다.<br />
 - HARD - 강제 Shutdown 수행 후 Instance를 재시작합니다.

##### Request Body

```json
{
	"action" : "reboot",
    "parameters":{
        "type":"{Reboot Type}"
    }
}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Reboot Type | body | String | - | Reboot 타입. "HARD" or "SOFT" |

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

#### Instance Resize
Instance의 Flavor를 변경하여 Resize를 수행합니다.
##### Request Body
```json
{
	"action": "resize",
    "parameters":{
        "flavor":"{Flavor ID}"
    }
}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
|  Flavor ID | body | String | - | 변경할 Flavor 식별자. [Flavor API](#flavor-api) 참조 |

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
지정한 Instance로 부터 Image를 생성합니다. 생성된 Image는 [Image API](#image-api)를 통해 조회할 수 있습니다.
Image 생성 대상이 되는 Instance는 STOP 상태여야 합니다.
##### Request Body
```json
{
    "action" : "uploadImage",
    "parameters" : {
        "name": "{Image Name}"
    }
}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Image Name | body | String | - | 생성할 Image 이름 |

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

|  Name | In | Type | Description |
|--|--|--|--|
| Created Image ID | body | String | 생성된 Image 식별자 |
| Created Image Name | body | String | 생성된 Image 이름 |

#### Floating IP 연결
외부 네트워크에서 접근 가능한 [Floating IP](#floating-ip-api)를 Instance에 연결합니다.

##### Request Body
```json
{
    "action": "addFloatingIp",
    "parameters": {
        "address": "{Floating IP Address}",
        "ipAddress": "{IP Address of the instance}"
    }
}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Floating IP Address | body | String | - | Instance에 연결할 Floating IP 주소 |
| IP Address of the instance | body | String | - | Floating IP를 연결할 Instance의 IP 주소 |

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
Instance에 연결되어 있는 [Floating IP](#floating-ip-api)의 연결을 해제합니다.

##### Request Body

```json
{
	"action": "removeFloatingIp",
    "parameters" : {
        "address": "{Floating IP Address}"
    }
}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Floating IP Address | body | String | - | 연결을 해제할 Floating IP 주소 |

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
Instance에 [Security Group](#security-group)을 추가 등록합니다.

##### Request Body
```json
{
	"action": "addSecurityGroup",
    "parameters": {
        "name": "{Security Group Name}"
    }
}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Security Group Name | body | String | - | Instance에 추가할 [Security Group](#security-group-api) 이름 |

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
Instance에 등록되어 있는 [Security Group](#security-group)을 제거합니다.

##### Request Body
```json
{
	"action": "removeSecurityGroup",
    "parameters": {
        "name": "{Security Group Name}"
    }
}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| Security Group Name | body | String | - | Instance에서 제거할 [Security Group](#security-group-api) 이름 |

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

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String| - | Token ID |

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
            "volumeSize": "{Volume Size}",
            "id": "{Flavor ID}",
            "name": "{Flavor Name}",
            "isPublic": "{Is Public}",
            "ram": "{RAM}",
            "vcpus": "{VCPUs}"
        }
    ]
}
```

|  Name | In | Type | Description |
|--|--|--|--|
| Disabled | Body | Boolean | Flavor 비활성화 여부 |
| Ephermeral | Body | Integer | 임시 디스크 사이즈, GB |
| Type | Body | String | Flavor 최적화 특성에 따라 구분되는 Type값. "general, "compute", "memory" |
| Volume Size | Body | Integer | Instance 생성 시 만들어지는 Root Disk 사이즈(GB). <br \>Root Disk가 고정된 크기로 만들어지는 Flavor(u2.\* / i2.\*)의 경우에만 해당 Parameter가 전달됩니다. |
| Flavor ID | Body | String | Flavor 식별자 |
| Flavor Name | Body | String | Flavor 이름 |
| Is Public | Body | Boolean | 모든 Project에서 사용 가능한 공용 Flavor 여부 |
| RAM | Body | Integer | Flavor가 갖는 RAM 총량. MB |
| VCPUs | Body | Integer | Instance에 할당되는 가상 CPU 코어 개수 |

### Keypair API
Instance 접근에 필요한 Keypair에 대한 생성, 삭제, 조회 기능을 제공합니다.
#### Keypair 조회
계정에 속한 Keypair를 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/keypairs?name={keypairName}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - |Token ID |
| keypairName | Query | String | O | 조회할 Keypair 이름. 기재하지 않을 경우 모든 keypair 정보를 조회합니다. |

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
            "fingerprint": "{Fingerprint Value}",
        	"createdAt": "{Created At}"
        }
    ]
}
```

|  Name | In | Type | Description |
|--|--|--|--|
| Keypair Name | Body | String | Keypair 이름 |
| Public Key Value | Body | String | Keypair의 Public Key 값 |
| Fingerprint Value | Body | String | Fingerprint 값 |
| Created At | Body | DateTime | Keypair 생성 시간. "keypairName" 을 지정한 단건 조회 시에만 노출됩니다. |

#### Keypair 생성 or 업로드
Keypair를 생성하거나, ssh로 생성한 Keypair를 업로드 합니다.

##### Method, URL
```
POST /v1.0/appkeys/{appkey}/keypairs
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```

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

| Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| Keypair Name | Body | String | - | Keypair 이름 |
| Public Key Value | Body | String | O | 업로드할 Public ssh key. 생략 시 새로운 keypair가 만들어지며, 만들어진 Keypair의 Private Key가 Response에 함께 전달됩니다.|

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

| Name | In | Type | Description |
| --- | --- | --- | --- |
| Keypair Name | Body | String | Keypair 이름 |
| Public Key Value | Body | String | Keypair의 Public ssh key |
| Private Key Value | Body | String | Keypair의 Private ssh key. Keypair 업로드(Request에 "publicKey" 항목을 포함)한 경우 생략됩니다. |
| Fingerprint Value | Body | String | Fingerprint 값 |

###### Private Key 저장
생성된 Private Key Value는 전문을 .pem 파일로 저장 후 해당 Keypair를 사용하도록 설정된 Instance에 접근 시 사용할 수 있습니다.
**생성된 Private Key Value는 다시 조회할 수 없으므로** 분실 또는 삭제되지 않도록 잘 보관해야 하며, 유출 방지를 위해 가급적 보조 저장매체(USB메모리)에 관리하는 것이 좋습니다.


#### Keypair 삭제
지정한 Keypair를 삭제합니다.
##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/keypairs?name={keypairName}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| keypairName | Query | String | - | 삭제할 Keypair 이름 |

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
GET /v1.0/appkeys/{appkey}/images
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

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
            "name": "{Image Name}",
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

|  Name | In | Type | Description |
|--|--|--|--|
| Created At | Body | String  | Image 생성 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Disk Format | Body | String | Image의 Disk Format. <br />"ami", "ari", "aki", "vhd", "vhdx", "vmdk", "raw", "qcow2", "vdi", "ploop", "iso" |
| Image ID | Body | String | Image 식별자 |
| Is Public | Body | Boolean | 모든 Project에서 사용 가능한 공용 Image 여부 |
| Min Disk | Body | Integer | Image 부팅에 필요한 최소 Disk 크기. GB |
| Min RAM | Body | Integer | Image 부팅에 필요한 최소 RAN 크기. MB |
| Image Name | Body | String | Image 이름 |
| Prop Key / Prop Value | Body | String | Image의 추가적인 속정 정보 |
| Protected | Body | Boolean | 삭제 보호 설정 여부 |
| Image Size | Body | Integer | Image 데이터의 크기. bytes |
| Image Status | Body | String | Image의 상태 |
| Updated At | Body | String | Image가 업데이트 된 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |

## Block Storage
### Block Storage API
Block Stroage 생성/삭제 및 조회 기능을 제공합니다. Block Storage를 Instance에 연결/해제하는 기능은 [Instance API](#instance-api)를 통해 제공됩니다.
#### Block Storage Status
Block Storage는 다음과 같은 Status 값을 갖습니다.

| Status | Description |
| --- | --- |
| creating | 생성 중 |
| available | Instance에 연결 가능한 상태 |
| attaching | Instance에 연결 중 |
| detaching | Instance에서 연결 해제 중 |
| in-use | Instance에 연결되어 사용 중인 상태 |
| deleting | 삭제 중 |
| error | 생성 중 에러 발생 |
| error_deleting | 삭제 중 에러 발생 |
| backing-up | 백업 진행 중 |
| restoring-backup | 백업 복구 중 |
| error_backing-up | 백업 진행 중 에러 발생 |
| error_restoring | 백업 복구 중 에러 발생 |
| downloading | Image 다운로드 중 |
| uploading | Image로 업로드 중 |

#### Block Storage 조회
Block Storage의 정보를 조회합니다.

##### Method, URL
```
GET /v1.0/appkeys/{appkey}/volumes?id={volumeId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| volumeId | Query | String | O | 조회할 Block Storage ID. 기재하지 않을 경우 모든 Block Storage의 정보를 조회합니다. |

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
                    "instanceId": "{Attached Instance ID}",
                    "attachmentId": "{Attachment ID}"
                }
            ],
            "availabilityZone": "{Availability Zone Name}",
            "createdAt": "{Created At}",
            "description": "{Description}",
            "id": "{Block Storage ID}",
            "metadata": {
                "{Metadata Key}": "{Metadata Value}"
            },
            "name": "{Block Storage Name}",
            "size": "{Size}",
            "status": "{Status}"
        }
    ]
}
```

|  Name | In | Type | Description |
|--|--|--|--|
| Device Name | Body | String  | Instance에 연결되어 있는 경우, Instance에서의 장치명. ex) "/dev/vdb" |
| Attached Instance ID | Body | String | Instance에 연결되어 있는 경우, 연결된 Instance의 ID |
| Attachment ID | Body | String | Instance에 연결되어 있는 경우, 연결 식별자 |
| Availability Zone Name | Body | String | Block Storage가 위치한 Zone 이름 |
| Created At | Body | String | Block Storage 생성 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Description | Body | String | Block Storage 설명 |
| Block Storage ID | Body | String | Block Storage 식별자 |
| Metadata Key / Value | Body | Boolean | Block Storage에 기재된 Meta data |
| Block Storage Name | Body | String | Block Storage 이름 |
| Size | Body | Integer | Block Storage 크기. GB |
| Status | Body | String | Block Storage 상태 |

#### Block Storage 생성
새로운 Block Storage를 생성합니다.

##### Method, URL
```
POST /v1.0/appkeys/{appkey}/volumes
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

##### Request Body
```json
{
    "volume": {
        "description": "{Description}",
        "availabilityZone":"{Availability Zone Name}",
        "size":"{Size}",
        "name":"{Block Storage Name}",
        "volumeType":"{Volume Type}",
        "metadata": {
        	"{Metadata Key}" : "{Metadata Value}"
        }
    }
}
```

| Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| Description | Body | String | O | Block Storage 설명 |
| Availability Zone Name | Body | String | - | Block Storage를 생성할 Availability Zone 이름 |
| Size | Body | Integer | - | Block Storage 크기. GB, 10 ~ 1000 범위, 10단위 입력 |
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
        "createdAt": "{Created At}",
        "description": "{Description}",
        "id": "{Block Storage ID}",
        "metadata": {
            "{Metadata Key}": "{Metadata Value}"
        },
        "name": "{Block Storage Name}",
        "size": "{Size}",
        "status": "{Status}"
    }
}
```

|  Name | In | Type | Description |
|--|--|--|--|
| Availability Zone Name | Body | String | Block Storage가 위치한 Zone 이름 |
| Created At | Body | String | Block Storage 생성 시간. yyyy-mm-ddTHH:MM:ssZ의 형태. 예) 2017-05-16T02:17:50.166563 |
| Description | Body | String | Block Storage 설명 |
| Block Storage ID | Body | String | Block Storage 식별자 |
| Metadata Key / Value | Body | Boolean | Block Storage에 기재된 Meta data |
| Block Storage Name | Body | String | Block Storage 이름 |
| Size | Body | Integer | Block Storage 크기. GB |
| Status | Body | String | Block Storage 상태 |

#### Block Storage 삭제
Block Storage를 삭제합니다. Status가 "available" "in-use" "error" "error_restoring" 인 Block Storage만 삭제할 수 있습니다.

##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/volumes?id={volumeId}
X-Auth-Token: {tokenId}
```
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| volumeId | Query | String | - | 삭제할 Block Storage ID |

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
Security Group 생성, 삭제, 조회 및 업데이트 기능을 제공합니다. Security Group을 Instance에 등록/해제하는 기능은 [Instance API](#instance-api)를 통해 제공됩니다.

#### Security Group 목록 조회
접근 가능한 Security Group의 정보를 조회합니다.

##### Method, URL
```
GET /v1.0/appkeys/{appkey}/security-groups?id={securityGroupId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |
| securityGroupId | Query | String | O | 조회할 Security Group 식별자. 기재하지 않을 경우 모든 Security Group의 정보를 조회합니다. |

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

|  Name | In | Type | Description |
|--|--|--|--|
| Description | Body | String | Security Group 설명 |
| Security Group ID | Body | String | Security Group 식별자 |
| Name | Body | String | Security Group 이름 |
| securityGroupRules | Body | List | Security Group Rule 목록, [Security Group Rules API](#security-group-rules-api) 참조 |

#### Security Group 생성
새로운 Security Group을 생성합니다.

##### Method, URL
```
POST /v1.0/appkeys/{appkey}/security-groups
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```

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

|  Name | In | Type | Description |
|--|--|--|--|
| Description | Body | String | Security Group 설명 |
| Security Group ID | Body | String | Security Group 식별자 |
| Name | Body | String | Security Group 이름 |
| securityGroupRules | Body | List | Security Group Rule 목록, [Security Group Rules API](#security-group-rules-api) 참조 |

#### Security Group 업데이트
Security Group의 이름, 설명을 변경합니다.

##### Method, URL
```
PUT /v1.0/appkeys/{appkey}/security-groups/{securityGroupId}
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```

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

|  Name | In | Type | Description |
|--|--|--|--|
| Security Group ID | Body | String | Security Group 식별자 |
| Name | Body | String | Security Group 이름 |
| Description | Body | String | Security Group 설명 |

#### Security Group 삭제
지정한 Security Group을 삭제합니다.

##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/security-groups?id={securityGroupId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |
| securityGroupId | Query | String | - | 삭제할 Security Group의 식별자 |

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

#### Security Group Rule 조회
접근 가능한 모든 Security Group Rule의 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/security-group-rules?id={securityGroupRuleId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |
| securityGroupRuleId | Query | String | O | 조회할 Security Group Rule 식별자. 기재하지 않을 경우 모든 Security Group Rule의 정보를 조회합니다. |

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

|  Name | In | Type | Description |
| --- | --- | --- | --- |
| Direction | Body | String | Rule이 적용되는 방향, "ingress" or "egress" |
| Ethernet Type | Body | String | "IPv4" or "IPv6" |
| Rule ID | Body | String | Security Group Rule 식별자 |
| Port Range MAX | Body | Integer | Rule이 적용되는 최대 Port 번호 |
| Port Range MIN | Body | Integer | Rule이 적용되는 최소 Port 번호 |
| Protocol | Body | String | IP Protocol. "icmp" "tcp" "udp" or "null" |
| Remote Group ID | Body | String | Rule이 적용되는 Remote Group의 식별자 |
| Remote IP Prefix | Body | String | Rule이 적용되는 Remote IP의 Prefix |
| Security Group ID | Body | String | Rule이 적용되는 Security Group의 식별자 |

#### Security Group Rule 생성
새로운 Security Group Rule을 생성합니다.
##### Method, URL
```
POST /v1.0/appkeys/{appkey}/security-group-rules
X-Auth-Token: {tokenId}
Content-Type: application/json;charset=UTF-8
```

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

|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| Direction | Body | String | - | Rule이 적용되는 방향, "ingress" or "egress" |
| Ethernet Type | Body | String | O | "IPv4" or "IPv6" |
| Port Range MAX | Body | Integer | O | Rule이 적용되는 최대 Port 번호. 1~65535 범위. 설정 시 "protocol" 항목 생략 불가 |
| Port Range MIN | Body | Integer | O | Rule이 적용되는 최소 Port 번호  1~65535 범위. 설정 시 "protocol" 항목 생략 불가 |
| Protocol | Body | String | O | IP Protocol. "icmp" "tcp" "udp" or "null" |
| Remote Group ID | Body | String | O | Rule이 적용되는 Remote Security Group의 식별자.<br />"remoteIpPrefix" 값을 설정할 경우 생략. |
| Remote IP Prefix | Body | String | O | Rule이 적용되는 Remote IP의 Prefix.<br />"remoteGroupId" 값을 설정할 경우 생략. |
| Security Group ID | Body | String | - | Rule이 적용되는 Security Group의 식별자 |

##### Response Body
```json
{
    "header" : {
        "isSuccessful" :  true,
        "resultCode" :  0,
        "resultMessage" :  "SUCCESS"
    },
    "securityGroupRule": {
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

|  Name | In | Type | Description |
| --- | --- | --- | --- |
| Direction | Body | String | Rule이 적용되는 방향, "ingress" or "egress" |
| Ethernet Type | Body | String | "IPv4" or "IPv6" |
| Rule ID | Body | String | Security Group Rule 식별자 |
| Port Range MAX | Body | Integer | Rule이 적용되는 최대 Port 번호. |
| Port Range MIN | Body | Integer | Rule이 적용되는 최소 Port 번호. |
| Protocol | Body | String | IP Protocol. "icmp" "tcp" "udp" or "null" |
| Remote Group ID | Body | String | Rule이 적용되는 Remote Security Group의 식별자 |
| Remote IP Prefix | Body | String | Rule이 적용되는 Remote IP의 Prefix |
| Security Group ID | Body | String | Rule이 적용되는 Security Group의 식별자 |

#### Security Group Rule 삭제
지정한 Security Group Rule을 삭제합니다.
##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/security-group-rules?id={securityGroupRuelsId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
| --- | --- | --- | --- | --- |
| tokenId | Header | String | - | Token ID |
| securityGroupRuleId | Query | String | - | 삭제할 Security Group Rule 식별자 |
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
Instance에서 연결할 수 있는 Network 정보 조회 기능을 제공합니다.
#### Network Status
Network는 다음 Status 값을 같습니다.

| Status | Description |
| -- | -- |
| BUILD | Network 구축 중 |
| ACTIVE | Network 활성화 상태 |
| DOWN | Network 비활성화 상태 |
| ERROR | 에러 발생 |

#### Network 조회
접근 가능한 Network의 정보를 조회합니다.

##### Method, URL
```
GET /v1.0/appkeys/{appkey}/networks?id={networkId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional |Description |
| -- | -- | -- | -- | -- |
| tokenId | Header | String | - | Token ID |
| networkId | Query | String | O | 조회할 Network 식별자. 기재하지 않을 경우 모든 Network의 정보를 조회합니다. |

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

|  Name | In | Type | Description |
|--|--|--|--|
| Administrative State | Body | Boolean |네트워크 관리 상태. true: up, false: down |
| Network ID | Body | String | 네트워크 식별자 |
| Network Name | Body | String | 네트워크 이름 |
| External Router Provided | Body | Boolean | Router를 통한 Floating IP 제공 가능 여부 |
| Network Status | Body | String | 네트워크 상태. ACTIVE, DOWN, BUILD or ERROR |
| Subnet ID | Body | String | Subnet 식별자 |

### Subnet API
#### Subnet 조회
접근 가능한 Subnet의 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/subnets
X-Auth-Token: {tokenId}
```

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

|  Name | In | Type | Description |
|--|--|--|--|
| Start IP | Body | String | 할당 Pool의 시작 IP. 예) 10.161.244.13 |
| End IP | Body | String | 할당 Pool의 마지막 IP. 예) 10.161.244.121 |
| CIDR | Body | String | Classless Inter-Domain Routing. 예) 10.161.244.0/25 |
| Enable DHCP | Body | Boolean | DHCP 활성화 여부 |
| Subnet ID | Body | String | Subnet 식별자 |
| IP Version | Body | Integer | Subnet의 IP version |
| Subnet Name | Body | Integer | Subnet 이름 |
| Network ID | Body | Integer | Subnet이 속한 네트워크 식별자 |

### Floating IP API
Floating IP 생성, 삭제, 정보 조회 기능을 제공합니다.

#### Floating IP Status
Floating IP는 다음 상태값을 갖습니다.

| Status | Description |
| -- | -- |
| ACTIVE | Floating IP가 Instance와 연결되어 사용중인 상태 |
| DOWN | Floating IP가 연결되어 있지 않은 상태 |
| ERROR | 에러 발생 |

#### Floating IP Pool 조회
Floating IP Pool 목록을 조회합니다.

##### Method, URL
```
GET /v1.0/appkeys/{appkey}/floating-ip-pools
X-Auth-Token: {tokenId}
```
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - |Token ID |

##### Request Body
이 API는 Request Body를 필요로 하지 않습니다.

##### Response Body
```json
{
    "header" : {
	    "resultMessage" :  "SUCCESS",
    	"isSuccessful" :  true,
    	"resultCode" :  0
    },
    "pools" : [
    	{
    		"id" :  "{Pool ID}",
    		"name" :  "{Pool Name}"
    	}
    ]
}
```
|  Name | In | Type | Description |
|--|--|--|--|
| Pool ID | Body | String | Floating IP Pool 식별자 |
| Pool Name | Body | String | Floating IP Pool 이름 |


#### Floating IP 조회
사용 가능한, 또는 사용 중인 Floating IP 정보를 조회합니다.
##### Method, URL
```
GET /v1.0/appkeys/{appkey}/floating-ips?id={floatingIpId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - |Token ID |
| floatingIpId | Query | String | O | 조회할 Floating IP의 식별자. 기재하지 않을 경우 모든 Floating IP의 정보를 조회합니다. |

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
            "portId": "{Port ID}",
            "routerId": "{Router ID}",
            "pool" : {
                "id" :  "{Pool ID}",
                "name" :  "{Pool Name}"
            },
            "status": "{Status}"
        }
    ]
}
```

|  Name | In | Type | Description |
|--|--|--|--|
| Floating IP ID | Body | String | Floating IP 식별자 |
| Floating IP Address | Body | String | Floating IP 주소 |
| Fixed IP Address | Body | String | Floating IP가 연결된 Instance NIC의 IP 주소. Status가 "ACTIVE" 인 경우에만 표시 |
| Port ID | Body | String | Floting IP가 연결된 Port의 식별자. Status가 "ACTIVE" 인 경우에만 표시 |
| Router ID | Body | String | Floating IP의 Router 식별자. Status가 "ACTIVE" 인 경우에만 표시 |
| Pool ID | Body | String | Floating IP가 속한 Pool 식별자 |
| Pool Name | Body | String | Floating IP가 속한 Pool 이름 |
| Status | Body | String | Floating IP의 상태 |

#### Floating IP 생성
Floating IP를 생성합니다.
##### Method, URL
```
POST /v1.0/appkeys/{appkey}/floating-ips
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |

##### Request Body
```json
{
	"pool" : {
		"id" :  "{Pool ID}"
	}
}
```
|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
|  Pool ID | Body | String | - | Floating IP Pool 식별자 |

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
        "floatingIpAddress": "{Floating IP Address}",
        "pool" : {
        	"id" :  "{Pool ID}",
        	"name" :  "{Pool Name}"
        },
        "status": "{Status}"
    }
}
```

|  Name | In | Type | Description |
|--|--|--|--|
| Floating IP ID | Body | String | Floating IP 식별자 |
| Floating IP Address | Body | String | Floating IP 주소 |
| Pool ID | Body | String | Floating IP가 속한 Pool 식별자 |
| Pool Name | Body | String | Floating IP가 속한 Pool 이름 |
| Status | Body | String | Floating IP의 상태 |

#### Floating IP 삭제
지정한 Floating IP를 삭제합니다. 사용중(ACTIVE)인 Floating IP는 연결 해제 후 삭제할 수 있습니다.
##### Method, URL
```
DELETE /v1.0/appkeys/{appkey}/floating-ips?id={floatingIpId}
X-Auth-Token: {tokenId}
```

|  Name | In | Type | Optional | Description |
|--|--|--|--|--|
| tokenId | Header | String | - | Token ID |
| floatingIpId | Path | String | - | 삭제할 Floating IP 식별자 |

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
