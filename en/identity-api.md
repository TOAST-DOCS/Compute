## Preparing for API v2 

## Common Preparations 

### Check API Endpoints 
TOAST Infrastructure Service API provides different endpoints for each type and region. However, the Identity API provides the same endpoint in all regions. 

| Type | Region | Endpoint |
|---|---|---|
| identity | All Regions | https://api-identity.infrastructure.cloud.toast.com |
| compute | Korea (Pangyo)<br>Korea(Pyeongchon)<br>Japan | https://kr1-api-instance.infrastructure.cloud.toast.com<br>https://kr2-api-instance.infrastructure.cloud.toast.com<br>https://jp1-api-instance.infrastructure.cloud.toast.com |
| network | Korea (Pangyo)<br>Korea(Pyeongchon)<br>Japan | https://kr1-api-network.infrastructure.cloud.toast.com<br>https://kr2-api-instance.infrastructure.cloud.toast.com<br>https://jp1-api-network.infrastructure.cloud.toast.com |
| image | Korea (Pangyo<br>Korea(Pyeongchon))<br>Japan | https://kr1-api-image.infrastructure.cloud.toast.com<br>https://kr2-api-instance.infrastructure.cloud.toast.com<br>https://jp1-api-image.infrastructure.cloud.toast.com |
| volumev2 | Korea (Pangyo)<br>Korea(Pyeongchon)<br>Japan | https://kr1-api-block-storage.infrastructure.cloud.toast.com<br>https://kr2-api-instance.infrastructure.cloud.toast.com<br>https://jp1-api-block-storage.infrastructure.cloud.toast.com |
| key-manager | Korea (Pangyo)<br>Korea(Pyeongchon)<br>Japan | https://kr1-api-key-manager.infrastructure.cloud.toast.com<br>https://kr2-api-instance.infrastructure.cloud.toast.com<br>https://jp1-api-key-manager.infrastructure.cloud.toast.com |

### Check Tenant ID 

Check tenant ID included to API request from **API Endpoint Setting** of **Compute > Instance > Management**. 

### Set API Passwords

To enable TOAST Infrastructure Service API, API password must be set up, separate from TOAST password. 

1. Go to **Compute > Instance > Management** and click **API Endpoint Setting**.
2. Specify API password for **API Password Setting** at the bottom of **API Endpoint Setting** . 

> API password is set for each account. Password set for one project can be applied to all the other projects of the user. 


## Token

### Get a Token

To get a token issued, use endpoints of the  `identity` type. The  `identity` service endpoint refers to `https://api-identity.infrastructure.cloud.toast.com` regardless of the region. 

Get a token required to call API. TOAST needs project-scoped tokens.  

```
POST /v2.0/tokens
```

#### Request

| Name | Type | Format | Required | Description |
|---|---|---|---|---|
| tenantId | Body | String | O | Tenant ID to get a token |
| passwordCredentials | Body | Object | O | User information object for authentication |
| username | Body | String | O | TOAST User ID |
| password | Body | String | O | API Password |

#### Example
<details><summary>Unfold</summary>
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

#### Response

| Name | Type | Attributes | Description |
|---|---|---|---|
| access | Body | Object | `access` object |
| access.token | Body | Object | `token` object |
| access.token.issued_at | Body | Datetime | Token issuance time (UTC)<br>In the`YYYY-MM-DDThh:mm:ss.SSSSSS` format |
| access.token.expires | Body | Datetime | Token expiration time (UTC)<br>In the`YYYY-MM-DDThh:mm:ssZ` format |
| access.token.id | Body | String | Token ID |
| access.token.tenant | Body | Object | `tenant` object |
| access.token.tenant.description | Body | String | Tenant description |
| access.token.tenant.enabled | Body | String | Enable tenant or not <br>If not enabled, unable to issue token or call API |
| access.token.tenant.id | Body | String | Tenant ID |
| access.token.tenant.name | Body | String | Tenant name |
| access.serviceCatalog | Body | Object | `serviceCatalog` object |
| access.serviceCatalog.endpoints | Body | Object | `endpoint` object |
| access.serviceCatalog.endpoints_links | Body | String | Endpoint link |
| access.serviceCatalog.type | Body | String | Endpoint service type |
| access.serviceCatalog.name | Body | String | Endpoint service name |
| access.user | Body | Object | `user` object |
| access.metadata | Body | Object | `metadata` object |

#### Example 
<details><summary>Unfold</summary>
<p>


```json
{
  "access": {
    "token": {
      "id": "e42a092ed6ee4d99949bf25f5f6ecc60",
      "expires": "2020-04-29T15:31:21Z",
      "tenant": {
        "id": "f5073eaa26b64cffbee89411df94ce01",
        "name": "c_VKkasVsh",
        "groupId": "XEj2zkHrbA7modGU",
        "description": "",
        "enabled": true,
        "project_domain": "NORMAL"
      },
      "issued_at": "2020-04-29T03:32:28.000405"
    },
    "serviceCatalog": [
      {
        "endpoints": [
          {
            "region": "KR2",
            "publicURL": "https://kr2-api-instance.infrastructure.cloud.toast.com/v2/f5073eaa26b64cffbee89411df94ce01"
          },
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-instance.infrastructure.cloud.toast.com/v2/f5073eaa26b64cffbee89411df94ce01"
          }
        ],
        "type": "compute",
        "name": "nova"
      },
      {
        "endpoints": [
          {
            "region": "KR2",
            "publicURL": "https://kr2-api-image.infrastructure.cloud.toast.com"
          },
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-image.infrastructure.cloud.toast.com"
          }
        ],
        "type": "image",
        "name": "glance"
      },
      {
        "endpoints": [
          {
            "region": "KR1",
            "publicURL": "https://api-identity.infrastructure.cloud.toast.com/v2.0"
          }
        ],
        "type": "identity",
        "name": "keystone"
      },
      {
        "endpoints": [
          {
            "region": "KR2",
            "publicURL": "https://kr2-api-key-manager.infrastructure.cloud.toast.com"
          },
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-key-manager.infrastructure.cloud.toast.com"
          }
        ],
        "type": "key-manager",
        "name": "barbican"
      },
      {
        "endpoints": [
          {
            "region": "KR2",
            "publicURL": "https://kr2-api-block-storage.infrastructure.cloud.toast.com/v2/f5073eaa26b64cffbee89411df94ce01"
          },
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-block-storage.infrastructure.cloud.toast.com/v2/f5073eaa26b64cffbee89411df94ce01"
          }
        ],
        "type": "volumev2",
        "name": "cinderv2"
      },
      {
        "endpoints": [
          {
            "region": "KR2",
            "publicURL": "https://kr2-api-network.infrastructure.cloud.toast.com"
          },
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-network.infrastructure.cloud.toast.com"
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
