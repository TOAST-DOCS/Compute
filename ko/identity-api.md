## API v2 사용 준비

## 공통 준비 사항

### API Endpoint 확인

TOAST 기본 인프라 서비스 API는 서비스와 리전 별로 엔드포인트가 나누어져 있습니다. 단, Identity API는 모든 리전에서 동일한 endpoint를 사용합니다.

| 서비스 | 리전 | 엔드포인트 |
|---|---|---|
| Identity | 모든 리전 | https://api-identity.infrastructure.cloud.toast.com |
| compute | 한국(판교) 리전<br>일본 리전 | https://kr1-api-compute.infrastructure.cloud.toast.com<br>https://jp1-api-compute.infrastructure.cloud.toast.com |
| network | 한국(판교) 리전<br>일본 리전 | https://kr1-api-network.infrastructure.cloud.toast.com<br>https://jp1-api-network.infrastructure.cloud.toast.com |
| image | 한국(판교) 리전<br>일본 리전 | https://kr1-api-image.infrastructure.cloud.toast.com<br>https://jp1-api-image.infrastructure.cloud.toast.com |
| volume | 한국(판교) 리전<br>일본 리전 | https://kr1-api-block-storage.infrastructure.cloud.toast.com<br>https://jp1-api-block-storage.infrastructure.cloud.toast.com |
| object-store | 한국(판교) 리전<br>일본 리전 | https://kr1-api-object-storage.infrastructure.cloud.toast.com<br>https://jp1-api-object-storage.infrastructure.cloud.toast.com |
| key-manager | 한국(판교) 리전<br>일본 리전 | https://kr1-api-key-manager.infrastructure.cloud.toast.com<br>https://jp1-api-key-manager.infrastructure.cloud.toast.com |

### 테넌트 ID 확인

API 요청에 포함되는 테넌트 ID는 **Compute > Instance > 관리** 페이지의 **API 엔드포인트 설정** 창에서 확인합니다.

### API 비밀번호 설정

TOAST 기본 인프라 서비스 API를 사용하기 위해서 TOAST 계정 비밀번호와는 별개로 API 비밀번호를 설정해야 합니다.

1. **Compute > Instance > 관리** 페이지의 **API 엔드포인트 설정** 버튼을 클릭합니다.
2. **API 엔드포인트 설정** 대화창 아래의 **API 비밀번호 설정**에 원하는 API 비밀번호를 지정합니다.

> API 비밀번호는 계정별로 설정됩니다. 한 프로젝트에서 설정된 비밀번호는 사용자가 속한 모든 프로젝트에서 사용할 수 있습니다.


## Token
### 토큰 발급하기

API 호출할 때 필요한 토큰을 발급 받습니다. TOAST에서는 프로젝트 한정 토큰(project-scoped token)을 사용합니다.

```
POST /v2.0/tokens
```

#### 요청

| 이름 | 종류 | 형식 | 필수 | 설명 |
|---|---|---|---|---|
| tenantId | Body | String | O | 토큰을 발급받을 테넌트 ID |
| passwordCredentials | Body | Object | O | 인증을 위한 사용자 정보 객체 |
| username | Body | String | O | TOAST 사용자 ID |
| password | Body | String | O | API 비밀 번호 |

#### 예시
<details><summary>펼쳐 보기</summary>
<p>

```json
{
    "auth": {
        "tenantId": "a07397e624b1a44bb96b76d451f7e3b23",
        "passwordCredentials": {
            "username": "user@example.com",
            "password": "secretsecret"
        }
    }
}
```

</p>
</details>

#### 응답

| 이름 | 종류 | 속성 | 설명 |
|---|---|---|---|
| access | Body | Object | `access` 객체 |
| access.token | Body | Object | `token` 객체 |
| access.token.issued_at | Body | Datetime | 토큰 발급 시간 (UTC)<br>`YYYY-MM-DDThh:mm:ss.SSSSSS`의 형태 |
| access.token.expires | Body | Datetime | 토큰 만료 시간 (UTC)<br>`YYYY-MM-DDThh:mm:ssZ`의 형태 |
| access.token.id | Body | String | 토큰 ID |
| access.token.tenant | Body | Object | `tenant` 객체 |
| access.token.tenant.description | Body | String | 테넌트 설명 |
| access.token.tenant.enabled | Body | String | Tenant의 활성화 여부<br>활성화가 되지 않으면 토큰 발급 및 API 호출 불가 |
| access.token.tenant.id | Body | String | 테넌트 ID |
| access.token.tenant.name | Body | String | 테넌트 이름 |
| access.serviceCatalog | Body | Object | `serviceCatalog` 객체 |
| access.serviceCatalog.endpoints | Body | Object | `endpoint` 객체 |
| access.serviceCatalog.endpoints_links | Body | String | 엔드포인트 링크 |
| access.serviceCatalog.type | Body | String | 엔드포인트 서비스 타입 |
| access.serviceCatalog.name | Body | String | 엔드포인트 서비스 이름 |
| access.user | Body | Object | `user` 객체 |
| access.metadata | Body | Object | `metadata` 객체 |

#### 예제
<details><summary>펼쳐 보기</summary>
<p>

```json
{
    "access": {
        "token": {
            "issued_at": "2020-02-22T17:09:57.647795",
            "expires": "2020-02-22T17:09:57Z",
            "id": "gAAAAABeeVymchFmeAIHc0JORI3l1BP9fhGiKxk4Z1t1VwEEUd5fm4THktl6wkq434MqoI4uLYrsVL-rzFut9M4BGa824HeXHj8mPz2oLCAB0cWMNU3WN5G9-cOT4LySU0F7TVxcvjq8ZN7V4rfWyL6gUCiZMvnlKx8KxxV4LWSBj9f1otcWXrg%3D",
            "tenant": {
                "description": null,
                "enabled": true,
                "id": "73f0aa26640f4971864919d0eb0f0880",
                "name": "c_VKkasVsh"
            }
        },
        "serviceCatalog": [
            {
                "endpoints": [
                    {
                        "region": "KR1",
                        "publicURL": "http://kr1-compute.example.com/v2/73f0aa26640f4971864919d0eb0f0880"
                    },
                    {
                        "region": "JP1",
                        "publicURL": "http://jp1-compute.example.com/v2/73f0aa26640f4971864919d0eb0f0880"
                    }
                ],
                "endpoints_links": [],
                "type": "compute",
                "name": "nova"
            },
            {
                "endpoints": [
                    {
                        "region": "KR1",
                        "publicURL": "http://identity.example.com/v2.0"
                    },
                    {
                        "region": "JP1",
                        "publicURL": "http://identity.example.com/v2.0"
                    }
                ],
                "endpoints_links": [],
                "type": "identity",
                "name": "keystone"
            }
        ],
        "user": {
            "username": "37be6ac0-d660-11e7-ae46-005056ac1498",
            "roles_links": [],
            "id": "436f727b7c9142f896ddd56be591dd7a",
            "roles": [
                {
                    "name": "project_admin"
                }
            ],
            "name": "37be6ac0-d660-11e7-ae46-005056ac1498"
        },
        "metadata": {
            "is_admin": 0,
            "roles": [
                "8341d3603a1d4d5985bff09f10704d4d"
            ]
        }
    }
}
```

</p>
</details>
