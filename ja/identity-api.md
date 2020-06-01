## API v2使用準備

## 共通準備事項

### API Endpoint確認

TOAST基本インフラサービスAPIは、サービスとリージョンごとにエンドポイントが分かれています。ただし、Identity APIはすべてのリージョンで同じendpointを使用します。

| サービス | リージョン | エンドポイント |
|---|---|---|
| Identity | すべてのリージョン | https://api-identity.infrastructure.cloud.toast.com |
| compute | 韓国(パンギョ)リージョン<br>日本リージョン | https://kr1-api-instance.infrastructure.cloud.toast.com<br>https://jp1-api-instance.infrastructure.cloud.toast.com |
| network | 韓国(パンギョ)リージョン<br>日本リージョン | https://kr1-api-network.infrastructure.cloud.toast.com<br>https://jp1-api-network.infrastructure.cloud.toast.com |
| image | 韓国(パンギョ)リージョン<br>日本リージョン | https://kr1-api-image.infrastructure.cloud.toast.com<br>https://jp1-api-image.infrastructure.cloud.toast.com |
| volume | 韓国(パンギョ)リージョン<br>日本リージョン | https://kr1-api-block-storage.infrastructure.cloud.toast.com<br>https://jp1-api-block-storage.infrastructure.cloud.toast.com |
| object-store | 韓国(パンギョ)リージョン<br>日本リージョン | https://kr1-api-object-storage.infrastructure.cloud.toast.com<br>https://jp1-api-object-storage.infrastructure.cloud.toast.com |
| key-manager | 韓国(パンギョ)リージョン<br>日本リージョン | https://kr1-api-key-manager.infrastructure.cloud.toast.com<br>https://jp1-api-key-manager.infrastructure.cloud.toast.com |

### テナントID確認

APIリクエストに含まれるテナントIDは、**Compute > Instance > 管理**ページの**APIエンドポイント設定**ウィンドウで確認します。

### APIパスワード設定

TOAST基本インフラサービスAPIを使用するためにTOASTアカウントパスワードとは別にAPIパスワードを設定する必要があります。

1. **Compute > Instance > 管理**ページの**APIエンドポイント設定**ボタンを押します。
2. **APIエンドポイント設定**ダイアログボックスの下部、**APIパスワード設定**にAPIパスワードを指定します。

> APIパスワードはアカウントごとに設定されます。あるプロジェクトで設定されたパスワードはユーザーが属すすべてのプロジェクトで使用できます。


## Token
### トークンを発行する

API呼び出し時に必要なトークンを発行します。TOASTでは、プロジェクト限定トークン(project-scoped token)を使用します。

```
POST /v2.0/tokens
```

#### リクエスト

| 名前 | 種類 | 形式 | 必須 | 説明 |
|---|---|---|---|---|
| tenantId | Body | String | O | トークンの発行を受けるテナントID |
| passwordCredentials | Body | Object | O | 認証用のユーザー情報オブジェクト |
| username | Body | String | O | TOASTユーザーID |
| password | Body | String | O | APIのパスワード |

#### 例
<details><summary>さらに表示</summary>
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
