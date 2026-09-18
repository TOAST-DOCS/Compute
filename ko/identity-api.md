{% set f = (build_flags | select("in", ["gov","ncgn","ninc","ngsc","ngovc","ngoic"]) | list | first) %}
{% set brand = {"gov":"NHN Cloud","ncgn":"NHN Cloud","ninc":"NHN Internet Cloud","ngsc":"NHN Government Security Cloud","ngovc":"NHN Government Cloud","ngoic":"NHN Government Internet Cloud"} %}
{% set dom = {"gov":"gov-nhncloudservice.com","ncgn":"gncloud.go.kr","ninc":"ninc.go.kr","ngsc":"ngsc.go.kr","ngovc":"ngovc.com","ngoic":"ngoic.com"} %}
<a id="api-v2-preparations"></a>
## API v2 사용 준비

<a id="common-preparations"></a>
## 공통 준비 사항

<a id="check-api-endpoints"></a>
### API 엔드포인트 확인

$[ brand[f] ]$ 기본 인프라 서비스 API는 타입과 리전별로 엔드포인트가 나뉘어 있습니다. 단, Identity API는 모든 리전에서 동일한 엔드포인트를 사용합니다.

{% if "gov" in build_flags %}
| 타입          | 리전 | 엔드포인트                                                                                                                                        |
|-------------|---|----------------------------------------------------------------------------------------------------------------------------------------------|
| identity    | 모든 리전 | https://api-identity-infrastructure.$[ dom[f] ]$                                                                                  |
| compute     | 한국(판교) 리전<br>한국(평촌) 리전 | https://kr1-api-instance-infrastructure.$[ dom[f] ]$<br>https://kr2-api-instance-infrastructure.$[ dom[f] ]$           |
| network     | 한국(판교) 리전<br>한국(평촌) 리전 | https://kr1-api-network-infrastructure.$[ dom[f] ]$<br>https://kr2-api-network-infrastructure.$[ dom[f] ]$             |
| image       | 한국(판교) 리전<br>한국(평촌) 리전 | https://kr1-api-image-infrastructure.$[ dom[f] ]$<br>https://kr2-api-image-infrastructure.$[ dom[f] ]$                 |
| volumev2    | 한국(판교) 리전<br>한국(평촌) 리전 | https://kr1-api-block-storage-infrastructure.$[ dom[f] ]$<br>https://kr2-api-block-storage-infrastructure.$[ dom[f] ]$ |
| nasv1       | 한국(판교) 리전<br>한국(평촌) 리전 | https://kr1-api-nas-infrastructure.$[ dom[f] ]$<br>https://kr2-api-nas-infrastructure.$[ dom[f] ]$ |
| key-manager | 한국(판교) 리전<br>한국(평촌) 리전 | https://kr1-api-key-manager-infrastructure.$[ dom[f] ]$<br>https://kr2-api-key-manager-infrastructure.$[ dom[f] ]$     |
{% elif "ncgn" in build_flags %}
| 타입 | 리전 | 엔드포인트 |
|---|---|---|
| identity | 모든 리전 | https://api-identity-infrastructure.$[ dom[f] ]$ |
| compute | 한국(대구) 리전 | https://kr1-api-instance-infrastructure.$[ dom[f] ]$ |
| network | 한국(대구) 리전 | https://kr1-api-network-infrastructure.$[ dom[f] ]$ |
| image | 한국(대구) 리전 | https://kr1-api-image-infrastructure.$[ dom[f] ]$ |
| volumev2 | 한국(대구) 리전 | https://kr1-api-block-storage-infrastructure.$[ dom[f] ]$ |
{% else %}
| 타입 | 리전 | 엔드포인트 |
|---|---|---|
| identity | 모든 리전 | https://api-identity-infrastructure.$[ dom[f] ]$ |
| compute | 한국(대구) 리전 | https://kr4-api-instance-infrastructure.$[ dom[f] ]$ |
| image | 한국(대구) 리전 | https://kr4-api-image-infrastructure.$[ dom[f] ]$ |
| volumev2 | 한국(대구) 리전 | https://kr4-api-block-storage-infrastructure.$[ dom[f] ]$ |
| network | 한국(대구) 리전 | https://kr4-api-network-infrastructure.$[ dom[f] ]$ |
| key-manager | 한국(대구) 리전 | https://kr4-api-key-manager-infrastructure.$[ dom[f] ]$ |
| kubernetes | 한국(대구) 리전 | https://kr4-api-kubernetes-infrastructure.$[ dom[f] ]$ |
| orchestration | 한국(대구) 리전 | https://kr4-api-orchestration-infrastructure.$[ dom[f] ]$ |
| nas | 한국(대구) 리전 | https://kr4-api-nas-infrastructure.$[ dom[f] ]$ |
{% endif %}

