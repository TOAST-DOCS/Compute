## Compute > Identity API 가이드

## 사전 준비

### API Endpoint 확인

TOAST 기본 인프라 서비스 API는 하위 서비스별로 엔드포인트가 분리되어 있습니다.
단 Keystone에 해당하는 Identity API는 하나만 존재하므로 모든 리전에서 공유할 수 있습니다.
현재 TOAST 기본 인프라 서비스에서 지원하는 API 엔드포인트 목록은 다음과 같습니다.

| 서비스 | 리전 | 엔드포인트 |
|---|---|---|
| Identity | 모든 리전 | https://api-identity.cloud.toast.com |
| compute | 한국(판교) 리전 | https://kr1-api-compute.cloud.toast.com |
| network | 한국(판교) 리전 | https://kr1-api-network.cloud.toast.com |
| image | 한국(판교) 리전 | https://kr1-api-image.cloud.toast.com |
| volume | 한국(판교) 리전 | https://kr1-api-volume.cloud.toast.com |

### API Password 설정

1. **Infrasturcutre** > **Compute** > **Instance** > 관리 메뉴 클릭
2. 상단의 **API 엔드포인트 설정** 버튼 클릭
3. **API 엔드포인트 설정** 대화창에서 원하는 API 비밀번호를 지정

> API 비밀번호는 계정별로 설정됩니다. 동일한 계정을 사용한다면 다른 프로젝트에서도 사용하실 수 있습니다.


## API Version

### 버전 목록 보기

TOAST Identity API에서 지원하는 버전 목록을 확인할 수 있습니다.

```
GET /
```
#### 요청
이 API는 요청 본문을 요구하지 않습니다.

#### 응답
<details><summary>펼쳐 보기</summary>
<p>

```json
{
    "versions": {
        "values": [
            {
                "id": "v3.4",
                "links": [
                    {
                        "href": "http://localhost:35357/v3/",
                        "rel": "self"
                    }
                ],
                "media-types": [
                    {
                        "base": "application/json",
                        "type": "application/vnd.openstack.identity-v3+json"
                    }
                ],
                "status": "stable",
                "updated": "2015-03-30T00:00:00Z"
            },
            {
                "id": "v2.0",
                "links": [
                    {
                        "href": "http://localhost:35357/v2.0/",
                        "rel": "self"
                    },
                    {
                        "href": "http://docs.openstack.org/",
                        "rel": "describedby",
                        "type": "text/html"
                    }
                ],
                "media-types": [
                    {
                        "base": "application/json",
                        "type": "application/vnd.openstack.identity-v2.0+json"
                    }
                ],
                "status": "stable",
                "updated": "2014-04-17T00:00:00Z"
            }
        ]
    }
}
```

</p>
</details>

### 버전 상세 보기
TOAST Identity API v2.0의 상세 정보를 확인할 수 있습니다.
```
GET /v2.0
```
#### 요청
이 API는 요청 본문을 요구하지 않습니다.

#### 응답
<details><summary>펼쳐 보기</summary>
<p>

```json
{
    "version": {
        "status": "stable",
        "updated": "2014-04-17T00:00:00Z",
        "media-types": [
            {
                "base": "application/json",
                "type": "application/vnd.openstack.identity-v2.0+json"
            }
        ],
        "id": "v2.0",
        "links": [
            {
                "href": "http://localhost:5000/v2.0/",
                "rel": "self"
            },
            {
                "href": "http://docs.openstack.org/",
                "rel": "describedby",
                "type": "text/html"
            }
        ]
    }
}
```

</p>
</details>

## Token
### 토큰 발급하기
API 호출할 때 필요한 Token을 발급합니다.
```
POST /v2.0/tokens
```
#### 요청

| 이름 | 종류 | 형식 | 필수 | 설명 |
|---|---|---|---|---|
| tenantName | Body | String | O | Token 발급받을 Tenant 이름<br>tenantId 또는 tenantName 중 하나를 반드시 지정해야 함 |
| tenantId | Body | String | O | Token 발급받을 Tenant ID<br>tenantId 또는 tenantName 중 하나를 반드시 지정해야 함 |
| passwordCredentials | Body | Object | O | 인증을 위한 사용자 정보 객체<br>사용자 ID + 비밀번호 조합이나 기존 Token ID를 지정해야 함 |
| username | Body | String | O | TOAST 사용자 ID |
| password | Body | String | O | API 비밀 번호 |
| token | Body | Object | O | 기존 Token 정보<br>사용자 ID 또는 API 비밀번호를 모를 때 사용 |
| id | Body | String | O | 기존 Token ID |

