## API v2 Preparations

## Common Preparations

### Check API Endpoints
The NHN Cloud Infrastructure Services API provides different endpoints for each type and region. However, the Identity API uses the same endpoint for all regions.

| Type | Region | Endpoint |
|---|---|---|
| identity | All Regions | https://api-identity-infrastructure.nhncloudservice.com |
| compute | Korea (Pangyo)<br>Korea (Pyeongchon)<br>Japan | https://kr1-api-instance-infrastructure.nhncloudservice.com<br>https://kr2-api-instance-infrastructure.nhncloudservice.com<br>https://jp1-api-instance-infrastructure.nhncloudservice.com |
| network | Korea (Pangyo)<br>Korea (Pyeongchon)<br>Japan | https://kr1-api-network-infrastructure.nhncloudservice.com<br>https://kr2-api-network-infrastructure.nhncloudservice.com<br>https://jp1-api-network-infrastructure.nhncloudservice.com |
| image | Korea (Pangyo)<br>Korea (Pyeongchon)<br>Japan | https://kr1-api-image-infrastructure.nhncloudservice.com<br>https://kr2-api-image-infrastructure.nhncloudservice.com<br>https://jp1-api-image-infrastructure.nhncloudservice.com |
| volumev2 | Korea (Pangyo)<br>Korea (Pyeongchon)<br>Japan | https://kr1-api-block-storage-infrastructure.nhncloudservice.com<br>https://kr2-api-block-storage-infrastructure.nhncloudservice.com<br>https://jp1-api-block-storage-infrastructure.nhncloudservice.com |
| Object-store | Korea (Pangyo)<br>Korea (Pyeongchon)<br>Japan | https://kr1-api-object-storage.nhncloudservice.com<br>https://kr2-api-object-storage.nhncloudservice.com<br>https://jp1-api-object-storage.nhncloudservice.com |
| key-manager | Korea (Pangyo)<br>Korea (Pyeongchon)<br>Japan | https://kr1-api-key-manager-infrastructure.nhncloudservice.com<br>https://kr2-api-key-manager-infrastructure.nhncloudservice.com<br>https://jp1-api-key-manager-infrastructure.nhncloudservice.com |

### Check Tenant ID 

You can check your tenant ID to include in API requests from **Set API Endpoint** in **Compute > Instance > Management**. 

### Set API Password

You must set an API endpoint password, which is separate from your NHN Cloud account password, in order to use the NHN Cloud Infrastructure Services API.

1. Go to **Compute > Instance > Management** and click **Set API Endpoint**.
2. Enter an API password in **Set API Password** under **API Endpoint Settings** . 

> An API password is set by account. You can use the same password set in one project for all of your other projects. 


## Token

### Obtain a Token

To obtain a token, use the `identity` type endpoint. The `identity` service endpoint is `https://api-identity-infrastructure.nhncloudservice.com` regardless of region.

You must obtain a token to make API calls. NHN Cloud uses project-scoped tokens.

```
POST /v2.0/tokens
```

#### Request

| Name | Type | Format | Required | Description |
|---|---|---|---|---|
| tenantId | Body | String | O | Tenant ID to obtain a token |
| passwordCredentials | Body | Object | O | User information for authentication |
| username | Body | String | O | NHN Cloud user ID (email format), IAM member ID |
| password | Body | String | O | API password |

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
| access.token.issued_at | Body | Datetime | Token issuance time (UTC)<br>`YYYY-MM-DDThh:mm:ss.SSSSSS` format |
| access.token.expires | Body | Datetime | Token expiration time (UTC)<br>`YYYY-MM-DDThh:mm:ssZ` format |
| access.token.id | Body | String | Token ID |
| access.token.tenant | Body | Object | `tenant` object |
| access.token.tenant.description | Body | String | Tenant description |
| access.token.tenant.enabled | Body | Boolean | Indicates whether the tenant is enabled<br>If disabled, unable to obtain token or make API calls |
| access.token.tenant.id | Body | String | Tenant ID |
| access.token.tenant.name | Body | String | Tenant name |
| access.serviceCatalog | Body | Object | `serviceCatalog` object |
| access.serviceCatalog.endpoints | Body | Object | `endpoint` object |
| access.serviceCatalog.endpoints_links | Body | String | Endpoint links |
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
            "publicURL": "https://kr2-api-instance-infrastructure.nhncloudservice.com/v2/f5073eaa26b64cffbee89411df94ce01"
          },
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-instance-infrastructure.nhncloudservice.com/v2/f5073eaa26b64cffbee89411df94ce01"
          }
        ],
        "type": "compute",
        "name": "nova"
      },
      {
        "endpoints": [
          {
            "region": "KR2",
            "publicURL": "https://kr2-api-image-infrastructure.nhncloudservice.com"
          },
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-image-infrastructure.nhncloudservice.com"
          }
        ],
        "type": "image",
        "name": "glance"
      },
      {
        "endpoints": [
          {
            "region": "KR1",
            "publicURL": "https://api-identity-infrastructure.nhncloudservice.com/v2.0"
          }
        ],
        "type": "identity",
        "name": "keystone"
      },
      {
        "endpoints": [
          {
            "region": "KR2",
            "publicURL": "https://kr2-api-key-manager-infrastructure.nhncloudservice.com"
          },
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-key-manager-infrastructure.nhncloudservice.com"
          }
        ],
        "type": "key-manager",
        "name": "barbican"
      },
      {
        "endpoints": [
          {
            "region": "KR2",
            "publicURL": "https://kr2-api-block-storage-infrastructure.nhncloudservice.com/v2/f5073eaa26b64cffbee89411df94ce01"
          },
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-block-storage-infrastructure.nhncloudservice.com/v2/f5073eaa26b64cffbee89411df94ce01"
          }
        ],
        "type": "volumev2",
        "name": "cinderv2"
      },
      {
        "endpoints": [
          {
            "region": "KR2",
            "publicURL": "https://kr2-api-network-infrastructure.nhncloudservice.com"
          },
          {
            "region": "KR1",
            "publicURL": "https://kr1-api-network-infrastructure.nhncloudservice.com"
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
