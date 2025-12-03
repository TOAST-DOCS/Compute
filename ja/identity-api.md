<a id="common-preparations"></a>
## API v2使用準備

<a id="check-api-endpoints"></a>
## 共通準備事項

<a id="check-tenant-id"></a>
### API Endpoint確認

NHN Cloud基本インフラサービスAPIは、タイプとリージョンごとにエンドポイントが分かれています。ただし、Identity APIはすべてのリージョンで同じendpointを使用します。

| タイプ | リージョン | エンドポイント |
|---|---|---|
| identity | すべてのリージョン | https://api-identity-infrastructure.nhncloudservice.com |
| compute | 韓国(パンギョ)リージョン<br>韓国(ピョンチョン)リージョン<br>日本リージョン<br>米国(カリフォルニア)リージョン | https://kr1-api-instance-infrastructure.nhncloudservice.com<br>https://kr2-api-instance-infrastructure.nhncloudservice.com<br>https://jp1-api-instance-infrastructure.nhncloudservice.com<br>https://us1-api-instance-infrastructure.nhncloudservice.com |
| network | 韓国(パンギョ)リージョン<br>韓国(ピョンチョン)リージョン<br>日本リージョン<br>米国(カリフォルニア)リージョン | https://kr1-api-network-infrastructure.nhncloudservice.com<br>https://kr2-api-network-infrastructure.nhncloudservice.com<br>https://jp1-api-network-infrastructure.nhncloudservice.com<br>https://us1-api-network-infrastructure.nhncloudservice.com |
| image | 韓国(パンギョ)リージョン<br>韓国(ピョンチョン)リージョン<br>日本リージョン<br>米国(カリフォルニア)リージョン | https://kr1-api-image-infrastructure.nhncloudservice.com<br>https://kr2-api-image-infrastructure.nhncloudservice.com<br>https://jp1-api-image-infrastructure.nhncloudservice.com<br>https://us1-api-image-infrastructure.nhncloudservice.com |
| volumev2 | 韓国(パンギョ)リージョン<br>韓国(ピョンチョン)リージョン<br>日本リージョン<br>米国(カリフォルニア)リージョン | https://kr1-api-block-storage-infrastructure.nhncloudservice.com<br>https://kr2-api-block-storage-infrastructure.nhncloudservice.com<br>https://jp1-api-block-storage-infrastructure.nhncloudservice.com<br>https://us1-api-block-storage-infrastructure.nhncloudservice.com |
| object-store | 韓国(パンギョ)リージョン<br>韓国(ピョンチョン)リージョン<br>日本リージョン<br>米国(カリフォルニア)リージョン | https://kr1-api-object-storage.nhncloudservice.com<br>https://kr2-api-object-storage.nhncloudservice.com<br>https://jp1-api-object-storage.nhncloudservice.com<br>https://us1-api-object-storage.nhncloudservice.com |
| key-manager | 韓国(パンギョ)リージョン<br>韓国(ピョンチョン)リージョン<br>日本リージョン<br>米国(カリフォルニア)リージョン | https://kr1-api-key-manager-infrastructure.nhncloudservice.com<br>https://kr2-api-key-manager-infrastructure.nhncloudservice.com<br>https://jp1-api-key-manager-infrastructure.nhncloudservice.com<br>https://us1-api-key-manager-infrastructure.nhncloudservice.com |

<a id="set-api-password"></a>
### テナントID確認

APIリクエストに含まれるテナントIDは、**Compute > Instance > 管理**ページの**APIエンドポイント設定**ウィンドウで確認します。

<a id="token"></a>
### APIパスワード設定

NHN Cloud基本インフラサービスAPIを使用するためにNHN Cloudアカウントパスワードとは別にAPIパスワードを設定する必要があります。
APIパスワードはアカウントごとに設定されます。1つのプロジェクトで設定されたパスワードは、ユーザーが属する全てのプロジェクトで使用できます。

1. **Compute > Instance > 管理**ページの**APIエンドポイント設定**ボタンを押します。
2. **APIエンドポイント設定**ダイアログボックスの下部、**APIパスワード設定**にAPIパスワードを指定します。

> [注意]  
> 現在使用中のパスワードには変更できません。  
> API パスワードを変更すると、既存の認証トークンは使用できなくなり、再発行が必要です。 


<a id="obtain-a-token"></a>
## Token

### トークンを発行する

トークンの発行は`identity`タイプエンドポイントを利用します。 `identity`サービスエンドポイントはリージョンに関係なく`https://api-identity-infrastructure.nhncloudservice.com`です。

API呼び出し時に必要なトークンを発行します。NHN Cloudでは、プロジェクト限定トークン(project-scoped token)を使用します。

> [注意]  
> ユーザーがプロジェクトで権限を失った場合、その認証情報は有効期限が切れて使用できなくなります。 
> NHN Cloudを退会してアカウントが削除される場合、そのアカウントで発行されたすべての認証情報は有効期限が切れて使用できなくなります。

```
POST /v2.0/tokens
```

#### リクエスト

| 名前 | 種類 | 形式 | 必須 | 説明 |
|---|---|---|---|---|
| tenantId | Body | String | O | トークンの発行を受けるテナントID |
| passwordCredentials | Body | Object | O | 認証用のユーザー情報オブジェクト |
| username | Body | String | O | NHN Cloud会員ID(メール形式)、IAMメンバーID |
| password | Body | String | O | APIのパスワード |

#### 例
<details><summary>さらに表示</summary>
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

#### レスポンス

| 名前 | 種類 | プロパティ | 説明 |
|---|---|---|---|
| access | Body | Object | `access`オブジェクト |
| access.token | Body | Object | `token`オブジェクト |
| access.token.issued_at | Body | Datetime | トークン発行日時(UTC)<br>`YYYY-MM-DDThh:mm:ss.SSSSSS`の形式 |
| access.token.expires | Body | Datetime | トークン有効期限(UTC)<br>`YYYY-MM-DDThh:mm:ssZ`の形式 |
| access.token.id | Body | String | トークンID |
| access.token.tenant | Body | Object | `tenant`オブジェクト |
| access.token.tenant.description | Body | String | テナントの説明 |
| access.token.tenant.enabled | Body | String | Tenant有効/無効<br>有効になっていない場合、トークン発行およびAPI呼び出し不可 |
| access.token.tenant.id | Body | String | テナントID |
| access.token.tenant.name | Body | String | テナント名 |
| access.serviceCatalog | Body | Object | `serviceCatalog`オブジェクト |
| access.serviceCatalog.endpoints | Body | Object | `endpoint`オブジェクト |
| access.serviceCatalog.endpoints_links | Body | String | エンドポイントリンク |
| access.serviceCatalog.type | Body | String | エンドポイントサービスタイプ |
| access.serviceCatalog.name | Body | String | エンドポイントサービス名 |
| access.user | Body | Object | `user`オブジェクト |
| access.metadata | Body | Object | `metadata`オブジェクト |

#### 例
<details><summary>さらに表示</summary>
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