#### 예시
<details><summary>펼쳐 보기</summary>
<p>

```json
{
    "auth": {
        "tenantName": "admin",
        "passwordCredentials": {
            "username": "admin",
            "password": "secretsecret"
        }
    }
}
```
```json
{
    "auth": {
        "tenantName": "demo",
        "token": {
            "id": "cbc36478b0bd8e67e89469c7749d4127"
        }
    }
}
```

</p>
</details>

#### 응답

| 이름 | 종류 | 속성 | 설명 |
|---|---|---|---|
| access | Body | Object | `access` 객체<br>발급받은 Token 및 카탈로그를 포함 |
| access.token | Body | Object | `token` 객체<br>Token 및 Scope를 포함 |
| access.token.issued_at | Body | Datetime | Token 발급 시간 (UTC)<br>yyyy-mm-ddTHH:MM:ss.SSSSSS의 형태 |
| access.token.expires | Body | Datetime | Token 만료 시간 (UTC)<br>yyyy-mm-ddTHH:MM:ssZ의 형태 |
| access.token.id | Body | String | Token ID |
| access.token.tenant | Body | Object | `tenant` 객체 |
| access.token.tenant.description | Body | String | Tenant에 대한 설명 |
| access.token.tenant.enabled | Body | String | Tenant의 활성화 여부<br>활성화가 되지 않으면 Token 발급 및 API 호출 불가 |
| access.token.tenant.id | Body | String | Tenant ID |
| access.token.tenant.name | Body | String | Tenant 이름 |
| access.serviceCatalog | Body | Object | `serviceCatalog` 객체 |
| access.serviceCatalog.endpoints | Body | Object | `endpoint` 객체<br>각 객체는 `adminURL`, `internalURL`, `publicURL`를 포함<br>Region 별로 분리되어 있음 |
| access.serviceCatalog.endpoints_links | Body | String | Endpoint에 대한 링크 |
| access.serviceCatalog.type | Body | String | 카탈로그에 포함되는 Service의 타입<br>`identity`, `compute`, `network`, `image`, `volumev2` 등이 있음 |
| access.serviceCatalog.name | Body | String | 카탈로그에 포함되는 Service의 이름<br>`keystone`, `nova`, `neutron` 등이 있음 |
| access.user | Body | Object | `user` 객체<br>`username`, `role_links`, `id`, `roles`, `name` 등이 있음 |
| access.metadata | Body | Object | `metadata` 객체 |

#### 예제
<details><summary>펼쳐 보기</summary>
<p>

```json
{
    "access": {
        "token": {
            "issued_at": "2014-01-30T17:09:57.647795",
            "expires": "2014-01-31T17:09:57Z",
            "id": "admin_id",
            "tenant": {
                "description": null,
                "enabled": true,
                "id": "73f0aa26640f4971864919d0eb0f0880",
                "name": "admin"
            }
        },
        "serviceCatalog": [
            {
                "endpoints": [
                    {
                        "adminURL": "http://23.253.72.207:8774/v2/73f0aa26640f4971864919d0eb0f0880",
                        "region": "RegionOne",
                        "internalURL": "http://23.253.72.207:8774/v2/73f0aa26640f4971864919d0eb0f0880",
                        "id": "2dad48f09e2a447a9bf852bcd93548ef",
                        "publicURL": "http://23.253.72.207:8774/v2/73f0aa26640f4971864919d0eb0f0880"
                    }
                ],
                "endpoints_links": [],
                "type": "compute",
                "name": "nova"
            },
            {
                "endpoints": [
                    {
                        "adminURL": "http://23.253.72.207:35357/v2.0",
                        "region": "RegionOne",
                        "internalURL": "http://23.253.72.207:5000/v2.0",
                        "id": "26af053673df4ef3a2340c4239e21ea2",
                        "publicURL": "http://23.253.72.207:5000/v2.0"
                    }
                ],
                "endpoints_links": [],
                "type": "identity",
                "name": "keystone"
            }
        ],
        "user": {
            "username": "admin",
            "roles_links": [],
            "id": "1f568815cb8148688e6ee9b2f7527dcc",
            "roles": [
                {
                    "name": "service"
                },
                {
                    "name": "admin"
                }
            ],
            "name": "admin"
        },
        "metadata": {
            "is_admin": 0,
            "roles": [
                "8341d3603a1d4d5985bff09f10704d4d",
                "2e66d57df76946fdbe034bc4da6fdec0"
            ]
        }
    }
}
```

</p>
</details>