<a id="check-tenant-id"></a>
### 테넌트 ID 확인

API 요청에 포함되는 테넌트 ID는 **Compute > Instance > 관리** 페이지의 **API 엔드포인트 설정** 대화 상자에서 확인합니다.

<a id="set-api-password"></a>
### API 비밀번호 설정

NHN Cloud 기본 인프라 서비스 API를 사용하려면 NHN Cloud 계정 비밀번호와는 별개로 API 비밀번호를 설정해야 합니다.
API 비밀번호는 계정별로 설정됩니다. 한 프로젝트에서 설정된 비밀번호는 사용자가 속한 모든 프로젝트에서 사용할 수 있습니다.

1. **Compute > Instance > 관리** 페이지의 **API 엔드포인트 설정** 버튼을 클릭합니다.
2. **API 엔드포인트 설정** 대화 상자 아래의 **API 비밀번호 설정**에 원하는 API 비밀번호를 지정합니다.

> [주의]
{% if "ncgn" in build_flags %}
{% else %}
> 현재 사용 중인 비밀번호로는 변경할 수 없습니다.
{% endif %}
> API 비밀번호 변경 시 기존 인증 토큰은 더 이상 사용할 수 없으며 재발급이 필요합니다.
{% if "ncgn" in build_flags %}

{% else %}
{% endif %}

{% if "gov" in build_flags or "ncgn" in build_flags %}
{% else %}

{% endif %}
<a id="token"></a>
## Token

<a id="obtain-a-token"></a>
### 토큰 발급하기

{% if "gov" in build_flags %}
토큰 발급은 `identity` 타입 엔드포인트를 이용합니다. `identity` 서비스 엔드포인트는 리전에 관계없이 `https://api-identity-infrastructure.$[ dom[f] ]$`입니다.
{% else %}
토큰 발급은 `identity` 타입 엔드포인트를 이용합니다.
{% endif %}

API를 호출할 때 필요한 토큰을 발급받습니다. NHN Cloud에서는 프로젝트 한정 토큰(project-scoped token)을 사용합니다.

> [주의]
> 사용자가 프로젝트에서 권한을 잃을 경우 해당 자격 증명은 만료되어 사용할 수 없습니다.
> NHN Cloud를 탈퇴하여 계정이 삭제되는 경우 해당 계정으로 발급받은 모든 자격 증명은 만료되어 사용할 수 없습니다.

```
POST /v2.0/tokens
```

#### 요청

| 이름 | 종류 | 형식 | 필수 | 설명 |
|---|---|---|---|---|
| tenantId | Body | String | O | 토큰을 발급받을 테넌트 ID |
| passwordCredentials | Body | Object | O | 인증을 위한 사용자 정보 객체 |
| username | Body | String | O | NHN Cloud 회원 ID(이메일 형식), IAM 멤버 ID |
| password | Body | String | O | API 비밀번호 |

#### 예시
<details><summary>펼쳐 보기</summary>
<p>

```json
{
    "auth": {
        "tenantId": "f5073eaa26b64cffbee89411df94ce01",
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
| access.token.issued_at | Body | Datetime | 토큰 발급 시간(UTC)<br>`YYYY-MM-DDThh:mm:ss.SSSSSS`의 형태 |
| access.token.expires | Body | Datetime | 토큰 만료 시간(UTC)<br>`YYYY-MM-DDThh:mm:ssZ`의 형태 |
| access.token.id | Body | String | 토큰 ID |
| access.token.tenant | Body | Object | `tenant` 객체 |
| access.token.tenant.description | Body | String | 테넌트 설명 |
| access.token.tenant.enabled | Body | String | 테넌트의 활성화 여부<br>활성화되지 않으면 토큰 발급 및 API 호출 불가 |
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
      "id": "e42a092ed6ee4d99949bf25f5f6ecc60",
{% if "gov" in build_flags %}
      "expires": "2020-04-29T15:31:21Z",
{% else %}
      "expires": "2025-11-29T15:31:21Z",
{% endif %}
      "tenant": {
        "id": "f5073eaa26b64cffbee89411df94ce01",
        "name": "c_VKkasVsh",
        "groupId": "XEj2zkHrbA7modGU",
        "description": "",
        "enabled": true,
        "project_domain": "NORMAL"
      },
{% if "gov" in build_flags %}
      "issued_at": "2020-04-29T03:32:28.000405"
{% else %}
      "issued_at": "2025-11-29T03:32:28.000405"
{% endif %}
    },
    "serviceCatalog": [
      {
        "endpoints": [
          {
{% if "gov" in build_flags or "ncgn" in build_flags %}
            "region": "KR1",
            "publicURL": "https://kr1-api-instance-infrastructure.$[ dom[f] ]$/v2/f5073eaa26b64cffbee89411df94ce01"
{% else %}
            "region": "KR4",
            "publicURL": "https://kr4-api-instance-infrastructure.$[ dom[f] ]$/v2/f5073eaa26b64cffbee89411df94ce01"
{% endif %}
          }
        ],
        "type": "compute",
        "name": "nova"
      },
      {
        "endpoints": [
          {
{% if "gov" in build_flags or "ncgn" in build_flags %}
            "region": "KR1",
            "publicURL": "https://kr1-api-image-infrastructure.$[ dom[f] ]$"
{% else %}
            "region": "KR4",
            "publicURL": "https://kr4-api-image-infrastructure.$[ dom[f] ]$"
{% endif %}
          }
        ],
        "type": "image",
        "name": "glance"
      },
      {
        "endpoints": [
          {
{% if "gov" in build_flags or "ncgn" in build_flags %}
            "region": "KR1",
{% else %}
            "region": "KR4",
{% endif %}
            "publicURL": "https://api-identity-infrastructure.$[ dom[f] ]$/v2.0"
          }
        ],
        "type": "identity",
        "name": "keystone"
{% if "gov" in build_flags %}
      },
      {
        "endpoints": [
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-key-manager-infrastructure.$[ dom[f] ]$"
          }
        ],
        "type": "key-manager",
        "name": "barbican"
      },
      {
        "endpoints": [
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-block-storage-infrastructure.$[ dom[f] ]$/v2/f5073eaa26b64cffbee89411df94ce01"
{% elif "ncgn" in build_flags %}
      },
      {
        "endpoints": [
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-block-storage-infrastructure.$[ dom[f] ]$/v2/f5073eaa26b64cffbee89411df94ce01"
{% else %}
      },
      {
        "endpoints": [
          {
            "region": "KR4",
            "publicURL": "https://kr4-api-block-storage-infrastructure.$[ dom[f] ]$/v2/f5073eaa26b64cffbee89411df94ce01"
{% endif %}
          }
        ],
        "type": "volumev2",
        "name": "cinderv2"
      },
      {
        "endpoints": [
          {
{% if "gov" in build_flags or "ncgn" in build_flags %}
            "region": "KR1",
            "publicURL": "https://kr1-api-network-infrastructure.$[ dom[f] ]$"
{% else %}
            "region": "KR4",
            "publicURL": "https://kr4-api-network-infrastructure.$[ dom[f] ]$"
{% endif %}
          }
        ],
        "type": "network",
        "name": "neutron"
      }
    ],
    "user": {
      "id": "436f727b7c9142f896ddd56be591dd7f",
      "username": "37be6ac0-d660-11e7-ae46-005056ac1497",
      "name": "37be6ac0-d660-11e7-ae46-005056ac1497",
      "roles": [
        {
          "name": "project_admin"
        }
      ],
      "roles_links": []
    },
    "metadata": {
      "roles": [
        "9fe2ff9ee4384b1894a90878d3e92bab"
      ],
      "is_admin": 0
    }
  }
}
```

</p>
</details>
